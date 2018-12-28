---
title: Résultats
description: Découvrez comment utiliser le F# « Result » tapez pour vous aider à écrire du code à tolérance d’erreur.
ms.date: 04/24/2017
ms.openlocfilehash: 8b419412b406018a21f2c23103c8193fec8766f2
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612710"
---
# <a name="results"></a>Résultats

En commençant par F# 4.1, il existe un `Result<'T,'TFailure>` type que vous pouvez utiliser pour l’écriture de code à tolérance d’erreur qui peut être composée.

## <a name="syntax"></a>Syntaxe

```fsharp
// The definition of Result in FSharp.Core
[<StructuralEquality; StructuralComparison>]
[<CompiledName("FSharpResult`2")>]
[<Struct>]
type Result<'T,'TError> = 
    | Ok of ResultValue:'T 
    | Error of ErrorValue:'TError
```

## <a name="remarks"></a>Notes

Notez que le type de résultat est un [union discriminée de struct](discriminated-unions.md#struct-discriminated-unions), qui est une autre fonctionnalité introduite dans F# 4.1.  Sémantique d’égalité structurelle s’appliquent ici.

Le `Result` type est généralement utilisé dans monadic-gestion des erreurs, qui sont souvent appelée [programmation orientée sur les chemins de fer](https://swlaschin.gitbooks.io/fsharpforfunandprofit/content/posts/recipe-part2.html) au sein de la F# Communauté.  L’exemple simple suivant illustre cette approche.

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

Comme vous pouvez le voir, il est assez facile de chaîner les diverses fonctions de validation si vous tous les forcez à retourner un `Result`.  Vous pouvez ainsi vous décomposez les fonctionnalités de ce genre en petits éléments qui sont aussi composables comme vous le souhaitez.  Cela a également la valeur ajoutée de *en appliquant* l’utilisation de [critères spéciaux](pattern-matching.md) à la fin d’un cycle de validation, ce qui réduit applique un degré plus élevé de l’exactitude du programme.

## <a name="see-also"></a>Voir aussi

- [Unions discriminées](discriminated-unions.md)
- [Critères spéciaux](pattern-matching.md)