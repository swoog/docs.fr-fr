---
title: is - Référence C#
ms.custom: seodec18
ms.date: 04/09/2019
f1_keywords:
- is_CSharpKeyword
- is
helpviewer_keywords:
- is keyword [C#]
ms.assetid: bc62316a-d41f-4f90-8300-c6f4f0556e43
ms.openlocfilehash: 9fb57caeafde9db5759300d938a85f4abf4d05f3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59672457"
---
# <a name="is-c-reference"></a><span data-ttu-id="e8555-102">is (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e8555-102">is (C# Reference)</span></span>

<span data-ttu-id="e8555-103">Vérifie si un objet est compatible avec un type donné, ou (avec C# 7.0) teste une expression par rapport à un modèle.</span><span class="sxs-lookup"><span data-stu-id="e8555-103">Checks if an object is compatible with a given type, or (starting with C# 7.0) tests an expression against a pattern.</span></span>

## <a name="testing-for-type-compatibility"></a><span data-ttu-id="e8555-104">Test de compatibilité de type</span><span class="sxs-lookup"><span data-stu-id="e8555-104">Testing for type compatibility</span></span>

<span data-ttu-id="e8555-105">Le mot clé `is` évalue la compatibilité de type au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e8555-105">The `is` keyword evaluates type compatibility at runtime.</span></span> <span data-ttu-id="e8555-106">Il détermine si une instance d’objet ou le résultat d’une expression peuvent être convertis en un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8555-106">It determines whether an object instance or the result of an expression can be converted to a specified type.</span></span> <span data-ttu-id="e8555-107">Sa syntaxe est</span><span class="sxs-lookup"><span data-stu-id="e8555-107">It has the syntax</span></span>

```csharp
   expr is type
```

<span data-ttu-id="e8555-108">où *expr* est une expression qui correspond à une instance d’un type, et où *type* est le nom du type dans lequel le résultat de *expr* doit être converti.</span><span class="sxs-lookup"><span data-stu-id="e8555-108">where *expr* is an expression that evaluates to an instance of some type, and *type* is the name of the type to which the result of *expr* is to be converted.</span></span> <span data-ttu-id="e8555-109">L’instruction `is` est `true` si *expr* est non-Null et si l’objet qui résulte de l’évaluation de l’expression peut être converti en *type* ; sinon, elle retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="e8555-109">The `is` statement is `true` if *expr* is non-null and the object that results from evaluating the expression can be converted to *type*; otherwise, it returns `false`.</span></span>

<span data-ttu-id="e8555-110">Par exemple, le code suivant détermine si `obj` peut être casté en une instance de type `Person` :</span><span class="sxs-lookup"><span data-stu-id="e8555-110">For example, the following code determines if `obj` can be cast to an instance of the `Person` type:</span></span>

[!code-csharp[is#1](../../../../samples/snippets/csharp/language-reference/keywords/is/is1.cs#1)]

<span data-ttu-id="e8555-111">L’instruction `is` a la valeur true si :</span><span class="sxs-lookup"><span data-stu-id="e8555-111">The `is` statement is true if:</span></span>

- <span data-ttu-id="e8555-112">*expr* est une instance du même type que *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-112">*expr* is an instance of the same type as *type*.</span></span>

- <span data-ttu-id="e8555-113">*expr* est une instance d’un type qui dérive de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-113">*expr* is an instance of a type that derives from *type*.</span></span> <span data-ttu-id="e8555-114">En d’autres termes, le résultat de *expr* peut être upcasté en une instance de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-114">In other words, the result of *expr* can be upcast to an instance of *type*.</span></span>

- <span data-ttu-id="e8555-115">*expr* a un type au moment de la compilation qui est une classe de base de *type* et *expr* a un type au moment de l’exécution égal à *type* ou dérivé de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-115">*expr* has a compile-time type that is a base class of *type*, and *expr* has a runtime type that is *type* or is derived from *type*.</span></span> <span data-ttu-id="e8555-116">Le *type au moment de la compilation* d’une variable est le type de la variable, tel qu’il est défini dans sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8555-116">The *compile-time type* of a variable is the variable's type as defined in its declaration.</span></span> <span data-ttu-id="e8555-117">Le *type au moment de l’exécution* d’une variable est le type de l’instance qui est assignée à cette variable.</span><span class="sxs-lookup"><span data-stu-id="e8555-117">The *runtime type* of a variable is the type of the instance that is assigned to that variable.</span></span>

- <span data-ttu-id="e8555-118">*expr* est une instance d’un type qui implémente l’interface *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-118">*expr* is an instance of a type that implements the *type* interface.</span></span>

<span data-ttu-id="e8555-119">L’exemple suivant montre que l’expression `is` a la valeur `true` pour chacune de ces conversions.</span><span class="sxs-lookup"><span data-stu-id="e8555-119">The following example shows that the `is` expression evaluates to `true` for each of these conversions.</span></span>

[!code-csharp[is#3](../../../../samples/snippets/csharp/language-reference/keywords/is/is3.cs#3)]

<span data-ttu-id="e8555-120">Le mot clé `is` génère un avertissement au moment de la compilation si l’expression est connue pour être toujours soit `true`, soit `false`.</span><span class="sxs-lookup"><span data-stu-id="e8555-120">The `is` keyword generates a compile-time warning if the expression is known to always be either `true` or `false`.</span></span> <span data-ttu-id="e8555-121">Il tient compte uniquement des conversions de référence, des conversions boxing et des conversions unboxing. Il ne tient pas compte des conversions définies par l’utilisateur ni des conversions définies par les opérateurs [implicit](implicit.md) et [explicit](explicit.md) d’un type.</span><span class="sxs-lookup"><span data-stu-id="e8555-121">It only considers reference conversions, boxing conversions, and unboxing conversions; it does not consider user-defined conversions or conversions defined by a type's [implicit](implicit.md) and [explicit](explicit.md) operators.</span></span> <span data-ttu-id="e8555-122">L’exemple suivant génère des avertissements, car le résultat de la conversion est connu au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="e8555-122">The following example generates warnings because the result of the conversion is known at compile time.</span></span> <span data-ttu-id="e8555-123">L’expression `is` des conversions de `int` à `long` et `double` retourne la valeur false, puisque ces conversions sont gérées par l’opérateur [implicit](implicit.md).</span><span class="sxs-lookup"><span data-stu-id="e8555-123">The `is` expression for conversions from `int` to `long` and `double` return false, since these conversions are handled by the [implicit](implicit.md) operator.</span></span>

[!code-csharp[is#2](../../../../samples/snippets/csharp/language-reference/keywords/is/is2.cs#2)]

<span data-ttu-id="e8555-124">`expr` ne peut pas être une méthode anonyme ou une expression lambda.</span><span class="sxs-lookup"><span data-stu-id="e8555-124">`expr` cannot be an anonymous method or lambda expression.</span></span> <span data-ttu-id="e8555-125">qui retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="e8555-125">It can be any other expression that returns a value.</span></span> <span data-ttu-id="e8555-126">L’exemple suivant utilise `is` pour évaluer la valeur de retour d’un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="e8555-126">The following example uses  `is` to evaluate the return value of a method call.</span></span>   
[!code-csharp[is#4](../../../../samples/snippets/csharp/language-reference/keywords/is/is4.cs#4)]

<span data-ttu-id="e8555-127">Avec C# 7.0, vous pouvez utiliser les critères spéciaux avec le [modèle de type](#type) pour écrire du code plus concis qui utilise l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="e8555-127">Starting with C# 7.0, you can use pattern matching with the [type pattern](#type) to write more concise code that uses the `is` statement.</span></span>

## <a name="pattern-matching-with-is"></a><span data-ttu-id="e8555-128">Utilisation des critères spéciaux avec `is`</span><span class="sxs-lookup"><span data-stu-id="e8555-128">Pattern matching with `is`</span></span>

<span data-ttu-id="e8555-129">À compter de C# 7.0, les instructions `is` et [switch](../../../csharp/language-reference/keywords/switch.md) prennent en charge les critères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="e8555-129">Starting with C# 7.0, the `is` and [switch](../../../csharp/language-reference/keywords/switch.md) statements support pattern matching.</span></span> <span data-ttu-id="e8555-130">Le mot clé `is` prend en charge les modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="e8555-130">The `is` keyword supports the following patterns:</span></span>

- <span data-ttu-id="e8555-131">[Modèle de type](#type) : permet de tester si une expression peut être convertie en un type spécifié et, si tel est le cas, caste l’expression en une variable de ce type.</span><span class="sxs-lookup"><span data-stu-id="e8555-131">[Type pattern](#type),  which tests whether an expression can be converted to a specified type and, if it can be, casts it to a variable of that type.</span></span>

- <span data-ttu-id="e8555-132">[Modèle de constante](#constant) : teste si une expression correspond à une valeur de constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8555-132">[Constant pattern](#constant), which tests whether an expression evaluates to a specified constant value.</span></span>

- <span data-ttu-id="e8555-133">[Modèle de variable](#var) : correspondance qui réussit toujours et lie la valeur d’une expression à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="e8555-133">[var pattern](#var), a match that always succeeds and binds the value of an expression to a new local variable.</span></span> 

### <a name="a-nametype-type-pattern"></a><span data-ttu-id="e8555-134"><a name="type" />Modèle de type</span><span class="sxs-lookup"><span data-stu-id="e8555-134"><a name="type" />Type pattern</span></span>

<span data-ttu-id="e8555-135">Lorsque vous utilisez le modèle de type pour rechercher des critères spéciaux, `is` permet de tester si une expression peut être convertie en un type spécifié et, si tel est le cas, effectuer un cast de l’expression en une variable de ce type.</span><span class="sxs-lookup"><span data-stu-id="e8555-135">When using the type pattern to perform pattern matching, `is` tests whether an expression can be converted to a specified type and, if it can be, casts it to a variable of that type.</span></span> <span data-ttu-id="e8555-136">Il s’agit d’une extension simple de l’instruction `is` qui permet une évaluation et une conversion de type concises.</span><span class="sxs-lookup"><span data-stu-id="e8555-136">It's a straightforward extension of the `is` statement that enables concise type evaluation and conversion.</span></span> <span data-ttu-id="e8555-137">La forme générale du modèle de type `is` est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e8555-137">The general form of the `is` type pattern is:</span></span>

```csharp
   expr is type varname 
```

<span data-ttu-id="e8555-138">où *expr* est une expression qui correspond à une instance d’un type, où *type* est le nom du type dans lequel le résultat de *expr* doit être converti, et où *varname* est l’objet dans lequel le résultat de *expr* est converti si le test `is` a la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="e8555-138">where *expr* is an expression that evaluates to an instance of some type, *type* is the name of the type to which the result of *expr* is to be converted, and *varname* is the object to which the result of *expr* is converted if the `is` test is `true`.</span></span> 

<span data-ttu-id="e8555-139">L’expression `is` est `true` si *expr* n’est pas `null` et que l’une des conditions suivantes est remplie :</span><span class="sxs-lookup"><span data-stu-id="e8555-139">The `is` expression is `true` if *expr* isn't `null`, and any of the following is true:</span></span>

- <span data-ttu-id="e8555-140">*expr* est une instance du même type que *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-140">*expr* is an instance of the same type as *type*.</span></span>

- <span data-ttu-id="e8555-141">*expr* est une instance d’un type qui dérive de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-141">*expr* is an instance of a type that derives from *type*.</span></span> <span data-ttu-id="e8555-142">En d’autres termes, le résultat de *expr* peut être upcasté en une instance de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-142">In other words, the result of *expr* can be upcast to an instance of *type*.</span></span>

- <span data-ttu-id="e8555-143">*expr* a un type au moment de la compilation qui est une classe de base de *type* et *expr* a un type au moment de l’exécution égal à *type* ou dérivé de *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-143">*expr* has a compile-time type that is a base class of *type*, and *expr* has a runtime type that is *type* or is derived from *type*.</span></span> <span data-ttu-id="e8555-144">Le *type au moment de la compilation* d’une variable est le type de la variable, tel qu’il est défini dans sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="e8555-144">The *compile-time type* of a variable is the variable's type as defined in its declaration.</span></span> <span data-ttu-id="e8555-145">Le *type au moment de l’exécution* d’une variable est le type de l’instance qui est assignée à cette variable.</span><span class="sxs-lookup"><span data-stu-id="e8555-145">The *runtime type* of a variable is the type of the instance that is assigned to that variable.</span></span>

- <span data-ttu-id="e8555-146">*expr* est une instance d’un type qui implémente l’interface *type*.</span><span class="sxs-lookup"><span data-stu-id="e8555-146">*expr* is an instance of a type that implements the *type* interface.</span></span>

<span data-ttu-id="e8555-147">À compter de C# 7.1, *expr* peut avoir un type à la compilation défini par un paramètre de type générique et ses contraintes.</span><span class="sxs-lookup"><span data-stu-id="e8555-147">Beginning with C# 7.1, *expr* may have a compile-time type defined by a generic type parameter and its constraints.</span></span> 

<span data-ttu-id="e8555-148">Si *exp* est `true` et que `is` est utilisé avec une instruction `if`, *varname* est assigné et sa portée locale se limite à l’instruction `if`.</span><span class="sxs-lookup"><span data-stu-id="e8555-148">If *expr* is `true` and `is` is used with an `if` statement, *varname* is assigned and has local scope within the `if` statement only.</span></span>

<span data-ttu-id="e8555-149">L’exemple suivant utilise le modèle de type `is` pour fournir l’implémentation de la méthode <xref:System.IComparable.CompareTo(System.Object)?displayProperty=nameWithType> d’un type.</span><span class="sxs-lookup"><span data-stu-id="e8555-149">The following example uses the `is` type pattern to provide the implementation of a type's <xref:System.IComparable.CompareTo(System.Object)?displayProperty=nameWithType> method.</span></span>

[!code-csharp[is#5](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern5.cs#5)]

<span data-ttu-id="e8555-150">Sans critères spéciaux, ce code peut être écrit comme suit.</span><span class="sxs-lookup"><span data-stu-id="e8555-150">Without pattern matching, this code might be written as follows.</span></span> <span data-ttu-id="e8555-151">L’utilisation de critères spéciaux de type génère un code lisible plus compact en éliminant la nécessité de tester si le résultat d’une conversion est un `null`.</span><span class="sxs-lookup"><span data-stu-id="e8555-151">The use of type pattern matching produces more compact, readable code by eliminating the need to test whether the result of a conversion is a `null`.</span></span>  

[!code-csharp[is#6](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern6.cs#6)]

<span data-ttu-id="e8555-152">Le modèle de type `is` génère également du code plus compact lorsqu’il détermine le type d’un type valeur.</span><span class="sxs-lookup"><span data-stu-id="e8555-152">The `is` type pattern also produces more compact code when determining the type of a value type.</span></span> <span data-ttu-id="e8555-153">L’exemple suivant utilise le modèle de type `is` pour déterminer si un objet est une instance `Person` ou `Dog` avant d’afficher la valeur d’une propriété appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8555-153">The following example uses the `is` type pattern to determine whether an object is a `Person` or a `Dog` instance before displaying the value of an appropriate property.</span></span> 

[!code-csharp[is#9](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern9.cs#9)]

<span data-ttu-id="e8555-154">Le code équivalent sans critères spéciaux nécessite une attribution distincte comprenant un cast explicite.</span><span class="sxs-lookup"><span data-stu-id="e8555-154">The equivalent code without pattern matching requires a separate assignment that includes an explicit cast.</span></span>

[!code-csharp[is#10](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern10.cs#10)]

### <a name="a-nameconstant--constant-pattern"></a><span data-ttu-id="e8555-155"><a name="constant" /> Modèle de constante</span><span class="sxs-lookup"><span data-stu-id="e8555-155"><a name="constant" /> Constant pattern</span></span>

<span data-ttu-id="e8555-156">Lorsque vous utilisez des critères spéciaux avec le modèle de constante, `is` teste si une expression est égale à une constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8555-156">When performing pattern matching with the constant pattern, `is` tests whether an expression equals a specified constant.</span></span> <span data-ttu-id="e8555-157">Avec C# 6 et les versions antérieures, le modèle de constante est pris en charge par l’instruction [switch](switch.md).</span><span class="sxs-lookup"><span data-stu-id="e8555-157">In C# 6 and earlier versions, the constant pattern is supported by the [switch](switch.md) statement.</span></span> <span data-ttu-id="e8555-158">À compter de C# 7.0, il est également pris en charge par l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="e8555-158">Starting with C# 7.0, it's supported by the `is` statement as well.</span></span> <span data-ttu-id="e8555-159">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e8555-159">Its syntax is:</span></span>

```csharp
   expr is constant
```

<span data-ttu-id="e8555-160">où *expr* est l’expression à évaluer, et où *constant* est la valeur à tester.</span><span class="sxs-lookup"><span data-stu-id="e8555-160">where *expr* is the expression to evaluate, and *constant* is the value to test for.</span></span> <span data-ttu-id="e8555-161">*constant* peut correspondre à l’une des expressions constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8555-161">*constant* can be any of the following constant expressions:</span></span> 

- <span data-ttu-id="e8555-162">Une valeur littérale</span><span class="sxs-lookup"><span data-stu-id="e8555-162">A literal value.</span></span>

- <span data-ttu-id="e8555-163">Le nom d’une variable `const` déclarée</span><span class="sxs-lookup"><span data-stu-id="e8555-163">The name of a declared `const` variable.</span></span>

- <span data-ttu-id="e8555-164">Une constante d’énumération</span><span class="sxs-lookup"><span data-stu-id="e8555-164">An enumeration constant.</span></span>

<span data-ttu-id="e8555-165">L’expression constante est évaluée de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="e8555-165">The constant expression is evaluated as follows:</span></span>

- <span data-ttu-id="e8555-166">Si *expr* et *constant* sont des types intégraux, l’opérateur d’égalité C# détermine si l’expression retourne `true` (autrement dit, si `expr == constant`).</span><span class="sxs-lookup"><span data-stu-id="e8555-166">If *expr* and *constant* are integral types, the C# equality operator determines whether the expression returns `true` (that is, whether `expr == constant`).</span></span>

- <span data-ttu-id="e8555-167">Sinon, la valeur de l’expression est déterminée par un appel à la méthode statique [Object.Equals(expr, constant)](xref:System.Object.Equals(System.Object,System.Object)).</span><span class="sxs-lookup"><span data-stu-id="e8555-167">Otherwise, the value of the expression is determined by a call to the static [Object.Equals(expr, constant)](xref:System.Object.Equals(System.Object,System.Object)) method.</span></span>  

<span data-ttu-id="e8555-168">L’exemple suivant combine le modèle de type et le modèle de constante pour tester si un objet est une instance `Dice` et, si c’est le cas, pour déterminer si la valeur obtenue après un lancer de dés est de 6.</span><span class="sxs-lookup"><span data-stu-id="e8555-168">The following example combines the type and constant patterns to test whether an object is a `Dice` instance and, if it is, to determine whether the value of a dice roll is 6.</span></span>

[!code-csharp[is#7](../../../../samples/snippets/csharp/language-reference/keywords/is/is-const-pattern7.cs#7)]

<span data-ttu-id="e8555-169">La vérification de `null` peut être effectuée à l’aide du modèle de constante.</span><span class="sxs-lookup"><span data-stu-id="e8555-169">Checking for `null` can be performed using the constant pattern.</span></span> <span data-ttu-id="e8555-170">Le mot clé `null` est pris en charge par l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="e8555-170">The `null` keyword is supported by the `is` statement.</span></span> <span data-ttu-id="e8555-171">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e8555-171">Its syntax is:</span></span>

```csharp 
   expr is null
```

<span data-ttu-id="e8555-172">L’exemple suivant illustre une comparaison des vérifications de `null` :</span><span class="sxs-lookup"><span data-stu-id="e8555-172">The following example shows a comparison of `null` checks:</span></span>

[!code-csharp[is#11](../../../../samples/snippets/csharp/language-reference/keywords/is/is-const-pattern11.cs#11)]
 
### <span data-ttu-id="e8555-173"><a name="var" /> Modèle de variable </a></span><span class="sxs-lookup"><span data-stu-id="e8555-173"><a name="var" /> var pattern </a></span></span>

<span data-ttu-id="e8555-174">Le modèle `var` est de type « catch-all », c’est-à-dire qu’il peut prendre tous les types et valeurs.</span><span class="sxs-lookup"><span data-stu-id="e8555-174">The `var` pattern is a catch-all for any type or value.</span></span> <span data-ttu-id="e8555-175">La valeur de *expr* est toujours affectée à une variable locale de même type que le type de *expr* au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="e8555-175">The value of *expr* is always assigned to a local variable the same type as the compile time type of *expr*.</span></span> <span data-ttu-id="e8555-176">Le résultat de l’expression `is` est toujours `true`.</span><span class="sxs-lookup"><span data-stu-id="e8555-176">The result of the `is` expression is always `true`.</span></span> <span data-ttu-id="e8555-177">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e8555-177">Its syntax is:</span></span>

```csharp 
   expr is var varname
```

<span data-ttu-id="e8555-178">L’exemple suivant utilise le modèle de variable pour assigner une expression à une variable nommée `obj`.</span><span class="sxs-lookup"><span data-stu-id="e8555-178">The following example uses the var pattern to assign an expression to a variable named `obj`.</span></span> <span data-ttu-id="e8555-179">Il affiche ensuite la valeur et le type de `obj`.</span><span class="sxs-lookup"><span data-stu-id="e8555-179">It then displays the value and the type of `obj`.</span></span>

[!code-csharp[is#8](../../../../samples/snippets/csharp/language-reference/keywords/is/is-var-pattern8.cs#8)]

## <a name="c-language-specification"></a><span data-ttu-id="e8555-180">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="e8555-180">C# Language Specification</span></span>
  
[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e8555-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8555-181">See also</span></span>

- [<span data-ttu-id="e8555-182">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e8555-182">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="e8555-183">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="e8555-183">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="e8555-184">typeof</span><span class="sxs-lookup"><span data-stu-id="e8555-184">typeof</span></span>](../../../csharp/language-reference/keywords/typeof.md)
- [<span data-ttu-id="e8555-185">as</span><span class="sxs-lookup"><span data-stu-id="e8555-185">as</span></span>](../../../csharp/language-reference/keywords/as.md)
- [<span data-ttu-id="e8555-186">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="e8555-186">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
