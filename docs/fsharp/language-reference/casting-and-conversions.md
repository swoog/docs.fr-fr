---
title: Cast et conversions (F#)
description: Découvrez comment le langage de programmation F# fournit des opérateurs de conversion pour les conversions arithmétiques entre différents types primitifs.
ms.date: 05/16/2016
ms.openlocfilehash: aca1a2523130ee485a7e7c9a6a45a410904cb246
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "45677927"
---
# <a name="casting-and-conversions-f"></a><span data-ttu-id="4f6cb-103">Cast et conversions (F#)</span><span class="sxs-lookup"><span data-stu-id="4f6cb-103">Casting and Conversions (F#)</span></span>

<span data-ttu-id="4f6cb-104">Cette rubrique décrit la prise en charge pour les conversions de type en F#.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-104">This topic describes support for type conversions in F#.</span></span>

## <a name="arithmetic-types"></a><span data-ttu-id="4f6cb-105">Types arithmétiques</span><span class="sxs-lookup"><span data-stu-id="4f6cb-105">Arithmetic Types</span></span>

<span data-ttu-id="4f6cb-106">F# fournit les opérateurs de conversion pour les conversions arithmétiques entre différents types primitifs, tels qu’entre entier et les types à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-106">F# provides conversion operators for arithmetic conversions between various primitive types, such as between integer and floating point types.</span></span> <span data-ttu-id="4f6cb-107">Les opérateurs de conversion de type intégral et char ont vérifié et formulaires désactivées ; opérateurs à virgule flottante et le `enum` n’est pas le cas de l’opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-107">The integral and char conversion operators have checked and unchecked forms; the floating point operators and the `enum` conversion operator do not.</span></span> <span data-ttu-id="4f6cb-108">Les formulaires non contrôlés sont définies dans `Microsoft.FSharp.Core.Operators` et les formes vérifiées sont définies dans `Microsoft.FSharp.Core.Operators.Checked`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-108">The unchecked forms are defined in `Microsoft.FSharp.Core.Operators` and the checked forms are defined in `Microsoft.FSharp.Core.Operators.Checked`.</span></span> <span data-ttu-id="4f6cb-109">Les formes vérifiées vérification de dépassement de capacité et génèrent une exception runtime si la valeur résultante dépasse les limites du type cible.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-109">The checked forms check for overflow and generate a runtime exception if the resulting value exceeds the limits of the target type.</span></span>

<span data-ttu-id="4f6cb-110">Chacun de ces opérateurs a le même nom que le nom du type de destination.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-110">Each of these operators has the same name as the name of the destination type.</span></span> <span data-ttu-id="4f6cb-111">Par exemple, dans le code suivant, dans lequel les types sont annotés explicitement, `byte` apparaît avec deux significations différentes.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-111">For example, in the following code, in which the types are explicitly annotated, `byte` appears with two different meanings.</span></span> <span data-ttu-id="4f6cb-112">La première occurrence est le type et le second est l’opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-112">The first occurrence is the type and the second is the conversion operator.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4401.fs)]

<span data-ttu-id="4f6cb-113">Le tableau suivant présente les opérateurs de conversion définis en F#.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-113">The following table shows conversion operators defined in F#.</span></span>

|<span data-ttu-id="4f6cb-114">Opérateur</span><span class="sxs-lookup"><span data-stu-id="4f6cb-114">Operator</span></span>|<span data-ttu-id="4f6cb-115">Description</span><span class="sxs-lookup"><span data-stu-id="4f6cb-115">Description</span></span>|
|--------|-----------|
|`byte`|<span data-ttu-id="4f6cb-116">Convertir en type byte, un type non signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-116">Convert to byte, an 8-bit unsigned type.</span></span>|
|`sbyte`|<span data-ttu-id="4f6cb-117">Convertir en octet signé.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-117">Convert to signed byte.</span></span>|
|`int16`|<span data-ttu-id="4f6cb-118">Convertir en un entier signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-118">Convert to a 16-bit signed integer.</span></span>|
|`uint16`|<span data-ttu-id="4f6cb-119">Convertir un entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-119">Convert to a 16-bit unsigned integer.</span></span>|
|`int32, int`|<span data-ttu-id="4f6cb-120">Convertir en un entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-120">Convert to a 32-bit signed integer.</span></span>|
|`uint32`|<span data-ttu-id="4f6cb-121">Convertir un entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-121">Convert to a 32-bit unsigned integer.</span></span>|
|`int64`|<span data-ttu-id="4f6cb-122">Convertir en un entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-122">Convert to a 64-bit signed integer.</span></span>|
|`uint64`|<span data-ttu-id="4f6cb-123">Convertir un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-123">Convert to a 64-bit unsigned integer.</span></span>|
|`nativeint`|<span data-ttu-id="4f6cb-124">Convertir en entier natif.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-124">Convert to a native integer.</span></span>|
|`unativeint`|<span data-ttu-id="4f6cb-125">Convertir en entier natif non signé.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-125">Convert to an unsigned native integer.</span></span>|
|`float, double`|<span data-ttu-id="4f6cb-126">Convertir à 64 bits double précision IEEE nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-126">Convert to a 64-bit double-precision IEEE floating point number.</span></span>|
|`float32, single`|<span data-ttu-id="4f6cb-127">Convertir à 32 bits simple précision IEEE nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-127">Convert to a 32-bit single-precision IEEE floating point number.</span></span>|
|`decimal`|<span data-ttu-id="4f6cb-128">Convertir en `System.Decimal`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-128">Convert to `System.Decimal`.</span></span>|
|`char`|<span data-ttu-id="4f6cb-129">Convertir en `System.Char`, un caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-129">Convert to `System.Char`, a Unicode character.</span></span>|
|`enum`|<span data-ttu-id="4f6cb-130">Convertir en un type énuméré.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-130">Convert to an enumerated type.</span></span>|
<span data-ttu-id="4f6cb-131">Outre les types primitifs intégrés, vous pouvez utiliser ces opérateurs avec les types qui implémentent `op_Explicit` ou `op_Implicit` méthodes avec les signatures appropriées.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-131">In addition to built-in primitive types, you can use these operators with types that implement `op_Explicit` or `op_Implicit` methods with appropriate signatures.</span></span> <span data-ttu-id="4f6cb-132">Par exemple, le `int` opérateur de conversion fonctionne avec n’importe quel type qui fournit une méthode statique `op_Explicit` qui prend le type en tant que paramètre et retourne `int`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-132">For example, the `int` conversion operator works with any type that provides a static method `op_Explicit` that takes the type as a parameter and returns `int`.</span></span> <span data-ttu-id="4f6cb-133">Constitue une exception à la règle générale que les méthodes ne peut pas être surchargés par type de retour, vous pouvez le faire `op_Explicit` et `op_Implicit`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-133">As a special exception to the general rule that methods cannot be overloaded by return type, you can do this for `op_Explicit` and `op_Implicit`.</span></span>

## <a name="enumerated-types"></a><span data-ttu-id="4f6cb-134">Types énumérés</span><span class="sxs-lookup"><span data-stu-id="4f6cb-134">Enumerated Types</span></span>

<span data-ttu-id="4f6cb-135">Le `enum` opérateur est un opérateur générique qui accepte un paramètre de type qui représente le type de la `enum` à convertir.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-135">The `enum` operator is a generic operator that takes one type parameter that represents the type of the `enum` to convert to.</span></span> <span data-ttu-id="4f6cb-136">Lorsqu’il convertit un type énuméré, tapez inférence tente de déterminer le type de le `enum` que vous souhaitez convertir.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-136">When it converts to an enumerated type, type inference attempts to determine the type of the `enum` that you want to convert to.</span></span> <span data-ttu-id="4f6cb-137">Dans l’exemple suivant, la variable `col1` n’est pas explicitement annotée, mais son type est déduit du test d’égalité ultérieur.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-137">In the following example, the variable `col1` is not explicitly annotated, but its type is inferred from the later equality test.</span></span> <span data-ttu-id="4f6cb-138">Par conséquent, le compilateur peut déduire que vous convertissez un `Color` énumération.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-138">Therefore, the compiler can deduce that you are converting to a `Color` enumeration.</span></span> <span data-ttu-id="4f6cb-139">Vous pouvez également fournir une annotation de type, comme avec `col2` dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-139">Alternatively, you can supply a type annotation, as with `col2` in the following example.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4402.fs)]

<span data-ttu-id="4f6cb-140">Vous pouvez également spécifier le type d’énumération cible explicitement comme un paramètre de type, comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4f6cb-140">You can also specify the target enumeration type explicitly as a type parameter, as in the following code:</span></span>

```fsharp
let col3 = enum<Color> 3
```

<span data-ttu-id="4f6cb-141">Notez que l’énumération effectue un cast de travail uniquement si le type sous-jacent de l’énumération est compatible avec le type en cours de conversion.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-141">Note that the enumeration casts work only if the underlying type of the enumeration is compatible with the type being converted.</span></span> <span data-ttu-id="4f6cb-142">Dans le code suivant, la conversion ne parvient pas à compiler en raison de l’incompatibilité entre `int32` et `uint32`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-142">In the following code, the conversion fails to compile because of the mismatch between `int32` and `uint32`.</span></span>

```fsharp
// Error: types are incompatible
let col4 : Color = enum 2u
```

<span data-ttu-id="4f6cb-143">Pour plus d’informations, consultez [énumérations](enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="4f6cb-143">For more information, see [Enumerations](enumerations.md).</span></span>

## <a name="casting-object-types"></a><span data-ttu-id="4f6cb-144">Conversion de Types d’objet</span><span class="sxs-lookup"><span data-stu-id="4f6cb-144">Casting Object Types</span></span>

<span data-ttu-id="4f6cb-145">Conversion entre types dans une hiérarchie d’objets est essentielle à la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-145">Conversion between types in an object hierarchy is fundamental to object-oriented programming.</span></span> <span data-ttu-id="4f6cb-146">Il existe deux types de conversions : cast ascendant (un upcast) et de conversion (cast) vers le bas.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-146">There are two basic types of conversions: casting up (upcasting) and casting down (downcasting).</span></span> <span data-ttu-id="4f6cb-147">Conversion d’une hiérarchie signifie effectuer un cast d’une référence d’objet dérivé vers une référence d’objet de base.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-147">Casting up a hierarchy means casting from a derived object reference to a base object reference.</span></span> <span data-ttu-id="4f6cb-148">Ce type de conversion est garanti tant que la classe de base est dans la hiérarchie d’héritage de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-148">Such a cast is guaranteed to work as long as the base class is in the inheritance hierarchy of the derived class.</span></span> <span data-ttu-id="4f6cb-149">Conversion d’une hiérarchie, à partir d’une référence d’objet de base à une référence d’objet dérivé, réussit uniquement si l’objet est en fait une instance du type cible appropriée (dérivée) ou un type dérivé du type de destination.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-149">Casting down a hierarchy, from a base object reference to a derived object reference, succeeds only if the object actually is an instance of the correct destination (derived) type or a type derived from the destination type.</span></span>

<span data-ttu-id="4f6cb-150">F# fournit des opérateurs pour ces types de conversions.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-150">F# provides operators for these types of conversions.</span></span> <span data-ttu-id="4f6cb-151">Le `:>` opérateur effectue un cast de la hiérarchie et le `:?>` opérateur effectue un cast vers le bas de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-151">The `:>` operator casts up the hierarchy, and the `:?>` operator casts down the hierarchy.</span></span>

### <a name="upcasting"></a><span data-ttu-id="4f6cb-152">Upcast</span><span class="sxs-lookup"><span data-stu-id="4f6cb-152">Upcasting</span></span>

<span data-ttu-id="4f6cb-153">Dans de nombreux langages orientés objet, un upcast est implicite ; en F#, les règles sont légèrement différentes.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-153">In many object-oriented languages, upcasting is implicit; in F#, the rules are slightly different.</span></span> <span data-ttu-id="4f6cb-154">Upcast est appliqué automatiquement lorsque vous passez des arguments aux méthodes sur un type d’objet.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-154">Upcasting is applied automatically when you pass arguments to methods on an object type.</span></span> <span data-ttu-id="4f6cb-155">Toutefois, pour les fonctions liées à let dans un module, un upcast n’est pas automatique, sauf si le type de paramètre est déclaré comme un type flexible.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-155">However, for let-bound functions in a module, upcasting is not automatic, unless the parameter type is declared as a flexible type.</span></span> <span data-ttu-id="4f6cb-156">Pour plus d’informations, consultez [Types flexibles](flexible-Types.md).</span><span class="sxs-lookup"><span data-stu-id="4f6cb-156">For more information, see [Flexible Types](flexible-Types.md).</span></span>

<span data-ttu-id="4f6cb-157">Le `:>` opérateur effectue un cast statique, ce qui signifie que la réussite de la conversion en est déterminée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-157">The `:>` operator performs a static cast, which means that the success of the cast is determined at compile time.</span></span> <span data-ttu-id="4f6cb-158">Si un cast qui utilise `:>` se compile correctement, il est un cast valid et ne risque pas d’échec au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-158">If a cast that uses `:>` compiles successfully, it is a valid cast and has no chance of failure at run time.</span></span>

<span data-ttu-id="4f6cb-159">Vous pouvez également utiliser le `upcast` opérateur pour effectuer une telle conversion.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-159">You can also use the `upcast` operator to perform such a conversion.</span></span> <span data-ttu-id="4f6cb-160">L’expression suivante spécifie une conversion de la hiérarchie :</span><span class="sxs-lookup"><span data-stu-id="4f6cb-160">The following expression specifies a conversion up the hierarchy:</span></span>

```fsharp
upcast expression
```

<span data-ttu-id="4f6cb-161">Lorsque vous utilisez l’opérateur upcast, le compilateur tente de déduire le type que vous convertissez à partir du contexte.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-161">When you use the upcast operator, the compiler attempts to infer the type you are converting to from the context.</span></span> <span data-ttu-id="4f6cb-162">Si le compilateur est incapable de déterminer le type de cible, le compilateur signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-162">If the compiler is unable to determine the target type, the compiler reports an error.</span></span>

### <a name="downcasting"></a><span data-ttu-id="4f6cb-163">Cast</span><span class="sxs-lookup"><span data-stu-id="4f6cb-163">Downcasting</span></span>

<span data-ttu-id="4f6cb-164">Le `:?>` opérateur effectue un cast dynamique, ce qui signifie que la réussite du cast est déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-164">The `:?>` operator performs a dynamic cast, which means that the success of the cast is determined at run time.</span></span> <span data-ttu-id="4f6cb-165">Un cast qui utilise le `:?>` opérateur n’est pas vérifié au moment de la compilation ; mais au moment de l’exécution, une tentative est effectuée pour effectuer un cast vers le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-165">A cast that uses the `:?>` operator is not checked at compile time; but at run time, an attempt is made to cast to the specified type.</span></span> <span data-ttu-id="4f6cb-166">Si l’objet est compatible avec le type de cible, le cast réussit.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-166">If the object is compatible with the target type, the cast succeeds.</span></span> <span data-ttu-id="4f6cb-167">Si l’objet n’est pas compatible avec le type de cible, le runtime déclenche un `InvalidCastException`.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-167">If the object is not compatible with the target type, the runtime raises an `InvalidCastException`.</span></span>

<span data-ttu-id="4f6cb-168">Vous pouvez également utiliser le `downcast` opérateur pour effectuer une conversion de type dynamique.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-168">You can also use the `downcast` operator to perform a dynamic type conversion.</span></span> <span data-ttu-id="4f6cb-169">L’expression suivante spécifie une conversion vers le bas de la hiérarchie à un type qui est déduit à partir du contexte du programme :</span><span class="sxs-lookup"><span data-stu-id="4f6cb-169">The following expression specifies a conversion down the hierarchy to a type that is inferred from program context:</span></span>

```fsharp
downcast expression
```

<span data-ttu-id="4f6cb-170">Comme pour le `upcast` opérateur, si le compilateur ne peut pas déduire un type de cible spécifique à partir du contexte, il signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-170">As for the `upcast` operator, if the compiler cannot infer a specific target type from the context, it reports an error.</span></span>

<span data-ttu-id="4f6cb-171">Le code suivant illustre l’utilisation de la `:>` et `:?>` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-171">The following code illustrates the use of the `:>` and `:?>` operators.</span></span> <span data-ttu-id="4f6cb-172">Le code montre que le `:?>` opérateur est mieux utilisé lorsque vous savez que la conversion réussira, car elle lève une exception `InvalidCastException` si la conversion échoue.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-172">The code illustrates that the `:?>` operator is best used when you know that conversion will succeed, because it throws `InvalidCastException` if the conversion fails.</span></span> <span data-ttu-id="4f6cb-173">Si vous ne connaissez pas qu’une conversion réussit, un test de type qui utilise un `match` expression est préférable, car il évite les surcharges de la génération d’une exception.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-173">If you do not know that a conversion will succeed, a type test that uses a `match` expression is better because it avoids the overhead of generating an exception.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4403.fs)]

<span data-ttu-id="4f6cb-174">Étant donné que les opérateurs génériques `downcast` et `upcast` reposent sur l’inférence de type pour déterminer le type d’arguments et de retour dans le code ci-dessus, vous pouvez remplacer</span><span class="sxs-lookup"><span data-stu-id="4f6cb-174">Because generic operators `downcast` and `upcast` rely on type inference to determine the argument and return type, in the above code, you can replace</span></span>

```fsharp
let base1 = d1 :> Base1
```

<span data-ttu-id="4f6cb-175">par</span><span class="sxs-lookup"><span data-stu-id="4f6cb-175">with</span></span>

```fsharp
let base1 = upcast d1
```

<span data-ttu-id="4f6cb-176">Dans le code précédent, le type d’argument et les types de retour sont `Derived1` et `Base1`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="4f6cb-176">In the previous code, the argument type and return types are `Derived1` and `Base1`, respectively.</span></span>

<span data-ttu-id="4f6cb-177">Pour plus d’informations sur les tests de type, consultez [Expressions de correspondance](match-Expressions.md).</span><span class="sxs-lookup"><span data-stu-id="4f6cb-177">For more information about type tests, see [Match Expressions](match-Expressions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4f6cb-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f6cb-178">See also</span></span>

- [<span data-ttu-id="4f6cb-179">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="4f6cb-179">F# Language Reference</span></span>](index.md)
