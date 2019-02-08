---
title: Options de valeur
description: En savoir plus sur les F# type d’Option de valeur, qui est une version de la structure du type d’Option.
ms.date: 02/06/2019
ms.openlocfilehash: e1036c83189c853b3704d94ca245e4818acc98c1
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828031"
---
# <a name="value-options"></a>Options de valeur

Le type d’Option de valeur dans F# sert à contiennent les deux circonstances suivantes :

1. Un scénario est adapté pour une [ F# Option](options.md).
2. À l’aide d’un struct fournit un gain de performances dans votre scénario.

Pas tous les scénarios sensibles aux performances sont « résolus » à l’aide de structs. Vous devez prendre en compte le coût supplémentaire de copie lors de leur utilisation au lieu de types référence. Toutefois, grand F# programmes instancier couramment des nombreux types facultatifs qui transitent par les chemins d’accès à chaud, et dans ce cas, les structs peuvent produire souvent de meilleures performances globales pendant la durée de vie d’un programme.

## <a name="definition"></a>Définition

Option la valeur est définie comme un [union discriminée de struct](discriminated-unions.md#struct-discriminated-unions) qui est similaire au type d’option de référence. Sa définition peut être considérée de cette façon :

```fsharp
[<StructuralEquality; StructuralComparison>]
[<Struct>]
type ValueOption<'T> =
    | ValueNone
    | ValueSome of 'T
```

Option la valeur est conforme à la comparaison et l’égalité structurelle. La principale différence est que le nom compilé, nom de type et noms d’incidents indiquent qu’il est un type valeur.

## <a name="using-value-options"></a>À l’aide des Options de valeur

Options de valeur sont utilisées comme [Options](options.md). `ValueSome` est utilisé pour indiquer qu’une valeur est présente, et `ValueNone` est utilisé lorsqu’une valeur n’est pas présente :

```fsharp
let tryParseDateTime (s: string) =
    match System.DateTime.TryParse(s) with
    | (true, dt) -> ValueSome dt
    | (false, _) -> ValueNone

let possibleDateString1 = "1990-12-25"
let possibleDateString2 = "This is not a date"

let result1 = tryParseDateTime possibleDateString1
let result2 = tryParseDateTime possibleDateString2

match (result1, result2) with
| ValueSome d1, ValueSome d2 -> printfn "Both are dates!"
| ValueSome d1, ValueNone -> printfn "Only the first is a date!"
| ValueNone, ValueSome d2 -> printfn "Only the second is a date!"
| ValueNone, ValueNone -> printfn "None of them are dates!"
```

Comme avec [Options](options.md), la convention d’affectation de noms pour une fonction qui retourne `ValueOption` consiste à ajouter le préfixe `try`.

## <a name="value-option-properties-and-methods"></a>Méthodes et propriétés d’Option de valeur

Il existe une propriété pour les Options de valeur pour l’instant : `Value`. Un <xref:System.InvalidOperationException> est générée si aucune valeur n’est présent lorsque cette propriété est appelée.

## <a name="value-option-functions"></a>Fonctions de valeur de Option

Il existe actuellement une fonction liée aux module pour les Options de valeur, `defaultValueArg`:

```fsharp
val defaultValueArg : arg:'T voption -> defaultValue:'T -> 'T 
```

Comme avec la `defaultArg` (fonction), `defaultValueArg` retourne la valeur sous-jacente de l’Option de valeur donnée si elle existe ; sinon, elle retourne la valeur par défaut spécifiée.

À ce stade, il n’existe aucune autre fonction liée aux module pour les Options de valeur.

## <a name="see-also"></a>Voir aussi

- [Options](options.md)
