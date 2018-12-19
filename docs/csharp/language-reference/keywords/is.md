---
title: is - Référence C#
ms.custom: seodec18
ms.date: 02/17/2017
f1_keywords:
- is_CSharpKeyword
- is
helpviewer_keywords:
- is keyword [C#]
ms.assetid: bc62316a-d41f-4f90-8300-c6f4f0556e43
ms.openlocfilehash: 4fd545ded9da20da2a6378bfdf561279cf343100
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240006"
---
# <a name="is-c-reference"></a><span data-ttu-id="96e59-102">is (référence C#)</span><span class="sxs-lookup"><span data-stu-id="96e59-102">is (C# Reference)</span></span> #

<span data-ttu-id="96e59-103">Vérifie si un objet est compatible avec un type donné, ou (avec C# 7.0) teste une expression par rapport à un modèle.</span><span class="sxs-lookup"><span data-stu-id="96e59-103">Checks if an object is compatible with a given type, or (starting with C# 7.0) tests an expression against a pattern.</span></span>

## <a name="testing-for-type-compatibility"></a><span data-ttu-id="96e59-104">Test de compatibilité de type</span><span class="sxs-lookup"><span data-stu-id="96e59-104">Testing for type compatibility</span></span> ##

<span data-ttu-id="96e59-105">Le mot clé `is` évalue la compatibilité de type au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="96e59-105">The `is` keyword evaluates type compatibility at runtime.</span></span> <span data-ttu-id="96e59-106">Il détermine si une instance d’objet ou le résultat d’une expression peuvent être convertis en un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="96e59-106">It determines whether an object instance or the result of an expression can be converted to a specified type.</span></span> <span data-ttu-id="96e59-107">Sa syntaxe est</span><span class="sxs-lookup"><span data-stu-id="96e59-107">It has the syntax</span></span>

```csharp
   expr is type
```

<span data-ttu-id="96e59-108">où *expr* est une expression qui correspond à une instance d’un type, et où *type* est le nom du type dans lequel le résultat de *expr* doit être converti.</span><span class="sxs-lookup"><span data-stu-id="96e59-108">where *expr* is an expression that evaluates to an instance of some type, and *type* is the name of the type to which the result of *expr* is to be converted.</span></span> <span data-ttu-id="96e59-109">L’instruction `is` est `true` si *expr* est non-Null et si l’objet qui résulte de l’évaluation de l’expression peut être converti en *type* ; sinon, elle retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="96e59-109">The `is` statement is `true` if *expr* is non-null and the object that results from evaluating the expression can be converted to *type*; otherwise, it returns `false`.</span></span>

<span data-ttu-id="96e59-110">Par exemple, le code suivant détermine si `obj` peut être casté en une instance de type `Person` :</span><span class="sxs-lookup"><span data-stu-id="96e59-110">For example, the following code determines if `obj` can be cast to an instance of the `Person` type:</span></span>

[!code-csharp[is#1](../../../../samples/snippets/csharp/language-reference/keywords/is/is1.cs#1)]

<span data-ttu-id="96e59-111">L’instruction `is` a la valeur true si :</span><span class="sxs-lookup"><span data-stu-id="96e59-111">The `is` statement is true if:</span></span>

- <span data-ttu-id="96e59-112">*expr* est une instance du même type que *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-112">*expr* is an instance of the same type as *type*.</span></span>

- <span data-ttu-id="96e59-113">*expr* est une instance d’un type qui dérive de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-113">*expr* is an instance of a type that derives from *type*.</span></span> <span data-ttu-id="96e59-114">En d’autres termes, le résultat de *expr* peut être upcasté en une instance de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-114">In other words, the result of *expr* can be upcast to an instance of *type*.</span></span>

- <span data-ttu-id="96e59-115">*expr* a un type au moment de la compilation qui est une classe de base de *type* et *expr* a un type au moment de l’exécution égal à *type* ou dérivé de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-115">*expr* has a compile-time type that is a base class of *type*, and *expr* has a runtime type that is *type* or is derived from *type*.</span></span> <span data-ttu-id="96e59-116">Le *type au moment de la compilation* d’une variable est le type de la variable, tel qu’il est défini dans sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="96e59-116">The *compile-time type* of a variable is the variable's type as defined in its declaration.</span></span> <span data-ttu-id="96e59-117">Le *type au moment de l’exécution* d’une variable est le type de l’instance qui est assignée à cette variable.</span><span class="sxs-lookup"><span data-stu-id="96e59-117">The *runtime type* of a variable is the type of the instance that is assigned to that variable.</span></span>

- <span data-ttu-id="96e59-118">*expr* est une instance d’un type qui implémente l’interface *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-118">*expr* is an instance of a type that implements the *type* interface.</span></span>

<span data-ttu-id="96e59-119">L’exemple suivant montre que l’expression `is` a la valeur `true` pour chacune de ces conversions.</span><span class="sxs-lookup"><span data-stu-id="96e59-119">The following example shows that the `is` expression evaluates to `true` for each of these conversions.</span></span>

[!code-csharp[is#3](../../../../samples/snippets/csharp/language-reference/keywords/is/is3.cs#3)]

<span data-ttu-id="96e59-120">Le mot clé `is` génère un avertissement au moment de la compilation si l’expression est connue pour être toujours soit `true`, soit `false`.</span><span class="sxs-lookup"><span data-stu-id="96e59-120">The `is` keyword generates a compile-time warning if the expression is known to always be either `true` or `false`.</span></span> <span data-ttu-id="96e59-121">Il tient compte uniquement des conversions de référence, des conversions boxing et des conversions unboxing. Il ne tient pas compte des conversions définies par l’utilisateur ni des conversions définies par les opérateurs [implicit](implicit.md) et [explicit](explicit.md) d’un type.</span><span class="sxs-lookup"><span data-stu-id="96e59-121">It only considers reference conversions, boxing conversions, and unboxing conversions; it does not consider user-defined conversions or conversions defined by a type's [implicit](implicit.md) and [explicit](explicit.md) operators.</span></span> <span data-ttu-id="96e59-122">L’exemple suivant génère des avertissements, car le résultat de la conversion est connu au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="96e59-122">The following example generates warnings because the result of the conversion is known at compile-time.</span></span> <span data-ttu-id="96e59-123">Notez que l’expression `is` pour les conversions de `int` à `long` et `double` retourne la valeur false, puisque ces conversions sont gérées par l’opérateur [implicit](implicit.md).</span><span class="sxs-lookup"><span data-stu-id="96e59-123">Note that the `is` expression for conversions from `int` to `long` and `double` return false, since these conversions are handled by the [implicit](implicit.md) operator.</span></span>

[!code-csharp[is#2](../../../../samples/snippets/csharp/language-reference/keywords/is/is2.cs#2)]

<span data-ttu-id="96e59-124">`expr` peut correspondre à toute expression qui retourne une valeur, à l’exception des méthodes anonymes et des expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="96e59-124">`expr` can be any expression that returns a value, with the exception of anonymous methods and lambda expressions.</span></span> <span data-ttu-id="96e59-125">L’exemple suivant utilise `is` pour évaluer la valeur de retour d’un appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="96e59-125">The following example uses  `is` to evaluate the return value of a method call.</span></span>   
[!code-csharp[is#4](../../../../samples/snippets/csharp/language-reference/keywords/is/is4.cs#4)]

<span data-ttu-id="96e59-126">Avec C# 7.0, vous pouvez utiliser les critères spéciaux avec le [modèle de type](#type) pour écrire du code plus concis qui utilise l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="96e59-126">Starting with C# 7.0, you can use pattern matching with the [type pattern](#type) to write more concise code that uses the `is` statement.</span></span>

## <a name="pattern-matching-with-is"></a><span data-ttu-id="96e59-127">Utilisation des critères spéciaux avec `is`</span><span class="sxs-lookup"><span data-stu-id="96e59-127">Pattern matching with `is`</span></span> ##

<span data-ttu-id="96e59-128">À compter de C# 7.0, les instructions `is` et [switch](../../../csharp/language-reference/keywords/switch.md) prennent en charge les critères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="96e59-128">Starting with C# 7.0, the `is` and [switch](../../../csharp/language-reference/keywords/switch.md) statements support pattern matching.</span></span> <span data-ttu-id="96e59-129">Le mot clé `is` prend en charge les modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="96e59-129">The `is` keyword supports the following patterns:</span></span>

- <span data-ttu-id="96e59-130">[Modèle de type](#type) : permet de tester si une expression peut être convertie en un type spécifié et, si tel est le cas, caste l’expression en une variable de ce type.</span><span class="sxs-lookup"><span data-stu-id="96e59-130">[Type pattern](#type),  which tests whether an expression can be converted to a specified type and, if it can be, casts it to a variable of that type.</span></span>

- <span data-ttu-id="96e59-131">[Modèle de constante](#constant) : teste si une expression correspond à une valeur de constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="96e59-131">[Constant pattern](#constant), which tests whether an expression evaluates to a specified constant value.</span></span>

- <span data-ttu-id="96e59-132">[Modèle de variable](#var) : correspondance qui réussit toujours et lie la valeur d’une expression à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="96e59-132">[var pattern](#var), a match that always succeeds and binds the value of an expression to a new local variable.</span></span> 

### <span data-ttu-id="96e59-133"><a name="type" /> Modèle de type </a></span><span class="sxs-lookup"><span data-stu-id="96e59-133"><a name="type" /> Type pattern </a></span></span>

<span data-ttu-id="96e59-134">Lorsque vous utilisez le modèle de type pour rechercher des critères spéciaux, `is` permet de tester si une expression peut être convertie en un type spécifié et, si tel est le cas, effectuer un cast de l’expression en une variable de ce type.</span><span class="sxs-lookup"><span data-stu-id="96e59-134">When using the type pattern to perform pattern matching, `is` tests whether an expression can be converted to a specified type and, if it can be, casts it to a variable of that type.</span></span> <span data-ttu-id="96e59-135">Il s’agit d’une extension simple de l’instruction `is` qui permet une évaluation et une conversion de type concises.</span><span class="sxs-lookup"><span data-stu-id="96e59-135">It is a straightforward extension of the `is` statement that enables concise type evaluation and conversion.</span></span> <span data-ttu-id="96e59-136">La forme générale du modèle de type `is` est la suivante :</span><span class="sxs-lookup"><span data-stu-id="96e59-136">The general form of the `is` type pattern is:</span></span>

```csharp
   expr is type varname 
```

<span data-ttu-id="96e59-137">où *expr* est une expression qui correspond à une instance d’un type, où *type* est le nom du type dans lequel le résultat de *expr* doit être converti, et où *varname* est l’objet dans lequel le résultat de *expr* est converti si le test `is` a la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="96e59-137">where *expr* is an expression that evaluates to an instance of some type, *type* is the name of the type to which the result of *expr* is to be converted, and *varname* is the object to which the result of *expr* is converted if the `is` test is `true`.</span></span> 

<span data-ttu-id="96e59-138">L’expression `is` est `true` si *expr* n’est pas `null` et que l’un des énoncés suivants est vrai :</span><span class="sxs-lookup"><span data-stu-id="96e59-138">The `is` expression is `true` if *expr* is not `null`, and any of the following is true:</span></span>

- <span data-ttu-id="96e59-139">*expr* est une instance du même type que *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-139">*expr* is an instance of the same type as *type*.</span></span>

- <span data-ttu-id="96e59-140">*expr* est une instance d’un type qui dérive de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-140">*expr* is an instance of a type that derives from *type*.</span></span> <span data-ttu-id="96e59-141">En d’autres termes, le résultat de *expr* peut être upcasté en une instance de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-141">In other words, the result of *expr* can be upcast to an instance of *type*.</span></span>

- <span data-ttu-id="96e59-142">*expr* a un type au moment de la compilation qui est une classe de base de *type* et *expr* a un type au moment de l’exécution égal à *type* ou dérivé de *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-142">*expr* has a compile-time type that is a base class of *type*, and *expr* has a runtime type that is *type* or is derived from *type*.</span></span> <span data-ttu-id="96e59-143">Le *type au moment de la compilation* d’une variable est le type de la variable, tel qu’il est défini dans sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="96e59-143">The *compile-time type* of a variable is the variable's type as defined in its declaration.</span></span> <span data-ttu-id="96e59-144">Le *type au moment de l’exécution* d’une variable est le type de l’instance qui est assignée à cette variable.</span><span class="sxs-lookup"><span data-stu-id="96e59-144">The *runtime type* of a variable is the type of the instance that is assigned to that variable.</span></span>

- <span data-ttu-id="96e59-145">*expr* est une instance d’un type qui implémente l’interface *type*.</span><span class="sxs-lookup"><span data-stu-id="96e59-145">*expr* is an instance of a type that implements the *type* interface.</span></span>

<span data-ttu-id="96e59-146">Si *exp* est `true` et que `is` est utilisé avec une instruction `if`, *varname* est assigné et sa portée locale se limite à l’instruction `if`.</span><span class="sxs-lookup"><span data-stu-id="96e59-146">If *expr* is `true` and `is` is used with an `if` statement, *varname* is assigned and has local scope within the `if` statement only.</span></span>

<span data-ttu-id="96e59-147">L’exemple suivant utilise le modèle de type `is` pour fournir l’implémentation de la méthode <xref:System.IComparable.CompareTo(System.Object)?displayProperty=nameWithType> d’un type.</span><span class="sxs-lookup"><span data-stu-id="96e59-147">The following example uses the `is` type pattern to provide the implementation of a type's <xref:System.IComparable.CompareTo(System.Object)?displayProperty=nameWithType> method.</span></span>

[!code-csharp[is#5](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern5.cs#5)]

<span data-ttu-id="96e59-148">Sans critères spéciaux, ce code peut être écrit comme suit.</span><span class="sxs-lookup"><span data-stu-id="96e59-148">Without pattern matching, this code might be written as follows.</span></span> <span data-ttu-id="96e59-149">L’utilisation de critères spéciaux de type génère un code lisible plus compact en éliminant la nécessité de tester si le résultat d’une conversion est un `null`.</span><span class="sxs-lookup"><span data-stu-id="96e59-149">The use of type pattern matching produces more compact, readable code by eliminating the need to test whether the result of a conversion is a `null`.</span></span>  

[!code-csharp[is#6](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern6.cs#6)]

<span data-ttu-id="96e59-150">Le modèle de type `is` génère également du code plus compact lorsqu’il détermine le type d’un type valeur.</span><span class="sxs-lookup"><span data-stu-id="96e59-150">The `is` type pattern also produces more compact code when determining the type of a value type.</span></span> <span data-ttu-id="96e59-151">L’exemple suivant utilise le modèle de type `is` pour déterminer si un objet est une instance `Person` ou `Dog` avant d’afficher la valeur d’une propriété appropriée.</span><span class="sxs-lookup"><span data-stu-id="96e59-151">The following example uses the `is` type pattern to determine whether an object is a `Person` or a `Dog` instance before displaying the value of an appropriate property.</span></span> 

[!code-csharp[is#9](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern9.cs#9)]

<span data-ttu-id="96e59-152">Le code équivalent sans critères spéciaux nécessite une attribution distincte comprenant un cast explicite.</span><span class="sxs-lookup"><span data-stu-id="96e59-152">The equivalent code without pattern matching requires a separate assignment that includes an explicit cast.</span></span>

[!code-csharp[is#10](../../../../samples/snippets/csharp/language-reference/keywords/is/is-type-pattern10.cs#10)]

### <a name="a-nameconstant--constant-pattern"></a><span data-ttu-id="96e59-153"><a name="constant" /> Modèle de constante</span><span class="sxs-lookup"><span data-stu-id="96e59-153"><a name="constant" /> Constant pattern</span></span> ###

<span data-ttu-id="96e59-154">Lorsque vous utilisez des critères spéciaux avec le modèle de constante, `is` teste si une expression est égale à une constante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="96e59-154">When performing pattern matching with the constant pattern, `is` tests whether an expression equals a specified constant.</span></span> <span data-ttu-id="96e59-155">Avec C# 6 et les versions antérieures, le modèle de constante est pris en charge par l’instruction [switch](switch.md).</span><span class="sxs-lookup"><span data-stu-id="96e59-155">In C# 6 and earlier versions, the constant pattern is supported by the [switch](switch.md) statement.</span></span> <span data-ttu-id="96e59-156">À compter de C# 7.0, ce modèle est également pris en charge par l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="96e59-156">Starting with C# 7.0, it is supported by the `is` statement as well.</span></span> <span data-ttu-id="96e59-157">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="96e59-157">Its syntax is:</span></span>

```csharp
   expr is constant
```

<span data-ttu-id="96e59-158">où *expr* est l’expression à évaluer, et où *constant* est la valeur à tester.</span><span class="sxs-lookup"><span data-stu-id="96e59-158">where *expr* is the expression to evaluate, and *constant* is the value to test for.</span></span> <span data-ttu-id="96e59-159">*constant* peut correspondre à l’une des expressions constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="96e59-159">*constant* can be any of the following constant expressions:</span></span> 

- <span data-ttu-id="96e59-160">Une valeur littérale</span><span class="sxs-lookup"><span data-stu-id="96e59-160">A literal value.</span></span>

- <span data-ttu-id="96e59-161">Le nom d’une variable `const` déclarée</span><span class="sxs-lookup"><span data-stu-id="96e59-161">The name of a declared `const` variable.</span></span>

- <span data-ttu-id="96e59-162">Une constante d’énumération</span><span class="sxs-lookup"><span data-stu-id="96e59-162">An enumeration constant.</span></span>

<span data-ttu-id="96e59-163">L’expression constante est évaluée de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="96e59-163">The constant expression is evaluated as follows:</span></span>

- <span data-ttu-id="96e59-164">Si *expr* et *constant* sont des types intégraux, l’opérateur d’égalité C# détermine si l’expression retourne `true` (autrement dit, si `expr == constant`).</span><span class="sxs-lookup"><span data-stu-id="96e59-164">If *expr* and *constant* are integral types, the C# equality operator determines whether the expression returns `true` (that is, whether `expr == constant`).</span></span>

- <span data-ttu-id="96e59-165">Sinon, la valeur de l’expression est déterminée par un appel à la méthode statique [Object.Equals(expr, constant)](xref:System.Object.Equals(System.Object,System.Object)).</span><span class="sxs-lookup"><span data-stu-id="96e59-165">Otherwise, the value of the expression is determined by a call to the static [Object.Equals(expr, constant)](xref:System.Object.Equals(System.Object,System.Object)) method.</span></span>  

<span data-ttu-id="96e59-166">L’exemple suivant combine le modèle de type et le modèle de constante pour tester si un objet est une instance `Dice` et, si c’est le cas, pour déterminer si la valeur obtenue après un lancer de dés est de 6.</span><span class="sxs-lookup"><span data-stu-id="96e59-166">The following example combines the type and constant patterns to test whether an object is a `Dice` instance and, if it is, to determine whether the value of a dice roll is 6.</span></span>

[!code-csharp[is#7](../../../../samples/snippets/csharp/language-reference/keywords/is/is-const-pattern7.cs#7)]

<span data-ttu-id="96e59-167">La vérification de `null` peut être effectuée à l’aide du modèle de constante.</span><span class="sxs-lookup"><span data-stu-id="96e59-167">Checking for `null` can be performed using the constant pattern.</span></span> <span data-ttu-id="96e59-168">Le mot clé `null` est pris en charge par l’instruction `is`.</span><span class="sxs-lookup"><span data-stu-id="96e59-168">The `null` keyword is supported by the `is` statement.</span></span> <span data-ttu-id="96e59-169">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="96e59-169">Its syntax is:</span></span>

```csharp 
   expr is null
```

<span data-ttu-id="96e59-170">L’exemple suivant illustre une comparaison des vérifications de `null` :</span><span class="sxs-lookup"><span data-stu-id="96e59-170">The following example shows a comparison of `null` checks:</span></span>

[!code-csharp[is#11](../../../../samples/snippets/csharp/language-reference/keywords/is/is-const-pattern11.cs#11)]
 
### <span data-ttu-id="96e59-171"><a name="var" /> Modèle de variable </a></span><span class="sxs-lookup"><span data-stu-id="96e59-171"><a name="var" /> var pattern </a></span></span>

<span data-ttu-id="96e59-172">Une recherche de critères spéciaux qui utilise le modèle de variable réussit toujours.</span><span class="sxs-lookup"><span data-stu-id="96e59-172">A pattern match with the var pattern always succeeds.</span></span> <span data-ttu-id="96e59-173">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="96e59-173">Its syntax is</span></span>

```csharp 
   expr is var varname
```

<span data-ttu-id="96e59-174">où la valeur de *expr* est toujours assignée à une variable locale nommée *varname*.</span><span class="sxs-lookup"><span data-stu-id="96e59-174">where the value of *expr* is always assigned to a local variable named *varname*.</span></span> <span data-ttu-id="96e59-175">*varname* est une variable statique du même type que *expr*.</span><span class="sxs-lookup"><span data-stu-id="96e59-175">*varname* is a static variable of the same type as *expr*.</span></span> <span data-ttu-id="96e59-176">L’exemple suivant utilise le modèle de variable pour assigner une expression à une variable nommée `obj`.</span><span class="sxs-lookup"><span data-stu-id="96e59-176">The following example uses the var pattern to assign an expression to a variable named `obj`.</span></span> <span data-ttu-id="96e59-177">Il affiche ensuite la valeur et le type de `obj`.</span><span class="sxs-lookup"><span data-stu-id="96e59-177">It then displays the value and the type of `obj`.</span></span>

[!code-csharp[is#8](../../../../samples/snippets/csharp/language-reference/keywords/is/is-var-pattern8.cs#8)]

<span data-ttu-id="96e59-178">Notez que si *expr* est `null`, l’expression `is` a toujours la valeur true et attribue `null` à *varname*.</span><span class="sxs-lookup"><span data-stu-id="96e59-178">Note that if *expr* is `null`, the `is` expression still is true and assigns `null` to *varname*.</span></span> 

## <a name="c-language-specification"></a><span data-ttu-id="96e59-179">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="96e59-179">C# Language Specification</span></span>
  
[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="96e59-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96e59-180">See also</span></span>

- [<span data-ttu-id="96e59-181">Référence C#</span><span class="sxs-lookup"><span data-stu-id="96e59-181">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="96e59-182">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="96e59-182">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="96e59-183">typeof</span><span class="sxs-lookup"><span data-stu-id="96e59-183">typeof</span></span>](../../../csharp/language-reference/keywords/typeof.md)  
- [<span data-ttu-id="96e59-184">as</span><span class="sxs-lookup"><span data-stu-id="96e59-184">as</span></span>](../../../csharp/language-reference/keywords/as.md)  
- [<span data-ttu-id="96e59-185">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="96e59-185">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)
