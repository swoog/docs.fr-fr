---
title: Utilisation de types Nullable (Guide de programmation C#)
description: Découvrez comment utiliser les types Nullable C#.
ms.date: 08/02/2018
helpviewer_keywords:
- nullable types [C#], about nullable types
ms.assetid: 0bacbe72-ce15-4b14-83e1-9c14e6380c28
ms.openlocfilehash: 600a18cc4dc9d3eda5577336f209c5814a7edb88
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42933125"
---
# <a name="using-nullable-types-c-programming-guide"></a><span data-ttu-id="9cab7-103">Utilisation de types Nullable (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9cab7-103">Using nullable types (C# Programming Guide)</span></span>

<span data-ttu-id="9cab7-104">Les types Nullable sont des types qui représentent toutes les valeurs d’un type sous-jacent `T` ainsi qu’une autre valeur [null](../../language-reference/keywords/null.md).</span><span class="sxs-lookup"><span data-stu-id="9cab7-104">Nullable types are types that represent all the values of an underlying value type `T`, and an additional [null](../../language-reference/keywords/null.md) value.</span></span> <span data-ttu-id="9cab7-105">Pour plus d’informations, consultez la rubrique [Types Nullable](index.md).</span><span class="sxs-lookup"><span data-stu-id="9cab7-105">For more information, see the [Nullable types](index.md) topic.</span></span>

<span data-ttu-id="9cab7-106">Vous pouvez faire référence à un type Nullable dans l’un des formats suivants : `Nullable<T>` ou `T?`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-106">You can refer to a nullable type in any of the following forms: `Nullable<T>` or `T?`.</span></span> <span data-ttu-id="9cab7-107">Ces deux formats sont interchangeables.</span><span class="sxs-lookup"><span data-stu-id="9cab7-107">These two forms are interchangeable.</span></span>  
  
## <a name="declaration-and-assignment"></a><span data-ttu-id="9cab7-108">Déclaration et affectation</span><span class="sxs-lookup"><span data-stu-id="9cab7-108">Declaration and assignment</span></span>

<span data-ttu-id="9cab7-109">Comme un type valeur peut être converti implicitement en type Nullable correspondant, vous affectez une valeur à un type Nullable comme vous le feriez pour son type valeur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9cab7-109">As a value type can be implicitly converted to the corresponding nullable type, you assign a value to a nullable type as you would for its underlying value type.</span></span> <span data-ttu-id="9cab7-110">Vous pouvez également affecter la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-110">You also can assign the `null` value.</span></span>  <span data-ttu-id="9cab7-111">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9cab7-111">For example:</span></span>
  
[!code-csharp[declare and assign](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#1)]

## <a name="examination-of-a-nullable-type-value"></a><span data-ttu-id="9cab7-112">Examen d’une valeur de type Nullable</span><span class="sxs-lookup"><span data-stu-id="9cab7-112">Examination of a nullable type value</span></span>

<span data-ttu-id="9cab7-113">Pour examiner une instance d’un type Nullable à la recherche de la valeur null et récupérer une valeur d’un type sous-jacent, utilisez les propriétés en lecture seule suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cab7-113">Use the following readonly properties to examine an instance of a nullable type for null and retrieve a value of an underlying type:</span></span>  
  
- <span data-ttu-id="9cab7-114"><xref:System.Nullable%601.HasValue%2A?displayProperty=nameWithType> indique si une instance d’un type Nullable a une valeur de son type sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9cab7-114"><xref:System.Nullable%601.HasValue%2A?displayProperty=nameWithType> indicates whether an instance of a nullable type has a value of its underlying type.</span></span>
  
- <span data-ttu-id="9cab7-115"><xref:System.Nullable%601.Value%2A?displayProperty=nameWithType> obtient la valeur d’un type sous-jacent si <xref:System.Nullable%601.HasValue%2A> est `true`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-115"><xref:System.Nullable%601.Value%2A?displayProperty=nameWithType> gets the value of an underlying type if <xref:System.Nullable%601.HasValue%2A> is `true`.</span></span> <span data-ttu-id="9cab7-116">Si <xref:System.Nullable%601.HasValue%2A> est `false`, la propriété <xref:System.Nullable%601.Value%2A> lève une <xref:System.InvalidOperationException>.</span><span class="sxs-lookup"><span data-stu-id="9cab7-116">If <xref:System.Nullable%601.HasValue%2A> is `false`, the <xref:System.Nullable%601.Value%2A> property throws an <xref:System.InvalidOperationException>.</span></span>
  
<span data-ttu-id="9cab7-117">Le code dans l’exemple suivant utilise la propriété `HasValue` pour tester si la variable contient une valeur avant de l’afficher :</span><span class="sxs-lookup"><span data-stu-id="9cab7-117">The code in the following example uses the `HasValue` property to test whether the variable contains a value before displaying it:</span></span>
  
[!code-csharp-interactive[use HasValue](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#2)]
  
<span data-ttu-id="9cab7-118">Vous pouvez également comparer une variable de type Nullable avec `null` au lieu d’utiliser la propriété `HasValue`, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="9cab7-118">You also can compare a nullable type variable with `null` instead of using the `HasValue` property, as the following example shows:</span></span>  
  
[!code-csharp-interactive[use comparison with null](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#3)]

<span data-ttu-id="9cab7-119">À compter de C# 7.0, vous pouvez utiliser les [critères spéciaux](../../pattern-matching.md) pour examiner et obtenir une valeur d’un type Nullable :</span><span class="sxs-lookup"><span data-stu-id="9cab7-119">Beginning with C# 7.0, you can use [pattern matching](../../pattern-matching.md) to both examine and get a value of a nullable type:</span></span>

[!code-csharp-interactive[use pattern matching](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#4)]

## <a name="conversion-from-a-nullable-type-to-an-underlying-type"></a><span data-ttu-id="9cab7-120">Conversion d’un type Nullable en type sous-jacent</span><span class="sxs-lookup"><span data-stu-id="9cab7-120">Conversion from a nullable type to an underlying type</span></span>

<span data-ttu-id="9cab7-121">Si vous devez affecter une valeur de type Nullable à un type non Nullable, utilisez l’[opérateur de fusion null `??`](../../language-reference/operators/null-coalescing-operator.md) pour spécifier la valeur à affecter si une valeur de type Nullable est null (vous pouvez également utiliser pour cela la méthode <xref:System.Nullable%601.GetValueOrDefault(%600)?displayProperty=nameWithType>) :</span><span class="sxs-lookup"><span data-stu-id="9cab7-121">If you need to assign a nullable type value to a non-nullable type, use the [null-coalescing operator `??`](../../language-reference/operators/null-coalescing-operator.md) to specify the value to be assigned if a nullable type value is null (you also can use the <xref:System.Nullable%601.GetValueOrDefault(%600)?displayProperty=nameWithType> method to do that):</span></span>
  
[!code-csharp-interactive[?? operator](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#5)]

<span data-ttu-id="9cab7-122">Utilisez la méthode <xref:System.Nullable%601.GetValueOrDefault?displayProperty=nameWithType> si la valeur à utiliser quand une valeur de type Nullable est null doit être la valeur par défaut du type valeur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="9cab7-122">Use the <xref:System.Nullable%601.GetValueOrDefault?displayProperty=nameWithType> method if the value to be used when a nullable type value is null should be the default value of the underlying value type.</span></span>
  
<span data-ttu-id="9cab7-123">Vous pouvez convertir explicitement un type Nullable en un type non Nullable.</span><span class="sxs-lookup"><span data-stu-id="9cab7-123">You can explicitly cast a nullable type to a non-nullable type.</span></span> <span data-ttu-id="9cab7-124">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9cab7-124">For example:</span></span>  
  
[!code-csharp[explicit cast](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#6)]

<span data-ttu-id="9cab7-125">Au moment de l’exécution, si la valeur d’un type Nullable est null, le cast explicite lève une <xref:System.InvalidOperationException>.</span><span class="sxs-lookup"><span data-stu-id="9cab7-125">At run time, if the value of a nullable type is null, the explicit cast throws an <xref:System.InvalidOperationException>.</span></span>

<span data-ttu-id="9cab7-126">Un type valeur non Nullable est implicitement converti en type Nullable correspondant.</span><span class="sxs-lookup"><span data-stu-id="9cab7-126">A non-nullable value type is implicitly converted to the corresponding nullable type.</span></span>
  
## <a name="operators"></a><span data-ttu-id="9cab7-127">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="9cab7-127">Operators</span></span>

<span data-ttu-id="9cab7-128">Les opérateurs unaire et binaire prédéfinis et tous les opérateurs définis par l’utilisateur existant pour les types valeur peuvent également être utilisés par les types Nullable.</span><span class="sxs-lookup"><span data-stu-id="9cab7-128">The predefined unary and binary operators and any user-defined operators that exist for value types may also be used by nullable types.</span></span> <span data-ttu-id="9cab7-129">Ces opérateurs produisent une valeur null si l’un des opérandes ou les deux sont null ; sinon, l’opérateur utilise les valeurs contenues pour calculer le résultat.</span><span class="sxs-lookup"><span data-stu-id="9cab7-129">These operators produce a null value if one or both operands are null; otherwise, the operator uses the contained values to calculate the result.</span></span> <span data-ttu-id="9cab7-130">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9cab7-130">For example:</span></span>  
  
[!code-csharp[operators](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#7)]
  
<span data-ttu-id="9cab7-131">Pour les opérateurs relationnels (`<`, `>`, `<=`, `>=`), si l’un des opérandes ou les deux sont null, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-131">For the relational operators (`<`, `>`, `<=`, `>=`), if one or both operands are null, the result is `false`.</span></span> <span data-ttu-id="9cab7-132">Ne partez pas du principe que parce qu’une comparaison spécifique (par exemple `<=`) retourne `false`, la comparaison opposée (`>`) retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-132">Do not assume that because a particular comparison (for example, `<=`) returns `false`, the opposite comparison (`>`) returns `true`.</span></span> <span data-ttu-id="9cab7-133">L’exemple suivant montre que 10 n’est</span><span class="sxs-lookup"><span data-stu-id="9cab7-133">The following example shows that 10 is</span></span>

- <span data-ttu-id="9cab7-134">ni supérieur ou égal à null,</span><span class="sxs-lookup"><span data-stu-id="9cab7-134">neither greater than or equal to null,</span></span>
- <span data-ttu-id="9cab7-135">ni inférieur à null.</span><span class="sxs-lookup"><span data-stu-id="9cab7-135">nor less than null.</span></span>
  
[!code-csharp-interactive[relational and equality operators](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#8)]
  
<span data-ttu-id="9cab7-136">L’exemple ci-dessus montre également qu’une comparaison d’égalité de deux types Nullable tous deux null donne la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="9cab7-136">The above example also shows that an equality comparison of two nullable types that are both null evaluates to `true`.</span></span>

## <a name="boxing-and-unboxing"></a><span data-ttu-id="9cab7-137">Boxing et unboxing</span><span class="sxs-lookup"><span data-stu-id="9cab7-137">Boxing and unboxing</span></span>

<span data-ttu-id="9cab7-138">Un type valeur Nullable est [boxed](../types/boxing-and-unboxing.md) d’après les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cab7-138">A nullable value type is [boxed](../types/boxing-and-unboxing.md) by the following rules:</span></span>

- <span data-ttu-id="9cab7-139">Si <xref:System.Nullable%601.HasValue%2A> retourne `false`, la référence null est générée.</span><span class="sxs-lookup"><span data-stu-id="9cab7-139">If <xref:System.Nullable%601.HasValue%2A> returns `false`, the null reference is produced.</span></span>  
- <span data-ttu-id="9cab7-140">Si <xref:System.Nullable%601.HasValue%2A> retourne `true`, une valeur du type valeur sous-jacent `T` est boxed, pas l’instance de <xref:System.Nullable%601>.</span><span class="sxs-lookup"><span data-stu-id="9cab7-140">If <xref:System.Nullable%601.HasValue%2A> returns `true`, a value of the underlying value type `T` is boxed, not the instance of <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="9cab7-141">Vous pouvez effectuer l’unboxing du type valeur boxed vers le type Nullable correspondant, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="9cab7-141">You can unbox the boxed value type to the corresponding nullable type, as the following example shows:</span></span>

[!code-csharp-interactive[boxing and unboxing](../../../../samples/snippets/csharp/programming-guide/nullable-types/NullableTypesUsage.cs#9)]

## <a name="the-bool-type"></a><span data-ttu-id="9cab7-142">Type bool?</span><span class="sxs-lookup"><span data-stu-id="9cab7-142">The bool? type</span></span>

<span data-ttu-id="9cab7-143">Le type Nullable `bool?` peut contenir trois valeurs différentes : [true](../../language-reference/keywords/true-literal.md), [false](../../language-reference/keywords/false-literal.md) et [null](../../language-reference/keywords/null.md).</span><span class="sxs-lookup"><span data-stu-id="9cab7-143">The `bool?` nullable type can contain three different values: [true](../../language-reference/keywords/true-literal.md), [false](../../language-reference/keywords/false-literal.md) and [null](../../language-reference/keywords/null.md).</span></span> <span data-ttu-id="9cab7-144">Le type `bool?` est comme le type de variable booléen utilisé dans SQL.</span><span class="sxs-lookup"><span data-stu-id="9cab7-144">The `bool?` type is like the Boolean variable type that is used in SQL.</span></span> <span data-ttu-id="9cab7-145">Pour vérifier que les résultats produits par les opérateurs `&` et `|` sont cohérents avec le type booléen à trois valeurs dans SQL, les opérateurs prédéfinis suivants sont fournis :</span><span class="sxs-lookup"><span data-stu-id="9cab7-145">To ensure that the results produced by the `&` and `|` operators are consistent with the three-valued Boolean type in SQL, the following predefined operators are provided:</span></span>

- `bool? operator &(bool? x, bool? y)`  
- `bool? operator |(bool? x, bool? y)`  
  
<span data-ttu-id="9cab7-146">La sémantique de ces opérateurs est définie par le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="9cab7-146">The semantics of these operators is defined by the following table:</span></span>  
  
|<span data-ttu-id="9cab7-147">x</span><span class="sxs-lookup"><span data-stu-id="9cab7-147">x</span></span>|<span data-ttu-id="9cab7-148">o</span><span class="sxs-lookup"><span data-stu-id="9cab7-148">y</span></span>|<span data-ttu-id="9cab7-149">x&y</span><span class="sxs-lookup"><span data-stu-id="9cab7-149">x&y</span></span>|<span data-ttu-id="9cab7-150">x&#124;y</span><span class="sxs-lookup"><span data-stu-id="9cab7-150">x&#124;y</span></span>|  
|-------|-------|---------|--------------|  
|<span data-ttu-id="9cab7-151">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-151">true</span></span>|<span data-ttu-id="9cab7-152">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-152">true</span></span>|<span data-ttu-id="9cab7-153">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-153">true</span></span>|<span data-ttu-id="9cab7-154">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-154">true</span></span>|  
|<span data-ttu-id="9cab7-155">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-155">true</span></span>|<span data-ttu-id="9cab7-156">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-156">false</span></span>|<span data-ttu-id="9cab7-157">false</span><span class="sxs-lookup"><span data-stu-id="9cab7-157">false</span></span>|<span data-ttu-id="9cab7-158">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-158">true</span></span>|  
|<span data-ttu-id="9cab7-159">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-159">true</span></span>|<span data-ttu-id="9cab7-160">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-160">null</span></span>|<span data-ttu-id="9cab7-161">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-161">null</span></span>|<span data-ttu-id="9cab7-162">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-162">true</span></span>|  
|<span data-ttu-id="9cab7-163">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-163">false</span></span>|<span data-ttu-id="9cab7-164">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-164">true</span></span>|<span data-ttu-id="9cab7-165">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-165">false</span></span>|<span data-ttu-id="9cab7-166">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-166">true</span></span>|  
|<span data-ttu-id="9cab7-167">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-167">false</span></span>|<span data-ttu-id="9cab7-168">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-168">false</span></span>|<span data-ttu-id="9cab7-169">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-169">false</span></span>|<span data-ttu-id="9cab7-170">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-170">false</span></span>|  
|<span data-ttu-id="9cab7-171">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-171">false</span></span>|<span data-ttu-id="9cab7-172">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-172">null</span></span>|<span data-ttu-id="9cab7-173">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-173">false</span></span>|<span data-ttu-id="9cab7-174">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-174">null</span></span>|  
|<span data-ttu-id="9cab7-175">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-175">null</span></span>|<span data-ttu-id="9cab7-176">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-176">true</span></span>|<span data-ttu-id="9cab7-177">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-177">null</span></span>|<span data-ttu-id="9cab7-178">true</span><span class="sxs-lookup"><span data-stu-id="9cab7-178">true</span></span>|  
|<span data-ttu-id="9cab7-179">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-179">null</span></span>|<span data-ttu-id="9cab7-180">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-180">false</span></span>|<span data-ttu-id="9cab7-181">False</span><span class="sxs-lookup"><span data-stu-id="9cab7-181">false</span></span>|<span data-ttu-id="9cab7-182">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-182">null</span></span>|  
|<span data-ttu-id="9cab7-183">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-183">null</span></span>|<span data-ttu-id="9cab7-184">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-184">null</span></span>|<span data-ttu-id="9cab7-185">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-185">null</span></span>|<span data-ttu-id="9cab7-186">null</span><span class="sxs-lookup"><span data-stu-id="9cab7-186">null</span></span>|  

<span data-ttu-id="9cab7-187">Notez que ces deux opérateurs ne suivent pas les règles décrites dans la section [Opérateurs](#operators) : le résultat d’une évaluation d’opérateur peut être non null même si l’un des opérandes est null.</span><span class="sxs-lookup"><span data-stu-id="9cab7-187">Note that these two operators don't follow the rules described in the [Operators](#operators) section: the result of an operator evaluation can be non-null even if one of the operands is null.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cab7-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cab7-188">See also</span></span>

 [<span data-ttu-id="9cab7-189">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="9cab7-189">Nullable types</span></span>](index.md)  
 [<span data-ttu-id="9cab7-190">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9cab7-190">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="9cab7-191">Que signifie réellement « Lifted » ?</span><span class="sxs-lookup"><span data-stu-id="9cab7-191">What exactly does 'lifted' mean?</span></span>](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)  
