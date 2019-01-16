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
ms.openlocfilehash: 6380fa4ec99f598be0d01db1061900520e94d5f1
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333406"
---
# <a name="c-operators"></a><span data-ttu-id="31ee5-102">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="31ee5-102">C# operators</span></span>

<span data-ttu-id="31ee5-103">C# fournit de nombreux opérateurs, qui sont des symboles spécifiant quelles opérations (mathématiques, indexation, appel de fonction, etc.) effectuer dans une expression.</span><span class="sxs-lookup"><span data-stu-id="31ee5-103">C# provides many operators, which are symbols that specify which operations (math, indexing, function call, etc.) to perform in an expression.</span></span> <span data-ttu-id="31ee5-104">Vous pouvez [surcharger](../../programming-guide/statements-expressions-operators/overloadable-operators.md) de nombreux opérateurs pour modifier leur signification quand ils sont appliqués à un type défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-104">You can [overload](../../programming-guide/statements-expressions-operators/overloadable-operators.md) many operators to change their meaning when applied to a user-defined type.</span></span>

<span data-ttu-id="31ee5-105">Les opérations sur les types intégraux (comme `==`, `!=`, `<`, `>`, `&` ou `|`) sont en général autorisées sur les types énumération (`enum`).</span><span class="sxs-lookup"><span data-stu-id="31ee5-105">Operations on integral types (such as `==`, `!=`, `<`, `>`, `&`, `|`) are generally allowed on enumeration (`enum`) types.</span></span>

<span data-ttu-id="31ee5-106">Les sections ci-dessous listent les opérateurs C# de la priorité la plus élevée à la plus basse.</span><span class="sxs-lookup"><span data-stu-id="31ee5-106">The sections below list the C# operators starting with the highest precedence to the lowest.</span></span> <span data-ttu-id="31ee5-107">Les opérateurs inclus dans chaque section partagent le même niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="31ee5-107">The operators within each section share the same precedence level.</span></span>

## <a name="primary-operators"></a><span data-ttu-id="31ee5-108">Opérateurs principaux</span><span class="sxs-lookup"><span data-stu-id="31ee5-108">Primary operators</span></span>

<span data-ttu-id="31ee5-109">Ce sont les opérateurs dont la priorité est la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="31ee5-109">These are the highest precedence operators.</span></span>

<span data-ttu-id="31ee5-110">[x.y](member-access-operator.md) : accès au membre.</span><span class="sxs-lookup"><span data-stu-id="31ee5-110">[x.y](member-access-operator.md) – member access.</span></span>

<span data-ttu-id="31ee5-111">[x?.y](null-conditional-operators.md) : accès au membre conditionnel Null.</span><span class="sxs-lookup"><span data-stu-id="31ee5-111">[x?.y](null-conditional-operators.md) – null conditional member access.</span></span> <span data-ttu-id="31ee5-112">Retourne `null` si l’opérande de gauche prend la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-112">Returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="31ee5-113">[x?[y]](null-conditional-operators.md) : accès à l’index conditionnel Null.</span><span class="sxs-lookup"><span data-stu-id="31ee5-113">[x?[y]](null-conditional-operators.md) - null conditional index access.</span></span> <span data-ttu-id="31ee5-114">Retourne `null` si l’opérande de gauche prend la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-114">Returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="31ee5-115">[f(x)](invocation-operator.md) : appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="31ee5-115">[f(x)](invocation-operator.md) – function invocation.</span></span>

