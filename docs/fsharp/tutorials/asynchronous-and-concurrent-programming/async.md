---
title: 'Programmation asynchrone en F #'
description: 'Découvrez comment F # de programmation asynchrone est effectuée via un modèle de programmation au niveau du langage qui est facile à utiliser et naturelle à la langue.'
author: cartermp
ms.author: phcart
ms.date: 06/20/2016
ms.topic: conceptual
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: a3047b98637cb4b142f374a2a2b5e7270e850fd6
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="async-programming-in-f"></a><span data-ttu-id="b9947-103">Programmation asynchrone en F #</span><span class="sxs-lookup"><span data-stu-id="b9947-103">Async Programming in F#</span></span> #

> [!NOTE]
> <span data-ttu-id="b9947-104">Certaines inexactitudes ont été détectés dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b9947-104">Some inaccuracies have been discovered in this article.</span></span>  <span data-ttu-id="b9947-105">Il est en cours de réécriture.</span><span class="sxs-lookup"><span data-stu-id="b9947-105">It is being rewritten.</span></span>  <span data-ttu-id="b9947-106">Consultez [problème #666](https://github.com/dotnet/docs/issues/666) pour en savoir plus sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="b9947-106">See [Issue #666](https://github.com/dotnet/docs/issues/666) to learn about the changes.</span></span>

<span data-ttu-id="b9947-107">Programmation F # asynchrone peut être obtenue via un modèle de programmation au niveau du langage conçu pour être facile à utiliser et naturelle à la langue.</span><span class="sxs-lookup"><span data-stu-id="b9947-107">Async programming in F# can be accomplished through a language-level programming model designed to be easy to use and natural to the language.</span></span>

<span data-ttu-id="b9947-108">Le cœur de la programmation asynchrone en F # est `Async<'T>`, une représentation sous forme de travail qui peut être déclenchée pour s’exécuter en arrière-plan, où `'T` est soit le type retourné via spéciale `return` mot clé ou `unit` si le flux de travail asynchrone n’a pas résultat à retourner.</span><span class="sxs-lookup"><span data-stu-id="b9947-108">The core of async programming in F# is `Async<'T>`, a representation of work that can be triggered to run in the background, where `'T` is either the type returned via the special `return` keyword or `unit` if the async workflow has no result to return.</span></span>

<span data-ttu-id="b9947-109">Comprendre le concept essentiel est que le type d’une expression async est `Async<'T>`, qui est simplement un _spécification_ de travail à faire dans un contexte asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b9947-109">The key concept to understand is that an async expression’s type is `Async<'T>`, which is merely a _specification_ of work to be done in an asynchronous context.</span></span> <span data-ttu-id="b9947-110">Il n’est pas exécuté jusqu'à ce que vous le démarrez explicitement avec une des fonctions de départ (tel que `Async.RunSynchronously`).</span><span class="sxs-lookup"><span data-stu-id="b9947-110">It is not executed until you explicitly start it with one of the starting functions (such as `Async.RunSynchronously`).</span></span> <span data-ttu-id="b9947-111">Bien qu’il s’agit d’une autre façon de réfléchir à travailler, il finit par être très simple dans la pratique.</span><span class="sxs-lookup"><span data-stu-id="b9947-111">Although this is a different way of thinking about doing work, it ends up being quite simple in practice.</span></span>

<span data-ttu-id="b9947-112">Par exemple, que vous vouliez télécharger le code HTML à partir de dotnetfoundation.org sans bloquer le thread principal.</span><span class="sxs-lookup"><span data-stu-id="b9947-112">For example, say you wanted to download the HTML from dotnetfoundation.org without blocking the main thread.</span></span> <span data-ttu-id="b9947-113">Vous pouvez l’atteindre comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9947-113">You can accomplish it like this:</span></span>

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

<span data-ttu-id="b9947-114">C’est tout !</span><span class="sxs-lookup"><span data-stu-id="b9947-114">And that’s it!</span></span> <span data-ttu-id="b9947-115">À l’exception de l’utilisation de `async`, `let!`, et `return`, il s’agit simplement normale du code F #.</span><span class="sxs-lookup"><span data-stu-id="b9947-115">Aside from the use of `async`, `let!`, and `return`, this is just normal F# code.</span></span>

<span data-ttu-id="b9947-116">Il existe quelques constructions syntaxiques qui sont à noter :</span><span class="sxs-lookup"><span data-stu-id="b9947-116">There are a few syntactical constructs which are worth noting:</span></span>

