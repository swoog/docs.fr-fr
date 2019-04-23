---
title: Opérateurs logiques booléens – Référence C#
description: Découvrez les opérateurs C# qui effectuent des opérations de négation logique, de conjonction (AND) et de disjonction inclusive et exclusive (OR) avec des opérandes booléens.
ms.date: 04/08/2019
author: pkulikov
f1_keywords:
- '!_CSharpKeyword'
- '&_CSharpKeyword'
- ^_CSharpKeyword
- '|_CSharpKeyword'
- '&&_CSharpKeyword'
- '||_CSharpKeyword'
helpviewer_keywords:
- logical operators [C#]
- short-circuiting operators [C#]
- logical negation operator [C#]
- NOT operator [C#]
- '! operator [C#]'
- AND operator [C#]
- ampersand operator [C#]
- conjunction operator [C#]
- '& operator [C#]'
- exclusive OR operator [C#]
- XOR operator [C#]
- ^ operator [C#]
- OR operator [C#]
- disjunction operator [C#]
- '| operator [C#]'
- conditional AND operator [C#]
- short-circuiting AND operator [C#]
- '&& operator [C#]'
- conditional OR operator [C#]
- short-circuiting OR operator [C#]
- '|| operator [C#]'
ms.openlocfilehash: de621b26334bbc9679ba7e48a9d5a0cbaec67eab
ms.sourcegitcommit: d21bee9dbd32b9540ad30f9d0e2e874227040be3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59427316"
---
# <a name="boolean-logical-operators-c-reference"></a><span data-ttu-id="7c72d-103">Opérateurs logiques booléens (référence C#)</span><span class="sxs-lookup"><span data-stu-id="7c72d-103">Boolean logical operators (C# Reference)</span></span>

<span data-ttu-id="7c72d-104">Les opérateurs suivants effectuent des opérations logiques avec les opérandes [booléens](../keywords/bool.md) :</span><span class="sxs-lookup"><span data-stu-id="7c72d-104">The following operators perform logical operations with the [bool](../keywords/bool.md) operands:</span></span>

- <span data-ttu-id="7c72d-105">opérateur unaire [`!` (négation logique)](#logical-negation-operator-) ;</span><span class="sxs-lookup"><span data-stu-id="7c72d-105">Unary [`!` (logical negation)](#logical-negation-operator-) operator.</span></span>
- <span data-ttu-id="7c72d-106">opérateurs binaires [`&` (AND logique)](#logical-and-operator-), [`|` (OR logique)](#logical-or-operator-) et [`^` (OR exclusif logique)](#logical-exclusive-or-operator-),</span><span class="sxs-lookup"><span data-stu-id="7c72d-106">Binary [`&` (logical AND)](#logical-and-operator-), [`|` (logical OR)](#logical-or-operator-), and [`^` (logical exclusive OR)](#logical-exclusive-or-operator-) operators.</span></span> <span data-ttu-id="7c72d-107">qui évaluent toujours les deux opérandes ;</span><span class="sxs-lookup"><span data-stu-id="7c72d-107">Those operators always evaluate both operands.</span></span>
- <span data-ttu-id="7c72d-108">opérateurs binaires [`&&` (AND logique conditionnel)](#conditional-logical-and-operator-) et [`||` (OR logique conditionnel)](#conditional-logical-or-operator-),</span><span class="sxs-lookup"><span data-stu-id="7c72d-108">Binary [`&&` (conditional logical AND)](#conditional-logical-and-operator-) and [`||` (conditional logical OR)](#conditional-logical-or-operator-) operators.</span></span> <span data-ttu-id="7c72d-109">qui n’évaluent le second opérande que si nécessaire ;</span><span class="sxs-lookup"><span data-stu-id="7c72d-109">Those operators evaluate the second operand only if it's necessary.</span></span>

<span data-ttu-id="7c72d-110">En ce qui concerne les opérandes de type [intégral](../keywords/integral-types-table.md), les opérateurs `&`, `|` et `^` effectuent des opérations logiques au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="7c72d-110">For the operands of [integral](../keywords/integral-types-table.md) types, the `&`, `|`, and `^` operators perform bitwise logical operations.</span></span>

## <a name="logical-negation-operator-"></a><span data-ttu-id="7c72d-111">L’opérateur de négation logique !</span><span class="sxs-lookup"><span data-stu-id="7c72d-111">Logical negation operator !</span></span>

<span data-ttu-id="7c72d-112">L’opérateur `!` calcule la négation logique de son opérande.</span><span class="sxs-lookup"><span data-stu-id="7c72d-112">The `!` operator computes logical negation of its operand.</span></span> <span data-ttu-id="7c72d-113">Autrement dit, il produit `true` si l’opérande donne `false` et `false` si l’opérande donne `true` :</span><span class="sxs-lookup"><span data-stu-id="7c72d-113">That is, it produces `true`, if the operand evaluates to `false`, and `false`, if the operand evaluates to `true`:</span></span>

[!code-csharp-interactive[logical negation](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#Negation)]

## <a name="logical-and-operator-amp"></a><span data-ttu-id="7c72d-114">L’opérateur AND logique &amp;</span><span class="sxs-lookup"><span data-stu-id="7c72d-114">Logical AND operator &amp;</span></span>

<span data-ttu-id="7c72d-115">L’opérateur `&` calcule le AND logique de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-115">The `&` operator computes the logical AND of its operands.</span></span> <span data-ttu-id="7c72d-116">Le résultat de `x & y` est `true` si `x` et `y` prennent la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-116">The result of `x & y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="7c72d-117">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-117">Otherwise, the result is `false`.</span></span>

<span data-ttu-id="7c72d-118">L’opérateur `&` évalue les deux opérandes, même si le premier opérande prend la valeur `false`. Le résultat est donc `false` quelle que soit la valeur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="7c72d-118">The `&` operator evaluates both operands even if the first operand evaluates to `false`, so that the result must be `false` regardless of the value of the second operand.</span></span>

<span data-ttu-id="7c72d-119">Dans l’exemple suivant, le second opérande de l’opérateur `&` est un appel de méthode, effectué indépendamment de la valeur du premier opérande :</span><span class="sxs-lookup"><span data-stu-id="7c72d-119">In the following example, the second operand of the `&` operator is a method call, which is performed regardless of the value of the first operand:</span></span>

[!code-csharp-interactive[logical AND](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#And)]

<span data-ttu-id="7c72d-120">[L’opérateur AND logique conditionnel](#conditional-logical-and-operator-) `&&` calcule également le AND logique de ses opérandes, mais n’évalue pas le deuxième opérande si le premier donne `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-120">The [conditional logical AND operator](#conditional-logical-and-operator-) `&&` also computes the logical AND of its operands, but doesn't evaluate the second operand if the first operand evaluates to `false`.</span></span>

<span data-ttu-id="7c72d-121">Dans le cas des opérandes de type intégral, l’opérateur `&` calcule le [AND logique au niveau du bit](and-operator.md#integer-logical-bitwise-and-operator) de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-121">For the operands of integral types, the `&` operator computes [bitwise logical AND](and-operator.md#integer-logical-bitwise-and-operator) of its operands.</span></span> <span data-ttu-id="7c72d-122">L’opérateur unaire `&` est [l’opérateur address-of](and-operator.md#unary-address-of-operator).</span><span class="sxs-lookup"><span data-stu-id="7c72d-122">The unary `&` operator is the [address-of operator](and-operator.md#unary-address-of-operator).</span></span>

## <a name="logical-exclusive-or-operator-"></a><span data-ttu-id="7c72d-123">L’opérateur OR exclusif logique ^</span><span class="sxs-lookup"><span data-stu-id="7c72d-123">Logical exclusive OR operator ^</span></span>

<span data-ttu-id="7c72d-124">L’opérateur `^` calcule le OR exclusif logique, également appelé XOR logique, de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-124">The `^` operator computes the logical exclusive OR, also known as the logical XOR, of its operands.</span></span> <span data-ttu-id="7c72d-125">Le résultat de `x ^ y` est `true` si `x` donne `true` et `y` donne `false`, ou `x` donne `false` et `y` donne `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-125">The result of `x ^ y` is `true` if `x` evaluates to `true` and `y` evaluates to `false`, or `x` evaluates to `false` and `y` evaluates to `true`.</span></span> <span data-ttu-id="7c72d-126">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-126">Otherwise, the result is `false`.</span></span> <span data-ttu-id="7c72d-127">Autrement dit, pour les opérandes `bool`, l’opérateur `^` calcule le même résultat que [l’opérateur d’inégalité](equality-operators.md#inequality-operator-) `!=`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-127">That is, for the `bool` operands, the `^` operator computes the same result as the [inequality operator](equality-operators.md#inequality-operator-) `!=`.</span></span>

[!code-csharp-interactive[logical exclusive OR](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#Xor)]

<span data-ttu-id="7c72d-128">Dans le cas des opérandes de type intégral, l’opérateur `^` calcule le [OR exclusif logique au niveau du bit](xor-operator.md) de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-128">For the operands of integral types, the `^` operator computes [bitwise logical exclusive OR](xor-operator.md) of its operands.</span></span>

## <a name="logical-or-operator-"></a><span data-ttu-id="7c72d-129">L’opérateur OU logique |</span><span class="sxs-lookup"><span data-stu-id="7c72d-129">Logical OR operator |</span></span>

<span data-ttu-id="7c72d-130">L’opérateur `|` calcule le OR logique de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-130">The `|` operator computes the logical OR of its operands.</span></span> <span data-ttu-id="7c72d-131">Le résultat de `x | y` est `true` si `x` ou `y` prend la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-131">The result of `x | y` is `true` if either `x` or `y` evaluates to `true`.</span></span> <span data-ttu-id="7c72d-132">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-132">Otherwise, the result is `false`.</span></span>

<span data-ttu-id="7c72d-133">L’opérateur `|` évalue les deux opérandes, même si le premier opérande prend la valeur `true`. Le résultat est donc `true` quelle que soit la valeur du deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="7c72d-133">The `|` operator evaluates both operands even if the first operand evaluates to `true`, so that the result must be `true` regardless of the value of the second operand.</span></span>

<span data-ttu-id="7c72d-134">Dans l’exemple suivant, le second opérande de l’opérateur `|` est un appel de méthode, effectué indépendamment de la valeur du premier opérande :</span><span class="sxs-lookup"><span data-stu-id="7c72d-134">In the following example, the second operand of the `|` operator is a method call, which is performed regardless of the value of the first operand:</span></span>

[!code-csharp-interactive[logical OR](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#Or)]

<span data-ttu-id="7c72d-135">[L’opérateur OR logique conditionnel](#conditional-logical-or-operator-) `||` calcule également le OR logique de ses opérandes, mais n’évalue pas le deuxième opérande si le premier donne `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-135">The [conditional logical OR operator](#conditional-logical-or-operator-) `||` also computes the logical OR of its operands, but doesn't evaluate the second operand if the first operand evaluates to `true`.</span></span>

<span data-ttu-id="7c72d-136">Dans le cas des opérandes de type intégral, l’opérateur `|` calcule le [OR logique au niveau du bit](or-operator.md) de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-136">For the operands of integral types, the `|` operator computes [bitwise logical OR](or-operator.md) of its operands.</span></span>

## <a name="conditional-logical-and-operator-ampamp"></a><span data-ttu-id="7c72d-137">L’opérateur AND logique conditionnel &amp;&amp;</span><span class="sxs-lookup"><span data-stu-id="7c72d-137">Conditional logical AND operator &amp;&amp;</span></span>

<span data-ttu-id="7c72d-138">L’opérateur AND logique conditionnel `&&`, également appelé opérateur AND logique de « court-circuit », calcule le AND logique de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-138">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its operands.</span></span> <span data-ttu-id="7c72d-139">Le résultat de `x && y` est `true` si `x` et `y` prennent la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-139">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="7c72d-140">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-140">Otherwise, the result is `false`.</span></span> <span data-ttu-id="7c72d-141">Si le premier opérande donne `false`, le deuxième n’est pas évalué.</span><span class="sxs-lookup"><span data-stu-id="7c72d-141">If the first operand evaluates to `false`, the second operand is not evaluated.</span></span>

<span data-ttu-id="7c72d-142">Dans l’exemple suivant, le deuxième opérande de l’opérateur `&&` est un appel de méthode, non effectué si le premier opérande donne `false` :</span><span class="sxs-lookup"><span data-stu-id="7c72d-142">In the following example, the second operand of the `&&` operator is a method call, which isn't performed if the first operand evaluates to `false`:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#ConditionalAnd)]

<span data-ttu-id="7c72d-143">[L’opérateur AND logique](#logical-and-operator-) `&` calcule également le AND logique de ses opérandes, mais évalue toujours les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-143">The [logical AND operator](#logical-and-operator-) `&` also computes the logical AND of its operands, but always evaluates both operands.</span></span>

## <a name="conditional-logical-or-operator-"></a><span data-ttu-id="7c72d-144">L’opérateur OR logique conditionnel ||</span><span class="sxs-lookup"><span data-stu-id="7c72d-144">Conditional logical OR operator ||</span></span>

<span data-ttu-id="7c72d-145">L’opérateur OR logique conditionnel `||`, également appelé opérateur OR logique de « court-circuit », calcule le OR logique de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-145">The conditional logical OR operator `||`, also known as the "short-circuiting" logical OR operator, computes the logical OR of its operands.</span></span> <span data-ttu-id="7c72d-146">Le résultat de `x || y` est `true` si `x` ou `y` prend la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-146">The result of `x || y` is `true` if either `x` or `y` evaluates to `true`.</span></span> <span data-ttu-id="7c72d-147">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-147">Otherwise, the result is `false`.</span></span> <span data-ttu-id="7c72d-148">Si le premier opérande donne `true`, le deuxième n’est pas évalué.</span><span class="sxs-lookup"><span data-stu-id="7c72d-148">If the first operand evaluates to `true`, the second operand is not evaluated.</span></span>

<span data-ttu-id="7c72d-149">Dans l’exemple suivant, le deuxième opérande de l’opérateur `||` est un appel de méthode, non effectué si le premier opérande donne `true` :</span><span class="sxs-lookup"><span data-stu-id="7c72d-149">In the following example, the second operand of the `||` operator is a method call, which isn't performed if the first operand evaluates to `true`:</span></span>

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#ConditionalOr)]

<span data-ttu-id="7c72d-150">[L’opérateur OR logique](#logical-or-operator-) `|` calcule également le OR logique de ses opérandes, mais évalue toujours les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="7c72d-150">The [logical OR operator](#logical-or-operator-) `|` also computes the logical OR of its operands, but always evaluates both operands.</span></span>

## <a name="nullable-boolean-logical-operators"></a><span data-ttu-id="7c72d-151">Les opérateurs logiques booléens Nullable</span><span class="sxs-lookup"><span data-stu-id="7c72d-151">Nullable Boolean logical operators</span></span>

<span data-ttu-id="7c72d-152">Dans le cas des opérandes `bool?`, les opérateurs `&` et `|` prennent en charge la logique à trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="7c72d-152">For the `bool?` operands, the `&` and `|` operators support the three-valued logic.</span></span> <span data-ttu-id="7c72d-153">La sémantique de ces opérateurs est définie par le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="7c72d-153">The semantics of these operators is defined by the following table:</span></span>  
  
|<span data-ttu-id="7c72d-154">x</span><span class="sxs-lookup"><span data-stu-id="7c72d-154">x</span></span>|<span data-ttu-id="7c72d-155">o</span><span class="sxs-lookup"><span data-stu-id="7c72d-155">y</span></span>|<span data-ttu-id="7c72d-156">x&y</span><span class="sxs-lookup"><span data-stu-id="7c72d-156">x&y</span></span>|<span data-ttu-id="7c72d-157">x&#124;y</span><span class="sxs-lookup"><span data-stu-id="7c72d-157">x&#124;y</span></span>|  
|----|----|----|----|  
|<span data-ttu-id="7c72d-158">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-158">true</span></span>|<span data-ttu-id="7c72d-159">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-159">true</span></span>|<span data-ttu-id="7c72d-160">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-160">true</span></span>|<span data-ttu-id="7c72d-161">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-161">true</span></span>|  
|<span data-ttu-id="7c72d-162">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-162">true</span></span>|<span data-ttu-id="7c72d-163">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-163">false</span></span>|<span data-ttu-id="7c72d-164">false</span><span class="sxs-lookup"><span data-stu-id="7c72d-164">false</span></span>|<span data-ttu-id="7c72d-165">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-165">true</span></span>|  
|<span data-ttu-id="7c72d-166">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-166">true</span></span>|<span data-ttu-id="7c72d-167">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-167">null</span></span>|<span data-ttu-id="7c72d-168">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-168">null</span></span>|<span data-ttu-id="7c72d-169">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-169">true</span></span>|  
|<span data-ttu-id="7c72d-170">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-170">false</span></span>|<span data-ttu-id="7c72d-171">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-171">true</span></span>|<span data-ttu-id="7c72d-172">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-172">false</span></span>|<span data-ttu-id="7c72d-173">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-173">true</span></span>|  
|<span data-ttu-id="7c72d-174">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-174">false</span></span>|<span data-ttu-id="7c72d-175">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-175">false</span></span>|<span data-ttu-id="7c72d-176">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-176">false</span></span>|<span data-ttu-id="7c72d-177">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-177">false</span></span>|  
|<span data-ttu-id="7c72d-178">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-178">false</span></span>|<span data-ttu-id="7c72d-179">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-179">null</span></span>|<span data-ttu-id="7c72d-180">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-180">false</span></span>|<span data-ttu-id="7c72d-181">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-181">null</span></span>|  
|<span data-ttu-id="7c72d-182">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-182">null</span></span>|<span data-ttu-id="7c72d-183">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-183">true</span></span>|<span data-ttu-id="7c72d-184">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-184">null</span></span>|<span data-ttu-id="7c72d-185">true</span><span class="sxs-lookup"><span data-stu-id="7c72d-185">true</span></span>|  
|<span data-ttu-id="7c72d-186">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-186">null</span></span>|<span data-ttu-id="7c72d-187">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-187">false</span></span>|<span data-ttu-id="7c72d-188">False</span><span class="sxs-lookup"><span data-stu-id="7c72d-188">false</span></span>|<span data-ttu-id="7c72d-189">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-189">null</span></span>|  
|<span data-ttu-id="7c72d-190">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-190">null</span></span>|<span data-ttu-id="7c72d-191">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-191">null</span></span>|<span data-ttu-id="7c72d-192">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-192">null</span></span>|<span data-ttu-id="7c72d-193">null</span><span class="sxs-lookup"><span data-stu-id="7c72d-193">null</span></span>|  

<span data-ttu-id="7c72d-194">Le comportement de ces opérateurs diffère du comportement classique des opérateurs avec des types valeur Nullable.</span><span class="sxs-lookup"><span data-stu-id="7c72d-194">The behavior of those operators differs from the typical operator behavior with nullable value types.</span></span> <span data-ttu-id="7c72d-195">En règle générale, un opérateur défini pour les opérandes d’un type valeur peut être également utilisé avec des opérandes du type valeur Nullable correspondant.</span><span class="sxs-lookup"><span data-stu-id="7c72d-195">Typically, an operator which is defined for operands of a value type can be also used with operands of the corresponding nullable value type.</span></span> <span data-ttu-id="7c72d-196">Il produit `null` si l’un de ses opérandes est `null`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-196">Such an operator produces `null` if any of its operands is `null`.</span></span> <span data-ttu-id="7c72d-197">Toutefois, les opérateurs `&` et `|` peuvent produire une valeur non Null même si l’un des opérandes est `null`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-197">However, the `&` and `|` operators can produce non-null even if one of the operands is `null`.</span></span> <span data-ttu-id="7c72d-198">Pour plus d’informations sur le comportement des opérateurs avec des types valeur Nullable, voir la section [Opérateurs](../../programming-guide/nullable-types/using-nullable-types.md#operators) de l’article [Utiliser des types Nullable](../../programming-guide/nullable-types/using-nullable-types.md).</span><span class="sxs-lookup"><span data-stu-id="7c72d-198">For more information about the operator behavior with nullable value types, see the [Operators](../../programming-guide/nullable-types/using-nullable-types.md#operators) section of the [Using nullable types](../../programming-guide/nullable-types/using-nullable-types.md) article.</span></span>

<span data-ttu-id="7c72d-199">Vous pouvez également utiliser les opérateurs `!` et `^` avec les opérandes `bool?`, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7c72d-199">You can also use the `!` and `^` operators with the `bool?` operands, as the following example shows:</span></span>

[!code-csharp-interactive[lifted negation and xor](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#WithNullableBoolean)]

<span data-ttu-id="7c72d-200">Les opérateurs logiques conditionnels `&&` et `||` ne prennent pas en charge les opérandes `bool?`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-200">The conditional logical operators `&&` and `||` don't support the `bool?` operands.</span></span>

## <a name="compound-assignment"></a><span data-ttu-id="7c72d-201">Assignation composée</span><span class="sxs-lookup"><span data-stu-id="7c72d-201">Compound assignment</span></span>

<span data-ttu-id="7c72d-202">Pour un opérateur binaire `op`, une expression d’assignation composée du formulaire</span><span class="sxs-lookup"><span data-stu-id="7c72d-202">For a binary operator `op`, a compound assignment expression of the form</span></span>

```csharp
x op= y
```

<span data-ttu-id="7c72d-203">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="7c72d-203">is equivalent to</span></span>

```csharp
x = x op y
```

<span data-ttu-id="7c72d-204">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="7c72d-204">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="7c72d-205">Les opérateurs `&`, `|` et `^` prennent en charge l’assignation composée, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7c72d-205">The `&`, `|`, and `^` operators support compound assignment, as the following example shows:</span></span>

[!code-csharp-interactive[compound assignment](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#CompoundAssignment)]

<span data-ttu-id="7c72d-206">Les opérateurs logiques conditionnels `&&` et `||` ne prennent pas en charge l’assignation composée.</span><span class="sxs-lookup"><span data-stu-id="7c72d-206">The conditional logical operators `&&` and `||` don't support compound assignment.</span></span>

## <a name="operator-precedence"></a><span data-ttu-id="7c72d-207">Précédence des opérateurs</span><span class="sxs-lookup"><span data-stu-id="7c72d-207">Operator precedence</span></span>

<span data-ttu-id="7c72d-208">La liste suivante présente les opérateurs logiques par ordre de précédence, de la plus élevée à la plus basse :</span><span class="sxs-lookup"><span data-stu-id="7c72d-208">The following list orders logical operators starting from the highest precedence to the lowest:</span></span>

- <span data-ttu-id="7c72d-209">Opérateur de négation logique</span><span class="sxs-lookup"><span data-stu-id="7c72d-209">Logical negation operator</span></span> `!`
- <span data-ttu-id="7c72d-210">Opérateur AND logique</span><span class="sxs-lookup"><span data-stu-id="7c72d-210">Logical AND operator</span></span> `&`
- <span data-ttu-id="7c72d-211">Opérateur OR exclusif logique</span><span class="sxs-lookup"><span data-stu-id="7c72d-211">Logical exclusive OR operator</span></span> `^`
- <span data-ttu-id="7c72d-212">Opérateur OU logique</span><span class="sxs-lookup"><span data-stu-id="7c72d-212">Logical OR operator</span></span> `|`
- <span data-ttu-id="7c72d-213">Opérateur AND logique conditionnel</span><span class="sxs-lookup"><span data-stu-id="7c72d-213">Conditional logical AND operator</span></span> `&&`
- <span data-ttu-id="7c72d-214">Opérateur OR logique conditionnel</span><span class="sxs-lookup"><span data-stu-id="7c72d-214">Conditional logical OR operator</span></span> `||`

<span data-ttu-id="7c72d-215">Utilisez des parenthèses, `()`, pour modifier l’ordre d’évaluation imposé par la précédence des opérateurs :</span><span class="sxs-lookup"><span data-stu-id="7c72d-215">Use parentheses, `()`, to change the order of evaluation imposed by operator precedence:</span></span>

[!code-csharp-interactive[operator precedence](~/samples/snippets/csharp/language-reference/operators/LogicalOperators.cs#Precedence)]

<span data-ttu-id="7c72d-216">Pour obtenir la liste complète des opérateurs C# classés par niveau de priorité, consultez [Opérateurs C#](index.md).</span><span class="sxs-lookup"><span data-stu-id="7c72d-216">For the complete list of C# operators ordered by precedence level, see [C# operators](index.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="7c72d-217">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="7c72d-217">Operator overloadability</span></span>

<span data-ttu-id="7c72d-218">Un type défini par l’utilisateur peut [surcharger](../keywords/operator.md) les opérateurs `!`, `&`, `|` et `^`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-218">A user-defined type can [overload](../keywords/operator.md) the `!`, `&`, `|`, and `^` operators.</span></span> <span data-ttu-id="7c72d-219">Quand un opérateur binaire est surchargé, l’opérateur d’assignation composée correspondant est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="7c72d-219">When a binary operator is overloaded, the corresponding compound assignment operator is also implicitly overloaded.</span></span> <span data-ttu-id="7c72d-220">Un type défini par l’utilisateur ne peut pas surcharger explicitement un opérateur d’assignation composée.</span><span class="sxs-lookup"><span data-stu-id="7c72d-220">A user-defined type cannot explicitly overload a compound assignment operator.</span></span>

<span data-ttu-id="7c72d-221">Un type défini par l’utilisateur ne peut pas surcharger les opérateurs logiques conditionnels `&&` et `||`.</span><span class="sxs-lookup"><span data-stu-id="7c72d-221">A user-defined type cannot overload the conditional logical operators `&&` and `||`.</span></span> <span data-ttu-id="7c72d-222">Toutefois, si un type défini par l’utilisateur surcharge les [opérateurs true et false](../keywords/true-false-operators.md) et l’opérateur `&` ou `|` d’une certaine manière, l’opération `&&` ou `||` peut être évaluée respectivement pour les opérandes de ce type.</span><span class="sxs-lookup"><span data-stu-id="7c72d-222">However, if a user-defined type overloads the [true and false operators](../keywords/true-false-operators.md) and the `&` or `|` operator in a certain way, the `&&` or `||` operation, respectively, can be evaluated for the operands of that type.</span></span> <span data-ttu-id="7c72d-223">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](~/_csharplang/spec/introduction.md).</span><span class="sxs-lookup"><span data-stu-id="7c72d-223">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](~/_csharplang/spec/introduction.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="7c72d-224">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="7c72d-224">C# language specification</span></span>

<span data-ttu-id="7c72d-225">Pour plus d’informations, consultez les sections suivantes de la [spécification du langage C#](~/_csharplang/spec/introduction.md) :</span><span class="sxs-lookup"><span data-stu-id="7c72d-225">For more information, see the following sections of the [C# language specification](~/_csharplang/spec/introduction.md):</span></span>

- [<span data-ttu-id="7c72d-226">Opérateur de négation logique</span><span class="sxs-lookup"><span data-stu-id="7c72d-226">Logical negation operator</span></span>](~/_csharplang/spec/expressions.md#logical-negation-operator)
- [<span data-ttu-id="7c72d-227">Opérateurs logiques</span><span class="sxs-lookup"><span data-stu-id="7c72d-227">Logical operators</span></span>](~/_csharplang/spec/expressions.md#logical-operators)
- [<span data-ttu-id="7c72d-228">Opérateurs logiques conditionnels</span><span class="sxs-lookup"><span data-stu-id="7c72d-228">Conditional logical operators</span></span>](~/_csharplang/spec/expressions.md#conditional-logical-operators)

## <a name="see-also"></a><span data-ttu-id="7c72d-229">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c72d-229">See also</span></span>

- [<span data-ttu-id="7c72d-230">Référence C#</span><span class="sxs-lookup"><span data-stu-id="7c72d-230">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7c72d-231">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="7c72d-231">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7c72d-232">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="7c72d-232">C# Operators</span></span>](index.md)
