---
title: Flux de travail asynchrones (F#)
description: 'En savoir plus sur la prise en charge dans le langage de programmation pour l’exécution de calculs asynchrones, F # qui s’exécutent sans bloquer l’exécution d’autres tâches.'
ms.date: 05/16/2016
ms.openlocfilehash: 2a6d5f8b61d63a722744f8f71a037e8bc460c64f
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43861560"
---
# <a name="asynchronous-workflows"></a>Flux de travail asynchrones

> [!NOTE]
Le lien des informations de référence sur les API pointe vers MSDN.  Les informations de référence sur les API docs.microsoft.com ne sont pas terminées.

Cette rubrique décrit la prise en charge en F # pour l’exécution de calculs asynchrones, autrement dit, sans bloquer l’exécution d’autres tâches. Par exemple, les calculs asynchrones peuvent être utilisés pour écrire des applications qui ont des interfaces utilisateur restent réactives aux utilisateurs que l’application effectue un autre travail.

## <a name="syntax"></a>Syntaxe

```fsharp
async { expression }
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, le calcul représenté par `expression` est configuré pour exécuter de façon asynchrone, autrement dit, sans bloquer le thread actuel de calcul lorsque des opérations asynchrones de veille, les e/s et les autres opérations asynchrones sont effectuées. Les calculs asynchrones sont souvent démarrés dans un thread d’arrière-plan pendant que l’exécution se poursuit sur le thread actuel. Le type de l’expression est `Async<'T>`, où `'T` est le type retourné par l’expression lorsque le `return` mot clé est utilisé. Le code dans une telle expression est appelé un *bloc asynchrone*, ou *bloc async*.

Il existe plusieurs façons de programmation asynchrone et la [ `Async` ](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7) classe fournit des méthodes qui prennent en charge plusieurs scénarios. L’approche générale consiste à créer `Async` objets qui représentent le calcul ou les calculs que vous souhaitez exécuter de façon asynchrone et puis démarrer ces calculs en utilisant l’une des fonctions de déclenchement. Les diverses fonctions de déclenchement offrent différents moyens de l’exécution de calculs asynchrones et que celui que vous utilisez dépend de si vous souhaitez utiliser le thread actuel, un thread d’arrière-plan ou un objet de tâche .NET Framework, et s’il existe de continuation fonctions qui s’exécute quand la fin du calcul. Par exemple, pour démarrer un calcul asynchrone sur le thread actuel, vous pouvez utiliser [ `Async.StartImmediate` ](https://msdn.microsoft.com/library/2f71d1cc-187f-48cf-ac66-e7fda41c46e3). Lorsque vous démarrez un calcul asynchrone à partir du thread d’interface utilisateur, vous ne bloquez pas la boucle d’événement majeur qui traite les actions utilisateur telles que les séquences de touches et les activités de la souris, ainsi, votre application reste réactive.

## <a name="asynchronous-binding-by-using-let"></a>Liaison asynchrone à l’aide de let !

Dans un flux de travail asynchrone, certaines expressions et les opérations sont synchrones, et certaines sont des calculs plus longs sont conçus pour retourner un résultat de façon asynchrone. Lorsque vous appelez une méthode de façon asynchrone, au lieu d’un ordinaire `let` de liaison, vous utilisez `let!`. L’effet de `let!` consiste à activer l’exécution continue sur d’autres calculs ou threads tandis que le calcul est exécuté. Après le côté droit de la `let!` liaison retourne, le reste du workflow asynchrone reprend l’exécution.

Le code suivant montre la différence entre `let` et `let!`. La ligne de code qui utilise `let` crée simplement un calcul asynchrone en tant qu’objet que vous pouvez exécuter ultérieurement à l’aide, par exemple, `Async.StartImmediate` ou [ `Async.RunSynchronously` ](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b). La ligne de code qui utilise `let!` démarre le calcul, puis le thread est suspendu jusqu'à ce que le résultat soit disponible, à quel point l’exécution se poursuit.

```fsharp
// let just stores the result as an asynchronous operation.
let (result1 : Async<byte[]>) = stream.AsyncRead(bufferSize)
// let! completes the asynchronous operation and returns the data.
let! (result2 : byte[])  = stream.AsyncRead(bufferSize)
```

En plus de `let!`, vous pouvez utiliser `use!` pour effectuer des liaisons asynchrones. La différence entre `let!` et `use!` est identique à la différence entre `let` et `use`. Pour `use!`, l’objet est supprimé à la fermeture de la portée actuelle. Notez que dans la version actuelle du langage F #, `use!` n’autorise pas une valeur doivent être initialisées sur null, même si `use` est.

## <a name="asynchronous-primitives"></a>Primitives asynchrones

Une méthode qui effectue une seule tâche asynchrone et retourne le résultat est appelée un *primitive asynchrone*, et celles-ci sont conçues spécifiquement pour une utilisation avec `let!`. Plusieurs primitives asynchrones sont définies dans la bibliothèque principale F #. Deux de ces méthodes pour les applications Web est définies dans le module [ `Microsoft.FSharp.Control.WebExtensions` ](https://msdn.microsoft.com/library/95ef17bc-ee3f-44ba-8a11-c90fcf4cf003): [ `WebRequest.AsyncGetResponse` ](https://msdn.microsoft.com/library/09a60c31-e6e2-4b5c-ad23-92a86e50060c) et [ `WebClient.AsyncDownloadString` ](https://msdn.microsoft.com/library/8a85a9b7-f712-4cac-a0ce-0a797f8ea32a). Les deux primitives téléchargent des données à partir d’une page Web, en fonction de l’URL. `AsyncGetResponse` génère un `System.Net.WebResponse` objet, et `AsyncDownloadString` génère une chaîne qui représente le code HTML pour une page Web.

Plusieurs primitives pour les opérations d’e/s asynchrones sont inclus dans le [ `Microsoft.FSharp.Control.CommonExtensions` ](https://msdn.microsoft.com/library/2edb67cb-6814-4a30-849f-b6dbdd042396) module. Ces méthodes d’extension de la `System.IO.Stream` classe sont [ `Stream.AsyncRead` ](https://msdn.microsoft.com/library/85698aaa-bdda-47e6-abed-3730f59fda5e) et [ `Stream.AsyncWrite` ](https://msdn.microsoft.com/library/1b0a2751-e42a-47e1-bd27-020224adc618).

Vous pouvez également écrire vos propres primitives asynchrones en définissant une fonction dont le corps complet est placé dans un bloc async.

Pour utiliser les méthodes asynchrones dans le .NET Framework sont conçues pour d’autres modèles asynchrones avec le modèle de programmation asynchrone F #, vous créez une fonction qui retourne un F # `Async` objet. La bibliothèque F # a des fonctions qui rendent cela plus faciles à faire.

Un exemple d’utilisation de flux de travail asynchrones est inclus ici ; Il existe de nombreux autres dans la documentation pour les méthodes de la [classe Async](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7).

Cet exemple montre comment utiliser des flux de travail asynchrones pour effectuer des calculs en parallèle.

Dans l’exemple de code suivant, une fonction `fetchAsync` Obtient le texte HTML retourné à partir d’une requête Web. Le `fetchAsync` fonction contient un bloc de code asynchrone. Lorsqu’une liaison est faite au résultat d’une primitive asynchrone, dans ce cas [ `AsyncDownloadString` ](https://msdn.microsoft.com/library/8a85a9b7-f712-4cac-a0ce-0a797f8ea32a), let ! est utilisé au lieu de let.

Vous utilisez la fonction [ `Async.RunSynchronously` ](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b) pour exécuter une opération asynchrone et attendre son résultat. Par exemple, vous pouvez exécuter plusieurs opérations asynchrones en parallèle à l’aide de la [ `Async.Parallel` ](https://msdn.microsoft.com/library/aa9b0355-2d55-4858-b943-cbe428de9dc4) fonctionne conjointement avec le `Async.RunSynchronously` (fonction). Le `Async.Parallel` fonction prend une liste de la `Async` des objets, définit le code pour chaque `Async` objet tâche à exécuter en parallèle et retourne un `Async` objet qui représente le calcul parallèle. Comme pour une seule opération, vous appelez `Async.RunSynchronously` pour démarrer l’exécution.

Le `runAll` fonction lance trois flux de travail asynchrones en parallèle et attend jusqu'à ce que ceux-ci ont terminé.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet8003.fs)]

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Expressions de calcul](computation-expressions.md)
- [Control.Async, classe](https://msdn.microsoft.com/visualfsharpdocs/conceptual/control.async-class-%5bfsharp%5d)
