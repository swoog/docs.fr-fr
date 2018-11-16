---
title: Programmation asynchroneF#
description: Découvrez comment F# programmation asynchrone est effectuée via un modèle de programmation au niveau du langage qui est facile à utiliser et plus naturel pour la langue.
ms.date: 06/20/2016
ms.openlocfilehash: de07f1252df56e3dfec5ea7a34a283b1c9508523
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "50195058"
---
# <a name="async-programming-in-f"></a><span data-ttu-id="e7eba-103">Programmation asynchroneF#</span><span class="sxs-lookup"><span data-stu-id="e7eba-103">Async Programming in F#</span></span> #

> [!NOTE]
> <span data-ttu-id="e7eba-104">Certains des inexactitudes ont été découverts dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e7eba-104">Some inaccuracies have been discovered in this article.</span></span>  <span data-ttu-id="e7eba-105">Il est en cours de réécriture.</span><span class="sxs-lookup"><span data-stu-id="e7eba-105">It is being rewritten.</span></span>  <span data-ttu-id="e7eba-106">Consultez [problème #666](https://github.com/dotnet/docs/issues/666) pour en savoir plus sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="e7eba-106">See [Issue #666](https://github.com/dotnet/docs/issues/666) to learn about the changes.</span></span>

<span data-ttu-id="e7eba-107">Programmation asynchrone F# peuvent être exécutées via un modèle de programmation au niveau du langage conçu pour être facile à utiliser et naturel de la langue.</span><span class="sxs-lookup"><span data-stu-id="e7eba-107">Async programming in F# can be accomplished through a language-level programming model designed to be easy to use and natural to the language.</span></span>

<span data-ttu-id="e7eba-108">Le cœur de la programmation asynchrone F# est `Async<'T>`, une représentation sous forme de travail qui peut être déclenchée pour exécuter en arrière-plan, où `'T` est soit le type retourné par le biais de spéciale `return` mot clé ou `unit` si le flux de travail asynchrones n’a aucun résultat à retourner.</span><span class="sxs-lookup"><span data-stu-id="e7eba-108">The core of async programming in F# is `Async<'T>`, a representation of work that can be triggered to run in the background, where `'T` is either the type returned via the special `return` keyword or `unit` if the async workflow has no result to return.</span></span>

<span data-ttu-id="e7eba-109">Le concept clé à comprendre est que le type d’une expression async est `Async<'T>`, qui est simplement un _spécification_ de travail à faire dans un contexte asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e7eba-109">The key concept to understand is that an async expression’s type is `Async<'T>`, which is merely a _specification_ of work to be done in an asynchronous context.</span></span> <span data-ttu-id="e7eba-110">Il n’est pas exécuté jusqu'à ce que vous le démarrez explicitement avec une des fonctions de départ (tel que `Async.RunSynchronously`).</span><span class="sxs-lookup"><span data-stu-id="e7eba-110">It is not executed until you explicitly start it with one of the starting functions (such as `Async.RunSynchronously`).</span></span> <span data-ttu-id="e7eba-111">Bien qu’il s’agit d’une autre manière de penser à travailler, il finit par être assez simple dans la pratique.</span><span class="sxs-lookup"><span data-stu-id="e7eba-111">Although this is a different way of thinking about doing work, it ends up being quite simple in practice.</span></span>

<span data-ttu-id="e7eba-112">Par exemple, supposons que vous souhaitez télécharger le code HTML à partir de dotnetfoundation.org sans bloquer le thread principal.</span><span class="sxs-lookup"><span data-stu-id="e7eba-112">For example, say you wanted to download the HTML from dotnetfoundation.org without blocking the main thread.</span></span> <span data-ttu-id="e7eba-113">Vous pouvez le faire comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7eba-113">You can accomplish it like this:</span></span>

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

<span data-ttu-id="e7eba-114">C’est tout !</span><span class="sxs-lookup"><span data-stu-id="e7eba-114">And that’s it!</span></span> <span data-ttu-id="e7eba-115">À part l’utilisation de `async`, `let!`, et `return`, il s’agit simplement normal F# code.</span><span class="sxs-lookup"><span data-stu-id="e7eba-115">Aside from the use of `async`, `let!`, and `return`, this is just normal F# code.</span></span>

<span data-ttu-id="e7eba-116">Il existe quelques constructions syntaxiques qui méritent votre attention :</span><span class="sxs-lookup"><span data-stu-id="e7eba-116">There are a few syntactical constructs which are worth noting:</span></span>