<span data-ttu-id="31ee5-116">[a&#91;x&#93;](index-operator.md) : indexation de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="31ee5-116">[a&#91;x&#93;](index-operator.md) – aggregate object indexing.</span></span>

<span data-ttu-id="31ee5-117">[x++](increment-operator.md) : incrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="31ee5-117">[x++](increment-operator.md) – postfix increment.</span></span> <span data-ttu-id="31ee5-118">Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="31ee5-118">Returns the value of x and then updates the storage location with the value of x that is one greater (typically adds the integer 1).</span></span>

<span data-ttu-id="31ee5-119">[x--](decrement-operator.md) : décrément suffixé.</span><span class="sxs-lookup"><span data-stu-id="31ee5-119">[x--](decrement-operator.md) –  postfix decrement.</span></span> <span data-ttu-id="31ee5-120">Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x diminuée de un (soustrait généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="31ee5-120">Returns the value of x and then updates the storage location with the value of x that is one less (typically subtracts the integer 1).</span></span>

<span data-ttu-id="31ee5-121">[new](../keywords/new-operator.md) : instanciation de type.</span><span class="sxs-lookup"><span data-stu-id="31ee5-121">[new](../keywords/new-operator.md) – type instantiation.</span></span>

<span data-ttu-id="31ee5-122">[typeof](../keywords/typeof.md) : retourne l’objet <xref:System.Type> qui représente l’opérande.</span><span class="sxs-lookup"><span data-stu-id="31ee5-122">[typeof](../keywords/typeof.md) – returns the <xref:System.Type> object representing the operand.</span></span>

<span data-ttu-id="31ee5-123">[checked](../keywords/checked.md) : active le contrôle de dépassement de capacité pour les opérations sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="31ee5-123">[checked](../keywords/checked.md) – enables overflow checking for integer operations.</span></span>

<span data-ttu-id="31ee5-124">[unchecked](../keywords/unchecked.md) : désactive le contrôle de dépassement de capacité pour les opérations sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="31ee5-124">[unchecked](../keywords/unchecked.md) – disables overflow checking for integer operations.</span></span> <span data-ttu-id="31ee5-125">Il s'agit du comportement de compilateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="31ee5-125">This is the default compiler behavior.</span></span>

<span data-ttu-id="31ee5-126">[default(T)](../../programming-guide/statements-expressions-operators/default-value-expressions.md) – produit la valeur par défaut du type T.</span><span class="sxs-lookup"><span data-stu-id="31ee5-126">[default(T)](../../programming-guide/statements-expressions-operators/default-value-expressions.md) – produces the default value of type T.</span></span>

<span data-ttu-id="31ee5-127">[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md) : déclare et retourne une instance de délégué.</span><span class="sxs-lookup"><span data-stu-id="31ee5-127">[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md) – declares and returns a delegate instance.</span></span>

<span data-ttu-id="31ee5-128">[sizeof](../keywords/sizeof.md) : retourne la taille en octets de l’opérande du type.</span><span class="sxs-lookup"><span data-stu-id="31ee5-128">[sizeof](../keywords/sizeof.md) – returns the size in bytes of the type operand.</span></span>

<span data-ttu-id="31ee5-129">[->](dereference-operator.md) : déréférencement de pointeur associé à l’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="31ee5-129">[->](dereference-operator.md) – pointer dereferencing combined with member access.</span></span>

## <a name="unary-operators"></a><span data-ttu-id="31ee5-130">Les opérateurs unaires.</span><span class="sxs-lookup"><span data-stu-id="31ee5-130">Unary operators</span></span>

<span data-ttu-id="31ee5-131">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-131">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-132">[+x](addition-operator.md) : retourne la valeur de x.</span><span class="sxs-lookup"><span data-stu-id="31ee5-132">[+x](addition-operator.md) – returns the value of x.</span></span>

<span data-ttu-id="31ee5-133">[-x](subtraction-operator.md) : négation numérique.</span><span class="sxs-lookup"><span data-stu-id="31ee5-133">[-x](subtraction-operator.md) – numeric negation.</span></span>

<span data-ttu-id="31ee5-134">[\!x](logical-negation-operator.md) : négation logique.</span><span class="sxs-lookup"><span data-stu-id="31ee5-134">[\!x](logical-negation-operator.md) – logical negation.</span></span>

<span data-ttu-id="31ee5-135">[~x](bitwise-complement-operator.md) : complément au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="31ee5-135">[~x](bitwise-complement-operator.md) – bitwise complement.</span></span>

<span data-ttu-id="31ee5-136">[++x](increment-operator.md) : incrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="31ee5-136">[++x](increment-operator.md) – prefix increment.</span></span> <span data-ttu-id="31ee5-137">Retourne la valeur de x après avoir mis à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).</span><span class="sxs-lookup"><span data-stu-id="31ee5-137">Returns the value of x after updating the storage location with the value of x that is one greater (typically adds the integer 1).</span></span>

<span data-ttu-id="31ee5-138">[--x](decrement-operator.md) : décrément préfixé.</span><span class="sxs-lookup"><span data-stu-id="31ee5-138">[--x](decrement-operator.md) – prefix decrement.</span></span> <span data-ttu-id="31ee5-139">Retourne la valeur de x après avoir mis à jour l’emplacement de stockage avec la valeur de x diminuée d’une unité (soustrait généralement l’entier 1).</span><span class="sxs-lookup"><span data-stu-id="31ee5-139">Returns the value of x after updating the storage location with the value of x that is one less (typically subtracts the integer 1).</span></span>

<span data-ttu-id="31ee5-140">[(T)x](invocation-operator.md) : cast de type.</span><span class="sxs-lookup"><span data-stu-id="31ee5-140">[(T)x](invocation-operator.md) – type casting.</span></span>

<span data-ttu-id="31ee5-141">[await](../keywords/await.md) : attend un `Task`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-141">[await](../keywords/await.md) – awaits a `Task`.</span></span>

<span data-ttu-id="31ee5-142">[&x](and-operator.md) : adresse de.</span><span class="sxs-lookup"><span data-stu-id="31ee5-142">[&x](and-operator.md) – address of.</span></span>

<span data-ttu-id="31ee5-143">[\*x](multiplication-operator.md) : déréférencement.</span><span class="sxs-lookup"><span data-stu-id="31ee5-143">[\*x](multiplication-operator.md) – dereferencing.</span></span>

## <a name="multiplicative-operators"></a><span data-ttu-id="31ee5-144">Opérateurs multiplicatifs</span><span class="sxs-lookup"><span data-stu-id="31ee5-144">Multiplicative operators</span></span>

<span data-ttu-id="31ee5-145">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-145">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-146">[x \* y](multiplication-operator.md) : multiplication.</span><span class="sxs-lookup"><span data-stu-id="31ee5-146">[x \* y](multiplication-operator.md) – multiplication.</span></span>

<span data-ttu-id="31ee5-147">[x / y](division-operator.md) : division.</span><span class="sxs-lookup"><span data-stu-id="31ee5-147">[x / y](division-operator.md) – division.</span></span> <span data-ttu-id="31ee5-148">Si les opérandes sont des entiers, le résultat est un entier tronqué vers zéro (par exemple, `-7 / 2 is -3`).</span><span class="sxs-lookup"><span data-stu-id="31ee5-148">If the operands are integers, the result is an integer truncated toward zero (for example, `-7 / 2 is -3`).</span></span>

<span data-ttu-id="31ee5-149">[x % y](remainder-operator.md) : reste.</span><span class="sxs-lookup"><span data-stu-id="31ee5-149">[x % y](remainder-operator.md) – remainder.</span></span> <span data-ttu-id="31ee5-150">Si les opérandes sont des entiers, cet opérateur renvoie le reste de la division de x par y.</span><span class="sxs-lookup"><span data-stu-id="31ee5-150">If the operands are integers, this returns the remainder of dividing x by y.</span></span>  <span data-ttu-id="31ee5-151">Si `q = x / y` et `r = x % y`, alors `x = q * y + r`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-151">If `q = x / y` and `r = x % y`, then `x = q * y + r`.</span></span>

## <a name="additive-operators"></a><span data-ttu-id="31ee5-152">Opérateurs additifs</span><span class="sxs-lookup"><span data-stu-id="31ee5-152">Additive operators</span></span>

<span data-ttu-id="31ee5-153">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-153">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-154">[x + y](addition-operator.md) : addition.</span><span class="sxs-lookup"><span data-stu-id="31ee5-154">[x + y](addition-operator.md) – addition.</span></span>

<span data-ttu-id="31ee5-155">[x – y](subtraction-operator.md) : soustraction.</span><span class="sxs-lookup"><span data-stu-id="31ee5-155">[x – y](subtraction-operator.md) – subtraction.</span></span>

## <a name="shift-operators"></a><span data-ttu-id="31ee5-156">Opérateurs de décalage</span><span class="sxs-lookup"><span data-stu-id="31ee5-156">Shift operators</span></span>

<span data-ttu-id="31ee5-157">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-157">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-158">[x <\<  y](left-shift-operator.md) : décalage des bits vers la gauche et remplissage avec zéro à droite.</span><span class="sxs-lookup"><span data-stu-id="31ee5-158">[x <\<  y](left-shift-operator.md) – shift bits left and fill with zero on the right.</span></span>

<span data-ttu-id="31ee5-159">[x >> y](right-shift-operator.md) : décalage des bits vers la droite.</span><span class="sxs-lookup"><span data-stu-id="31ee5-159">[x >> y](right-shift-operator.md) – shift bits right.</span></span> <span data-ttu-id="31ee5-160">Si l'opérande de gauche est `int` ou `long`, alors les bits de gauche sont remplis avec le bit de signe.</span><span class="sxs-lookup"><span data-stu-id="31ee5-160">If the left operand is `int` or `long`, then left bits are filled with the sign bit.</span></span> <span data-ttu-id="31ee5-161">Si l'opérande de gauche est `uint` ou `ulong`, alors les bits de gauche sont remplis avec zéro.</span><span class="sxs-lookup"><span data-stu-id="31ee5-161">If the left operand is `uint` or `ulong`, then left bits are filled with zero.</span></span>

## <a name="relational-and-type-testing-operators"></a><span data-ttu-id="31ee5-162">Opérateurs relationnels et de test de type</span><span class="sxs-lookup"><span data-stu-id="31ee5-162">Relational and type-testing operators</span></span>

<span data-ttu-id="31ee5-163">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-163">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-164">[x \< y](less-than-operator.md) : inférieur à (true si x est inférieur à y).</span><span class="sxs-lookup"><span data-stu-id="31ee5-164">[x \< y](less-than-operator.md) – less than (true if x is less than y).</span></span>

<span data-ttu-id="31ee5-165">[x > y](greater-than-operator.md) : supérieur à (true si x est supérieur à y).</span><span class="sxs-lookup"><span data-stu-id="31ee5-165">[x > y](greater-than-operator.md) – greater than (true if x is greater than y).</span></span>

<span data-ttu-id="31ee5-166">[x \<= y](less-than-equal-operator.md) : supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="31ee5-166">[x \<= y](less-than-equal-operator.md) – less than or equal to.</span></span>

<span data-ttu-id="31ee5-167">[x >= y](greater-than-equal-operator.md) : supérieur ou égal à.</span><span class="sxs-lookup"><span data-stu-id="31ee5-167">[x >= y](greater-than-equal-operator.md) – greater than or equal to.</span></span>

<span data-ttu-id="31ee5-168">[is](../keywords/is.md) : compatibilité du type.</span><span class="sxs-lookup"><span data-stu-id="31ee5-168">[is](../keywords/is.md) – type compatibility.</span></span> <span data-ttu-id="31ee5-169">Retourne true si l’opérande de gauche évalué peut être converti en type spécifié dans l’opérande de droite (type statique).</span><span class="sxs-lookup"><span data-stu-id="31ee5-169">Returns true if the evaluated left operand can be cast to the type specified in the right operand (a static type).</span></span>

<span data-ttu-id="31ee5-170">[as](../keywords/as.md) : conversion de type.</span><span class="sxs-lookup"><span data-stu-id="31ee5-170">[as](../keywords/as.md) – type conversion.</span></span> <span data-ttu-id="31ee5-171">Retourne l'opérande de gauche converti en type spécifié par l'opérande de droite (type statique), mais `as` retourne `null` où `(T)x` lèverait une exception.</span><span class="sxs-lookup"><span data-stu-id="31ee5-171">Returns the left operand cast to the type specified by the right operand (a static type), but `as` returns `null` where `(T)x` would throw an exception.</span></span>

## <a name="equality-operators"></a><span data-ttu-id="31ee5-172">Opérateurs d'égalité</span><span class="sxs-lookup"><span data-stu-id="31ee5-172">Equality operators</span></span>

<span data-ttu-id="31ee5-173">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-173">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-174">[x == y](equality-comparison-operator.md) : égalité.</span><span class="sxs-lookup"><span data-stu-id="31ee5-174">[x == y](equality-comparison-operator.md) – equality.</span></span> <span data-ttu-id="31ee5-175">Par défaut, pour les types de référence autres que `string`, cet opérateur retourne l'égalité de référence (test d'identité).</span><span class="sxs-lookup"><span data-stu-id="31ee5-175">By default, for reference types other than `string`, this returns reference equality (identity test).</span></span> <span data-ttu-id="31ee5-176">Toutefois, des types peuvent surcharger `==`, donc si votre objectif est de tester l'identité, il est préférable d'utiliser la méthode `ReferenceEquals` sur `object`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-176">However, types can overload `==`, so if your intent is to test identity, it is best to use the `ReferenceEquals` method on `object`.</span></span>

