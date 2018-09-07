---
title: Cellules de référence (F#)
description: 'Découvrez comment les cellules de référence F # sont des emplacements de stockage qui vous permettent de créer des valeurs mutables avec la sémantique de référence.'
ms.date: 05/16/2016
ms.openlocfilehash: e2e1a91c62fd76e4992bc5ae11bb672766850718
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44079294"
---
# <a name="reference-cells"></a><span data-ttu-id="75cda-103">Cellules de référence</span><span class="sxs-lookup"><span data-stu-id="75cda-103">Reference Cells</span></span>

<span data-ttu-id="75cda-104">*Cellules de référence* sont des emplacements de stockage qui vous permettent de créer des valeurs mutables avec la sémantique de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-104">*Reference cells* are storage locations that enable you to create mutable values with reference semantics.</span></span>

## <a name="syntax"></a><span data-ttu-id="75cda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75cda-105">Syntax</span></span>

```fsharp
ref expression
```

## <a name="remarks"></a><span data-ttu-id="75cda-106">Notes</span><span class="sxs-lookup"><span data-stu-id="75cda-106">Remarks</span></span>

<span data-ttu-id="75cda-107">Pour créer une cellule de référence qui encapsule la valeur, utilisez l'opérateur `ref`.</span><span class="sxs-lookup"><span data-stu-id="75cda-107">You use the `ref` operator before a value to create a new reference cell that encapsulates the value.</span></span> <span data-ttu-id="75cda-108">Vous pouvez ensuite modifier la valeur sous-jacente, car elle est mutable.</span><span class="sxs-lookup"><span data-stu-id="75cda-108">You can then change the underlying value because it is mutable.</span></span>

<span data-ttu-id="75cda-109">Une cellule de référence contient une valeur réelle, et pas uniquement une adresse.</span><span class="sxs-lookup"><span data-stu-id="75cda-109">A reference cell holds an actual value; it is not just an address.</span></span> <span data-ttu-id="75cda-110">Lorsque vous créez une cellule de référence à l'aide de l'opérateur `ref`, vous créez une copie de la valeur sous-jacente en tant que valeur mutable encapsulée.</span><span class="sxs-lookup"><span data-stu-id="75cda-110">When you create a reference cell by using the `ref` operator, you create a copy of the underlying value as an encapsulated mutable value.</span></span>

<span data-ttu-id="75cda-111">Vous pouvez déréférencer une cellule de référence à l'aide de l'opérateur `!` (bang).</span><span class="sxs-lookup"><span data-stu-id="75cda-111">You can dereference a reference cell by using the `!` (bang) operator.</span></span>

<span data-ttu-id="75cda-112">L'exemple de code suivant illustre la déclaration et l'utilisation de cellules de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-112">The following code example illustrates the declaration and use of reference cells.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2201.fs)]

<span data-ttu-id="75cda-113">Le résultat est `50`.</span><span class="sxs-lookup"><span data-stu-id="75cda-113">The output is `50`.</span></span>

<span data-ttu-id="75cda-114">Les cellules de référence sont des instances du type d'enregistrement générique `Ref` qui est déclaré comme suit.</span><span class="sxs-lookup"><span data-stu-id="75cda-114">Reference cells are instances of the `Ref` generic record type, which is declared as follows.</span></span>

```fsharp
type Ref<'a> =
{ mutable contents: 'a }
```

<span data-ttu-id="75cda-115">Le type `'a ref` (affiché par le compilateur et IntelliSense dans l'IDE) est un synonyme de `Ref<'a>`</span><span class="sxs-lookup"><span data-stu-id="75cda-115">The type `'a ref` is a synonym for `Ref<'a>`.</span></span> <span data-ttu-id="75cda-116">(définition sous-jacente).</span><span class="sxs-lookup"><span data-stu-id="75cda-116">The compiler and IntelliSense in the IDE display the former for this type, but the underlying definition is the latter.</span></span>

<span data-ttu-id="75cda-117">L'opérateur `ref` crée une cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-117">The `ref` operator creates a new reference cell.</span></span> <span data-ttu-id="75cda-118">Le code suivant est la déclaration de l'opérateur `ref`.</span><span class="sxs-lookup"><span data-stu-id="75cda-118">The following code is the declaration of the `ref` operator.</span></span>

```fsharp
let ref x = { contents = x }
```

<span data-ttu-id="75cda-119">Le tableau suivant répertorie les fonctionnalités disponibles sur la cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-119">The following table shows the features that are available on the reference cell.</span></span>

|<span data-ttu-id="75cda-120">Opérateur, membre ou champ</span><span class="sxs-lookup"><span data-stu-id="75cda-120">Operator, member, or field</span></span>|<span data-ttu-id="75cda-121">Description</span><span class="sxs-lookup"><span data-stu-id="75cda-121">Description</span></span>|<span data-ttu-id="75cda-122">Type</span><span class="sxs-lookup"><span data-stu-id="75cda-122">Type</span></span>|<span data-ttu-id="75cda-123">Définition</span><span class="sxs-lookup"><span data-stu-id="75cda-123">Definition</span></span>|
|--------------------------|-----------|----|----------|
|<span data-ttu-id="75cda-124">`!` (opérateur de déréférence)</span><span class="sxs-lookup"><span data-stu-id="75cda-124">`!` (dereference operator)</span></span>|<span data-ttu-id="75cda-125">Retourne la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="75cda-125">Returns the underlying value.</span></span>|`'a ref -> 'a`|`let (!) r = r.contents`|
|<span data-ttu-id="75cda-126">`:=` (opérateur d'assignation)</span><span class="sxs-lookup"><span data-stu-id="75cda-126">`:=` (assignment operator)</span></span>|<span data-ttu-id="75cda-127">Modifie la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="75cda-127">Changes the underlying value.</span></span>|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|
|<span data-ttu-id="75cda-128">`ref` (opérateur)</span><span class="sxs-lookup"><span data-stu-id="75cda-128">`ref` (operator)</span></span>|<span data-ttu-id="75cda-129">Encapsule une valeur dans une nouvelle cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-129">Encapsulates a value into a new reference cell.</span></span>|`'a -> 'a ref`|`let ref x = { contents = x }`|
|<span data-ttu-id="75cda-130">`Value` (propriété)</span><span class="sxs-lookup"><span data-stu-id="75cda-130">`Value` (property)</span></span>|<span data-ttu-id="75cda-131">Obtient ou définit la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="75cda-131">Gets or sets the underlying value.</span></span>|`unit -> 'a`|`member x.Value = x.contents`|
|<span data-ttu-id="75cda-132">`contents` (champ d'enregistrement)</span><span class="sxs-lookup"><span data-stu-id="75cda-132">`contents` (record field)</span></span>|<span data-ttu-id="75cda-133">Obtient ou définit la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="75cda-133">Gets or sets the underlying value.</span></span>|`'a`|`let ref x = { contents = x }`|
<span data-ttu-id="75cda-134">Vous pouvez accéder à la valeur sous-jacente de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="75cda-134">There are several ways to access the underlying value.</span></span> <span data-ttu-id="75cda-135">La valeur retournée par l'opérateur de déréférence (`!`) n'est pas une valeur assignable.</span><span class="sxs-lookup"><span data-stu-id="75cda-135">The value returned by the dereference operator (`!`) is not an assignable value.</span></span> <span data-ttu-id="75cda-136">Par conséquent, si vous modifiez la valeur sous-jacente, vous devez utiliser à la place l'opérateur d'assignation (`:=`).</span><span class="sxs-lookup"><span data-stu-id="75cda-136">Therefore, if you are modifying the underlying value, you must use the assignment operator (`:=`) instead.</span></span>

<span data-ttu-id="75cda-137">La propriété `Value` et le champ `contents` sont des valeurs assignables.</span><span class="sxs-lookup"><span data-stu-id="75cda-137">Both the `Value` property and the `contents` field are assignable values.</span></span> <span data-ttu-id="75cda-138">Par conséquent, vous pouvez les utiliser pour accéder ou modifier la valeur sous-jacente, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="75cda-138">Therefore, you can use these to either access or change the underlying value, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2203.fs)]

<span data-ttu-id="75cda-139">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="75cda-139">The output is as follows.</span></span>

```
10
10
11
12
```

<span data-ttu-id="75cda-140">Le champ `contents` est fourni à des fins de compatibilité avec d'autres versions de ML et produit un avertissement au cours de la compilation.</span><span class="sxs-lookup"><span data-stu-id="75cda-140">The field `contents` is provided for compatibility with other versions of ML and will produce a warning during compilation.</span></span> <span data-ttu-id="75cda-141">Pour désactiver l'avertissement, utilisez l'option de compilateur `--mlcompatibility`.</span><span class="sxs-lookup"><span data-stu-id="75cda-141">To disable the warning, use the `--mlcompatibility` compiler option.</span></span> <span data-ttu-id="75cda-142">Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="75cda-142">For more information, see [Compiler Options](compiler-options.md).</span></span>

<span data-ttu-id="75cda-143">Les programmeurs c# doivent savoir que `ref` en c# n’est pas la même chose que `ref` en F #.</span><span class="sxs-lookup"><span data-stu-id="75cda-143">C# programmers should know that `ref` in C# is not the same thing as `ref` in F#.</span></span> <span data-ttu-id="75cda-144">Les constructions équivalentes en F # sont [ByRef](byrefs.md), qui sont un concept différent à partir de cellules de référence.</span><span class="sxs-lookup"><span data-stu-id="75cda-144">The equivalent constructs in F# are [byrefs](byrefs.md), which are a different concept from reference cells.</span></span>

<span data-ttu-id="75cda-145">Les valeurs marquées en tant que `mutable`peut être promue automatiquement en `'a ref` si capturées par une fermeture ; consultez [valeurs](values/index.md).</span><span class="sxs-lookup"><span data-stu-id="75cda-145">Values marked as `mutable`may be automatically promoted to `'a ref` if captured by a closure; see [Values](values/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="75cda-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75cda-146">See also</span></span>

- [<span data-ttu-id="75cda-147">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="75cda-147">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="75cda-148">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="75cda-148">Parameters and Arguments</span></span>](parameters-and-arguments.md)
- [<span data-ttu-id="75cda-149">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="75cda-149">Symbol and Operator Reference</span></span>](symbol-and-operator-reference/index.md)
- [<span data-ttu-id="75cda-150">Valeurs</span><span class="sxs-lookup"><span data-stu-id="75cda-150">Values</span></span>](values/index.md)