*   <span data-ttu-id="e7eba-117">`let!` lie le résultat d’une expression async (qui s’exécute sur un autre contexte).</span><span class="sxs-lookup"><span data-stu-id="e7eba-117">`let!` binds the result of an async expression (which runs on another context).</span></span>
*   <span data-ttu-id="e7eba-118">`use!` fonctionne comme `let!`, mais supprime ses ressources liées lorsqu’il devient hors de portée.</span><span class="sxs-lookup"><span data-stu-id="e7eba-118">`use!` works just like `let!`, but disposes its bound resources when it goes out of scope.</span></span>
*   <span data-ttu-id="e7eba-119">`do!` un flux de travail asynchrone qui ne retourne rien attendra.</span><span class="sxs-lookup"><span data-stu-id="e7eba-119">`do!` will await an async workflow which doesn’t return anything.</span></span>
*   <span data-ttu-id="e7eba-120">`return` renvoie simplement un résultat à partir d’une expression async.</span><span class="sxs-lookup"><span data-stu-id="e7eba-120">`return` simply returns a result from an async expression.</span></span>
*   <span data-ttu-id="e7eba-121">`return!` exécute un autre flux de travail asynchrone et retourne sa valeur de retour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e7eba-121">`return!` executes another async workflow and returns its return value as a result.</span></span>

<span data-ttu-id="e7eba-122">En outre, normal `let`, `use`, et `do` mots clés peuvent être utilisés avec les versions async comme ils le feraient dans une fonction normale.</span><span class="sxs-lookup"><span data-stu-id="e7eba-122">Additionally, normal `let`, `use`, and `do` keywords can be used alongside the async versions just as they would in a normal function.</span></span>

## <a name="how-to-start-async-code-in-f"></a><span data-ttu-id="e7eba-123">Comment démarrer le Code asynchrone dansF#</span><span class="sxs-lookup"><span data-stu-id="e7eba-123">How to start Async Code in F#</span></span> #

<span data-ttu-id="e7eba-124">Comme mentionné précédemment, le code asynchrone est une spécification de travail à faire dans un autre contexte qui doit être démarrée explicitement.</span><span class="sxs-lookup"><span data-stu-id="e7eba-124">As mentioned earlier, async code is a specification of work to be done in another context which needs to be explicitly started.</span></span> <span data-ttu-id="e7eba-125">Voici deux méthodes principales pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="e7eba-125">Here are two primary ways to accomplish this:</span></span>

1.  <span data-ttu-id="e7eba-126">`Async.RunSynchronously` démarre un flux de travail asynchrone sur un autre thread et attend son résultat.</span><span class="sxs-lookup"><span data-stu-id="e7eba-126">`Async.RunSynchronously` will start an async workflow on another thread and await its result.</span></span>

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

2.  <span data-ttu-id="e7eba-127">`Async.Start` démarre un flux de travail asynchrone sur un autre thread et sera **pas** attend son résultat.</span><span class="sxs-lookup"><span data-stu-id="e7eba-127">`Async.Start` will start an async workflow on another thread, and will **not** await its result.</span></span>

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

