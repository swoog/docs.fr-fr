---
title: uint, mot clé (référence C#)
ms.date: 03/14/2017
f1_keywords:
- uint
- uint_CSharpKeyword
helpviewer_keywords:
- uint keyword [C#]
ms.openlocfilehash: 86cbb216bd960251ebd78916fae7865aa10aa5fc
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149690"
---
# <a name="uint-c-reference"></a><span data-ttu-id="0ca79-102">uint (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0ca79-102">uint (C# Reference)</span></span>

<span data-ttu-id="0ca79-103">Le mot clé `uint` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0ca79-103">The `uint` keyword signifies an integral type that stores values according to the size and range shown in the following table.</span></span>

|<span data-ttu-id="0ca79-104">Type</span><span class="sxs-lookup"><span data-stu-id="0ca79-104">Type</span></span>|<span data-ttu-id="0ca79-105">Plage</span><span class="sxs-lookup"><span data-stu-id="0ca79-105">Range</span></span>|<span data-ttu-id="0ca79-106">Size</span><span class="sxs-lookup"><span data-stu-id="0ca79-106">Size</span></span>|<span data-ttu-id="0ca79-107">Type .NET</span><span class="sxs-lookup"><span data-stu-id="0ca79-107">.NET type</span></span>|
|----------|-----------|----------|-------------------------|
|`uint`|<span data-ttu-id="0ca79-108">de 0 à 4 294 967 295</span><span class="sxs-lookup"><span data-stu-id="0ca79-108">0 to 4,294,967,295</span></span>|<span data-ttu-id="0ca79-109">Entier 32 bits non signé</span><span class="sxs-lookup"><span data-stu-id="0ca79-109">Unsigned 32-bit integer</span></span>|<xref:System.UInt32?displayProperty=nameWithType>|

<span data-ttu-id="0ca79-110">**Note** Le type `uint` n’est pas conforme CLS.</span><span class="sxs-lookup"><span data-stu-id="0ca79-110">**Note** The `uint` type is not CLS-compliant.</span></span> <span data-ttu-id="0ca79-111">Utilisez `int` autant que possible.</span><span class="sxs-lookup"><span data-stu-id="0ca79-111">Use `int` whenever possible.</span></span>

## <a name="literals"></a><span data-ttu-id="0ca79-112">Littéraux</span><span class="sxs-lookup"><span data-stu-id="0ca79-112">Literals</span></span>

<span data-ttu-id="0ca79-113">Vous pouvez déclarer et initialiser une variable `uint` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="0ca79-113">You can declare and initialize a `uint` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span> <span data-ttu-id="0ca79-114">Si le littéral entier est en dehors de la plage autorisée pour le type `uint` (autrement dit, s’il est inférieur à <xref:System.UInt32.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="0ca79-114">If the integer literal is outside the range of `uint` (that is, if it is less than <xref:System.UInt32.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt32.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span>

<span data-ttu-id="0ca79-115">Dans l’exemple suivant, les entiers égaux à 3 000 000 000 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `uint`.</span><span class="sxs-lookup"><span data-stu-id="0ca79-115">In the following example, integers equal to 3,000,000,000 that are represented as decimal, hexadecimal, and binary literals are assigned to `uint` values.</span></span>

[!code-csharp[uint](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UInt)]

> [!NOTE]
> <span data-ttu-id="0ca79-116">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="0ca79-116">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="0ca79-117">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="0ca79-117">Decimal literals have no prefix.</span></span>

<span data-ttu-id="0ca79-118">À partir de C# 7.0, quelques fonctionnalités ont été ajoutées pour améliorer la lisibilité :</span><span class="sxs-lookup"><span data-stu-id="0ca79-118">Starting with C# 7.0, a couple of features have been added to enhance readability:</span></span>

- <span data-ttu-id="0ca79-119">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="0ca79-119">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
- <span data-ttu-id="0ca79-120">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="0ca79-120">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="0ca79-121">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="0ca79-121">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="0ca79-122">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="0ca79-122">Some examples are shown below.</span></span>

[!code-csharp[uint](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UIntS)]

<span data-ttu-id="0ca79-123">Les littéraux entiers peuvent également inclure un suffixe qui désigne le type.</span><span class="sxs-lookup"><span data-stu-id="0ca79-123">Integer literals can also include a suffix that denotes the type.</span></span> <span data-ttu-id="0ca79-124">Le suffixe `U` ou « u » désigne un type `uint` ou `ulong`, selon la valeur numérique du littéral.</span><span class="sxs-lookup"><span data-stu-id="0ca79-124">The suffix `U` or 'u' denotes either a `uint` or a `ulong`, depending on the numeric value of the literal.</span></span> <span data-ttu-id="0ca79-125">L’exemple suivant utilise le suffixe `u` pour désigner un entier non signé des deux types.</span><span class="sxs-lookup"><span data-stu-id="0ca79-125">The following example uses the `u` suffix to denote an unsigned integer of both types.</span></span> <span data-ttu-id="0ca79-126">Notez que le premier littéral est un type `uint`, car sa valeur est inférieure à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>, tandis que le deuxième est un type `ulong`, car sa valeur est supérieure à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0ca79-126">Note that the first literal is a `uint` because its value is less than <xref:System.UInt32.MaxValue?displayProperty=nameWithType>, while the second is a `ulong` because its value is greater than <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span></span>

[!code-csharp[usuffix](~/samples/snippets/csharp/language-reference/keywords/numeric-suffixes.cs#1)]

<span data-ttu-id="0ca79-127">Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :</span><span class="sxs-lookup"><span data-stu-id="0ca79-127">If an integer literal has no suffix, its type is the first of the following types in which its value can be represented:</span></span>

1. [<span data-ttu-id="0ca79-128">int</span><span class="sxs-lookup"><span data-stu-id="0ca79-128">int</span></span>](int.md)
2. `uint`
3. [<span data-ttu-id="0ca79-129">long</span><span class="sxs-lookup"><span data-stu-id="0ca79-129">long</span></span>](long.md)
4. [<span data-ttu-id="0ca79-130">ulong</span><span class="sxs-lookup"><span data-stu-id="0ca79-130">ulong</span></span>](ulong.md)

## <a name="conversions"></a><span data-ttu-id="0ca79-131">Conversions</span><span class="sxs-lookup"><span data-stu-id="0ca79-131">Conversions</span></span>

<span data-ttu-id="0ca79-132">Il existe une conversion implicite prédéfinie de `uint` en [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) et [decimal](decimal.md).</span><span class="sxs-lookup"><span data-stu-id="0ca79-132">There is a predefined implicit conversion from `uint` to [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md), or [decimal](decimal.md).</span></span> <span data-ttu-id="0ca79-133">Exemple :</span><span class="sxs-lookup"><span data-stu-id="0ca79-133">For example:</span></span>

```csharp
float myFloat = 4294967290;   // OK: implicit conversion to float
```

<span data-ttu-id="0ca79-134">Il existe une conversion implicite prédéfinie de [byte](byte.md), [ushort](ushort.md) ou [char](char.md) en `uint`.</span><span class="sxs-lookup"><span data-stu-id="0ca79-134">There is a predefined implicit conversion from [byte](byte.md), [ushort](ushort.md), or [char](char.md) to `uint`.</span></span> <span data-ttu-id="0ca79-135">Dans le cas contraire, vous devez utiliser un cast.</span><span class="sxs-lookup"><span data-stu-id="0ca79-135">Otherwise you must use a cast.</span></span> <span data-ttu-id="0ca79-136">Par exemple, l’instruction d’assignation suivante génère une erreur de compilation sans cast :</span><span class="sxs-lookup"><span data-stu-id="0ca79-136">For example, the following assignment statement will produce a compilation error without a cast:</span></span>

```csharp
long aLong = 22;
// Error -- no implicit conversion from long:
uint uInt1 = aLong;
// OK -- explicit conversion:
uint uInt2 = (uint)aLong;
```

<span data-ttu-id="0ca79-137">Remarquez également qu’il n’existe pas de conversion implicite des types virgule flottante en `uint`.</span><span class="sxs-lookup"><span data-stu-id="0ca79-137">Notice also that there is no implicit conversion from floating-point types to `uint`.</span></span> <span data-ttu-id="0ca79-138">Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="0ca79-138">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>

```csharp
// Error -- no implicit conversion from double:
uint x = 3.0;
// OK -- explicit conversion:
uint y = (uint)3.0;
```

<span data-ttu-id="0ca79-139">Pour plus d’informations sur les expressions arithmétiques dans lesquelles coexistent des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).</span><span class="sxs-lookup"><span data-stu-id="0ca79-139">For information about arithmetic expressions with mixed floating-point types and integral types, see [float](float.md) and [double](double.md).</span></span>

<span data-ttu-id="0ca79-140">Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ca79-140">For more information about implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](implicit-numeric-conversions-table.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="0ca79-141">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0ca79-141">C# language specification</span></span>

<span data-ttu-id="0ca79-142">Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="0ca79-142">For more information, see [Integral types](~/_csharplang/spec/types.md#integral-types) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="0ca79-143">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="0ca79-143">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ca79-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ca79-144">See also</span></span>

- <xref:System.UInt32>
- [<span data-ttu-id="0ca79-145">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0ca79-145">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0ca79-146">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0ca79-146">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="0ca79-147">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="0ca79-147">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="0ca79-148">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="0ca79-148">Integral Types Table</span></span>](integral-types-table.md)
- [<span data-ttu-id="0ca79-149">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="0ca79-149">Built-In Types Table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="0ca79-150">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="0ca79-150">Implicit Numeric Conversions Table</span></span>](implicit-numeric-conversions-table.md)
- [<span data-ttu-id="0ca79-151">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="0ca79-151">Explicit Numeric Conversions Table</span></span>](explicit-numeric-conversions-table.md)