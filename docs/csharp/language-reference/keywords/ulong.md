---
title: ulong (référence C#)
ms.date: 03/14/2017
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ulong_CSharpKeyword
- ulong
helpviewer_keywords:
- ulong keyword [C#]
ms.assetid: f2ece624-837a-40cf-92c5-343e7f33397c
caps.latest.revision: 16
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 049d1cc4b30e16535f20cee8e0ad80e5c80b4a49
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="ulong-c-reference"></a><span data-ttu-id="f67ff-102">ulong (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f67ff-102">ulong (C# Reference)</span></span>

<span data-ttu-id="f67ff-103">Le mot clé `ulong` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f67ff-103">The `ulong` keyword denotes an integral type that stores values according to the size and range shown in the following table.</span></span>  
  
|<span data-ttu-id="f67ff-104">Type</span><span class="sxs-lookup"><span data-stu-id="f67ff-104">Type</span></span>|<span data-ttu-id="f67ff-105">Plage</span><span class="sxs-lookup"><span data-stu-id="f67ff-105">Range</span></span>|<span data-ttu-id="f67ff-106">Size</span><span class="sxs-lookup"><span data-stu-id="f67ff-106">Size</span></span>|<span data-ttu-id="f67ff-107">Type .NET Framework</span><span class="sxs-lookup"><span data-stu-id="f67ff-107">.NET Framework type</span></span>|  
|----------|-----------|----------|-------------------------|  
|`ulong`|<span data-ttu-id="f67ff-108">de 0 à 18 446 744 073 709 551 615</span><span class="sxs-lookup"><span data-stu-id="f67ff-108">0 to 18,446,744,073,709,551,615</span></span>|<span data-ttu-id="f67ff-109">Entier 64 bits non signé</span><span class="sxs-lookup"><span data-stu-id="f67ff-109">Unsigned 64-bit integer</span></span>|<xref:System.UInt64?displayProperty=nameWithType>|  
  
## <a name="literals"></a><span data-ttu-id="f67ff-110">Littéraux</span><span class="sxs-lookup"><span data-stu-id="f67ff-110">Literals</span></span>  

<span data-ttu-id="f67ff-111">Vous pouvez déclarer et initialiser une variable `ulong` en lui affectant un littéral décimal, un littéral ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="f67ff-111">You can declare and initialize a `ulong` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span>  <span data-ttu-id="f67ff-112">Si le littéral entier est en dehors de la plage autorisée pour le type `ulong` (autrement dit, s’il est inférieur à <xref:System.UInt64.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt64.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="f67ff-112">If the integer literal is outside the range of `ulong` (that is, if it is less than <xref:System.UInt64.MinValue?displayProperty=nameWithType> or greater than <xref:System.UInt64.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span> 

<span data-ttu-id="f67ff-113">Dans l’exemple suivant, les entiers égaux à 7 934 076 125 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `ulong`.</span><span class="sxs-lookup"><span data-stu-id="f67ff-113">In the following example, integers equal to 7,934,076,125 that are represented as decimal, hexadecimal, and binary literals are assigned to `ulong` values.</span></span>  
  
[!code-csharp[ulong](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#ULong)]  

> [!NOTE] 
> <span data-ttu-id="f67ff-114">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="f67ff-114">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="f67ff-115">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="f67ff-115">Decimal literals have no prefix.</span></span> 

<span data-ttu-id="f67ff-116">À compter de C# 7.0, des fonctionnalités ont été ajoutées pour améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="f67ff-116">Starting with C# 7.0, a couple of features have been added to enhance readability.</span></span> 
 - <span data-ttu-id="f67ff-117">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="f67ff-117">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
 - <span data-ttu-id="f67ff-118">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="f67ff-118">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="f67ff-119">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="f67ff-119">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="f67ff-120">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="f67ff-120">Some examples are shown below.</span></span>

[!code-csharp[long](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#LongS)]  
 
 <span data-ttu-id="f67ff-121">Les littéraux entiers peuvent également inclure un suffixe qui désigne le type.</span><span class="sxs-lookup"><span data-stu-id="f67ff-121">Integer literals can also include a suffix that denotes the type.</span></span> <span data-ttu-id="f67ff-122">Le suffixe `UL` ou `ul` identifie sans ambiguïté un littéral numérique comme une valeur `ulong`.</span><span class="sxs-lookup"><span data-stu-id="f67ff-122">The suffix `UL` or `ul` unambiguously identifies a numeric literal as a `ulong` value.</span></span> <span data-ttu-id="f67ff-123">Le suffixe `L` désigne un type `ulong` si la valeur du littéral dépasse <xref:System.Int64.MaxValue?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f67ff-123">The `L` suffix denotes a `ulong` if the literal value exceeds <xref:System.Int64.MaxValue?displayProperty=nameWithType>.</span></span> <span data-ttu-id="f67ff-124">Le suffixe `U` ou `u` désigne un type `ulong` si la valeur du littéral dépasse <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="f67ff-124">And the `U` or `u` suffix denotes a `ulong` if the literal value exceeds <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.</span></span> <span data-ttu-id="f67ff-125">L’exemple suivant utilise le suffixe `ul` pour désigner un entier long :</span><span class="sxs-lookup"><span data-stu-id="f67ff-125">The following example uses the `ul` suffix to denote a long integer:</span></span>
 
[!code-csharp[ulsuffix](../../../../samples/snippets/csharp/language-reference/keywords/numeric-suffixes.cs#2)]

<span data-ttu-id="f67ff-126">Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :</span><span class="sxs-lookup"><span data-stu-id="f67ff-126">If an integer literal has no suffix, its type is the first of the following types in which its value can be represented:</span></span> 

1. [<span data-ttu-id="f67ff-127">int</span><span class="sxs-lookup"><span data-stu-id="f67ff-127">int</span></span>](int.md)
2. [<span data-ttu-id="f67ff-128">uint</span><span class="sxs-lookup"><span data-stu-id="f67ff-128">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)
3. [<span data-ttu-id="f67ff-129">long</span><span class="sxs-lookup"><span data-stu-id="f67ff-129">long</span></span>](long.md)
4. `ulong`

## <a name="compiler-overload-resolution"></a><span data-ttu-id="f67ff-130">Résolution de surcharge du compilateur</span><span class="sxs-lookup"><span data-stu-id="f67ff-130">Compiler overload resolution</span></span>
  
 <span data-ttu-id="f67ff-131">Une utilisation courante du suffixe est d’appeler des méthodes surchargées.</span><span class="sxs-lookup"><span data-stu-id="f67ff-131">A common use of the suffix is with calling overloaded methods.</span></span> <span data-ttu-id="f67ff-132">Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `ulong` et [int](../../../csharp/language-reference/keywords/int.md) :</span><span class="sxs-lookup"><span data-stu-id="f67ff-132">Consider, for example, the following overloaded methods that use `ulong` and [int](../../../csharp/language-reference/keywords/int.md) parameters:</span></span>  
  
```csharp  
public static void SampleMethod(int i) {}  
public static void SampleMethod(ulong l) {}  
```  
  
 <span data-ttu-id="f67ff-133">L’utilisation d’un suffixe avec le paramètre `ulong` garantit que le type correct est appelé, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f67ff-133">Using a suffix with the `ulong` parameter guarantees that the correct type is called, for example:</span></span>  
  
```csharp  
SampleMethod(5);    // Calling the method with the int parameter  
SampleMethod(5UL);  // Calling the method with the ulong parameter  
```  
  
## <a name="conversions"></a><span data-ttu-id="f67ff-134">Conversions</span><span class="sxs-lookup"><span data-stu-id="f67ff-134">Conversions</span></span>  
 <span data-ttu-id="f67ff-135">Il existe une conversion implicite prédéfinie de `ulong` en [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) ou [decimal](../../../csharp/language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="f67ff-135">There is a predefined implicit conversion from `ulong` to [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span>  
  
 <span data-ttu-id="f67ff-136">Il n’existe aucune conversion implicite de `ulong` en un type intégral.</span><span class="sxs-lookup"><span data-stu-id="f67ff-136">There is no implicit conversion from `ulong` to any integral type.</span></span> <span data-ttu-id="f67ff-137">Par exemple, l’instruction suivante génère une erreur de compilation sans cast explicite :</span><span class="sxs-lookup"><span data-stu-id="f67ff-137">For example, the following statement will produce a compilation error without an explicit cast:</span></span>  
  
```csharp  
long long1 = 8UL;   // Error: no implicit conversion from ulong  
```  
  
 <span data-ttu-id="f67ff-138">Il existe une conversion implicite prédéfinie de [byte](../../../csharp/language-reference/keywords/byte.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), [uint](../../../csharp/language-reference/keywords/uint.md) ou [char](../../../csharp/language-reference/keywords/char.md) en `ulong`.</span><span class="sxs-lookup"><span data-stu-id="f67ff-138">There is a predefined implicit conversion from [byte](../../../csharp/language-reference/keywords/byte.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), [uint](../../../csharp/language-reference/keywords/uint.md), or [char](../../../csharp/language-reference/keywords/char.md) to `ulong`.</span></span>  
  
 <span data-ttu-id="f67ff-139">De plus, il n’existe pas de conversion implicite des types virgule flottante en `ulong`.</span><span class="sxs-lookup"><span data-stu-id="f67ff-139">Also, there is no implicit conversion from floating-point types to `ulong`.</span></span> <span data-ttu-id="f67ff-140">Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :</span><span class="sxs-lookup"><span data-stu-id="f67ff-140">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>  
  
```csharp  
// Error -- no implicit conversion from double:  
ulong x = 3.0;  
// OK -- explicit conversion:  
ulong y = (ulong)3.0;    
```  
  
 <span data-ttu-id="f67ff-141">Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](../../../csharp/language-reference/keywords/float.md) et [double](../../../csharp/language-reference/keywords/double.md).</span><span class="sxs-lookup"><span data-stu-id="f67ff-141">For information on arithmetic expressions with mixed floating-point types and integral types, see [float](../../../csharp/language-reference/keywords/float.md) and [double](../../../csharp/language-reference/keywords/double.md).</span></span>  
  
 <span data-ttu-id="f67ff-142">Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [tableau des conversions numériques implicites](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="f67ff-142">For more information on implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="f67ff-143">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="f67ff-143">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f67ff-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f67ff-144">See Also</span></span>  
 <xref:System.UInt64>  
 [<span data-ttu-id="f67ff-145">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f67ff-145">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="f67ff-146">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f67ff-146">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="f67ff-147">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="f67ff-147">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="f67ff-148">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="f67ff-148">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
 [<span data-ttu-id="f67ff-149">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="f67ff-149">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
 [<span data-ttu-id="f67ff-150">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="f67ff-150">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
 [<span data-ttu-id="f67ff-151">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="f67ff-151">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)
