---
title: ushort, mot clé - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ushort
- ushort_CSharpKeyword
helpviewer_keywords:
- ushort keyword [C#]
ms.assetid: 1a7dbaae-b7a0-4111-872a-c88a6d3981ac
ms.openlocfilehash: 934e25576a8a24c176a54ec6af984459b513fe5a
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53614455"
---
# <a name="ushort-c-reference"></a><span data-ttu-id="f9175-102">ushort (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f9175-102">ushort (C# Reference)</span></span>

<span data-ttu-id="f9175-103">Le mot clé `ushort` indique un type de données intégral qui stocke des valeurs selon la taille et la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f9175-103">The `ushort` keyword indicates an integral data type that stores values according to the size and range shown in the following table.</span></span>

|<span data-ttu-id="f9175-104">Type</span><span class="sxs-lookup"><span data-stu-id="f9175-104">Type</span></span>|<span data-ttu-id="f9175-105">Plage</span><span class="sxs-lookup"><span data-stu-id="f9175-105">Range</span></span>|<span data-ttu-id="f9175-106">Size</span><span class="sxs-lookup"><span data-stu-id="f9175-106">Size</span></span>|<span data-ttu-id="f9175-107">Type .NET</span><span class="sxs-lookup"><span data-stu-id="f9175-107">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`ushort`|<span data-ttu-id="f9175-108">0 à 65 535</span><span class="sxs-lookup"><span data-stu-id="f9175-108">0 to 65,535</span></span>|<span data-ttu-id="f9175-109">Entier 16 bits non signé</span><span class="sxs-lookup"><span data-stu-id="f9175-109">Unsigned 16-bit integer</span></span>|<xref:System.UInt16?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="f9175-110">Littéraux</span><span class="sxs-lookup"><span data-stu-id="f9175-110">Literals</span></span>

<span data-ttu-id="f9175-111">Vous pouvez déclarer et initialiser une variable `ushort` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="f9175-111">You can declare and initialize a `ushort` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span> <span data-ttu-id="f9175-112">Si le littéral entier est en dehors de la plage autorisée pour le type `ushort` (autrement dit, s’il est inférieur à <xref:System.UInt16.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt16.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="f9175-112">If the integer literal is outside the range of `ushort` (that is, if it is less than <xref:System.UInt16.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt16.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span>

<span data-ttu-id="f9175-113">Dans l’exemple suivant, les entiers égaux à 65 034 représentés comme des littéraux décimaux, hexadécimaux et binaires sont implicitement convertis à partir de valeurs [int](int.md) en `ushort`.</span><span class="sxs-lookup"><span data-stu-id="f9175-113">In the following example, integers equal to 65,034 that are represented as decimal, hexadecimal, and binary literals are implicitly converted from [int](int.md) to `ushort` values.</span></span>

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShort)]

> [!NOTE]
> <span data-ttu-id="f9175-114">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="f9175-114">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="f9175-115">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="f9175-115">Decimal literals have no prefix.</span></span>

<span data-ttu-id="f9175-116">À partir de C# 7.0, quelques fonctionnalités ont été ajoutées pour améliorer la lisibilité :</span><span class="sxs-lookup"><span data-stu-id="f9175-116">Starting with C# 7.0, a couple of features have been added to enhance readability:</span></span>

- <span data-ttu-id="f9175-117">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="f9175-117">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
- <span data-ttu-id="f9175-118">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="f9175-118">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="f9175-119">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="f9175-119">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="f9175-120">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="f9175-120">Some examples are shown below.</span></span>

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShortS)]

## <a name="compiler-overload-resolution"></a><span data-ttu-id="f9175-121">Résolution de surcharge du compilateur</span><span class="sxs-lookup"><span data-stu-id="f9175-121">Compiler overload resolution</span></span>

