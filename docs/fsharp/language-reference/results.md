---
title: 'Résultats (F #)'
description: "Découvrez comment utiliser le type 'Entraîner' F # pour vous aider à écrire du code à tolérance d’erreur."
ms.date: 04/24/2017
ms.openlocfilehash: a7ce2e1f6b8c6a32d99a2feaf9547c4b67b152b8
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44213038"
---
# <a name="results"></a><span data-ttu-id="7b27b-103">Résultats</span><span class="sxs-lookup"><span data-stu-id="7b27b-103">Results</span></span>

<span data-ttu-id="7b27b-104">À partir de F # 4.1, il existe un `Result<'T,'TFailure>` type que vous pouvez utiliser pour l’écriture de code à tolérance d’erreur qui peut être composée.</span><span class="sxs-lookup"><span data-stu-id="7b27b-104">Starting with F# 4.1, there is a `Result<'T,'TFailure>` type which you can use for writing error-tolerant code which can be composed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b27b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b27b-105">Syntax</span></span>

```fsharp
// The definition of Result in FSharp.Core
[<StructuralEquality; StructuralComparison>]
[<CompiledName("FSharpResult`2")>]
[<Struct>]
type Result<'T,'TError> = 
    | Ok of ResultValue:'T 
    | Error of ErrorValue:'TError
```

## <a name="remarks"></a><span data-ttu-id="7b27b-106">Notes</span><span class="sxs-lookup"><span data-stu-id="7b27b-106">Remarks</span></span>

<span data-ttu-id="7b27b-107">Notez que le type de résultat est un [union discriminée de struct](discriminated-unions.md#struct-discriminated-unions), qui est une autre fonctionnalité introduite dans F # 4.1.</span><span class="sxs-lookup"><span data-stu-id="7b27b-107">Note that the result type is a [struct discriminated union](discriminated-unions.md#struct-discriminated-unions), which is another feature introduced in F# 4.1.</span></span>  <span data-ttu-id="7b27b-108">Sémantique d’égalité structurelle s’appliquent ici.</span><span class="sxs-lookup"><span data-stu-id="7b27b-108">Structural equality semantics apply here.</span></span>

<span data-ttu-id="7b27b-109">Le `Result` type est généralement utilisé dans monadic-gestion des erreurs, qui sont souvent appelée [programmation orientée sur les chemins de fer](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/posts/recipe-part2.html) au sein de la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="7b27b-109">The `Result` type is typically used in monadic error-handling, which is often referred to as [Railway-oriented Programming](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/posts/recipe-part2.html) within the F# community.</span></span>  <span data-ttu-id="7b27b-110">L’exemple simple suivant illustre cette approche.</span><span class="sxs-lookup"><span data-stu-id="7b27b-110">The following trivial example demonstrates this approach.</span></span>

```fsharp
// Define a simple type which has fields that can be validated
type Request = 
    { Name: string
      Email: string }

// Define some logic for what defines a valid name.
//
// Generates a Result which is an Ok if the name validates;
// otherwise, it generates a Result which is an Error.
let validateName req =
    match req.Name with
    | null -> Error "No name found."
    | "" -> Error "Name is empty."
    | "bananas" -> Error "Bananas is not a name."
    | _ -> Ok req

// Similarly, define some email validation logic.
let validateEmail req =
    match req.Email with
    | null -> Error "No email found."
    | "" -> Error "Email is empty."
    | s when s.EndsWith("bananas.com") -> Error "No email from bananas.com is allowed."
    | _ -> Ok req

let validateRequest reqResult =
    reqResult 
    |> Result.bind validateName
    |> Result.bind validateEmail

let test() = 
    // Now, create a Request and pattern match on the result.
    let req1 = { Name = "Phillip"; Email = "phillip@contoso.biz" }
    let res1 = validateRequest (Ok req1)
    match res1 with
    | Ok req -> printfn "My request was valid! Name: %s Email %s" req.Name req.Email
    | Error e -> printfn "Error: %s" e
    // Prints: "My request was valid!  Name: Phillip Email: phillip@consoto.biz"

    let req2 = { Name = "Phillip"; Email = "phillip@bananas.com" }
    let res2 = validateRequest (Ok req2)
    match res2 with
    | Ok req -> printfn "My request was valid! Name: %s Email %s" req.Name req.Email
    | Error e -> printfn "Error: %s" e
    // Prints: "Error: No email from bananas.com is allowed."

test()
```

<span data-ttu-id="7b27b-111">Comme vous pouvez le voir, il est assez facile de chaîner les diverses fonctions de validation si vous tous les forcez à retourner un `Result`.</span><span class="sxs-lookup"><span data-stu-id="7b27b-111">As you can see, it's quite easy to chain together various validation functions if you force them all to return a `Result`.</span></span>  <span data-ttu-id="7b27b-112">Vous pouvez ainsi vous décomposez les fonctionnalités de ce genre en petits éléments qui sont aussi composables comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="7b27b-112">This lets you break up functionality like this into small pieces which are as composable as you need them to be.</span></span>  <span data-ttu-id="7b27b-113">Cela a également la valeur ajoutée de *en appliquant* l’utilisation de [critères spéciaux](pattern-matching.md) à la fin d’un cycle de validation, ce qui réduit applique un degré plus élevé de l’exactitude du programme.</span><span class="sxs-lookup"><span data-stu-id="7b27b-113">This also has the added value of *enforcing* the use of [pattern matching](pattern-matching.md) at the end of a round of validation, which in turns enforces a higher degree of program correctness.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b27b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b27b-114">See also</span></span>

- [<span data-ttu-id="7b27b-115">Unions discriminées</span><span class="sxs-lookup"><span data-stu-id="7b27b-115">Discriminated Unions</span></span>](discriminated-unions.md)
- [<span data-ttu-id="7b27b-116">Critères spéciaux</span><span class="sxs-lookup"><span data-stu-id="7b27b-116">Pattern Matching</span></span>](pattern-matching.md)