*   <span data-ttu-id="b9947-117">`let!` lie le résultat d’une expression async (qui s’exécute sur un autre contexte).</span><span class="sxs-lookup"><span data-stu-id="b9947-117">`let!` binds the result of an async expression (which runs on another context).</span></span>
*   <span data-ttu-id="b9947-118">`use!` fonctionne comme `let!`, mais supprime ses ressources liées lorsqu’il devient hors de portée.</span><span class="sxs-lookup"><span data-stu-id="b9947-118">`use!` works just like `let!`, but disposes its bound resources when it goes out of scope.</span></span>
*   <span data-ttu-id="b9947-119">`do!` un flux de travail asynchrone qui ne retourne rien attendra.</span><span class="sxs-lookup"><span data-stu-id="b9947-119">`do!` will await an async workflow which doesn’t return anything.</span></span>
*   <span data-ttu-id="b9947-120">`return` simplement retourne un résultat d’une expression asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b9947-120">`return` simply returns a result from an async expression.</span></span>
*   <span data-ttu-id="b9947-121">`return!` exécute un autre flux de travail asynchrone et retourne sa valeur de retour comme résultat.</span><span class="sxs-lookup"><span data-stu-id="b9947-121">`return!` executes another async workflow and returns its return value as a result.</span></span>

<span data-ttu-id="b9947-122">En outre, normal `let`, `use`, et `do` mots clés peuvent être utilisés avec les versions asynchrones, comme ils le feraient dans une fonction normale.</span><span class="sxs-lookup"><span data-stu-id="b9947-122">Additionally, normal `let`, `use`, and `do` keywords can be used alongside the async versions just as they would in a normal function.</span></span>

## <a name="how-to-start-async-code-in-f"></a><span data-ttu-id="b9947-123">Comment démarrer le Code asynchrone en F #</span><span class="sxs-lookup"><span data-stu-id="b9947-123">How to start Async Code in F#</span></span> #

<span data-ttu-id="b9947-124">Comme mentionné précédemment, code asynchrone est une spécification de travail à effectuer dans un autre contexte, qui doit être démarrée explicitement.</span><span class="sxs-lookup"><span data-stu-id="b9947-124">As mentioned earlier, async code is a specification of work to be done in another context which needs to be explicitly started.</span></span> <span data-ttu-id="b9947-125">Voici deux façons d’y parvenir :</span><span class="sxs-lookup"><span data-stu-id="b9947-125">Here are two primary ways to accomplish this:</span></span>

1.  <span data-ttu-id="b9947-126">`Async.RunSynchronously` démarre un flux de travail asynchrone sur un autre thread et attend son résultat.</span><span class="sxs-lookup"><span data-stu-id="b9947-126">`Async.RunSynchronously` will start an async workflow on another thread and await its result.</span></span>

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

2.  <span data-ttu-id="b9947-127">`Async.Start` démarre un flux de travail asynchrone sur un autre thread et seront **pas** attend son résultat.</span><span class="sxs-lookup"><span data-stu-id="b9947-127">`Async.Start` will start an async workflow on another thread, and will **not** await its result.</span></span>

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

