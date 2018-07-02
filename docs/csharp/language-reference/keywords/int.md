---
title: int (référence C#)
ms.date: 03/14/2017
f1_keywords:
- int_CSharpKeyword
- int
helpviewer_keywords:
- int keyword [C#]
ms.assetid: 212447b4-5d2a-41aa-88ab-84fe710bdb52
ms.openlocfilehash: 41ee5ecdae815eaddf8652a4873c060fb8f92bc3
ms.sourcegitcommit: f9e38d31288fe5962e6be5b0cc286da633482873
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37028264"
---
# <a name="int-c-reference"></a><span data-ttu-id="5df25-102">int (référence C#)</span><span class="sxs-lookup"><span data-stu-id="5df25-102">int (C# Reference)</span></span>

<span data-ttu-id="5df25-103">`int` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5df25-103">`int` denotes an integral type that stores values according to the size and range shown in the following table.</span></span>  
  
|<span data-ttu-id="5df25-104">Type</span><span class="sxs-lookup"><span data-stu-id="5df25-104">Type</span></span>|<span data-ttu-id="5df25-105">Plage</span><span class="sxs-lookup"><span data-stu-id="5df25-105">Range</span></span>|<span data-ttu-id="5df25-106">Size</span><span class="sxs-lookup"><span data-stu-id="5df25-106">Size</span></span>|<span data-ttu-id="5df25-107">Type .NET</span><span class="sxs-lookup"><span data-stu-id="5df25-107">.NET type</span></span>|  
|----------|-----------|----------|-------------------------|  
|`int`|<span data-ttu-id="5df25-108">-2,147,483,648 en 2,147,483,647</span><span class="sxs-lookup"><span data-stu-id="5df25-108">-2,147,483,648 to 2,147,483,647</span></span>|<span data-ttu-id="5df25-109">Entier 32 bits signé</span><span class="sxs-lookup"><span data-stu-id="5df25-109">Signed 32-bit integer</span></span>|<xref:System.Int32?displayProperty=nameWithType>|  
  
## <a name="literals"></a><span data-ttu-id="5df25-110">Littéraux</span><span class="sxs-lookup"><span data-stu-id="5df25-110">Literals</span></span>  
 
<span data-ttu-id="5df25-111">Vous pouvez déclarer et initialiser une variable `int` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).</span><span class="sxs-lookup"><span data-stu-id="5df25-111">You can declare and initialize an `int` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7.0) a binary literal to it.</span></span>  <span data-ttu-id="5df25-112">Si le littéral entier est en dehors de la plage autorisée pour le type `int` (autrement dit, s’il est inférieur à <xref:System.Int32.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.Int32.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="5df25-112">If the integer literal is outside the range of `int` (that is, if it is less than <xref:System.Int32.MinValue?displayProperty=nameWithType> or greater than <xref:System.Int32.MaxValue?displayProperty=nameWithType>), a compilation error occurs.</span></span> 

<span data-ttu-id="5df25-113">Dans l’exemple suivant, les entiers égaux à 90 946 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `int`.</span><span class="sxs-lookup"><span data-stu-id="5df25-113">In the following example, integers equal to 90,946 that are represented as decimal, hexadecimal, and binary literals are assigned to `int` values.</span></span>  
  
[!code-csharp[int](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#Int)]  

> [!NOTE] 
> <span data-ttu-id="5df25-114">Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="5df25-114">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="5df25-115">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="5df25-115">Decimal literals have no prefix.</span></span> 

<span data-ttu-id="5df25-116">À compter de C# 7.0, des fonctionnalités ont été ajoutées pour améliorer la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="5df25-116">Starting with C# 7.0, a couple of features have been added to enhance readability.</span></span> 
 - <span data-ttu-id="5df25-117">C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="5df25-117">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
 - <span data-ttu-id="5df25-118">C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe.</span><span class="sxs-lookup"><span data-stu-id="5df25-118">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="5df25-119">Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.</span><span class="sxs-lookup"><span data-stu-id="5df25-119">A decimal literal isn't permitted to have a leading underscore.</span></span>

<span data-ttu-id="5df25-120">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="5df25-120">Some examples are shown below.</span></span>

[!code-csharp[int](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#IntS)]  
 
 <span data-ttu-id="5df25-121">Les littéraux entiers peuvent également inclure un suffixe désignant le type, bien qu’il n’existe aucun suffixe qui désigne le type `int`.</span><span class="sxs-lookup"><span data-stu-id="5df25-121">Integer literals can also include a suffix that denotes the type, although there is no suffix that denotes the `int` type.</span></span> <span data-ttu-id="5df25-122">Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :</span><span class="sxs-lookup"><span data-stu-id="5df25-122">If an integer literal has no suffix, its type is the first of the following types in which its value can be represented:</span></span> 

1. `int`
2. [<span data-ttu-id="5df25-123">uint</span><span class="sxs-lookup"><span data-stu-id="5df25-123">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)
3. [<span data-ttu-id="5df25-124">long</span><span class="sxs-lookup"><span data-stu-id="5df25-124">long</span></span>](../../../csharp/language-reference/keywords/long.md)
4. [<span data-ttu-id="5df25-125">ulong</span><span class="sxs-lookup"><span data-stu-id="5df25-125">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md) 
 
<span data-ttu-id="5df25-126">Dans ces exemples, le littéral 90946 est de type `int`.</span><span class="sxs-lookup"><span data-stu-id="5df25-126">In these examples, the literal 90946 is of type `int`.</span></span>
  
## <a name="conversions"></a><span data-ttu-id="5df25-127">Conversions</span><span class="sxs-lookup"><span data-stu-id="5df25-127">Conversions</span></span>  
 <span data-ttu-id="5df25-128">Il existe une conversion implicite prédéfinie de `int` en [long](../../../csharp/language-reference/keywords/long.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) ou [decimal](../../../csharp/language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="5df25-128">There is a predefined implicit conversion from `int` to [long](../../../csharp/language-reference/keywords/long.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span> <span data-ttu-id="5df25-129">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5df25-129">For example:</span></span>  
  
```csharp  
// '123' is an int, so an implicit conversion takes place here:  
float f = 123;  
```  
  
 <span data-ttu-id="5df25-130">Il existe une conversion implicite prédéfinie de [sbyte](../../../csharp/language-reference/keywords/sbyte.md), [byte](../../../csharp/language-reference/keywords/byte.md), [short](../../../csharp/language-reference/keywords/short.md), [ushort](../../../csharp/language-reference/keywords/ushort.md) ou [char](../../../csharp/language-reference/keywords/char.md) en `int`.</span><span class="sxs-lookup"><span data-stu-id="5df25-130">There is a predefined implicit conversion from [sbyte](../../../csharp/language-reference/keywords/sbyte.md), [byte](../../../csharp/language-reference/keywords/byte.md), [short](../../../csharp/language-reference/keywords/short.md), [ushort](../../../csharp/language-reference/keywords/ushort.md), or [char](../../../csharp/language-reference/keywords/char.md) to `int`.</span></span> <span data-ttu-id="5df25-131">Par exemple, l’instruction d’assignation suivante génère une erreur de compilation sans cast :</span><span class="sxs-lookup"><span data-stu-id="5df25-131">For example, the following assignment statement will produce a compilation error without a cast:</span></span>  
  
```csharp  
long aLong = 22;  
int i1 = aLong;       // Error: no implicit conversion from long.  
int i2 = (int)aLong;  // OK: explicit conversion.  
```  
  
 <span data-ttu-id="5df25-132">Remarquez également qu’il n’existe pas de conversion implicite des types virgule flottante en `int`.</span><span class="sxs-lookup"><span data-stu-id="5df25-132">Notice also that there is no implicit conversion from floating-point types to `int`.</span></span> <span data-ttu-id="5df25-133">Par exemple, l’instruction suivante génère une erreur du compilateur à moins qu’un cast explicite soit utilisé :</span><span class="sxs-lookup"><span data-stu-id="5df25-133">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>  
  
```csharp  
int x = 3.0;         // Error: no implicit conversion from double.  
int y = (int)3.0;    // OK: explicit conversion.  
```  
  
 <span data-ttu-id="5df25-134">Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](../../../csharp/language-reference/keywords/float.md) et [double](../../../csharp/language-reference/keywords/double.md).</span><span class="sxs-lookup"><span data-stu-id="5df25-134">For more information on arithmetic expressions with mixed floating-point types and integral types, see [float](../../../csharp/language-reference/keywords/float.md) and [double](../../../csharp/language-reference/keywords/double.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="5df25-135">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="5df25-135">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5df25-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5df25-136">See Also</span></span>  
 <xref:System.Int32>  
 [<span data-ttu-id="5df25-137">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5df25-137">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="5df25-138">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5df25-138">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="5df25-139">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="5df25-139">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="5df25-140">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="5df25-140">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
 [<span data-ttu-id="5df25-141">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="5df25-141">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
 [<span data-ttu-id="5df25-142">Tableau des conversions numériques implicites</span><span class="sxs-lookup"><span data-stu-id="5df25-142">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
 [<span data-ttu-id="5df25-143">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="5df25-143">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)
