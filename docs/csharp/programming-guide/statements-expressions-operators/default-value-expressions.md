---
title: Expressions de valeur par défaut (Guide de programmation C#)
description: Les expressions de valeur par défaut produisent la valeur par défaut des types référence et des types valeur
ms.date: 04/25/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- generics [C#], default keyword
- default keyword [C#], generic programming
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 174ac79c9e2c4a4e628816b1178d420ec7cfc809
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="default-value-expressions-c-programming-guide"></a><span data-ttu-id="c8733-103">Expressions de valeur par défaut (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="c8733-103">default value expressions (C# programming guide)</span></span>

<span data-ttu-id="c8733-104">Une expression de valeur par défaut `default(T)` produit la valeur par défaut d’un type `T`.</span><span class="sxs-lookup"><span data-stu-id="c8733-104">A default value expression `default(T)` produces the default value of a type `T`.</span></span> <span data-ttu-id="c8733-105">Le tableau suivant montre les valeurs qui sont produites pour différents types :</span><span class="sxs-lookup"><span data-stu-id="c8733-105">The following table shows which values are produced for various types:</span></span>

|<span data-ttu-id="c8733-106">Type</span><span class="sxs-lookup"><span data-stu-id="c8733-106">Type</span></span>|<span data-ttu-id="c8733-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c8733-107">Default value</span></span>|
|---------|---------|
|<span data-ttu-id="c8733-108">tout type référence ;</span><span class="sxs-lookup"><span data-stu-id="c8733-108">Any reference type</span></span>|`null`|
|<span data-ttu-id="c8733-109">Type de valeur numérique</span><span class="sxs-lookup"><span data-stu-id="c8733-109">Numeric value type</span></span>|<span data-ttu-id="c8733-110">Zéro</span><span class="sxs-lookup"><span data-stu-id="c8733-110">Zero</span></span>|
|[<span data-ttu-id="c8733-111">bool</span><span class="sxs-lookup"><span data-stu-id="c8733-111">bool</span></span>](../../language-reference/keywords/bool.md)|`false`|
|[<span data-ttu-id="c8733-112">char</span><span class="sxs-lookup"><span data-stu-id="c8733-112">char</span></span>](../../language-reference/keywords/char.md)|`'\0'`|
|[<span data-ttu-id="c8733-113">enum</span><span class="sxs-lookup"><span data-stu-id="c8733-113">enum</span></span>](../../language-reference/keywords/enum.md)|<span data-ttu-id="c8733-114">Valeur produite par l’expression `(E)0`, où `E` est l’identificateur de l’enum.</span><span class="sxs-lookup"><span data-stu-id="c8733-114">The value produced by the expression `(E)0`, where `E` is the enum identifier.</span></span>|
|[<span data-ttu-id="c8733-115">struct</span><span class="sxs-lookup"><span data-stu-id="c8733-115">struct</span></span>](../../language-reference/keywords/struct.md)|<span data-ttu-id="c8733-116">Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="c8733-116">The value produced by setting all value type fields to their default value and all reference type fields to `null`.</span></span>|
|<span data-ttu-id="c8733-117">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="c8733-117">Nullable type</span></span>|<span data-ttu-id="c8733-118">Instance pour laquelle la propriété <xref:System.Nullable%601.HasValue%2A> a la valeur `false` et la propriété <xref:System.Nullable%601.Value%2A> n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c8733-118">An instance for which the <xref:System.Nullable%601.HasValue%2A> property is `false` and the <xref:System.Nullable%601.Value%2A> property is undefined.</span></span>|

<span data-ttu-id="c8733-119">Les expressions de valeur par défaut sont particulièrement utiles dans les méthodes et classes génériques.</span><span class="sxs-lookup"><span data-stu-id="c8733-119">Default value expressions are particularly useful in generic classes and methods.</span></span> <span data-ttu-id="c8733-120">Le problème qui se pose avec l’utilisation des génériques est de savoir comment assigner une valeur par défaut à un type paramétrable `T` quand vous ne connaissez pas les éléments suivants à l’avance :</span><span class="sxs-lookup"><span data-stu-id="c8733-120">One issue that arises using generics is how to assign a default value of a parameterized type `T` when you don't know the following in advance:</span></span>

- <span data-ttu-id="c8733-121">Si `T` est un type référence ou un type valeur.</span><span class="sxs-lookup"><span data-stu-id="c8733-121">Whether `T` is a reference type or a value type.</span></span>
- <span data-ttu-id="c8733-122">Si `T` est un type valeur, qu’il s’agisse d’une valeur numérique ou d’un struct.</span><span class="sxs-lookup"><span data-stu-id="c8733-122">If `T` is a value type, whether it's a numeric value or a struct.</span></span>

 <span data-ttu-id="c8733-123">Avec une variable `t` d’un type paramétré `T`, l’instruction `t = null` est valide uniquement si `T` est un type référence.</span><span class="sxs-lookup"><span data-stu-id="c8733-123">Given a variable `t` of a parameterized type `T`, the statement `t = null` is only valid if `T` is a reference type.</span></span> <span data-ttu-id="c8733-124">L’affectation de `t = 0` fonctionne uniquement pour les types valeur numériques mais pas pour les structs.</span><span class="sxs-lookup"><span data-stu-id="c8733-124">The assignment `t = 0` only works for numeric value types but not for structs.</span></span> <span data-ttu-id="c8733-125">Pour résoudre ce problème, utilisez une expression de valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="c8733-125">To solve that, use a default value expression:</span></span>

```csharp
T t = default(T);
```

<span data-ttu-id="c8733-126">L’expression `default(T)` n’est pas limitée aux classes et aux méthodes génériques.</span><span class="sxs-lookup"><span data-stu-id="c8733-126">The `default(T)` expression is not limited to generic classes and methods.</span></span> <span data-ttu-id="c8733-127">Vous pouvez utiliser les expressions de valeur par défaut avec n’importe quel type managé.</span><span class="sxs-lookup"><span data-stu-id="c8733-127">Default value expressions can be used with any managed type.</span></span> <span data-ttu-id="c8733-128">Toutes ces expressions sont valides :</span><span class="sxs-lookup"><span data-stu-id="c8733-128">Any of these expressions are valid:</span></span>

 [!code-csharp[csProgGuideGenerics#1](../../../../samples/snippets/csharp/programming-guide/statements-expressions-operators/default-value-expressions.cs)]

 <span data-ttu-id="c8733-129">L’exemple suivant de la classe `GenericList<T>` montre comment utiliser l’opérateur `default(T)` dans une classe générique.</span><span class="sxs-lookup"><span data-stu-id="c8733-129">The following example from the `GenericList<T>` class shows how to use the `default(T)` operator in a generic class.</span></span> <span data-ttu-id="c8733-130">Pour plus d’informations, consultez [Introduction aux génériques](../generics/introduction-to-generics.md).</span><span class="sxs-lookup"><span data-stu-id="c8733-130">For more information, see [Introduction to Generics](../generics/introduction-to-generics.md).</span></span>

 [!code-csharp[csProgGuideGenerics#2](../../../../samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#Snippet41)]

## <a name="default-literal-and-type-inference"></a><span data-ttu-id="c8733-131">Littéral par défaut et inférence de type</span><span class="sxs-lookup"><span data-stu-id="c8733-131">default literal and type inference</span></span>

<span data-ttu-id="c8733-132">À partir de C# 7.1, vous pouvez utiliser les littéraux `default` pour les expressions de valeur par défaut quand le compilateur peut déduire le type de l’expression.</span><span class="sxs-lookup"><span data-stu-id="c8733-132">Beginning with C# 7.1, the `default` literal can be used for default value expressions when the compiler can infer the type of the expression.</span></span> <span data-ttu-id="c8733-133">Le littéral `default` génère la même valeur que l’équivalent `default(T)`, où `T` est le type déduit.</span><span class="sxs-lookup"><span data-stu-id="c8733-133">The `default` literal produces the same value as the equivalent `default(T)` where `T` is the inferred type.</span></span> <span data-ttu-id="c8733-134">Vous pouvez ainsi alléger votre code en réduisant la redondance de déclarer un type plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="c8733-134">This can make code more concise by reducing the redundancy of declaring a type more than once.</span></span> <span data-ttu-id="c8733-135">Vous pouvez utiliser le littéral `default` dans l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="c8733-135">The `default` literal can be used in any of the following locations:</span></span>

- <span data-ttu-id="c8733-136">initialiseur de variable</span><span class="sxs-lookup"><span data-stu-id="c8733-136">variable initializer</span></span>
- <span data-ttu-id="c8733-137">assignation de variable</span><span class="sxs-lookup"><span data-stu-id="c8733-137">variable assignment</span></span>
- <span data-ttu-id="c8733-138">déclaration de la valeur par défaut d’un paramètre facultatif</span><span class="sxs-lookup"><span data-stu-id="c8733-138">declaring the default value for an optional parameter</span></span>
- <span data-ttu-id="c8733-139">valeur pour un argument d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="c8733-139">providing the value for a method call argument</span></span>
- <span data-ttu-id="c8733-140">instruction return (ou expression dans un membre expression-bodied)</span><span class="sxs-lookup"><span data-stu-id="c8733-140">return statement (or expression in an expression bodied member)</span></span>

<span data-ttu-id="c8733-141">L’exemple suivant illustre plusieurs utilisations du littéral `default` dans une expression de valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="c8733-141">The following example shows many usages of the `default` literal in a default value expression:</span></span>

[!code-csharp[csProgGuideGenerics#3](../../../../samples/snippets/csharp/programming-guide/statements-expressions-operators/default-literal.cs)]

## <a name="see-also"></a><span data-ttu-id="c8733-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8733-142">See also</span></span>

 <xref:System.Collections.Generic>  
 [<span data-ttu-id="c8733-143">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c8733-143">C# Programming Guide</span></span>](../index.md)  
 [<span data-ttu-id="c8733-144">Génériques (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="c8733-144">Generics (C# Programming Guide)</span></span>](../generics/index.md)  
 [<span data-ttu-id="c8733-145">Méthodes génériques</span><span class="sxs-lookup"><span data-stu-id="c8733-145">Generic Methods</span></span>](../generics/generic-methods.md)  
 [<span data-ttu-id="c8733-146">Génériques en .NET</span><span class="sxs-lookup"><span data-stu-id="c8733-146">Generics in .NET</span></span>](~/docs/standard/generics/index.md)  
 [<span data-ttu-id="c8733-147">Tableau des valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="c8733-147">Default values table</span></span>](../../language-reference/keywords/default-values-table.md)