<span data-ttu-id="e7eba-128">Il existe plusieurs manières pour démarrer un flux de travail asynchrones disponible pour des scénarios plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e7eba-128">There are other ways to start an async workflow available for more specific scenarios.</span></span> <span data-ttu-id="e7eba-129">Elles sont détaillées [dans la référence Async](https://msdn.microsoft.com/library/ee370232.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7eba-129">They are detailed [in the Async reference](https://msdn.microsoft.com/library/ee370232.aspx).</span></span>

### <a name="a-note-on-threads"></a><span data-ttu-id="e7eba-130">Remarque sur les Threads</span><span class="sxs-lookup"><span data-stu-id="e7eba-130">A Note on Threads</span></span>

<span data-ttu-id="e7eba-131">La phrase « dans un autre thread » est mentionnée ci-dessus, mais il est important de savoir que **cela ne signifie pas que les workflows asynchrones sont une façade pour le multithreading**.</span><span class="sxs-lookup"><span data-stu-id="e7eba-131">The phrase "on another thread" is mentioned above, but it is important to know that **this does not mean that async workflows are a facade for multithreading**.</span></span> <span data-ttu-id="e7eba-132">Le flux de travail réellement « passe » entre les threads, les emprunts pour une petite quantité de temps pour effectuer des tâches utiles.</span><span class="sxs-lookup"><span data-stu-id="e7eba-132">The workflow actually "jumps" between threads, borrowing them for a small amount of time to do useful work.</span></span> <span data-ttu-id="e7eba-133">Lorsqu’un flux de travail asynchrone est en fait « en attente » (par exemple, un appel réseau renvoyer quelque chose), n’importe quel thread qu'au moment où il a été d’emprunt est libérée jusqu'à accédez effectuer des tâches utiles sur autre chose.</span><span class="sxs-lookup"><span data-stu-id="e7eba-133">When an async workflow is effectively "waiting" (for example, waiting for a network call to return something), any thread it was borrowing at the time is freed up to go do useful work on something else.</span></span> <span data-ttu-id="e7eba-134">Cela permet aux workflows asynchrones utilisent le système, sur qu'elles s’exécutent aussi efficacement que possible et les rend particulièrement importantes pour les scénarios à volume élevé d’e/s.</span><span class="sxs-lookup"><span data-stu-id="e7eba-134">This allows async workflows to utilize the system they run on as effectively as possible, and makes them especially strong for high-volume I/O scenarios.</span></span>

## <a name="how-to-add-parallelism-to-async-code"></a><span data-ttu-id="e7eba-135">Comment ajouter un parallélisme à du Code asynchrone</span><span class="sxs-lookup"><span data-stu-id="e7eba-135">How to Add Parallelism to Async Code</span></span>

<span data-ttu-id="e7eba-136">Parfois, éventuellement besoin pour effectuer plusieurs tâches asynchrones en parallèle, collecter leurs résultats et les interpréter d’une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="e7eba-136">Sometimes you may need to perform multiple asynchronous jobs in parallel, collect their results, and interpret them in some way.</span></span> <span data-ttu-id="e7eba-137">`Async.Parallel` vous permet de procéder sans avoir besoin d’utiliser la bibliothèque parallèle de tâches, ce qui évite devoir forcer `Task<'T>` et `Async<'T>` types.</span><span class="sxs-lookup"><span data-stu-id="e7eba-137">`Async.Parallel` allows you to do this without needing to use the Task Parallel Library, which would involve needing to coerce `Task<'T>` and `Async<'T>` types.</span></span>

<span data-ttu-id="e7eba-138">L’exemple suivant utilise `Async.Parallel` pour télécharger le code HTML à partir de quatre sites populaires en parallèle, attendez que ces tâches à effectuer, puis imprimer le code HTML qui a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="e7eba-138">The following example will use `Async.Parallel` to download the HTML from four popular sites in parallel, wait for those tasks to complete, and then print the HTML which was downloaded.</span></span>

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

## <a name="important-info-and-advice"></a><span data-ttu-id="e7eba-139">Informations et conseils importants</span><span class="sxs-lookup"><span data-stu-id="e7eba-139">Important Info and Advice</span></span>

*   <span data-ttu-id="e7eba-140">Ajoutez « Async » à la fin de toutes les fonctions que vous allez consommer</span><span class="sxs-lookup"><span data-stu-id="e7eba-140">Append "Async" to the end of any functions you’ll consume</span></span>

 <span data-ttu-id="e7eba-141">Bien qu’il s’agit simplement d’une convention d’affectation de noms, il simplifie les choses comme la détectabilité d’API.</span><span class="sxs-lookup"><span data-stu-id="e7eba-141">Although this is just a naming convention, it does make things like API discoverability easier.</span></span> <span data-ttu-id="e7eba-142">En particulier s’il existe des versions synchrones et asynchrones de la routine de même, il est judicieux de déclarer explicitement le c'est-à-dire asynchrone via le nom.</span><span class="sxs-lookup"><span data-stu-id="e7eba-142">Particularly if there are synchronous and asynchronous versions of the same routine, it’s a good idea to explicitly state which is asynchronous via the name.</span></span>

*   <span data-ttu-id="e7eba-143">Écouter le compilateur !</span><span class="sxs-lookup"><span data-stu-id="e7eba-143">Listen to the compiler!</span></span>

 <span data-ttu-id="e7eba-144">F#du compilateur est très strict, rendant presque impossible de faire quelque chose troublant comme exécuter « async » code de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="e7eba-144">F#’s compiler is very strict, making it nearly impossible to do something troubling like run "async" code synchronously.</span></span> <span data-ttu-id="e7eba-145">Si vous avez un avertissement, qui est un signe que le code n’exécutera la façon dont vous pensez qu’elle soit.</span><span class="sxs-lookup"><span data-stu-id="e7eba-145">If you come across a warning, that’s a sign that the code won’t execute how you think it will.</span></span> <span data-ttu-id="e7eba-146">Si vous pouvez rendre le compilateur heureux, votre code s’exécutera probablement comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e7eba-146">If you can make the compiler happy, your code will most likely execute as expected.</span></span>

## <a name="for-the-cvb-programmer-looking-into-f"></a><span data-ttu-id="e7eba-147">Pour le C#programmeur /VB étudiéesF#</span><span class="sxs-lookup"><span data-stu-id="e7eba-147">For the C#/VB Programmer Looking Into F#</span></span> #

<span data-ttu-id="e7eba-148">Cette section suppose que vous êtes familiarisé avec le modèle async dans C#/VB.</span><span class="sxs-lookup"><span data-stu-id="e7eba-148">This section assumes you’re familiar with the async model in C#/VB.</span></span> <span data-ttu-id="e7eba-149">Si vous n’êtes pas, [de programmation asynchrone dans C# ](../../../csharp/async.md) est un point de départ.</span><span class="sxs-lookup"><span data-stu-id="e7eba-149">If you are not, [Async Programming in C#](../../../csharp/async.md) is a starting point.</span></span>

<span data-ttu-id="e7eba-150">Il existe une différence fondamentale entre la C#/VB async modèle et le F# modèle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e7eba-150">There is a fundamental difference between the C#/VB async model and the F# async model.</span></span>

<span data-ttu-id="e7eba-151">Lorsque vous appelez une fonction qui retourne un `Task` ou `Task<'T>`, que le travail a déjà commencé l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e7eba-151">When you call a function which returns a `Task` or `Task<'T>`, that job has already begun execution.</span></span> <span data-ttu-id="e7eba-152">Le handle retourné représente une tâche asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e7eba-152">The handle returned represents an already-running asynchronous job.</span></span> <span data-ttu-id="e7eba-153">En revanche, lorsque vous appelez une fonction async F#, le `Async<'a>` retourné représente une tâche qui sera **généré** à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="e7eba-153">In contrast, when you call an async function in F#, the `Async<'a>` returned represents a job which will be **generated** at some point.</span></span> <span data-ttu-id="e7eba-154">Présentation de ce modèle est puissante, car elle permet des tâches asynchrones dans F# chaîner plus facilement, effectuée de manière conditionnelle et être démarrée avec une granularité plus fine du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e7eba-154">Understanding this model is powerful, because it allows for asynchronous jobs in F# to be chained together easier, performed conditionally, and be started with a finer grain of control.</span></span>

<span data-ttu-id="e7eba-155">Il existe quelques autres similitudes et différences à noter.</span><span class="sxs-lookup"><span data-stu-id="e7eba-155">There are a few other similarities and differences worth noting.</span></span>

### <a name="similarities"></a><span data-ttu-id="e7eba-156">Similitudes</span><span class="sxs-lookup"><span data-stu-id="e7eba-156">Similarities</span></span>

*   <span data-ttu-id="e7eba-157">`let!`, `use!`, et `do!` sont analogues aux `await` lors de l’appel d’une tâche asynchrone à partir d’un `async{ }` bloc.</span><span class="sxs-lookup"><span data-stu-id="e7eba-157">`let!`, `use!`, and `do!` are analogous to `await` when calling an async job from within an `async{ }` block.</span></span>

 <span data-ttu-id="e7eba-158">Les trois mots clés ne peuvent être utilisées dans un `async { }` bloc, de façon similaire à la `await` ne peut être appelée à l’intérieur d’un `async` (méthode).</span><span class="sxs-lookup"><span data-stu-id="e7eba-158">The three keywords can only be used within an `async { }` block, similar to how `await` can only be invoked inside an `async` method.</span></span> <span data-ttu-id="e7eba-159">En bref, `let!` concerne lorsque vous souhaitez capturer et utiliser un résultat, `use!` est similaire, mais quelque chose dont les ressources doivent obtenir nettoyés après qu’il est utilisé, et `do!` concerne lorsque vous souhaitez attendre d’un flux de travail asynchrone sans valeur de retour à la fin avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="e7eba-159">In short, `let!` is for when you want to capture and use a result, `use!` is the same but for something whose resources should get cleaned after it’s used, and `do!` is for when you want to wait for an async workflow with no return value to finish before moving on.</span></span>

*   <span data-ttu-id="e7eba-160">F#prend en charge le parallélisme des données de manière similaire.</span><span class="sxs-lookup"><span data-stu-id="e7eba-160">F# supports data-parallelism in a similar way.</span></span>

 <span data-ttu-id="e7eba-161">Bien qu’il fonctionne très différemment, `Async.Parallel` correspond à `Task.WhenAll` pour le scénario de souhaitant les résultats d’un ensemble de travaux d’async lorsque toutes terminées.</span><span class="sxs-lookup"><span data-stu-id="e7eba-161">Although it operates very differently, `Async.Parallel` corresponds to `Task.WhenAll` for the scenario of wanting the results of a set of async jobs when they all complete.</span></span>

### <a name="differences"></a><span data-ttu-id="e7eba-162">Différences</span><span class="sxs-lookup"><span data-stu-id="e7eba-162">Differences</span></span>

*   <span data-ttu-id="e7eba-163">Imbriqué `let!` n’est pas autorisé, contrairement à imbriqué `await`</span><span class="sxs-lookup"><span data-stu-id="e7eba-163">Nested `let!` is not allowed, unlike nested `await`</span></span>

 <span data-ttu-id="e7eba-164">Contrairement aux `await`, qui peuvent être imbriqué indéfiniment, `let!` ne peut pas et doit avoir son résultat à lié avant de l’utiliser à l’intérieur d’un autre `let!`, `do!`, ou `use!`.</span><span class="sxs-lookup"><span data-stu-id="e7eba-164">Unlike `await`, which can be nested indefinitely, `let!` cannot and must have its result bound before using it inside of another `let!`, `do!`, or `use!`.</span></span>

*   <span data-ttu-id="e7eba-165">Prise en charge l’annulation est plus simple dans F# que dans C#/VB.</span><span class="sxs-lookup"><span data-stu-id="e7eba-165">Cancellation support is simpler in F# than in C#/VB.</span></span>

 <span data-ttu-id="e7eba-166">Prise en charge de l’annulation d’une tâche au milieu son exécution dans C#/VB nécessite la vérification le `IsCancellationRequested` propriété ou appeler `ThrowIfCancellationRequested()` sur un `CancellationToken` objet qui est passé à la méthode async.</span><span class="sxs-lookup"><span data-stu-id="e7eba-166">Supporting cancellation of a task midway through its execution in C#/VB requires checking the `IsCancellationRequested` property or calling `ThrowIfCancellationRequested()` on a `CancellationToken` object that’s passed into the async method.</span></span>

<span data-ttu-id="e7eba-167">En revanche, F# les workflows asynchrones sont plus naturellement pouvant être annulés.</span><span class="sxs-lookup"><span data-stu-id="e7eba-167">In contrast, F# async workflows are more naturally cancellable.</span></span> <span data-ttu-id="e7eba-168">L’annulation est un processus en trois étapes simples.</span><span class="sxs-lookup"><span data-stu-id="e7eba-168">Cancellation is a simple three-step process.</span></span>

1.  <span data-ttu-id="e7eba-169">Créez un `CancellationTokenSource`.</span><span class="sxs-lookup"><span data-stu-id="e7eba-169">Create a new `CancellationTokenSource`.</span></span>
2.  <span data-ttu-id="e7eba-170">Transmettre une fonction de départ.</span><span class="sxs-lookup"><span data-stu-id="e7eba-170">Pass it into a starting function.</span></span>
3.  <span data-ttu-id="e7eba-171">Appeler `Cancel` sur le jeton.</span><span class="sxs-lookup"><span data-stu-id="e7eba-171">Call `Cancel` on the token.</span></span>

<span data-ttu-id="e7eba-172">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e7eba-172">Example:</span></span>

```fsharp
open System
open System.Net
open System.Threading

let uploadDataAsync url data = 
    async {
        let uri = Uri(url)
        use webClient = new WebClient()
        webClient.UploadStringAsync(uri, data)
    }

let workflow = uploadDataAsync "https://url-to-upload-to.com" "hello, world!"

let token = new CancellationTokenSource()
Async.Start (workflow, token.Token)

// Immediately cancel uploadDataAsync after it's been started.
token.Cancel()
```

<span data-ttu-id="e7eba-173">C’est tout !</span><span class="sxs-lookup"><span data-stu-id="e7eba-173">And that’s it!</span></span>

## <a name="further-resources"></a><span data-ttu-id="e7eba-174">Ressources supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="e7eba-174">Further resources:</span></span>

*   [<span data-ttu-id="e7eba-175">Flux de travail asynchrone sur MSDN</span><span class="sxs-lookup"><span data-stu-id="e7eba-175">Async Workflows on MSDN</span></span>](https://msdn.microsoft.com/library/dd233250.aspx)
*   [<span data-ttu-id="e7eba-176">Séquences asynchrones pourF#</span><span class="sxs-lookup"><span data-stu-id="e7eba-176">Asynchronous Sequences for F#</span></span>](https://fsprojects.github.io/FSharp.Control.AsyncSeq/library/AsyncSeq.html)
*   [<span data-ttu-id="e7eba-177">F#Utilitaires de données HTTP</span><span class="sxs-lookup"><span data-stu-id="e7eba-177">F# Data HTTP Utilities</span></span>](https://fsharp.github.io/FSharp.Data/library/Http.html)
