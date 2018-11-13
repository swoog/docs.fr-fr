---
title: short (référence C#)
ms.date: 03/14/2017
f1_keywords:
- short
- short_CSharpKeyword
helpviewer_keywords:
- short keyword [C#]
ms.assetid: 04c10688-e51a-4a87-bfec-83f7fb42ff11
ms.openlocfilehash: d3b374c01c78a63e8341023b65dc3e57542ec1fd
ms.sourcegitcommit: 3b1cb8467bd73dee854b604e306c0e7e3882d91a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50184151"
---
# <a name="short-c-reference"></a><span data-ttu-id="51d61-102">short (référence C#)</span><span class="sxs-lookup"><span data-stu-id="51d61-102">short (C# Reference)</span></span>

<span data-ttu-id="51d61-103">`short` désigne un type de données intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="51d61-103">`short` denotes an integral data type that stores values according to the size and range shown in the following table.</span></span>

|<span data-ttu-id="51d61-104">Type</span><span class="sxs-lookup"><span data-stu-id="51d61-104">Type</span></span>|<span data-ttu-id="51d61-105">Plage</span><span class="sxs-lookup"><span data-stu-id="51d61-105">Range</span></span>|<span data-ttu-id="51d61-106">Size</span><span class="sxs-lookup"><span data-stu-id="51d61-106">Size</span></span>|<span data-ttu-id="51d61-107">Type .NET</span><span class="sxs-lookup"><span data-stu-id="51d61-107">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`short`|<span data-ttu-id="51d61-108">de -32 768 à 32 767</span><span class="sxs-lookup"><span data-stu-id="51d61-108">-32,768 to 32,767</span></span>|<span data-ttu-id="51d61-109">Entier 16 bits signé</span><span class="sxs-lookup"><span data-stu-id="51d61-109">Signed 16-bit integer</span></span>|<xref:System.Int16?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="51d61-110">Littéraux</span><span class="sxs-lookup"><span data-stu-id="51d61-110">Literals</span></span>

<span data-ttu-id="51d61-111">Vous pouvez déclarer et initialiser une variable `short` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="51d61-111">You can declare and initialize a `short` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span>  <span data-ttu-id="51d61-112">Si le littéral entier est en dehors de la plage autorisée pour le type `short` (autrement dit, s’il est inférieur à <xref:System.Int16.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.Int16.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="51d61-112">If the integer literal is outside the range of `short` (that is, if it is less than <xref:System.Int16.MinValue?displayProperty=nameWithType> or greater than <xref:System.Int16.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span>

<span data-ttu-id="51d61-113">Dans l’exemple suivant, les entiers égaux à 1 034 représentés comme des littéraux décimaux, hexadécimaux et binaires sont implicitement convertis à partir de valeurs [int](int.md) en `short`.</span><span class="sxs-lookup"><span data-stu-id="51d61-113">In the following example, integers equal to 1,034 that are represented as decimal, hexadecimal, and binary literals are implicitly converted from [int](int.md) to `short` values.</span></span>

[!code-csharp[Short](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#Short)]

> [!NOTE]
> <span data-ttu-id="51d61-114">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="51d61-114">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="51d61-115">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="51d61-115">Decimal literals have no prefix.</span></span>

<span data-ttu-id="51d61-116">À compter de C# 7.0, des fonctionnalités ont été ajoutées pour améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="51d61-116">Starting with C# 7.0, a couple of features have been added to enhance readability.</span></span>

- <span data-ttu-id="51d61-117">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="51d61-117">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
- <span data-ttu-id="51d61-118">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="51d61-118">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="51d61-119">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="51d61-119">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="51d61-120">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="51d61-120">Some examples are shown below.</span></span>

[!code-csharp[Short](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#ShortS)]

## <a name="compiler-overload-resolution"></a><span data-ttu-id="51d61-121">Résolution de surcharge du compilateur</span><span class="sxs-lookup"><span data-stu-id="51d61-121">Compiler overload resolution</span></span>

<span data-ttu-id="51d61-122">Un cast doit être utilisé lors de l’appel de méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="51d61-122">A cast must be used when calling overloaded methods.</span></span> <span data-ttu-id="51d61-123">Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `short` et [int](int.md) :</span><span class="sxs-lookup"><span data-stu-id="51d61-123">Consider, for example, the following overloaded methods that use `short` and [int](int.md) parameters:</span></span>

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(short s) {}
```

<span data-ttu-id="51d61-124">L’utilisation du cast `short` garantit l’appel du type correct, par exemple :</span><span class="sxs-lookup"><span data-stu-id="51d61-124">Using the `short` cast guarantees that the correct type is called, for example:</span></span>

```csharp
SampleMethod(5);         // Calling the method with the int parameter
SampleMethod((short)5);  // Calling the method with the short parameter
```

## <a name="conversions"></a><span data-ttu-id="51d61-125">Conversions</span><span class="sxs-lookup"><span data-stu-id="51d61-125">Conversions</span></span>

<span data-ttu-id="51d61-126">Il existe une conversion implicite prédéfinie de `short` en [int](int.md), [long](long.md), [float](float.md), [double](double.md) ou [decimal](decimal.md).</span><span class="sxs-lookup"><span data-stu-id="51d61-126">There is a predefined implicit conversion from `short` to [int](int.md), [long](long.md), [float](float.md), [double](double.md), or [decimal](decimal.md).</span></span>

<span data-ttu-id="51d61-127">Vous ne pouvez pas convertir implicitement des types numériques non littéraux de taille de stockage supérieure à `short` (consultez le [tableau des types intégraux](integral-types-table.md) pour voir les tailles de stockage des types intégraux).</span><span class="sxs-lookup"><span data-stu-id="51d61-127">You cannot implicitly convert nonliteral numeric types of larger storage size to `short` (see [Integral Types Table](integral-types-table.md) for the storage sizes of integral types).</span></span> <span data-ttu-id="51d61-128">Prenez l’exemple des deux variables `short``x` et `y` suivantes :</span><span class="sxs-lookup"><span data-stu-id="51d61-128">Consider, for example, the following two `short` variables `x` and `y`:</span></span>

```csharp
short x = 5, y = 12;
```

<span data-ttu-id="51d61-129">L’instruction d’assignation suivante entraîne une erreur de compilation, car l’expression arithmétique située à droite de l’opérateur d’assignation donne la valeur [int](int.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="51d61-129">The following assignment statement produces a compilation error because the arithmetic expression on the right-hand side of the assignment operator evaluates to [int](int.md) by default.</span></span>

```csharp
short z  = x + y;        // Compiler error CS0266: no conversion from int to short
```

<span data-ttu-id="51d61-130">Pour corriger ce problème, utilisez un cast :</span><span class="sxs-lookup"><span data-stu-id="51d61-130">To fix this problem, use a cast:</span></span>

```csharp
short z  = (short)(x + y);   // Explicit conversion
```

<span data-ttu-id="51d61-131">Il est toutefois possible d’utiliser les instructions suivantes, dans lesquelles la variable de destination a une taille de stockage égale ou supérieure :</span><span class="sxs-lookup"><span data-stu-id="51d61-131">It is also possible to use the following statements, where the destination variable has the same storage size or a larger storage size:</span></span>

```csharp
int m = x + y;
long n = x + y;
```

<span data-ttu-id="51d61-132">Il n’existe pas de conversion implicite des types virgule flottante en `short`.</span><span class="sxs-lookup"><span data-stu-id="51d61-132">There is no implicit conversion from floating-point types to `short`.</span></span> <span data-ttu-id="51d61-133">Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="51d61-133">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>

```csharp
short x = 3.0;          // Error: no implicit conversion from double
short y = (short)3.0;   // OK: explicit conversion
```

<span data-ttu-id="51d61-134">Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).</span><span class="sxs-lookup"><span data-stu-id="51d61-134">For information on arithmetic expressions with mixed floating-point types and integral types, see [float](float.md) and [double](double.md).</span></span>

<span data-ttu-id="51d61-135">Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="51d61-135">For more information on implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](implicit-numeric-conversions-table.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="51d61-136">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="51d61-136">C# language specification</span></span>

<span data-ttu-id="51d61-137">Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="51d61-137">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="51d61-138">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="51d61-138">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="51d61-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51d61-139">See also</span></span>

- <xref:System.Int16>
- [<span data-ttu-id="51d61-140">Référence C#</span><span class="sxs-lookup"><span data-stu-id="51d61-140">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="51d61-141">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="51d61-141">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="51d61-142">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="51d61-142">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="51d61-143">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="51d61-143">Integral Types Table</span></span>](integral-types-table.md)
- [<span data-ttu-id="51d61-144">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="51d61-144">Built-In Types Table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="51d61-145">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="51d61-145">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)
- [<span data-ttu-id="51d61-146">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="51d61-146">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)