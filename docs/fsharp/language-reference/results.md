---
title: 'Résultats (F #)'
description: 'Découvrez comment utiliser le type « Résultat ») (F # pour vous aider à écrire du code à tolérance d’erreur.'
author: cartermp
ms.author: phcart
ms.date: 04/24/2017
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 35fd1d3b1590291e18aa28460cf5939606c21d3a
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="results"></a><span data-ttu-id="15a7c-103">Résultats</span><span class="sxs-lookup"><span data-stu-id="15a7c-103">Results</span></span>

<span data-ttu-id="15a7c-104">À compter de F # 4.1, il existe un `Result<'T,'TFailure>` type que vous pouvez utiliser pour écrire du code à tolérance d’erreur qui peut être composée.</span><span class="sxs-lookup"><span data-stu-id="15a7c-104">Starting with F# 4.1, there is a `Result<'T,'TFailure>` type which you can use for writing error-tolerant code which can be composed.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15a7c-105">Syntax</span></span>

```fsharp
// The definition of Result in FSharp.Core
[<StructuralEquality; StructuralComparison>]
[<CompiledName("FSharpResult`2")>]
[<Struct>]
type Result<'T,'TError> = 
    | Ok of ResultValue:'T 
    | Error of ErrorValue:'TError
```

## <a name="remarks"></a><span data-ttu-id="15a7c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="15a7c-106">Remarks</span></span>

<span data-ttu-id="15a7c-107">Notez que le type de résultat est un [union discriminée de struct](discriminated-unions.md#struct-discriminated-unions), qui est une autre fonctionnalité introduite dans F # 4.1.</span><span class="sxs-lookup"><span data-stu-id="15a7c-107">Note that the result type is a [struct discriminated union](discriminated-unions.md#struct-discriminated-unions), which is another feature introduced in F# 4.1.</span></span>  <span data-ttu-id="15a7c-108">Sémantique d’égalité structurelle s’appliquent ici.</span><span class="sxs-lookup"><span data-stu-id="15a7c-108">Structural equality semantics apply here.</span></span>

<span data-ttu-id="15a7c-109">Le `Result` type est généralement utilisé dans monadic gestion des erreurs, qui sont souvent appelée [fer une programmation orientée](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/posts/recipe-part2.html) au sein de la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="15a7c-109">The `Result` type is typically used in monadic error-handling, which is often referred to as [Railway-oriented Programming](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/posts/recipe-part2.html) within the F# community.</span></span>  <span data-ttu-id="15a7c-110">L’exemple simple suivant illustre cette approche.</span><span class="sxs-lookup"><span data-stu-id="15a7c-110">The following trivial example demonstrates this approach.</span></span>

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

<span data-ttu-id="15a7c-111">Comme vous pouvez le voir, il est très facile de chaîner les diverses fonctions de validation si vous forcez toutes les pour retourner un `Result`.</span><span class="sxs-lookup"><span data-stu-id="15a7c-111">As you can see, it's quite easy to chain together various validation functions if you force them all to return a `Result`.</span></span>  <span data-ttu-id="15a7c-112">Ce permet de diviser des fonctionnalités de ce genre en petits éléments qui sont comme composable que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="15a7c-112">This lets you break up functionality like this into small pieces which are as composable as you need them to be.</span></span>  <span data-ttu-id="15a7c-113">Cela a également la valeur ajoutée de *en appliquant* l’utilisation de [recherche de correspondance](pattern-matching.md) à la fin d’un arrondi de validation, qui applique un degré plus élevé de l’exactitude du programme.</span><span class="sxs-lookup"><span data-stu-id="15a7c-113">This also has the added value of *enforcing* the use of [pattern matching](pattern-matching.md) at the end of a round of validation, which in turns enforces a higher degree of program correctness.</span></span>

## <a name="see-also"></a><span data-ttu-id="15a7c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15a7c-114">See Also</span></span>

[<span data-ttu-id="15a7c-115">Unions discriminées</span><span class="sxs-lookup"><span data-stu-id="15a7c-115">Discriminated Unions</span></span>](discriminated-unions.md)

[<span data-ttu-id="15a7c-116">Critères spéciaux</span><span class="sxs-lookup"><span data-stu-id="15a7c-116">Pattern Matching</span></span>](pattern-matching.md)