<span data-ttu-id="b9947-128">Autres manières de démarrer un flux de travail asynchrones disponible pour des scénarios plus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b9947-128">There are other ways to start an async workflow available for more specific scenarios.</span></span> <span data-ttu-id="b9947-129">Elles sont décrites en détail [dans la référence Async](https://msdn.microsoft.com/library/ee370232.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9947-129">They are detailed [in the Async reference](https://msdn.microsoft.com/library/ee370232.aspx).</span></span>

### <a name="a-note-on-threads"></a><span data-ttu-id="b9947-130">Remarque sur les Threads</span><span class="sxs-lookup"><span data-stu-id="b9947-130">A Note on Threads</span></span>

<span data-ttu-id="b9947-131">La phrase « dans un autre thread » est mentionnée ci-dessus, mais il est important de savoir que **cela ne signifie pas que le flux de travail asynchrone est façade pour le multithreading**.</span><span class="sxs-lookup"><span data-stu-id="b9947-131">The phrase "on another thread" is mentioned above, but it is important to know that **this does not mean that async workflows are a facade for multithreading**.</span></span> <span data-ttu-id="b9947-132">Le flux de travail réellement « accède » entre les threads, les emprunts pour une petite quantité de temps nécessaire pour effectuer des tâches utiles.</span><span class="sxs-lookup"><span data-stu-id="b9947-132">The workflow actually "jumps" between threads, borrowing them for a small amount of time to do useful work.</span></span> <span data-ttu-id="b9947-133">Lorsqu’un flux de travail asynchrone est effectivement « en attente » (par exemple, un appel réseau retourner un élément), n’importe quel thread qu'au moment où il a été d’emprunt est libérée jusqu'à accédez effectuez des tâches utiles sur autre chose.</span><span class="sxs-lookup"><span data-stu-id="b9947-133">When an async workflow is effectively "waiting" (for example, waiting for a network call to return something), any thread it was borrowing at the time is freed up to go do useful work on something else.</span></span> <span data-ttu-id="b9947-134">Cela permet aux workflows asynchrones d’utiliser le système, sur qu'elles s’exécutent aussi efficacement que possible et les rend particulièrement fort pour les scénarios d’e/s élevées.</span><span class="sxs-lookup"><span data-stu-id="b9947-134">This allows async workflows to utilize the system they run on as effectively as possible, and makes them especially strong for high-volume I/O scenarios.</span></span>

## <a name="how-to-add-parallelism-to-async-code"></a><span data-ttu-id="b9947-135">L’ajout de parallélisme à Code asynchrone</span><span class="sxs-lookup"><span data-stu-id="b9947-135">How to Add Parallelism to Async Code</span></span>

<span data-ttu-id="b9947-136">Parfois éventuellement besoin pour effectuer plusieurs tâches asynchrones en parallèle, collecter leurs résultats et les interpréter d’une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="b9947-136">Sometimes you may need to perform multiple asynchronous jobs in parallel, collect their results, and interpret them in some way.</span></span> <span data-ttu-id="b9947-137">`Async.Parallel` vous permet de faire sans devoir utiliser la bibliothèque parallèle de tâches, ce qui évite d’avoir à forcer `Task<'T>` et `Async<'T>` types.</span><span class="sxs-lookup"><span data-stu-id="b9947-137">`Async.Parallel` allows you to do this without needing to use the Task Parallel Library, which would involve needing to coerce `Task<'T>` and `Async<'T>` types.</span></span>

<span data-ttu-id="b9947-138">L’exemple suivant utilise `Async.Parallel` pour télécharger le code HTML à partir de quatre sites populaires en parallèle, attendez que ces tâches à effectuer, puis l’imprimer le code HTML qui a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="b9947-138">The following example will use `Async.Parallel` to download the HTML from four popular sites in parallel, wait for those tasks to complete, and then print the HTML which was downloaded.</span></span>

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

## <a name="important-info-and-advice"></a><span data-ttu-id="b9947-139">Informations et conseils importants</span><span class="sxs-lookup"><span data-stu-id="b9947-139">Important Info and Advice</span></span>

*   <span data-ttu-id="b9947-140">Ajoutez « Async » à la fin de toutes les fonctions que vous allez utiliser</span><span class="sxs-lookup"><span data-stu-id="b9947-140">Append "Async" to the end of any functions you’ll consume</span></span>

 <span data-ttu-id="b9947-141">Bien qu’il s’agit simplement d’une convention d’affectation de noms, elle simplifie choses comme les API détectabilité.</span><span class="sxs-lookup"><span data-stu-id="b9947-141">Although this is just a naming convention, it does make things like API discoverability easier.</span></span> <span data-ttu-id="b9947-142">En particulier s’il existe des versions synchrones et asynchrones de la routine de même, il est judicieux de déclarer explicitement qui est asynchrone via le nom.</span><span class="sxs-lookup"><span data-stu-id="b9947-142">Particularly if there are synchronous and asynchronous versions of the same routine, it’s a good idea to explicitly state which is asynchronous via the name.</span></span>

*   <span data-ttu-id="b9947-143">Écouter le compilateur !</span><span class="sxs-lookup"><span data-stu-id="b9947-143">Listen to the compiler!</span></span>

 <span data-ttu-id="b9947-144">Compilateur F # est très stricte, rend pratiquement impossible d’effectuer une action troubling comme exécuter « async » code synchrone.</span><span class="sxs-lookup"><span data-stu-id="b9947-144">F#’s compiler is very strict, making it nearly impossible to do something troubling like run "async" code synchronously.</span></span> <span data-ttu-id="b9947-145">Si vous avez un avertissement, qui est un signe que le code ne sera pas exécuté comment vous pensez qu’il sera.</span><span class="sxs-lookup"><span data-stu-id="b9947-145">If you come across a warning, that’s a sign that the code won’t execute how you think it will.</span></span> <span data-ttu-id="b9947-146">Si le compilateur peut rendre heureux, votre code s’exécutera probablement comme prévu.</span><span class="sxs-lookup"><span data-stu-id="b9947-146">If you can make the compiler happy, your code will most likely execute as expected.</span></span>

## <a name="for-the-cvb-programmer-looking-into-f"></a><span data-ttu-id="b9947-147">Pour un programmeur C# /Visual Basic A-t-il F #</span><span class="sxs-lookup"><span data-stu-id="b9947-147">For the C#/VB Programmer Looking Into F#</span></span> #

<span data-ttu-id="b9947-148">Cette section suppose que vous êtes familiarisé avec le modèle asynchrone en C# / VB.</span><span class="sxs-lookup"><span data-stu-id="b9947-148">This section assumes you’re familiar with the async model in C#/VB.</span></span> <span data-ttu-id="b9947-149">Si vous n’êtes pas, [de programmation asynchrone en c#](../../../csharp/async.md) est un point de départ.</span><span class="sxs-lookup"><span data-stu-id="b9947-149">If you are not, [Async Programming in C#](../../../csharp/async.md) is a starting point.</span></span>

<span data-ttu-id="b9947-150">Il existe une différence fondamentale entre le modèle d’async C# /Visual Basic et le modèle asynchrone F #.</span><span class="sxs-lookup"><span data-stu-id="b9947-150">There is a fundamental difference between the C#/VB async model and the F# async model.</span></span>

<span data-ttu-id="b9947-151">Lorsque vous appelez une fonction qui retourne un `Task` ou `Task<'T>`, que le travail a déjà commencé l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b9947-151">When you call a function which returns a `Task` or `Task<'T>`, that job has already begun execution.</span></span> <span data-ttu-id="b9947-152">Le handle retourné représente une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b9947-152">The handle returned represents an already-running asynchronous job.</span></span> <span data-ttu-id="b9947-153">En revanche, lorsque vous appelez une fonction async en F #, le `Async<'a>` retourné représente une tâche qui sera **généré** à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="b9947-153">In contrast, when you call an async function in F#, the `Async<'a>` returned represents a job which will be **generated** at some point.</span></span> <span data-ttu-id="b9947-154">Présentation de ce modèle est puissante, car elle permet des tâches asynchrones dans F # pour être chaînés ensemble, exécutées de manière conditionnelle et être démarrée avec une granularité plus fine du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b9947-154">Understanding this model is powerful, because it allows for asynchronous jobs in F# to be chained together easier, performed conditionally, and be started with a finer grain of control.</span></span>

<span data-ttu-id="b9947-155">Il existe quelques autres similitudes et différences à noter.</span><span class="sxs-lookup"><span data-stu-id="b9947-155">There are a few other similarities and differences worth noting.</span></span>

### <a name="similarities"></a><span data-ttu-id="b9947-156">Similitudes</span><span class="sxs-lookup"><span data-stu-id="b9947-156">Similarities</span></span>

*   <span data-ttu-id="b9947-157">`let!`, `use!`, et `do!` sont analogues aux `await` lors de l’appel d’une tâche asynchrone à partir d’un `async{ }` bloc.</span><span class="sxs-lookup"><span data-stu-id="b9947-157">`let!`, `use!`, and `do!` are analogous to `await` when calling an async job from within an `async{ }` block.</span></span>

 <span data-ttu-id="b9947-158">Les trois mots clés ne peuvent être utilisées dans un `async { }` bloc, similaire à la `await` peut uniquement être appelée à l’intérieur d’un `async` (méthode).</span><span class="sxs-lookup"><span data-stu-id="b9947-158">The three keywords can only be used within an `async { }` block, similar to how `await` can only be invoked inside an `async` method.</span></span> <span data-ttu-id="b9947-159">En bref, `let!` concerne lorsque vous souhaitez capturer et utiliser un résultat, `use!` est similaire, mais pour un élément dont les ressources doivent obtenir nettoyées après leur utilisation, et `do!` concerne lorsque vous souhaitez attendre d’un flux de travail asynchrone sans valeur de retour à la fin avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b9947-159">In short, `let!` is for when you want to capture and use a result, `use!` is the same but for something whose resources should get cleaned after it’s used, and `do!` is for when you want to wait for an async workflow with no return value to finish before moving on.</span></span>

*   <span data-ttu-id="b9947-160">F # prend en charge de parallélisme de données de la même façon.</span><span class="sxs-lookup"><span data-stu-id="b9947-160">F# supports data-parallelism in a similar way.</span></span>

 <span data-ttu-id="b9947-161">Bien qu’il fonctionne très différemment, `Async.Parallel` correspond à `Task.WhenAll` pour le scénario de souhaitant les résultats d’un ensemble de travaux d’async lorsque toutes les fois terminées.</span><span class="sxs-lookup"><span data-stu-id="b9947-161">Although it operates very differently, `Async.Parallel` corresponds to `Task.WhenAll` for the scenario of wanting the results of a set of async jobs when they all complete.</span></span>

### <a name="differences"></a><span data-ttu-id="b9947-162">Différences</span><span class="sxs-lookup"><span data-stu-id="b9947-162">Differences</span></span>

*   <span data-ttu-id="b9947-163">Imbriqué `let!` n’est pas autorisé, contrairement aux imbriqué `await`</span><span class="sxs-lookup"><span data-stu-id="b9947-163">Nested `let!` is not allowed, unlike nested `await`</span></span>

 <span data-ttu-id="b9947-164">Contrairement aux `await`, qui peut être imbriqué indéfiniment, `let!` ne peut pas et doit avoir son résultat à lié avant de l’utiliser à l’intérieur d’un autre `let!`, `do!`, ou `use!`.</span><span class="sxs-lookup"><span data-stu-id="b9947-164">Unlike `await`, which can be nested indefinitely, `let!` cannot and must have its result bound before using it inside of another `let!`, `do!`, or `use!`.</span></span>

*   <span data-ttu-id="b9947-165">Prise en charge l’annulation est plus simple en F # à en C# / VB.</span><span class="sxs-lookup"><span data-stu-id="b9947-165">Cancellation support is simpler in F# than in C#/VB.</span></span>

 <span data-ttu-id="b9947-166">Prise en charge de l’annulation d’une tâche au milieu son exécution dans C# /Visual Basic requiert une vérification de la `IsCancellationRequested` propriété ou l’appel `ThrowIfCancellationRequested()` sur un `CancellationToken` objet qui est passé à la méthode async.</span><span class="sxs-lookup"><span data-stu-id="b9947-166">Supporting cancellation of a task midway through its execution in C#/VB requires checking the `IsCancellationRequested` property or calling `ThrowIfCancellationRequested()` on a `CancellationToken` object that’s passed into the async method.</span></span>

<span data-ttu-id="b9947-167">En revanche, les workflows asynchrones F # sont plus naturellement pouvant être annulés.</span><span class="sxs-lookup"><span data-stu-id="b9947-167">In contrast, F# async workflows are more naturally cancellable.</span></span> <span data-ttu-id="b9947-168">L’annulation est un processus en trois étapes simple.</span><span class="sxs-lookup"><span data-stu-id="b9947-168">Cancellation is a simple three-step process.</span></span>

1.  <span data-ttu-id="b9947-169">Créez un `CancellationTokenSource`.</span><span class="sxs-lookup"><span data-stu-id="b9947-169">Create a new `CancellationTokenSource`.</span></span>
2.  <span data-ttu-id="b9947-170">Passer à une fonction de départ.</span><span class="sxs-lookup"><span data-stu-id="b9947-170">Pass it into a starting function.</span></span>
3.  <span data-ttu-id="b9947-171">Appeler `Cancel` sur le jeton.</span><span class="sxs-lookup"><span data-stu-id="b9947-171">Call `Cancel` on the token.</span></span>

<span data-ttu-id="b9947-172">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b9947-172">Example:</span></span>

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

let token = new CancellationTokenSource()
Async.Start (workflow, token)

// Immediately cancel uploadDataAsync after it's been started.
token.Cancel()
```

<span data-ttu-id="b9947-173">C’est tout !</span><span class="sxs-lookup"><span data-stu-id="b9947-173">And that’s it!</span></span>

## <a name="further-resources"></a><span data-ttu-id="b9947-174">Ressources supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="b9947-174">Further resources:</span></span>

*   [<span data-ttu-id="b9947-175">Flux de travail asynchrone sur MSDN</span><span class="sxs-lookup"><span data-stu-id="b9947-175">Async Workflows on MSDN</span></span>](https://msdn.microsoft.com/library/dd233250.aspx)
*   [<span data-ttu-id="b9947-176">Séquences asynchrones pour F #</span><span class="sxs-lookup"><span data-stu-id="b9947-176">Asynchronous Sequences for F#</span></span>](https://fsprojects.github.io/FSharp.Control.AsyncSeq/library/AsyncSeq.html)
*   [<span data-ttu-id="b9947-177">Utilitaires de F # de données HTTP</span><span class="sxs-lookup"><span data-stu-id="b9947-177">F# Data HTTP Utilities</span></span>](https://fsharp.github.io/FSharp.Data/library/Http.html)
