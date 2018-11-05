---
title: Qu’est F#
description: Découvrez quels le F# est langage de programmation et nouveautés de programmation F#. En savoir plus sur les types de données enrichis, fonctions et comment ils s’imbriquent.
ms.date: 08/03/2018
ms.openlocfilehash: 193747f380c61a387ed79ecca6abbcd90ee74376
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43863294"
---
# <a name="what-is-f"></a>Qu’est F# #

F# est un langage de programmation fonctionnel qui le rend facile à écrire du code correct et facile à gérer.

Programmation F# implique principalement la définition des types et fonctions qui sont de type déduit et généralisées automatiquement. Cela permet de prendre en compte restent sur le domaine du problème et la manipulation de ses données, plutôt que les détails de la programmation.

```fsharp
open System // Gets access to functionality in System namespace.

// Defines a function that takes a name and produces a greeting.
let getGreeting name =
    sprintf "Hello, %s! Isn't F# great?" name

[<EntryPoint>]
let main args =
    // Defines a list of names
    let names = [ "Don"; "Julia"; "Xi" ]

    // Prints a greeting for each name!
    names
    |> List.map getGreeting
    |> List.iter (fun greeting -> printfn "%s" greeting)

    0
```

F# comporte de nombreuses fonctionnalités, notamment :

* Syntaxe simplifiée
* Immuable par défaut
* Généralisation automatique et inférence de type
* Fonctions de première classe
* Types de données puissants
* Critères spéciaux
* Programmation asynchrone

Un ensemble complet de fonctionnalités sont documentées dans le [référence du langage F#](language-reference/index.md).

## <a name="rich-data-types"></a>Types de données riches

Types de données tels que [enregistrements](language-reference/records.md) et [Unions discriminées](language-reference/discriminated-unions.md) vous permettent de représenter des données complexes et domaines.

```fsharp
// Group data with Records
type SuccessfulWithdrawal = {
    Amount: decimal
    Balance: decimal
}

type FailedWithdrawal = {
    Amount: decimal
    Balance: decimal
    IsOverdraft: bool
}

// Use discriminated unions to represent data of 1 or more forms
type WithdrawalResult =
    | Success of SuccessfulWithdrawal
    | InsufficientFunds of FailedWithdrawal
    | CardExpired of System.DateTime
    | UndisclosedFailure
```

F# enregistrements et les unions discriminées sont non null, immuable et comparables par défaut, ce qui les rend très facile à utiliser.

## <a name="enforced-correctness-with-functions-and-pattern-matching"></a>Exactitude appliqué avec les fonctions et les critères spéciaux

Fonctions F# sont faciles à déclarer et puissantes dans la pratique. Lorsqu’il est combiné avec [critères spéciaux](language-reference/pattern-matching.md), ils vous permettent de définir un comportement dont l’exactitude est appliquée par le compilateur.

```fsharp
// Returns a WithdrawalResult
let withdrawMoney amount = // Implementation elided

let handleWithdrawal amount =
    let w = withdrawMoney amount

    // The F# compiler enforces accounting for each case!
    match w with
    | Success s -> printfn "Successfully withdrew %f" s.Amount
    | InsufficientFunds f -> printfn "Failed: balance is %f" f.Balance
    | CardExpired d -> printfn "Failed: card expired on %O" d
    | UndisclosedFailure -> printfn "Failed: unknown :("
```

Fonctions F# sont également une excellente, ce qui signifie que peuvent être passés comme paramètres et retournés à partir d’autres fonctions.

## <a name="functions-to-define-operations-on-objects"></a>Fonctions pour définir des opérations sur des objets

F# offre une prise en charge complète pour les objets qui sont des types de données utiles lorsque vous avez besoin fusionner des données et des fonctionnalités. Les fonctions F# sont utilisées pour manipuler des objets.

```fsharp
type Set<[<EqualityConditionOn>] ‘T when ‘T: comparison>(elements: seq<'T>) =
    member s.IsEmpty = // Implementation elided
    member s.Contains (value) =// Implementation elided
    member s.Add (value) = // Implementation elided
    // ...
    // Further Implementation elided
    // ...
    interface IEnumerable<‘T>
    interface IReadOnlyCollection<‘T>

[<RequireQualifiedAccess>]
module Set =
    let isEmpty (set: Set<'T>) = set.IsEmpty

    let contains element (set: Set<'T>) = set.Contains(element)

    let add value (set: Set<'T>) = set.Add(value)
```

Au lieu d’écrire du code qui est orienté objet, en F#, vous serez souvent écrire du code que traite qu’un autre type de données pour les fonctions pour manipuler des objets. Fonctionnalités telles que [interfaces génériques](language-reference/interfaces.md), [expressions d’objet](language-reference/object-expressions.md)et l’utilisation judicieuse des [membres](language-reference/members/index.md) sont courantes dans les programmes F# plus volumineux.

## <a name="next-steps"></a>Étapes suivantes

Pour en savoir plus sur un ensemble plus important des fonctionnalités de F#, consultez le [visite guidée de F#](tour.md).