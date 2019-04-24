---
title: Opérateurs C#
ms.date: 04/04/2018
f1_keywords:
- cs.operators
helpviewer_keywords:
- boolean operators [C#]
- expressions [C#], operators
- logical operators [C#]
- operators [C#]
- Visual C#, operators
- indirection operators [C#]
- assignment operators [C#]
- shift operators [C#]
- relational operators [C#]
- bitwise operators [C#]
- address operators [C#]
- keywords [C#], operators
- arithmetic operators [C#]
ms.assetid: 0301e31f-22ad-49af-ac3c-d5eae7f0ac43
ms.openlocfilehash: f4267caeb6301950b9f6a8b9545a47b9f48e7920
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59977377"
---
# <a name="c-operators"></a><span data-ttu-id="5a3cb-102">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="5a3cb-102">C# operators</span></span>

<span data-ttu-id="5a3cb-103">C# fournit de nombreux opérateurs, qui sont des symboles spécifiant quelles opérations (mathématiques, indexation, appel de fonction, etc.) effectuer dans une expression.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-103">C# provides many operators, which are symbols that specify which operations (math, indexing, function call, etc.) to perform in an expression.</span></span> <span data-ttu-id="5a3cb-104">Vous pouvez [surcharger](../../programming-guide/statements-expressions-operators/overloadable-operators.md) de nombreux opérateurs pour modifier leur signification quand ils sont appliqués à un type défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-104">You can [overload](../../programming-guide/statements-expressions-operators/overloadable-operators.md) many operators to change their meaning when applied to a user-defined type.</span></span>

<span data-ttu-id="5a3cb-105">Les opérations sur les types intégraux (comme `==`, `!=`, `<`, `>`, `&` ou `|`) sont en général autorisées sur les types énumération (`enum`).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-105">Operations on integral types (such as `==`, `!=`, `<`, `>`, `&`, `|`) are generally allowed on enumeration (`enum`) types.</span></span>

<span data-ttu-id="5a3cb-106">Les sections ci-dessous listent les opérateurs C# de la priorité la plus élevée à la plus basse.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-106">The sections below list the C# operators starting with the highest precedence to the lowest.</span></span> <span data-ttu-id="5a3cb-107">Les opérateurs inclus dans chaque section partagent le même niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-107">The operators within each section share the same precedence level.</span></span>

## <a name="primary-operators"></a><span data-ttu-id="5a3cb-108">Opérateurs principaux</span><span class="sxs-lookup"><span data-stu-id="5a3cb-108">Primary operators</span></span>

<span data-ttu-id="5a3cb-109">Ce sont les opérateurs dont la priorité est la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-109">These are the highest precedence operators.</span></span>

<span data-ttu-id="5a3cb-110">[x.y](member-access-operator.md) : accès au membre.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-110">[x.y](member-access-operator.md) – member access.</span></span>

<span data-ttu-id="5a3cb-111">[x?.y](null-conditional-operators.md) : accès au membre conditionnel Null.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-111">[x?.y](null-conditional-operators.md) – null conditional member access.</span></span> <span data-ttu-id="5a3cb-112">Retourne `null` si l’opérande de gauche prend la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-112">Returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="5a3cb-113">[x?[y]](null-conditional-operators.md) : accès à l’index conditionnel Null.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-113">[x?[y]](null-conditional-operators.md) - null conditional index access.</span></span> <span data-ttu-id="5a3cb-114">Retourne `null` si l’opérande de gauche prend la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-114">Returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="5a3cb-115">[f(x)](invocation-operator.md) : appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-115">[f(x)](invocation-operator.md) – function invocation.</span></span>

<span data-ttu-id="5a3cb-116">[a&#91;x&#93;](index-operator.md) : indexation de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-116">[a&#91;x&#93;](index-operator.md) – aggregate object indexing.</span></span>

<span data-ttu-id="5a3cb-117">[x++](arithmetic-operators.md#increment-operator-) : incrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-117">[x++](arithmetic-operators.md#increment-operator-) – postfix increment.</span></span> <span data-ttu-id="5a3cb-118">Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-118">Returns the value of x and then updates the storage location with the value of x that is one greater (typically adds the integer 1).</span></span>

<span data-ttu-id="5a3cb-119">[x--](arithmetic-operators.md#decrement-operator---) : décrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-119">[x--](arithmetic-operators.md#decrement-operator---) –  postfix decrement.</span></span> <span data-ttu-id="5a3cb-120">Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x diminuée de un (soustrait généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-120">Returns the value of x and then updates the storage location with the value of x that is one less (typically subtracts the integer 1).</span></span>

<span data-ttu-id="5a3cb-121">[new](../keywords/new-operator.md) : instanciation de type.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-121">[new](../keywords/new-operator.md) – type instantiation.</span></span>

<span data-ttu-id="5a3cb-122">[typeof](../keywords/typeof.md) : retourne l’objet <xref:System.Type> qui représente l’opérande.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-122">[typeof](../keywords/typeof.md) – returns the <xref:System.Type> object representing the operand.</span></span>

<span data-ttu-id="5a3cb-123">[checked](../keywords/checked.md) : active le contrôle de dépassement de capacité pour les opérations sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-123">[checked](../keywords/checked.md) – enables overflow checking for integer operations.</span></span>

<span data-ttu-id="5a3cb-124">[unchecked](../keywords/unchecked.md) : désactive le contrôle de dépassement de capacité pour les opérations sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-124">[unchecked](../keywords/unchecked.md) – disables overflow checking for integer operations.</span></span> <span data-ttu-id="5a3cb-125">Il s'agit du comportement de compilateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-125">This is the default compiler behavior.</span></span>

<span data-ttu-id="5a3cb-126">[default(T)](../../programming-guide/statements-expressions-operators/default-value-expressions.md) – produit la valeur par défaut du type T.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-126">[default(T)](../../programming-guide/statements-expressions-operators/default-value-expressions.md) – produces the default value of type T.</span></span>

<span data-ttu-id="5a3cb-127">[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md) : déclare et retourne une instance de délégué.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-127">[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md) – declares and returns a delegate instance.</span></span>

<span data-ttu-id="5a3cb-128">[sizeof](../keywords/sizeof.md) : retourne la taille en octets de l’opérande du type.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-128">[sizeof](../keywords/sizeof.md) – returns the size in bytes of the type operand.</span></span>

<span data-ttu-id="5a3cb-129">[->](dereference-operator.md) : déréférencement de pointeur associé à l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-129">[->](dereference-operator.md) – pointer dereferencing combined with member access.</span></span>

## <a name="unary-operators"></a><span data-ttu-id="5a3cb-130">Les opérateurs unaires.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-130">Unary operators</span></span>

<span data-ttu-id="5a3cb-131">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-131">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-132">[+x](addition-operator.md) : retourne la valeur de x.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-132">[+x](addition-operator.md) – returns the value of x.</span></span>

<span data-ttu-id="5a3cb-133">[-x](subtraction-operator.md) : négation numérique.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-133">[-x](subtraction-operator.md) – numeric negation.</span></span>

<span data-ttu-id="5a3cb-134">[\!x](boolean-logical-operators.md#logical-negation-operator-) : négation logique.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-134">[\!x](boolean-logical-operators.md#logical-negation-operator-) – logical negation.</span></span>

<span data-ttu-id="5a3cb-135">[~x](bitwise-and-shift-operators.md#bitwise-complement-operator-) : complément au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-135">[~x](bitwise-and-shift-operators.md#bitwise-complement-operator-) – bitwise complement.</span></span>

<span data-ttu-id="5a3cb-136">[++x](arithmetic-operators.md#increment-operator-) : incrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-136">[++x](arithmetic-operators.md#increment-operator-) – prefix increment.</span></span> <span data-ttu-id="5a3cb-137">Retourne la valeur de x après avoir mis à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-137">Returns the value of x after updating the storage location with the value of x that is one greater (typically adds the integer 1).</span></span>

<span data-ttu-id="5a3cb-138">[--x](arithmetic-operators.md#decrement-operator---) : décrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-138">[--x](arithmetic-operators.md#decrement-operator---) – prefix decrement.</span></span> <span data-ttu-id="5a3cb-139">Retourne la valeur de x après avoir mis à jour l’emplacement de stockage avec la valeur de x diminuée d’une unité (soustrait généralement l’entier 1).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-139">Returns the value of x after updating the storage location with the value of x that is one less (typically subtracts the integer 1).</span></span>

<span data-ttu-id="5a3cb-140">[(T)x](invocation-operator.md) : cast de type.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-140">[(T)x](invocation-operator.md) – type casting.</span></span>

<span data-ttu-id="5a3cb-141">[await](../keywords/await.md) : attend un `Task`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-141">[await](../keywords/await.md) – awaits a `Task`.</span></span>

<span data-ttu-id="5a3cb-142">[&x](and-operator.md) : adresse de.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-142">[&x](and-operator.md) – address of.</span></span>

<span data-ttu-id="5a3cb-143">[\*x](multiplication-operator.md) : déréférencement.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-143">[\*x](multiplication-operator.md) – dereferencing.</span></span>

<span data-ttu-id="5a3cb-144">[Opérateur true ](../keywords/true-false-operators.md) : retourne la valeur [bool](../keywords/bool.md) `true` pour indiquer qu’un opérande est true.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-144">[true operator](../keywords/true-false-operators.md) - returns the [bool](../keywords/bool.md) value `true` to indicate that an operand is definitely true.</span></span>

<span data-ttu-id="5a3cb-145">[Opérateur false](../keywords/true-false-operators.md) : retourne la valeur [bool](../keywords/bool.md) `true` pour indiquer qu’un opérande est false.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-145">[false operator](../keywords/true-false-operators.md) - returns the [bool](../keywords/bool.md) value `true` to indicate that an operand is definitely false.</span></span>

## <a name="multiplicative-operators"></a><span data-ttu-id="5a3cb-146">Opérateurs multiplicatifs</span><span class="sxs-lookup"><span data-stu-id="5a3cb-146">Multiplicative operators</span></span>

<span data-ttu-id="5a3cb-147">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-147">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-148">[x \* y](arithmetic-operators.md#multiplication-operator-) : multiplication.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-148">[x \* y](arithmetic-operators.md#multiplication-operator-) – multiplication.</span></span>

<span data-ttu-id="5a3cb-149">[x / y](arithmetic-operators.md#division-operator-) : division.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-149">[x / y](arithmetic-operators.md#division-operator-) – division.</span></span> <span data-ttu-id="5a3cb-150">Si les opérandes sont des entiers, le résultat est un entier tronqué vers zéro (par exemple, `-7 / 2 is -3`).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-150">If the operands are integers, the result is an integer truncated toward zero (for example, `-7 / 2 is -3`).</span></span>

<span data-ttu-id="5a3cb-151">[x % y](arithmetic-operators.md#remainder-operator-) : reste.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-151">[x % y](arithmetic-operators.md#remainder-operator-) – remainder.</span></span> <span data-ttu-id="5a3cb-152">Si les opérandes sont des entiers, cet opérateur renvoie le reste de la division de x par y.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-152">If the operands are integers, this returns the remainder of dividing x by y.</span></span>  <span data-ttu-id="5a3cb-153">Si `q = x / y` et `r = x % y`, alors `x = q * y + r`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-153">If `q = x / y` and `r = x % y`, then `x = q * y + r`.</span></span>

## <a name="additive-operators"></a><span data-ttu-id="5a3cb-154">Opérateurs additifs</span><span class="sxs-lookup"><span data-stu-id="5a3cb-154">Additive operators</span></span>

<span data-ttu-id="5a3cb-155">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-155">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-156">[x + y](arithmetic-operators.md#addition-operator-) : addition.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-156">[x + y](arithmetic-operators.md#addition-operator-) – addition.</span></span>

<span data-ttu-id="5a3cb-157">[x – y](arithmetic-operators.md#subtraction-operator--) : soustraction.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-157">[x – y](arithmetic-operators.md#subtraction-operator--) – subtraction.</span></span>

## <a name="shift-operators"></a><span data-ttu-id="5a3cb-158">Opérateurs de décalage</span><span class="sxs-lookup"><span data-stu-id="5a3cb-158">Shift operators</span></span>

<span data-ttu-id="5a3cb-159">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-159">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-160">[x <\<  y](bitwise-and-shift-operators.md#left-shift-operator-) : décalage des bits vers la gauche et remplissage avec zéro à droite.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-160">[x <\<  y](bitwise-and-shift-operators.md#left-shift-operator-) – shift bits left and fill with zero on the right.</span></span>

<span data-ttu-id="5a3cb-161">[x >> y](bitwise-and-shift-operators.md#right-shift-operator-) : décalage des bits vers la droite.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-161">[x >> y](bitwise-and-shift-operators.md#right-shift-operator-) – shift bits right.</span></span> <span data-ttu-id="5a3cb-162">Si l'opérande de gauche est `int` ou `long`, alors les bits de gauche sont remplis avec le bit de signe.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-162">If the left operand is `int` or `long`, then left bits are filled with the sign bit.</span></span> <span data-ttu-id="5a3cb-163">Si l'opérande de gauche est `uint` ou `ulong`, alors les bits de gauche sont remplis avec zéro.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-163">If the left operand is `uint` or `ulong`, then left bits are filled with zero.</span></span>

## <a name="relational-and-type-testing-operators"></a><span data-ttu-id="5a3cb-164">Opérateurs relationnels et de test de type</span><span class="sxs-lookup"><span data-stu-id="5a3cb-164">Relational and type-testing operators</span></span>

<span data-ttu-id="5a3cb-165">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-165">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-166">[x \< y](less-than-operator.md) : inférieur à (true si x est inférieur à y).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-166">[x \< y](less-than-operator.md) – less than (true if x is less than y).</span></span>

<span data-ttu-id="5a3cb-167">[x > y](greater-than-operator.md) : supérieur à (true si x est supérieur à y).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-167">[x > y](greater-than-operator.md) – greater than (true if x is greater than y).</span></span>

<span data-ttu-id="5a3cb-168">[x \<= y](less-than-equal-operator.md) : supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-168">[x \<= y](less-than-equal-operator.md) – less than or equal to.</span></span>

<span data-ttu-id="5a3cb-169">[x >= y](greater-than-equal-operator.md) : supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-169">[x >= y](greater-than-equal-operator.md) – greater than or equal to.</span></span>

<span data-ttu-id="5a3cb-170">[is](../keywords/is.md) : compatibilité du type.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-170">[is](../keywords/is.md) – type compatibility.</span></span> <span data-ttu-id="5a3cb-171">Retourne true si l’opérande de gauche évalué peut être converti en type spécifié dans l’opérande de droite (type statique).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-171">Returns true if the evaluated left operand can be cast to the type specified in the right operand (a static type).</span></span>

<span data-ttu-id="5a3cb-172">[as](../keywords/as.md) : conversion de type.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-172">[as](../keywords/as.md) – type conversion.</span></span> <span data-ttu-id="5a3cb-173">Retourne l'opérande de gauche converti en type spécifié par l'opérande de droite (type statique), mais `as` retourne `null` où `(T)x` lèverait une exception.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-173">Returns the left operand cast to the type specified by the right operand (a static type), but `as` returns `null` where `(T)x` would throw an exception.</span></span>

## <a name="equality-operators"></a><span data-ttu-id="5a3cb-174">Opérateurs d'égalité</span><span class="sxs-lookup"><span data-stu-id="5a3cb-174">Equality operators</span></span>

<span data-ttu-id="5a3cb-175">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-175">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-176">[x == y](equality-operators.md#equality-operator-) : égalité.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-176">[x == y](equality-operators.md#equality-operator-) – equality.</span></span> <span data-ttu-id="5a3cb-177">Par défaut, pour les types de référence autres que `string`, cet opérateur retourne l'égalité de référence (test d'identité).</span><span class="sxs-lookup"><span data-stu-id="5a3cb-177">By default, for reference types other than `string`, this returns reference equality (identity test).</span></span> <span data-ttu-id="5a3cb-178">Toutefois, des types peuvent surcharger `==`, donc si votre objectif est de tester l'identité, il est préférable d'utiliser la méthode `ReferenceEquals` sur `object`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-178">However, types can overload `==`, so if your intent is to test identity, it is best to use the `ReferenceEquals` method on `object`.</span></span>

<span data-ttu-id="5a3cb-179">[x != y](equality-operators.md#inequality-operator-) : différent.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-179">[x != y](equality-operators.md#inequality-operator-) – not equal.</span></span> <span data-ttu-id="5a3cb-180">Consultez le commentaire sur `==`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-180">See comment for `==`.</span></span> <span data-ttu-id="5a3cb-181">Si un type surcharge `==`, alors il doit surcharger `!=`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-181">If a type overloads `==`, then it must overload `!=`.</span></span>

## <a name="logical-and-operator"></a><span data-ttu-id="5a3cb-182">Opérateur AND logique</span><span class="sxs-lookup"><span data-stu-id="5a3cb-182">Logical AND operator</span></span>

<span data-ttu-id="5a3cb-183">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-183">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-184">`x & y` – [AND logique](boolean-logical-operators.md#logical-and-operator-) dans le cas des opérandes `bool` ou [AND logique au niveau du bit](bitwise-and-shift-operators.md#logical-and-operator-) dans le cas des opérandes de type intégral.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-184">`x & y` – [logical AND](boolean-logical-operators.md#logical-and-operator-) for the `bool` operands or [bitwise logical AND](bitwise-and-shift-operators.md#logical-and-operator-) for the operands of the integral types.</span></span>

## <a name="logical-xor-operator"></a><span data-ttu-id="5a3cb-185">Opérateur XOR logique</span><span class="sxs-lookup"><span data-stu-id="5a3cb-185">Logical XOR operator</span></span>

<span data-ttu-id="5a3cb-186">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-186">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-187">`x ^ y` – [XOR logique](boolean-logical-operators.md#logical-exclusive-or-operator-) dans le cas des opérandes `bool` ou [XOR logique au niveau du bit](bitwise-and-shift-operators.md#logical-exclusive-or-operator-) dans le cas des opérandes de type intégral.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-187">`x ^ y` – [logical XOR](boolean-logical-operators.md#logical-exclusive-or-operator-) for the `bool` operands or [bitwise logical XOR](bitwise-and-shift-operators.md#logical-exclusive-or-operator-) for the operands of the integral types.</span></span>

## <a name="logical-or-operator"></a><span data-ttu-id="5a3cb-188">Opérateur OU logique</span><span class="sxs-lookup"><span data-stu-id="5a3cb-188">Logical OR operator</span></span>

<span data-ttu-id="5a3cb-189">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-189">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-190">`x | y` – [OR logique](boolean-logical-operators.md#logical-or-operator-) dans le cas des opérandes `bool` ou [OR logique au niveau du bit](bitwise-and-shift-operators.md#logical-or-operator-) dans le cas des opérandes de type intégral.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-190">`x | y` – [logical OR](boolean-logical-operators.md#logical-or-operator-) for the `bool` operands or [bitwise logical OR](bitwise-and-shift-operators.md#logical-or-operator-) for the operands of the integral types.</span></span>

## <a name="conditional-and-operator"></a><span data-ttu-id="5a3cb-191">Opérateur AND conditionnel</span><span class="sxs-lookup"><span data-stu-id="5a3cb-191">Conditional AND operator</span></span>

<span data-ttu-id="5a3cb-192">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-192">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-193">[x && y](boolean-logical-operators.md#conditional-logical-and-operator-) : ET logique.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-193">[x && y](boolean-logical-operators.md#conditional-logical-and-operator-) – logical AND.</span></span> <span data-ttu-id="5a3cb-194">Si le premier opérande prend la valeur false, C# n’évalue pas le second opérande.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-194">If the first operand evaluates to false, then C# does not evaluate the second operand.</span></span>

## <a name="conditional-or-operator"></a><span data-ttu-id="5a3cb-195">Opérateur OR conditionnel</span><span class="sxs-lookup"><span data-stu-id="5a3cb-195">Conditional OR operator</span></span>

<span data-ttu-id="5a3cb-196">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-196">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-197">[x &#124;&#124; y](boolean-logical-operators.md#conditional-logical-or-operator-) : OU logique.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-197">[x &#124;&#124; y](boolean-logical-operators.md#conditional-logical-or-operator-) – logical OR.</span></span> <span data-ttu-id="5a3cb-198">Si le premier opérande prend la valeur true, C# n’évalue pas le second opérande.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-198">If the first operand evaluates to true, then C# does not evaluate the second operand.</span></span>

## <a name="null-coalescing-operator"></a><span data-ttu-id="5a3cb-199">Opérateur de fusion de Null</span><span class="sxs-lookup"><span data-stu-id="5a3cb-199">Null-coalescing operator</span></span>

<span data-ttu-id="5a3cb-200">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-200">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-201">[x ?? y](null-coalescing-operator.md) : retourne `x` si non `null` ; dans le cas contraire, retourne `y`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-201">[x ?? y](null-coalescing-operator.md) – returns `x` if it is non-`null`; otherwise, returns `y`.</span></span>

## <a name="conditional-operator"></a><span data-ttu-id="5a3cb-202">Opérateur conditionnel</span><span class="sxs-lookup"><span data-stu-id="5a3cb-202">Conditional operator</span></span>

<span data-ttu-id="5a3cb-203">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-203">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-204">[t ? x : y](conditional-operator.md) : si le test `t` prend la valeur true, alors évalue et retourne `x` ; sinon, évalue et retourne `y`.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-204">[t ? x : y](conditional-operator.md) – if test `t` evaluates to true, then evaluate and return `x`; otherwise, evaluate and return `y`.</span></span>

## <a name="assignment-and-lambda-operators"></a><span data-ttu-id="5a3cb-205">Opérateurs d'assignation et lambda</span><span class="sxs-lookup"><span data-stu-id="5a3cb-205">Assignment and Lambda operators</span></span>

<span data-ttu-id="5a3cb-206">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-206">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="5a3cb-207">[x = y](assignment-operator.md) : affectation.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-207">[x = y](assignment-operator.md) – assignment.</span></span>

<span data-ttu-id="5a3cb-208">[x += y](addition-assignment-operator.md) : incrément.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-208">[x += y](addition-assignment-operator.md) – increment.</span></span> <span data-ttu-id="5a3cb-209">Additionne la valeur de `y` à la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-209">Add the value of `y` to the value of `x`, store the result in `x`, and return the new value.</span></span> <span data-ttu-id="5a3cb-210">Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# ajoute en tant que gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-210">If `x` designates an `event`, then `y` must be an appropriate function that C# adds as an event handler.</span></span>

<span data-ttu-id="5a3cb-211">[x -= y](subtraction-assignment-operator.md) : décrément.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-211">[x -= y](subtraction-assignment-operator.md) – decrement.</span></span> <span data-ttu-id="5a3cb-212">Soustrait la valeur de `y` de la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-212">Subtract the value of `y` from the value of `x`, store the result in `x`, and return the new value.</span></span> <span data-ttu-id="5a3cb-213">Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# supprime en tant que gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-213">If `x` designates an `event`, then `y` must be an appropriate function that C# removes as an event handler.</span></span>

<span data-ttu-id="5a3cb-214">[x \*= y](arithmetic-operators.md#compound-assignment) : affectation de multiplication.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-214">[x \*= y](arithmetic-operators.md#compound-assignment) – multiplication assignment.</span></span> <span data-ttu-id="5a3cb-215">Multiplie la valeur de `y` par la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-215">Multiply the value of `y` to the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-216">[x /= y](arithmetic-operators.md#compound-assignment) : affectation de division.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-216">[x /= y](arithmetic-operators.md#compound-assignment) – division assignment.</span></span> <span data-ttu-id="5a3cb-217">Divise la valeur de `x` par la valeur de `y`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-217">Divide the value of `x` by the value of `y`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-218">[x %= y](arithmetic-operators.md#compound-assignment) : assignation de reste.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-218">[x %= y](arithmetic-operators.md#compound-assignment) – remainder assignment.</span></span> <span data-ttu-id="5a3cb-219">Divise la valeur de `x` par la valeur de `y`, stocke le reste dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-219">Divide the value of `x` by the value of `y`, store the remainder in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-220">[x &= y](boolean-logical-operators.md#compound-assignment) : affectation ET.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-220">[x &= y](boolean-logical-operators.md#compound-assignment) – AND assignment.</span></span> <span data-ttu-id="5a3cb-221">Assigne l'opérateur AND à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-221">AND the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-222">[x &#124;= y](boolean-logical-operators.md#compound-assignment) : affectation OU.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-222">[x &#124;= y](boolean-logical-operators.md#compound-assignment) – OR assignment.</span></span> <span data-ttu-id="5a3cb-223">Assigne l'opérateur OR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-223">OR the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-224">[x ^= y](boolean-logical-operators.md#compound-assignment) : affectation XOR.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-224">[x ^= y](boolean-logical-operators.md#compound-assignment) – XOR assignment.</span></span> <span data-ttu-id="5a3cb-225">Assigne l'opérateur XOR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-225">XOR the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-226">[x <<= y](bitwise-and-shift-operators.md#compound-assignment) : affectation de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-226">[x <<= y](bitwise-and-shift-operators.md#compound-assignment) – left-shift assignment.</span></span> <span data-ttu-id="5a3cb-227">Décale la valeur de `x` vers la gauche de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-227">Shift the value of `x` left by `y` places, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-228">[x >>= y](bitwise-and-shift-operators.md#compound-assignment) : affectation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-228">[x >>= y](bitwise-and-shift-operators.md#compound-assignment) – right-shift assignment.</span></span> <span data-ttu-id="5a3cb-229">Décale la valeur de `x` vers la droite de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-229">Shift the value of `x` right by `y` places, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="5a3cb-230">[=>](lambda-operator.md) : déclaration lambda.</span><span class="sxs-lookup"><span data-stu-id="5a3cb-230">[=>](lambda-operator.md) – lambda declaration.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a3cb-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a3cb-231">See also</span></span>

- [<span data-ttu-id="5a3cb-232">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5a3cb-232">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5a3cb-233">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5a3cb-233">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5a3cb-234">C#</span><span class="sxs-lookup"><span data-stu-id="5a3cb-234">C#</span></span>](../../index.md)
- [<span data-ttu-id="5a3cb-235">Opérateurs surchargeables</span><span class="sxs-lookup"><span data-stu-id="5a3cb-235">Overloadable operators</span></span>](../../programming-guide/statements-expressions-operators/overloadable-operators.md)
- [<span data-ttu-id="5a3cb-236">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="5a3cb-236">C# Keywords</span></span>](../keywords/index.md)
