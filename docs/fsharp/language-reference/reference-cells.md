---
title: Cellules de référence (F#)
description: 'Découvrez comment les cellules de référence F # sont des emplacements de stockage qui vous permettent de créer des valeurs mutables avec la sémantique de référence.'
ms.date: 05/16/2016
ms.openlocfilehash: 133aec6b162a13306a05c9afa172f859890565eb
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43892417"
---
# <a name="reference-cells"></a><span data-ttu-id="36ac2-103">Cellules de référence</span><span class="sxs-lookup"><span data-stu-id="36ac2-103">Reference Cells</span></span>

<span data-ttu-id="36ac2-104">*Cellules de référence* sont des emplacements de stockage qui vous permettent de créer des valeurs mutables avec la sémantique de référence.</span><span class="sxs-lookup"><span data-stu-id="36ac2-104">*Reference cells* are storage locations that enable you to create mutable values with reference semantics.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ac2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36ac2-105">Syntax</span></span>

```fsharp
ref expression
```

## <a name="remarks"></a><span data-ttu-id="36ac2-106">Notes</span><span class="sxs-lookup"><span data-stu-id="36ac2-106">Remarks</span></span>

<span data-ttu-id="36ac2-107">Pour créer une cellule de référence qui encapsule la valeur, utilisez l'opérateur `ref`.</span><span class="sxs-lookup"><span data-stu-id="36ac2-107">You use the `ref` operator before a value to create a new reference cell that encapsulates the value.</span></span> <span data-ttu-id="36ac2-108">Vous pouvez ensuite modifier la valeur sous-jacente, car elle est mutable.</span><span class="sxs-lookup"><span data-stu-id="36ac2-108">You can then change the underlying value because it is mutable.</span></span>

<span data-ttu-id="36ac2-109">Une cellule de référence contient une valeur réelle, et pas uniquement une adresse.</span><span class="sxs-lookup"><span data-stu-id="36ac2-109">A reference cell holds an actual value; it is not just an address.</span></span> <span data-ttu-id="36ac2-110">Lorsque vous créez une cellule de référence à l'aide de l'opérateur `ref`, vous créez une copie de la valeur sous-jacente en tant que valeur mutable encapsulée.</span><span class="sxs-lookup"><span data-stu-id="36ac2-110">When you create a reference cell by using the `ref` operator, you create a copy of the underlying value as an encapsulated mutable value.</span></span>

<span data-ttu-id="36ac2-111">Vous pouvez déréférencer une cellule de référence à l'aide de l'opérateur `!` (bang).</span><span class="sxs-lookup"><span data-stu-id="36ac2-111">You can dereference a reference cell by using the `!` (bang) operator.</span></span>

<span data-ttu-id="36ac2-112">L'exemple de code suivant illustre la déclaration et l'utilisation de cellules de référence.</span><span class="sxs-lookup"><span data-stu-id="36ac2-112">The following code example illustrates the declaration and use of reference cells.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2201.fs)]

<span data-ttu-id="36ac2-113">Le résultat est `50`.</span><span class="sxs-lookup"><span data-stu-id="36ac2-113">The output is `50`.</span></span>

<span data-ttu-id="36ac2-114">Les cellules de référence sont des instances du type d'enregistrement générique `Ref` qui est déclaré comme suit.</span><span class="sxs-lookup"><span data-stu-id="36ac2-114">Reference cells are instances of the `Ref` generic record type, which is declared as follows.</span></span>

```fsharp
type Ref<'a> =
{ mutable contents: 'a }
```