<span data-ttu-id="31ee5-177">[x != y](not-equal-operator.md) : différent.</span><span class="sxs-lookup"><span data-stu-id="31ee5-177">[x != y](not-equal-operator.md) – not equal.</span></span> <span data-ttu-id="31ee5-178">Consultez le commentaire sur `==`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-178">See comment for `==`.</span></span> <span data-ttu-id="31ee5-179">Si un type surcharge `==`, alors il doit surcharger `!=`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-179">If a type overloads `==`, then it must overload `!=`.</span></span>

## <a name="logical-and-operator"></a><span data-ttu-id="31ee5-180">Opérateur AND logique</span><span class="sxs-lookup"><span data-stu-id="31ee5-180">Logical AND operator</span></span>

<span data-ttu-id="31ee5-181">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-181">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-182">[x & y](and-operator.md) : ET logique ou au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="31ee5-182">[x & y](and-operator.md) – logical or bitwise AND.</span></span> <span data-ttu-id="31ee5-183">Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-183">You can generally use this with integer types and `enum` types.</span></span>

## <a name="logical-xor-operator"></a><span data-ttu-id="31ee5-184">Opérateur XOR logique</span><span class="sxs-lookup"><span data-stu-id="31ee5-184">Logical XOR operator</span></span>

<span data-ttu-id="31ee5-185">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-185">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-186">[x ^ y](xor-operator.md) : XOR logique ou au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="31ee5-186">[x ^ y](xor-operator.md) – logical or bitwise XOR.</span></span> <span data-ttu-id="31ee5-187">Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-187">You can generally use this with integer types and `enum` types.</span></span>