<span data-ttu-id="f9175-122">Vous devez utiliser un cast lors de l’appel de méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="f9175-122">A cast must be used when you call overloaded methods.</span></span> <span data-ttu-id="f9175-123">Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `ushort` et [int](int.md) :</span><span class="sxs-lookup"><span data-stu-id="f9175-123">Consider, for example, the following overloaded methods that use `ushort` and [int](int.md) parameters:</span></span>

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ushort s) {}
```

<span data-ttu-id="f9175-124">L’utilisation du cast `ushort` garantit l’appel du type correct, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f9175-124">Using the `ushort` cast guarantees that the correct type is called, for example:</span></span>

```csharp
// Calls the method with the int parameter:
SampleMethod(5);
// Calls the method with the ushort parameter:
SampleMethod((ushort)5);
```

## <a name="conversions"></a><span data-ttu-id="f9175-125">Conversions</span><span class="sxs-lookup"><span data-stu-id="f9175-125">Conversions</span></span>

<span data-ttu-id="f9175-126">Il existe une conversion implicite prédéfinie de `ushort` en [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) ou [decimal](decimal.md).</span><span class="sxs-lookup"><span data-stu-id="f9175-126">There is a predefined implicit conversion from `ushort` to [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md), or [decimal](decimal.md).</span></span>

<span data-ttu-id="f9175-127">Il existe une conversion implicite prédéfinie de [byte](byte.md) ou [char](char.md) en `ushort`.</span><span class="sxs-lookup"><span data-stu-id="f9175-127">There is a predefined implicit conversion from [byte](byte.md) or [char](char.md) to `ushort`.</span></span> <span data-ttu-id="f9175-128">Sinon, vous devez utiliser un cast pour effectuer une conversion explicite.</span><span class="sxs-lookup"><span data-stu-id="f9175-128">Otherwise a cast must be used to perform an explicit conversion.</span></span> <span data-ttu-id="f9175-129">Considérons, par exemple, les deux variables `ushort` `x` et `y` suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9175-129">Consider, for example, the following two `ushort` variables `x` and `y`:</span></span>

```csharp
ushort x = 5, y = 12;
```

<span data-ttu-id="f9175-130">L’instruction d’assignation suivante entraîne une erreur de compilation, car l’expression arithmétique située à droite de l’opérateur d’assignation donne la valeur `int` par défaut.</span><span class="sxs-lookup"><span data-stu-id="f9175-130">The following assignment statement will produce a compilation error, because the arithmetic expression on the right side of the assignment operator evaluates to `int` by default.</span></span>

```csharp
ushort z = x + y;   // Error: conversion from int to ushort
```

<span data-ttu-id="f9175-131">Pour corriger ce problème, utilisez un cast :</span><span class="sxs-lookup"><span data-stu-id="f9175-131">To fix this problem, use a cast:</span></span>

```csharp
ushort z = (ushort)(x + y);   // OK: explicit conversion
```

<span data-ttu-id="f9175-132">Il est cependant possible d’utiliser les instructions suivantes dans lesquelles la variable de destination a une taille de stockage égale ou supérieure :</span><span class="sxs-lookup"><span data-stu-id="f9175-132">It is possible though to use the following statements, where the destination variable has the same storage size or a larger storage size:</span></span>

```csharp
int m = x + y;
long n = x + y;
```

<span data-ttu-id="f9175-133">Notez aussi qu’il n’existe pas de conversion implicite des types virgule flottante en `ushort`.</span><span class="sxs-lookup"><span data-stu-id="f9175-133">Notice also that there is no implicit conversion from floating-point types to `ushort`.</span></span> <span data-ttu-id="f9175-134">Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="f9175-134">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>

```csharp
// Error -- no implicit conversion from double:
ushort x = 3.0;
// OK -- explicit conversion:
ushort y = (ushort)3.0;
```

<span data-ttu-id="f9175-135">Pour plus d’informations sur les expressions arithmétiques dans lesquelles coexistent des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).</span><span class="sxs-lookup"><span data-stu-id="f9175-135">For information about arithmetic expressions with mixed floating-point types and integral types, see [float](float.md) and [double](double.md).</span></span>

<span data-ttu-id="f9175-136">Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9175-136">For more information about implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](implicit-numeric-conversions-table.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="f9175-137">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="f9175-137">C# language specification</span></span>

<span data-ttu-id="f9175-138">Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="f9175-138">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="f9175-139">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="f9175-139">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9175-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9175-140">See also</span></span>

- <xref:System.UInt16>
- [<span data-ttu-id="f9175-141">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f9175-141">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="f9175-142">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f9175-142">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="f9175-143">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="f9175-143">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="f9175-144">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="f9175-144">Integral Types Table</span></span>](integral-types-table.md)
- [<span data-ttu-id="f9175-145">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="f9175-145">Built-In Types Table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="f9175-146">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="f9175-146">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)
- [<span data-ttu-id="f9175-147">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="f9175-147">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)