<span data-ttu-id="36ac2-115">Le type `'a ref` (affiché par le compilateur et IntelliSense dans l'IDE) est un synonyme de `Ref<'a>`</span><span class="sxs-lookup"><span data-stu-id="36ac2-115">The type `'a ref` is a synonym for `Ref<'a>`.</span></span> <span data-ttu-id="36ac2-116">(définition sous-jacente).</span><span class="sxs-lookup"><span data-stu-id="36ac2-116">The compiler and IntelliSense in the IDE display the former for this type, but the underlying definition is the latter.</span></span>

<span data-ttu-id="36ac2-117">L'opérateur `ref` crée une cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="36ac2-117">The `ref` operator creates a new reference cell.</span></span> <span data-ttu-id="36ac2-118">Le code suivant est la déclaration de l'opérateur `ref`.</span><span class="sxs-lookup"><span data-stu-id="36ac2-118">The following code is the declaration of the `ref` operator.</span></span>

```fsharp
let ref x = { contents = x }
```

<span data-ttu-id="36ac2-119">Le tableau suivant répertorie les fonctionnalités disponibles sur la cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="36ac2-119">The following table shows the features that are available on the reference cell.</span></span>

|<span data-ttu-id="36ac2-120">Opérateur, membre ou champ</span><span class="sxs-lookup"><span data-stu-id="36ac2-120">Operator, member, or field</span></span>|<span data-ttu-id="36ac2-121">Description</span><span class="sxs-lookup"><span data-stu-id="36ac2-121">Description</span></span>|<span data-ttu-id="36ac2-122">Type</span><span class="sxs-lookup"><span data-stu-id="36ac2-122">Type</span></span>|<span data-ttu-id="36ac2-123">Définition</span><span class="sxs-lookup"><span data-stu-id="36ac2-123">Definition</span></span>|
|--------------------------|-----------|----|----------|
|<span data-ttu-id="36ac2-124">`!` (opérateur de déréférence)</span><span class="sxs-lookup"><span data-stu-id="36ac2-124">`!` (dereference operator)</span></span>|<span data-ttu-id="36ac2-125">Retourne la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="36ac2-125">Returns the underlying value.</span></span>|`'a ref -> 'a`|`let (!) r = r.contents`|
|<span data-ttu-id="36ac2-126">`:=` (opérateur d'assignation)</span><span class="sxs-lookup"><span data-stu-id="36ac2-126">`:=` (assignment operator)</span></span>|<span data-ttu-id="36ac2-127">Modifie la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="36ac2-127">Changes the underlying value.</span></span>|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|
|<span data-ttu-id="36ac2-128">`ref` (opérateur)</span><span class="sxs-lookup"><span data-stu-id="36ac2-128">`ref` (operator)</span></span>|<span data-ttu-id="36ac2-129">Encapsule une valeur dans une nouvelle cellule de référence.</span><span class="sxs-lookup"><span data-stu-id="36ac2-129">Encapsulates a value into a new reference cell.</span></span>|`'a -> 'a ref`|`let ref x = { contents = x }`|
|<span data-ttu-id="36ac2-130">`Value` (propriété)</span><span class="sxs-lookup"><span data-stu-id="36ac2-130">`Value` (property)</span></span>|<span data-ttu-id="36ac2-131">Obtient ou définit la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="36ac2-131">Gets or sets the underlying value.</span></span>|`unit -> 'a`|`member x.Value = x.contents`|
|<span data-ttu-id="36ac2-132">`contents` (champ d'enregistrement)</span><span class="sxs-lookup"><span data-stu-id="36ac2-132">`contents` (record field)</span></span>|<span data-ttu-id="36ac2-133">Obtient ou définit la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="36ac2-133">Gets or sets the underlying value.</span></span>|`'a`|`let ref x = { contents = x }`|
<span data-ttu-id="36ac2-134">Vous pouvez accéder à la valeur sous-jacente de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="36ac2-134">There are several ways to access the underlying value.</span></span> <span data-ttu-id="36ac2-135">La valeur retournée par l'opérateur de déréférence (`!`) n'est pas une valeur assignable.</span><span class="sxs-lookup"><span data-stu-id="36ac2-135">The value returned by the dereference operator (`!`) is not an assignable value.</span></span> <span data-ttu-id="36ac2-136">Par conséquent, si vous modifiez la valeur sous-jacente, vous devez utiliser à la place l'opérateur d'assignation (`:=`).</span><span class="sxs-lookup"><span data-stu-id="36ac2-136">Therefore, if you are modifying the underlying value, you must use the assignment operator (`:=`) instead.</span></span>

<span data-ttu-id="36ac2-137">La propriété `Value` et le champ `contents` sont des valeurs assignables.</span><span class="sxs-lookup"><span data-stu-id="36ac2-137">Both the `Value` property and the `contents` field are assignable values.</span></span> <span data-ttu-id="36ac2-138">Par conséquent, vous pouvez les utiliser pour accéder ou modifier la valeur sous-jacente, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="36ac2-138">Therefore, you can use these to either access or change the underlying value, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2203.fs)]

<span data-ttu-id="36ac2-139">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="36ac2-139">The output is as follows.</span></span>

```
10
10
11
12
```

<span data-ttu-id="36ac2-140">Le champ `contents` est fourni à des fins de compatibilité avec d'autres versions de ML et produit un avertissement au cours de la compilation.</span><span class="sxs-lookup"><span data-stu-id="36ac2-140">The field `contents` is provided for compatibility with other versions of ML and will produce a warning during compilation.</span></span> <span data-ttu-id="36ac2-141">Pour désactiver l'avertissement, utilisez l'option de compilateur `--mlcompatibility`.</span><span class="sxs-lookup"><span data-stu-id="36ac2-141">To disable the warning, use the `--mlcompatibility` compiler option.</span></span> <span data-ttu-id="36ac2-142">Pour plus d’informations, consultez l’article [Options du compilateur](compiler-options.md).</span><span class="sxs-lookup"><span data-stu-id="36ac2-142">For more information, see [Compiler Options](compiler-options.md).</span></span>

<span data-ttu-id="36ac2-143">Le code suivant illustre l'utilisation de cellules de référence dans le cadre du passage de paramètres.</span><span class="sxs-lookup"><span data-stu-id="36ac2-143">The following code illustrates the use of reference cells in parameter passing.</span></span> <span data-ttu-id="36ac2-144">Le type de l’incrémentation du possède une méthode incrément qui prend un paramètre qui inclut le type de paramètre byref.</span><span class="sxs-lookup"><span data-stu-id="36ac2-144">The Incrementor type has a method Increment that takes a parameter that includes byref in the parameter type.</span></span> <span data-ttu-id="36ac2-145">Dans le type de paramètre byref indique que les appelants doivent passer une cellule de référence ou l’adresse d’une variable normale du type spécifié, dans ce cas type int. Le code restant illustre comment appeler incrément avec ces deux types d’arguments et illustre l’utilisation de l’opérateur ref sur une variable pour créer une cellule de référence (ref myDelta1).</span><span class="sxs-lookup"><span data-stu-id="36ac2-145">The byref in the parameter type indicates that callers must pass a reference cell or the address of a typical variable of the specified type, in this case int. The remaining code illustrates how to call Increment with both of these types of arguments, and shows the use of the ref operator on a variable to create a reference cell (ref myDelta1).</span></span> <span data-ttu-id="36ac2-146">Il montre ensuite l'utilisation de l'opérateur d'adresse (&amp;) pour générer un argument approprié.</span><span class="sxs-lookup"><span data-stu-id="36ac2-146">It then shows the use of the address-of operator (&amp;) to generate an appropriate argument.</span></span> <span data-ttu-id="36ac2-147">Enfin, la méthode de l’incrément est appelée à nouveau à l’aide d’une cellule de référence est déclarée à l’aide d’une liaison let.</span><span class="sxs-lookup"><span data-stu-id="36ac2-147">Finally, the Increment method is called again by using a reference cell that is declared by using a let binding.</span></span> <span data-ttu-id="36ac2-148">La dernière ligne de code illustre l’utilisation de la !</span><span class="sxs-lookup"><span data-stu-id="36ac2-148">The final line of code demonstrates the use of the !</span></span> <span data-ttu-id="36ac2-149">opérateur pour déréférencer la cellule de référence pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="36ac2-149">operator to dereference the reference cell for printing.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2204.fs)]

<span data-ttu-id="36ac2-150">Pour plus d’informations sur le passage par référence, consultez [paramètres et Arguments](parameters-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="36ac2-150">For more information about how to pass by reference, see [Parameters and Arguments](parameters-and-arguments.md).</span></span>

>[!NOTE]
<span data-ttu-id="36ac2-151">Les programmeurs c# doivent savoir que ref différemment en F # fonctionne et en c#.</span><span class="sxs-lookup"><span data-stu-id="36ac2-151">C# programmers should know that ref works differently in F# than it does in C#.</span></span> <span data-ttu-id="36ac2-152">Par exemple, l’utilisation de ref lorsque vous passez un argument n’a pas le même effet en F # comme il le fait en c#.</span><span class="sxs-lookup"><span data-stu-id="36ac2-152">For example, the use of ref when you pass an argument does not have the same effect in F# as it does in C#.</span></span>

>[!NOTE]
<span data-ttu-id="36ac2-153">`mutable` les variables peuvent être automatiquement promues en `'a ref` si capturées par une fermeture ; consultez [valeurs](values/index.md).</span><span class="sxs-lookup"><span data-stu-id="36ac2-153">`mutable` variables may be automatically promoted to `'a ref` if captured by a closure; see [Values](values/index.md).</span></span>

## <a name="consuming-c-ref-returns"></a><span data-ttu-id="36ac2-154">Utilisation de c# `ref` retourne</span><span class="sxs-lookup"><span data-stu-id="36ac2-154">Consuming C# `ref` returns</span></span>

<span data-ttu-id="36ac2-155">À partir de F # 4.1, vous pouvez consommer `ref` retourne généré en c#.</span><span class="sxs-lookup"><span data-stu-id="36ac2-155">Starting with F# 4.1, you can consume `ref` returns generated in C#.</span></span>  <span data-ttu-id="36ac2-156">Le résultat de cet appel est un `byref<_>` pointeur.</span><span class="sxs-lookup"><span data-stu-id="36ac2-156">The result of such a call is a `byref<_>` pointer.</span></span>

<span data-ttu-id="36ac2-157">La méthode c# suivante :</span><span class="sxs-lookup"><span data-stu-id="36ac2-157">The following C# method:</span></span>

```csharp
namespace RefReturns
{
    public static class RefClass
    {
        public static ref int Find(int val, int[] vals)
        {
            for (int i = 0; i < vals.Length; i++)
            {
                if (vals[i] == val)
                {
                    return ref numbers[i]; // Returns the location, not the value
                }
            }

            throw new IndexOutOfRangeException($"{nameof(number)} not found");
        }
    }
}
```

<span data-ttu-id="36ac2-158">Peut être appelée en toute transparence par F # avec aucune syntaxe spéciale :</span><span class="sxs-lookup"><span data-stu-id="36ac2-158">Can be transparently called by F# with no special syntax:</span></span>

```fsharp
open RefReturns

let consumeRefReturn() =
    let result = RefClass.Find(3, [| 1; 2; 3; 4; 5 |]) // 'result' is of type 'byref<int>'.
    ()
```

<span data-ttu-id="36ac2-159">Vous pouvez également déclarer des fonctions qui peut prendre un `ref` renvoyer en tant qu’entrée, par exemple :</span><span class="sxs-lookup"><span data-stu-id="36ac2-159">You can also declare functions which could take a `ref` return as input, for example:</span></span>

```fsharp
let f (x: byref<int>) = &x
```

<span data-ttu-id="36ac2-160">Il n’existe actuellement aucun moyen de générer un `ref` retour dans F #, qui peut être utilisée dans c#.</span><span class="sxs-lookup"><span data-stu-id="36ac2-160">There is currently no way to generate a `ref` return in F# which could be consumed in C#.</span></span>

## <a name="see-also"></a><span data-ttu-id="36ac2-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36ac2-161">See also</span></span>

- [<span data-ttu-id="36ac2-162">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="36ac2-162">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="36ac2-163">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="36ac2-163">Parameters and Arguments</span></span>](parameters-and-arguments.md)
- [<span data-ttu-id="36ac2-164">Informations de référence des symboles et opérateurs</span><span class="sxs-lookup"><span data-stu-id="36ac2-164">Symbol and Operator Reference</span></span>](symbol-and-operator-reference/index.md)
- [<span data-ttu-id="36ac2-165">Valeurs</span><span class="sxs-lookup"><span data-stu-id="36ac2-165">Values</span></span>](values/index.md)
