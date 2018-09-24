---
title: double, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- double
- double_CSharpKeyword
helpviewer_keywords:
- double data type [C#]
ms.assetid: 0980e11b-6004-4102-abcf-cfc280fc6991
ms.openlocfilehash: 4c11065d9354d44c1da8354c6f7b4f52d7b84c10
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46577007"
---
# <a name="double-c-reference"></a><span data-ttu-id="5f0ab-102">double (référence C#)</span><span class="sxs-lookup"><span data-stu-id="5f0ab-102">double (C# Reference)</span></span>

<span data-ttu-id="5f0ab-103">Le mot clé `double` désigne un type simple qui stocke des valeurs à virgule flottante de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-103">The `double` keyword signifies a simple type that stores 64-bit floating-point values.</span></span> <span data-ttu-id="5f0ab-104">Le tableau suivant montre la précision et la plage approximative pour le type `double`.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-104">The following table shows the precision and approximate range for the `double` type.</span></span>

|<span data-ttu-id="5f0ab-105">Type</span><span class="sxs-lookup"><span data-stu-id="5f0ab-105">Type</span></span>|<span data-ttu-id="5f0ab-106">Plage approximative</span><span class="sxs-lookup"><span data-stu-id="5f0ab-106">Approximate range</span></span>|<span data-ttu-id="5f0ab-107">Précision</span><span class="sxs-lookup"><span data-stu-id="5f0ab-107">Precision</span></span>|<span data-ttu-id="5f0ab-108">Type .NET</span><span class="sxs-lookup"><span data-stu-id="5f0ab-108">.NET type</span></span>|
|----------|-----------------------|---------------|-------------------------|
|`double`|<span data-ttu-id="5f0ab-109">De ±5,0 × 10<sup>−324</sup> à ±1,7 × 10<sup>308</sup></span><span class="sxs-lookup"><span data-stu-id="5f0ab-109">±5.0 × 10<sup>−324</sup> to ±1.7 × 10<sup>308</sup></span></span>|<span data-ttu-id="5f0ab-110">15 à 16 chiffres</span><span class="sxs-lookup"><span data-stu-id="5f0ab-110">15-16 digits</span></span>|<xref:System.Double?displayProperty=nameWithType>|

## <a name="literals"></a><span data-ttu-id="5f0ab-111">Littéraux</span><span class="sxs-lookup"><span data-stu-id="5f0ab-111">Literals</span></span>

<span data-ttu-id="5f0ab-112">Par défaut, un littéral numérique réel sur le côté droit de l’opérateur d’assignation est traité comme `double`.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-112">By default, a real numeric literal on the right side of the assignment operator is treated as `double`.</span></span> <span data-ttu-id="5f0ab-113">Toutefois, si vous souhaitez qu’un nombre entier soit traité comme `double`, utilisez le suffixe d ou D, par exemple :</span><span class="sxs-lookup"><span data-stu-id="5f0ab-113">However, if you want an integer number to be treated as `double`, use the suffix d or D, for example:</span></span>

```csharp
double x = 3D;
```

## <a name="conversions"></a><span data-ttu-id="5f0ab-114">Conversions</span><span class="sxs-lookup"><span data-stu-id="5f0ab-114">Conversions</span></span>

<span data-ttu-id="5f0ab-115">Vous pouvez combiner des types numériques intégraux et des types virgule flottante dans une expression.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-115">You can mix numeric integral types and floating-point types in an expression.</span></span> <span data-ttu-id="5f0ab-116">Dans ce cas, les types intégraux sont convertis en types virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-116">In this case, the integral types are converted to floating-point types.</span></span> <span data-ttu-id="5f0ab-117">L’évaluation de l’expression est exécutée d’après les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f0ab-117">The evaluation of the expression is performed according to the following rules:</span></span>

- <span data-ttu-id="5f0ab-118">Si l’un des types virgule flottante est `double`, l’expression prend la valeur `double`, ou [bool](../../../csharp/language-reference/keywords/bool.md) dans les comparaisons relationnelles et les comparaisons d’égalité.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-118">If one of the floating-point types is `double`, the expression evaluates to `double`, or to [bool](../../../csharp/language-reference/keywords/bool.md) in relational comparisons and comparisons for equality.</span></span>

- <span data-ttu-id="5f0ab-119">Si l’expression n’a pas de type `double`, elle prend la valeur [float](../../../csharp/language-reference/keywords/float.md), ou [bool](../../../csharp/language-reference/keywords/bool.md) dans les comparaisons relationnelles et les comparaisons d’égalité.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-119">If there is no `double` type in the expression, it evaluates to [float](../../../csharp/language-reference/keywords/float.md), or to [bool](../../../csharp/language-reference/keywords/bool.md) in relational comparisons and comparisons for equality.</span></span>

 <span data-ttu-id="5f0ab-120">Une expression à virgule flottante peut contenir les ensembles de valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5f0ab-120">A floating-point expression can contain the following sets of values:</span></span>

- <span data-ttu-id="5f0ab-121">Zéro positif et négatif.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-121">Positive and negative zero.</span></span>

- <span data-ttu-id="5f0ab-122">Infini positif et négatif.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-122">Positive and negative infinity.</span></span>

- <span data-ttu-id="5f0ab-123">Valeur NaN (N’est pas un nombre).</span><span class="sxs-lookup"><span data-stu-id="5f0ab-123">Not-a-Number value (NaN).</span></span>

- <span data-ttu-id="5f0ab-124">L’ensemble fini de valeurs différentes de zéro.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-124">The finite set of nonzero values.</span></span>

<span data-ttu-id="5f0ab-125">Pour plus d’informations sur ces valeurs, consultez IEEE Standard for Binary Floating-Point Arithmetic, disponible sur le site web de l’[IEEE](https://www.ieee.org).</span><span class="sxs-lookup"><span data-stu-id="5f0ab-125">For more information about these values, see IEEE Standard for Binary Floating-Point Arithmetic, available on the [IEEE](https://www.ieee.org) Web site.</span></span>

## <a name="example"></a><span data-ttu-id="5f0ab-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f0ab-126">Example</span></span>

<span data-ttu-id="5f0ab-127">Dans l’exemple suivant, un [int](../../../csharp/language-reference/keywords/int.md), un [short](../../../csharp/language-reference/keywords/short.md), un [float](../../../csharp/language-reference/keywords/float.md)et un `double` sont ajoutés pour donner un résultat `double`.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-127">In the following example, an [int](../../../csharp/language-reference/keywords/int.md), a [short](../../../csharp/language-reference/keywords/short.md), a [float](../../../csharp/language-reference/keywords/float.md), and a `double` are added together giving a `double` result.</span></span>

[!code-csharp[csrefKeywordsTypes#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#9)]

## <a name="c-language-specification"></a><span data-ttu-id="5f0ab-128">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="5f0ab-128">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="5f0ab-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f0ab-129">See Also</span></span>

- [<span data-ttu-id="5f0ab-130">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5f0ab-130">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="5f0ab-131">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5f0ab-131">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="5f0ab-132">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="5f0ab-132">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="5f0ab-133">Tableau des valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="5f0ab-133">Default Values Table</span></span>](../../../csharp/language-reference/keywords/default-values-table.md)  
- [<span data-ttu-id="5f0ab-134">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="5f0ab-134">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
- [<span data-ttu-id="5f0ab-135">Tableau des types virgule flottante</span><span class="sxs-lookup"><span data-stu-id="5f0ab-135">Floating-Point Types Table</span></span>](../../../csharp/language-reference/keywords/floating-point-types-table.md)  
- [<span data-ttu-id="5f0ab-136">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="5f0ab-136">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
- [<span data-ttu-id="5f0ab-137">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="5f0ab-137">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  