## <a name="logical-or-operator"></a><span data-ttu-id="31ee5-188">Opérateur OU logique</span><span class="sxs-lookup"><span data-stu-id="31ee5-188">Logical OR operator</span></span>

<span data-ttu-id="31ee5-189">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-189">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-190">[x &#124; y](or-operator.md) : OU logique ou au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="31ee5-190">[x &#124; y](or-operator.md) – logical or bitwise OR.</span></span> <span data-ttu-id="31ee5-191">Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-191">You can generally use this with integer types and `enum` types.</span></span>

## <a name="conditional-and-operator"></a><span data-ttu-id="31ee5-192">Opérateur AND conditionnel</span><span class="sxs-lookup"><span data-stu-id="31ee5-192">Conditional AND operator</span></span>

<span data-ttu-id="31ee5-193">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-193">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-194">[x && y](conditional-and-operator.md) : ET logique.</span><span class="sxs-lookup"><span data-stu-id="31ee5-194">[x && y](conditional-and-operator.md) – logical AND.</span></span> <span data-ttu-id="31ee5-195">Si le premier opérande prend la valeur false, C# n’évalue pas le second opérande.</span><span class="sxs-lookup"><span data-stu-id="31ee5-195">If the first operand evaluates to false, then C# does not evaluate the second operand.</span></span>

## <a name="conditional-or-operator"></a><span data-ttu-id="31ee5-196">Opérateur OR conditionnel</span><span class="sxs-lookup"><span data-stu-id="31ee5-196">Conditional OR operator</span></span>

<span data-ttu-id="31ee5-197">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-197">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-198">[x &#124;&#124; y](conditional-or-operator.md) : OU logique.</span><span class="sxs-lookup"><span data-stu-id="31ee5-198">[x &#124;&#124; y](conditional-or-operator.md) – logical OR.</span></span> <span data-ttu-id="31ee5-199">Si le premier opérande prend la valeur true, C# n’évalue pas le second opérande.</span><span class="sxs-lookup"><span data-stu-id="31ee5-199">If the first operand evaluates to true, then C# does not evaluate the second operand.</span></span>

## <a name="null-coalescing-operator"></a><span data-ttu-id="31ee5-200">Opérateur de fusion de Null</span><span class="sxs-lookup"><span data-stu-id="31ee5-200">Null-coalescing operator</span></span>

<span data-ttu-id="31ee5-201">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-201">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-202">[x ?? y](null-coalescing-operator.md) : retourne `x` si non `null` ; dans le cas contraire, retourne `y`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-202">[x ?? y](null-coalescing-operator.md) – returns `x` if it is non-`null`; otherwise, returns `y`.</span></span>

## <a name="conditional-operator"></a><span data-ttu-id="31ee5-203">Opérateur conditionnel</span><span class="sxs-lookup"><span data-stu-id="31ee5-203">Conditional operator</span></span>

<span data-ttu-id="31ee5-204">Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-204">This operator has higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-205">[t ? x : y](conditional-operator.md) : si le test `t` prend la valeur true, alors évalue et retourne `x` ; sinon, évalue et retourne `y`.</span><span class="sxs-lookup"><span data-stu-id="31ee5-205">[t ? x : y](conditional-operator.md) – if test `t` evaluates to true, then evaluate and return `x`; otherwise, evaluate and return `y`.</span></span>

## <a name="assignment-and-lambda-operators"></a><span data-ttu-id="31ee5-206">Opérateurs d'assignation et lambda</span><span class="sxs-lookup"><span data-stu-id="31ee5-206">Assignment and Lambda operators</span></span>

<span data-ttu-id="31ee5-207">Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.</span><span class="sxs-lookup"><span data-stu-id="31ee5-207">These operators have higher precedence than the next section and lower precedence than the previous section.</span></span>

<span data-ttu-id="31ee5-208">[x = y](assignment-operator.md) : affectation.</span><span class="sxs-lookup"><span data-stu-id="31ee5-208">[x = y](assignment-operator.md) – assignment.</span></span>

<span data-ttu-id="31ee5-209">[x += y](addition-assignment-operator.md) : incrément.</span><span class="sxs-lookup"><span data-stu-id="31ee5-209">[x += y](addition-assignment-operator.md) – increment.</span></span> <span data-ttu-id="31ee5-210">Additionne la valeur de `y` à la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-210">Add the value of `y` to the value of `x`, store the result in `x`, and return the new value.</span></span> <span data-ttu-id="31ee5-211">Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# ajoute en tant que gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="31ee5-211">If `x` designates an `event`, then `y` must be an appropriate function that C# adds as an event handler.</span></span>

<span data-ttu-id="31ee5-212">[x -= y](subtraction-assignment-operator.md) : décrément.</span><span class="sxs-lookup"><span data-stu-id="31ee5-212">[x -= y](subtraction-assignment-operator.md) – decrement.</span></span> <span data-ttu-id="31ee5-213">Soustrait la valeur de `y` de la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-213">Subtract the value of `y` from the value of `x`, store the result in `x`, and return the new value.</span></span> <span data-ttu-id="31ee5-214">Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# supprime en tant que gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="31ee5-214">If `x` designates an `event`, then `y` must be an appropriate function that C# removes as an event handler</span></span>

<span data-ttu-id="31ee5-215">[x \*= y](multiplication-assignment-operator.md) : affectation de multiplication.</span><span class="sxs-lookup"><span data-stu-id="31ee5-215">[x \*= y](multiplication-assignment-operator.md) – multiplication assignment.</span></span> <span data-ttu-id="31ee5-216">Multiplie la valeur de `y` par la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-216">Multiply the value of `y` to the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-217">[x /= y](division-assignment-operator.md) : affectation de division.</span><span class="sxs-lookup"><span data-stu-id="31ee5-217">[x /= y](division-assignment-operator.md) – division assignment.</span></span> <span data-ttu-id="31ee5-218">Divise la valeur de `x` par la valeur de `y`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-218">Divide the value of `x` by the value of `y`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-219">[x %= y](remainder-assignment-operator.md) : assignation de reste.</span><span class="sxs-lookup"><span data-stu-id="31ee5-219">[x %= y](remainder-assignment-operator.md) – remainder assignment.</span></span> <span data-ttu-id="31ee5-220">Divise la valeur de `x` par la valeur de `y`, stocke le reste dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-220">Divide the value of `x` by the value of `y`, store the remainder in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-221">[x &= y](and-assignment-operator.md) : affectation ET.</span><span class="sxs-lookup"><span data-stu-id="31ee5-221">[x &= y](and-assignment-operator.md) – AND assignment.</span></span> <span data-ttu-id="31ee5-222">Assigne l'opérateur AND à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-222">AND the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-223">[x &#124;= y](or-assignment-operator.md) : affectation OU.</span><span class="sxs-lookup"><span data-stu-id="31ee5-223">[x &#124;= y](or-assignment-operator.md) – OR assignment.</span></span> <span data-ttu-id="31ee5-224">Assigne l'opérateur OR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-224">OR the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-225">[x ^= y](xor-assignment-operator.md) : affectation XOR.</span><span class="sxs-lookup"><span data-stu-id="31ee5-225">[x ^= y](xor-assignment-operator.md) – XOR assignment.</span></span> <span data-ttu-id="31ee5-226">Assigne l'opérateur XOR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-226">XOR the value of `y` with the value of `x`, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-227">[x <<= y](left-shift-assignment-operator.md) : affectation de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="31ee5-227">[x <<= y](left-shift-assignment-operator.md) – left-shift assignment.</span></span> <span data-ttu-id="31ee5-228">Décale la valeur de `x` vers la gauche de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-228">Shift the value of `x` left by `y` places, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-229">[x >>= y](right-shift-assignment-operator.md) : affectation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="31ee5-229">[x >>= y](right-shift-assignment-operator.md) – right-shift assignment.</span></span> <span data-ttu-id="31ee5-230">Décale la valeur de `x` vers la droite de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="31ee5-230">Shift the value of `x` right by `y` places, store the result in `x`, and return the new value.</span></span>

<span data-ttu-id="31ee5-231">[=>](lambda-operator.md) : déclaration lambda.</span><span class="sxs-lookup"><span data-stu-id="31ee5-231">[=>](lambda-operator.md) – lambda declaration.</span></span>

## <a name="arithmetic-overflow"></a><span data-ttu-id="31ee5-232">Dépassement arithmétique</span><span class="sxs-lookup"><span data-stu-id="31ee5-232">Arithmetic overflow</span></span>

<span data-ttu-id="31ee5-233">Les opérateurs arithmétiques ([+](addition-operator.md), [-](subtraction-operator.md), [\*](multiplication-operator.md) et [/](division-operator.md)) peuvent produire des résultats qui sont en dehors de la plage de valeurs possibles pour le type numérique concerné.</span><span class="sxs-lookup"><span data-stu-id="31ee5-233">The arithmetic operators ([+](addition-operator.md), [-](subtraction-operator.md), [\*](multiplication-operator.md), [/](division-operator.md)) can produce results that are outside the range of possible values for the numeric type involved.</span></span> <span data-ttu-id="31ee5-234">Reportez-vous à la section d'un opérateur particulier pour obtenir plus d'informations, mais en règle générale, les points suivants s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="31ee5-234">You should refer to the section on a particular operator for details, but in general:</span></span>

- <span data-ttu-id="31ee5-235">Le dépassement arithmétique d'un entier lève soit une exception <xref:System.OverflowException> ou ignore les bits les plus significatifs du résultat.</span><span class="sxs-lookup"><span data-stu-id="31ee5-235">Integer arithmetic overflow either throws an <xref:System.OverflowException> or discards the most significant bits of the result.</span></span> <span data-ttu-id="31ee5-236">La division d'un entier par zéro lève toujours une exception <xref:System.DivideByZeroException>.</span><span class="sxs-lookup"><span data-stu-id="31ee5-236">Integer division by zero always throws a <xref:System.DivideByZeroException>.</span></span>

   <span data-ttu-id="31ee5-237">En cas de dépassement d’un entier, ce qui se produit dépend du contexte d’exécution, lequel peut être [checked ou unchecked](../keywords/checked-and-unchecked.md).</span><span class="sxs-lookup"><span data-stu-id="31ee5-237">When integer overflow occurs, what happens depends on the execution context, which can be [checked or unchecked](../keywords/checked-and-unchecked.md).</span></span> <span data-ttu-id="31ee5-238">Dans un contexte checked, une exception <xref:System.OverflowException> est levée.</span><span class="sxs-lookup"><span data-stu-id="31ee5-238">In a checked context, an <xref:System.OverflowException> is thrown.</span></span> <span data-ttu-id="31ee5-239">Dans un contexte unchecked, les bits les plus significatifs du résultat sont ignorés et l'exécution se poursuit.</span><span class="sxs-lookup"><span data-stu-id="31ee5-239">In an unchecked context, the most significant bits of the result are discarded and execution continues.</span></span> <span data-ttu-id="31ee5-240">Ainsi, C# vous donne la possibilité de traiter ou d'ignorer le dépassement.</span><span class="sxs-lookup"><span data-stu-id="31ee5-240">Thus, C# gives you the choice of handling or ignoring overflow.</span></span> <span data-ttu-id="31ee5-241">Par défaut, les opérations arithmétiques se produisent dans un contexte *unchecked*.</span><span class="sxs-lookup"><span data-stu-id="31ee5-241">By default, arithmetic operations occur in an *unchecked* context.</span></span>

   <span data-ttu-id="31ee5-242">En plus des opérations arithmétiques, des casts entre types intégraux peuvent générer un dépassement (par exemple en cas de conversion de type de [long](../keywords/long.md) en [int](../keywords/int.md)). Ils sont sujets à une exécution checked ou unchecked.</span><span class="sxs-lookup"><span data-stu-id="31ee5-242">In addition to the arithmetic operations, integral-type to integral-type casts can cause overflow (such as when you cast a [long](../keywords/long.md) to an [int](../keywords/int.md)), and are subject to checked or unchecked execution.</span></span> <span data-ttu-id="31ee5-243">En revanche, les opérateurs de bits et les opérateurs de décalage ne génèrent jamais de dépassement.</span><span class="sxs-lookup"><span data-stu-id="31ee5-243">However, bitwise operators and shift operators never cause overflow.</span></span>

- <span data-ttu-id="31ee5-244">Le dépassement arithmétique ou la division par zéro d'une virgule flottante ne lèvent jamais d'exception, car les types à virgule flottante se basent sur IEEE 754 et peuvent représenter l'infini et NaN (n'est pas un nombre).</span><span class="sxs-lookup"><span data-stu-id="31ee5-244">Floating-point arithmetic overflow or division by zero never throws an exception, because floating-point types are based on IEEE 754 and so have provisions for representing infinity and NaN (Not a Number).</span></span>

- <span data-ttu-id="31ee5-245">Le dépassement arithmétique d’un nombre [décimal](../keywords/decimal.md) lève toujours une exception <xref:System.OverflowException>.</span><span class="sxs-lookup"><span data-stu-id="31ee5-245">[Decimal](../keywords/decimal.md) arithmetic overflow always throws an <xref:System.OverflowException>.</span></span> <span data-ttu-id="31ee5-246">La division d'un nombre décimal par zéro lève toujours une exception <xref:System.DivideByZeroException>.</span><span class="sxs-lookup"><span data-stu-id="31ee5-246">Decimal division by zero always throws a <xref:System.DivideByZeroException>.</span></span>

## <a name="see-also"></a><span data-ttu-id="31ee5-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31ee5-247">See also</span></span>

- [<span data-ttu-id="31ee5-248">Référence C#</span><span class="sxs-lookup"><span data-stu-id="31ee5-248">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="31ee5-249">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="31ee5-249">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="31ee5-250">C#</span><span class="sxs-lookup"><span data-stu-id="31ee5-250">C#</span></span>](../../index.md)
- [<span data-ttu-id="31ee5-251">Opérateurs surchargeables</span><span class="sxs-lookup"><span data-stu-id="31ee5-251">Overloadable Operators</span></span>](../../programming-guide/statements-expressions-operators/overloadable-operators.md)
- [<span data-ttu-id="31ee5-252">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="31ee5-252">C# Keywords</span></span>](../keywords/index.md)