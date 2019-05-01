---
title: Options de valeur
description: En savoir plus sur les F# type d’Option de valeur, qui est une version de la structure du type d’Option.
ms.date: 02/06/2019
ms.openlocfilehash: e1036c83189c853b3704d94ca245e4818acc98c1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61982577"
---
# <a name="value-options"></a><span data-ttu-id="1f3ae-103">Options de valeur</span><span class="sxs-lookup"><span data-stu-id="1f3ae-103">Value Options</span></span>

<span data-ttu-id="1f3ae-104">Le type d’Option de valeur dans F# sert à contiennent les deux circonstances suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f3ae-104">The Value Option type in F# is used when the following two circumstances hold:</span></span>

1. <span data-ttu-id="1f3ae-105">Un scénario est adapté pour une [ F# Option](options.md).</span><span class="sxs-lookup"><span data-stu-id="1f3ae-105">A scenario is appropriate for an [F# Option](options.md).</span></span>
2. <span data-ttu-id="1f3ae-106">À l’aide d’un struct fournit un gain de performances dans votre scénario.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-106">Using a struct provides a performance benefit in your scenario.</span></span>

<span data-ttu-id="1f3ae-107">Pas tous les scénarios sensibles aux performances sont « résolus » à l’aide de structs.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-107">Not all performance-sensitive scenarios are "solved" by using structs.</span></span> <span data-ttu-id="1f3ae-108">Vous devez prendre en compte le coût supplémentaire de copie lors de leur utilisation au lieu de types référence.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-108">You must consider the additional cost of copying when using them instead of reference types.</span></span> <span data-ttu-id="1f3ae-109">Toutefois, grand F# programmes instancier couramment des nombreux types facultatifs qui transitent par les chemins d’accès à chaud, et dans ce cas, les structs peuvent produire souvent de meilleures performances globales pendant la durée de vie d’un programme.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-109">However, large F# programs commonly instantiate many optional types that flow through hot paths, and in such cases, structs can often yield better overall performance over the lifetime of a program.</span></span>

## <a name="definition"></a><span data-ttu-id="1f3ae-110">Définition</span><span class="sxs-lookup"><span data-stu-id="1f3ae-110">Definition</span></span>

<span data-ttu-id="1f3ae-111">Option la valeur est définie comme un [union discriminée de struct](discriminated-unions.md#struct-discriminated-unions) qui est similaire au type d’option de référence.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-111">Value Option is defined as a [struct discriminated union](discriminated-unions.md#struct-discriminated-unions) that is similar to the reference option type.</span></span> <span data-ttu-id="1f3ae-112">Sa définition peut être considérée de cette façon :</span><span class="sxs-lookup"><span data-stu-id="1f3ae-112">Its definition can be thought of this way:</span></span>

```fsharp
[<StructuralEquality; StructuralComparison>]
[<Struct>]
type ValueOption<'T> =
    | ValueNone
    | ValueSome of 'T
```

<span data-ttu-id="1f3ae-113">Option la valeur est conforme à la comparaison et l’égalité structurelle.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-113">Value Option conforms to structural equality and comparison.</span></span> <span data-ttu-id="1f3ae-114">La principale différence est que le nom compilé, nom de type et noms d’incidents indiquent qu’il est un type valeur.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-114">The main difference is that the compiled name, type name, and case names all indicate that it is a value type.</span></span>

## <a name="using-value-options"></a><span data-ttu-id="1f3ae-115">À l’aide des Options de valeur</span><span class="sxs-lookup"><span data-stu-id="1f3ae-115">Using Value Options</span></span>

<span data-ttu-id="1f3ae-116">Options de valeur sont utilisées comme [Options](options.md).</span><span class="sxs-lookup"><span data-stu-id="1f3ae-116">Value Options are used just like [Options](options.md).</span></span> <span data-ttu-id="1f3ae-117">`ValueSome` est utilisé pour indiquer qu’une valeur est présente, et `ValueNone` est utilisé lorsqu’une valeur n’est pas présente :</span><span class="sxs-lookup"><span data-stu-id="1f3ae-117">`ValueSome` is used to indicate that a value is present, and `ValueNone` is used when a value is not present:</span></span>

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

<span data-ttu-id="1f3ae-118">Comme avec [Options](options.md), la convention d’affectation de noms pour une fonction qui retourne `ValueOption` consiste à ajouter le préfixe `try`.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-118">As with [Options](options.md), the naming convention for a function that returns `ValueOption` is to prefix it with `try`.</span></span>

## <a name="value-option-properties-and-methods"></a><span data-ttu-id="1f3ae-119">Méthodes et propriétés d’Option de valeur</span><span class="sxs-lookup"><span data-stu-id="1f3ae-119">Value Option properties and methods</span></span>

<span data-ttu-id="1f3ae-120">Il existe une propriété pour les Options de valeur pour l’instant : `Value`.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-120">There is one property for Value Options at this time: `Value`.</span></span> <span data-ttu-id="1f3ae-121">Un <xref:System.InvalidOperationException> est générée si aucune valeur n’est présent lorsque cette propriété est appelée.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-121">An <xref:System.InvalidOperationException> is raised if no value is present when this property is invoked.</span></span>

## <a name="value-option-functions"></a><span data-ttu-id="1f3ae-122">Fonctions de valeur de Option</span><span class="sxs-lookup"><span data-stu-id="1f3ae-122">Value Option functions</span></span>

<span data-ttu-id="1f3ae-123">Il existe actuellement une fonction liée aux module pour les Options de valeur, `defaultValueArg`:</span><span class="sxs-lookup"><span data-stu-id="1f3ae-123">There is currently one module-bound function for Value Options, `defaultValueArg`:</span></span>

```fsharp
val defaultValueArg : arg:'T voption -> defaultValue:'T -> 'T 
```

<span data-ttu-id="1f3ae-124">Comme avec la `defaultArg` (fonction), `defaultValueArg` retourne la valeur sous-jacente de l’Option de valeur donnée si elle existe ; sinon, elle retourne la valeur par défaut spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-124">As with the `defaultArg` function, `defaultValueArg` returns the underlying value of the given Value Option if it exists; otherwise, it returns the specified default value.</span></span>

<span data-ttu-id="1f3ae-125">À ce stade, il n’existe aucune autre fonction liée aux module pour les Options de valeur.</span><span class="sxs-lookup"><span data-stu-id="1f3ae-125">At this time, there are no other module-bound functions for Value Options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f3ae-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f3ae-126">See also</span></span>

- [<span data-ttu-id="1f3ae-127">Options</span><span class="sxs-lookup"><span data-stu-id="1f3ae-127">Options</span></span>](options.md)
