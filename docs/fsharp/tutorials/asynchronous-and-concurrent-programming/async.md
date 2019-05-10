---
title: Programmation asynchrone
description: Découvrez comment F# programmation asynchrone est effectuée via un modèle de programmation au niveau du langage qui est facile à utiliser et plus naturel pour la langue.
ms.date: 06/20/2016
ms.openlocfilehash: 8cd7d7bcecabe8ea2c33a4787fe9ebbadd67fe67
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64753591"
---
# <a name="async-programming-in-f"></a>Programmation asynchrone en F\#

> [!NOTE]
> Certains des inexactitudes ont été découverts dans cet article.  Il est en cours de réécriture.  Consultez [problème #666](https://github.com/dotnet/docs/issues/666) pour en savoir plus sur les modifications.

Programmation asynchrone F# peuvent être exécutées via un modèle de programmation au niveau du langage conçu pour être facile à utiliser et naturel de la langue.

Le cœur de la programmation asynchrone F# est `Async<'T>`, une représentation sous forme de travail qui peut être déclenchée pour exécuter en arrière-plan, où `'T` est soit le type retourné par le biais de spéciale `return` mot clé ou `unit` si le flux de travail asynchrones n’a aucun résultat à retourner.

Le concept clé à comprendre est que le type d’une expression async est `Async<'T>`, qui est simplement un _spécification_ de travail à faire dans un contexte asynchrone. Il n’est pas exécuté jusqu'à ce que vous le démarrez explicitement avec une des fonctions de départ (tel que `Async.RunSynchronously`). Bien qu’il s’agit d’une autre manière de penser à travailler, il finit par être assez simple dans la pratique.

Par exemple, supposons que vous souhaitez télécharger le code HTML à partir de dotnetfoundation.org sans bloquer le thread principal. Vous pouvez le faire comme suit :

```fsharp
open System
open System.Net

let fetchHtmlAsync url =
    async {
        let uri = Uri(url)
        use webClient = new WebClient()

        // Execution of fetchHtmlAsync won't continue until the result
        // of AsyncDownloadString is bound.
        let! html = webClient.AsyncDownloadString(uri)
        return html
    }

let html = "https://dotnetfoundation.org" |> fetchHtmlAsync |> Async.RunSynchronously
printfn "%s" html
```

C’est tout ! À part l’utilisation de `async`, `let!`, et `return`, il s’agit simplement normal F# code.

Il existe quelques constructions syntaxiques qui méritent votre attention :

* `let!` lie le résultat d’une expression async (qui s’exécute sur un autre contexte).
* `use!` fonctionne comme `let!`, mais supprime ses ressources liées lorsqu’il devient hors de portée.
* `do!` un flux de travail asynchrone qui ne retourne rien attendra.
* `return` renvoie simplement un résultat à partir d’une expression async.
* `return!` exécute un autre flux de travail asynchrone et retourne sa valeur de retour en conséquence.

En outre, normal `let`, `use`, et `do` mots clés peuvent être utilisés avec les versions async comme ils le feraient dans une fonction normale.

## <a name="how-to-start-async-code-in-f"></a>Comment démarrer le Code asynchrone en F\#

Comme mentionné précédemment, le code asynchrone est une spécification de travail à faire dans un autre contexte qui doit être démarrée explicitement. Voici deux méthodes principales pour y parvenir :

1. `Async.RunSynchronously` démarre un flux de travail asynchrone sur un autre thread et attend son résultat.

    ```fsharp
    open System
    open System.Net

    let fetchHtmlAsync url =
        async {
            let uri = Uri(url)
            use webClient = new WebClient()
            let! html = webClient.AsyncDownloadString(uri)
            return html
        }

    // Execution will pause until fetchHtmlAsync finishes
    let html = "https://dotnetfoundation.org" |> fetchHtmlAsync |> Async.RunSynchronously

    // you actually have the result from fetchHtmlAsync now!
    printfn "%s" html
    ```

2. `Async.Start` démarre un flux de travail asynchrone sur un autre thread et sera **pas** attend son résultat.

    ```fsharp
    open System
    open System.Net

    let uploadDataAsync url data =
        async {
            let uri = Uri(url)
            use webClient = new WebClient()
            webClient.UploadStringAsync(uri, data)
        }

    let workflow = uploadDataAsync "https://url-to-upload-to.com" "hello, world!"

    // Execution will continue after calling this!
    Async.Start(workflow)

    printfn "%s" "uploadDataAsync is running in the background..."
    ```

Il existe plusieurs manières pour démarrer un flux de travail asynchrones disponible pour des scénarios plus spécifiques. Elles sont détaillées [dans la référence Async](https://msdn.microsoft.com/library/ee370232.aspx).

### <a name="a-note-on-threads"></a>Remarque sur les Threads

La phrase « dans un autre thread » est mentionnée ci-dessus, mais il est important de savoir que **cela ne signifie pas que les workflows asynchrones sont une façade pour le multithreading**. Le flux de travail réellement « passe » entre les threads, les emprunts pour une petite quantité de temps pour effectuer des tâches utiles. Lorsqu’un flux de travail asynchrone est en fait « en attente » (par exemple, un appel réseau renvoyer quelque chose), n’importe quel thread qu'au moment où il a été d’emprunt est libérée jusqu'à accédez effectuer des tâches utiles sur autre chose. Cela permet aux workflows asynchrones utilisent le système, sur qu'elles s’exécutent aussi efficacement que possible et les rend particulièrement importantes pour les scénarios à volume élevé d’e/s.

## <a name="how-to-add-parallelism-to-async-code"></a>Comment ajouter un parallélisme à du Code asynchrone

Parfois, éventuellement besoin pour effectuer plusieurs tâches asynchrones en parallèle, collecter leurs résultats et les interpréter d’une certaine façon. `Async.Parallel` vous permet de procéder sans avoir besoin d’utiliser la bibliothèque parallèle de tâches, ce qui évite devoir forcer `Task<'T>` et `Async<'T>` types.

L’exemple suivant utilise `Async.Parallel` pour télécharger le code HTML à partir de quatre sites populaires en parallèle, attendez que ces tâches à effectuer, puis imprimer le code HTML qui a été téléchargé.

```fsharp
open System
open System.Net

let urlList =
    [ "https://www.microsoft.com"
      "https://www.google.com"
      "https://www.amazon.com"
      "https://www.facebook.com" ]

let fetchHtmlAsync url =
    async {
        let uri = Uri(url)
        use webClient = new WebClient()
        let! html = webClient.AsyncDownloadString(uri)
        return html
    }

let getHtmlList urls =
    urls
    |> Seq.map fetchHtmlAsync   // Build an Async<'T> for each site
    |> Async.Parallel           // Returns an Async<'T []>
    |> Async.RunSynchronously   // Wait for the result of the parallel work

let htmlList = getHtmlList urlList

// We now have the downloaded HTML for each site!
for html in htmlList do
    printfn "%s" html
```

## <a name="important-info-and-advice"></a>Informations et conseils importants

* Ajoutez « Async » à la fin de toutes les fonctions que vous allez consommer

 Bien qu’il s’agit simplement d’une convention d’affectation de noms, il simplifie les choses comme la détectabilité d’API. En particulier s’il existe des versions synchrones et asynchrones de la routine de même, il est judicieux de déclarer explicitement le c'est-à-dire asynchrone via le nom.

* Écouter le compilateur !

F#du compilateur est très strict, rendant presque impossible de faire quelque chose troublant comme exécuter « async » code de façon synchrone. Si vous avez un avertissement, qui est un signe que le code n’exécutera la façon dont vous pensez qu’elle soit. Si vous pouvez rendre le compilateur heureux, votre code s’exécutera probablement comme prévu.

## <a name="for-the-cvb-programmer-looking-into-f"></a>Pour le C#programmeur /VB étudiées F\#

Cette section suppose que vous êtes familiarisé avec le modèle async dans C#/VB. Si vous n’êtes pas, [de programmation asynchrone dans C# ](../../../csharp/async.md) est un point de départ.

Il existe une différence fondamentale entre la C#/VB async modèle et le F# modèle asynchrone.

Lorsque vous appelez une fonction qui retourne un `Task` ou `Task<'T>`, que le travail a déjà commencé l’exécution. Le handle retourné représente une tâche asynchrone en cours d’exécution. En revanche, lorsque vous appelez une fonction async F#, le `Async<'a>` retourné représente une tâche qui sera **généré** à un moment donné. Présentation de ce modèle est puissante, car elle permet des tâches asynchrones dans F# chaîner plus facilement, effectuée de manière conditionnelle et être démarrée avec une granularité plus fine du contrôle.

Il existe quelques autres similitudes et différences à noter.

### <a name="similarities"></a>Similitudes

* `let!`, `use!`, et `do!` sont analogues aux `await` lors de l’appel d’une tâche asynchrone à partir d’un `async{ }` bloc.

  Les trois mots clés ne peuvent être utilisées dans un `async { }` bloc, de façon similaire à la `await` ne peut être appelée à l’intérieur d’un `async` (méthode). En bref, `let!` concerne lorsque vous souhaitez capturer et utiliser un résultat, `use!` est similaire, mais quelque chose dont les ressources doivent obtenir nettoyés après qu’il est utilisé, et `do!` concerne lorsque vous souhaitez attendre d’un flux de travail asynchrone sans valeur de retour à la fin avant de continuer.

* F#prend en charge le parallélisme des données de manière similaire.

  Bien qu’il fonctionne très différemment, `Async.Parallel` correspond à `Task.WhenAll` pour le scénario de souhaitant les résultats d’un ensemble de travaux d’async lorsque toutes terminées.

### <a name="differences"></a>Différences

* Imbriqué `let!` n’est pas autorisé, contrairement à imbriqué `await`

  Contrairement aux `await`, qui peuvent être imbriqué indéfiniment, `let!` ne peut pas et doit avoir son résultat à lié avant de l’utiliser à l’intérieur d’un autre `let!`, `do!`, ou `use!`.

* Prise en charge l’annulation est plus simple dans F# que dans C#/VB.

  Prise en charge de l’annulation d’une tâche au milieu son exécution dans C#/VB nécessite la vérification le `IsCancellationRequested` propriété ou appeler `ThrowIfCancellationRequested()` sur un `CancellationToken` objet qui est passé à la méthode async.

En revanche, F# les workflows asynchrones sont plus naturellement pouvant être annulés. L’annulation est un processus en trois étapes simples.

1. Créez un `CancellationTokenSource`.
2. Transmettre une fonction de départ.
3. Appeler `Cancel` sur le jeton.

Exemple :

```fsharp
open System.Threading

// Create a workflow which will loop forever.
let workflow =
    async {
        while true do
            printfn "Working..."
            do! Async.Sleep 1000
    }

let tokenSource = new CancellationTokenSource()

// Start the workflow in the background
Async.Start (workflow, tokenSource.Token)

// Executing the next line will stop the workflow
tokenSource.Cancel()
```

C’est tout !

## <a name="further-resources"></a>Ressources supplémentaires :

* [Flux de travail asynchrone sur MSDN](https://msdn.microsoft.com/library/dd233250.aspx)
* [Séquences asynchrones pourF#](https://fsprojects.github.io/FSharp.Control.AsyncSeq/library/AsyncSeq.html)
* [F#Utilitaires de données HTTP](https://fsharp.github.io/FSharp.Data/library/Http.html)
