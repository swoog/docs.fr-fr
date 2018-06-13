---
title: Tableau des conversions numériques implicites (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: 2d417a2020656f300de0517526742679388f262e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33217192"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="406a1-102">Tableau des conversions numériques implicites (référence C#)</span><span class="sxs-lookup"><span data-stu-id="406a1-102">Implicit Numeric Conversions Table (C# Reference)</span></span>
<span data-ttu-id="406a1-103">Le tableau suivant montre les conversions numériques implicites prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="406a1-103">The following table shows the predefined implicit numeric conversions.</span></span> <span data-ttu-id="406a1-104">Les conversions implicites peuvent se produire dans de nombreuses situations, comme les appels de méthode et les instructions d’assignation.</span><span class="sxs-lookup"><span data-stu-id="406a1-104">Implicit conversions might occur in many situations, including method invoking and assignment statements.</span></span>  
  
|<span data-ttu-id="406a1-105">From</span><span class="sxs-lookup"><span data-stu-id="406a1-105">From</span></span>|<span data-ttu-id="406a1-106">À</span><span class="sxs-lookup"><span data-stu-id="406a1-106">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="406a1-107">sbyte</span><span class="sxs-lookup"><span data-stu-id="406a1-107">sbyte</span></span>](../../../csharp/language-reference/keywords/sbyte.md)|<span data-ttu-id="406a1-108">`short`, `int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-108">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-109">byte</span><span class="sxs-lookup"><span data-stu-id="406a1-109">byte</span></span>](../../../csharp/language-reference/keywords/byte.md)|<span data-ttu-id="406a1-110">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-110">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-111">short</span><span class="sxs-lookup"><span data-stu-id="406a1-111">short</span></span>](../../../csharp/language-reference/keywords/short.md)|<span data-ttu-id="406a1-112">`int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-112">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-113">ushort</span><span class="sxs-lookup"><span data-stu-id="406a1-113">ushort</span></span>](../../../csharp/language-reference/keywords/ushort.md)|<span data-ttu-id="406a1-114">`int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-114">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-115">int</span><span class="sxs-lookup"><span data-stu-id="406a1-115">int</span></span>](../../../csharp/language-reference/keywords/int.md)|<span data-ttu-id="406a1-116">`long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-116">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-117">uint</span><span class="sxs-lookup"><span data-stu-id="406a1-117">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)|<span data-ttu-id="406a1-118">`long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-118">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-119">long</span><span class="sxs-lookup"><span data-stu-id="406a1-119">long</span></span>](../../../csharp/language-reference/keywords/long.md)|<span data-ttu-id="406a1-120">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-120">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-121">char</span><span class="sxs-lookup"><span data-stu-id="406a1-121">char</span></span>](../../../csharp/language-reference/keywords/char.md)|<span data-ttu-id="406a1-122">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-122">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="406a1-123">float</span><span class="sxs-lookup"><span data-stu-id="406a1-123">float</span></span>](../../../csharp/language-reference/keywords/float.md)|`double`|  
|[<span data-ttu-id="406a1-124">ulong</span><span class="sxs-lookup"><span data-stu-id="406a1-124">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md)|<span data-ttu-id="406a1-125">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="406a1-125">`float`, `double`, or `decimal`</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="406a1-126">Notes</span><span class="sxs-lookup"><span data-stu-id="406a1-126">Remarks</span></span>  
  
-   <span data-ttu-id="406a1-127">C’est la précision, et non la magnitude, qui peut être perdue lors de conversions de `int`, `uint`, `long` ou `ulong` à `float`, et de `long` ou `ulong` à `double`.</span><span class="sxs-lookup"><span data-stu-id="406a1-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`,  `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
-   <span data-ttu-id="406a1-128">Il n’y a pas de conversion implicite possible vers le type `char`.</span><span class="sxs-lookup"><span data-stu-id="406a1-128">There are no implicit conversions to the `char` type.</span></span>  
  
-   <span data-ttu-id="406a1-129">Il n’y a pas non plus de conversion implicite possible entre les types virgule flottante et le type `decimal`.</span><span class="sxs-lookup"><span data-stu-id="406a1-129">There are no implicit conversions between floating-point types and the `decimal` type.</span></span>  
  
-   <span data-ttu-id="406a1-130">Une expression constante de type `int` peut être convertie en `sbyte`, `byte`, `short`, `ushort`, `uint` ou `ulong`, à condition que la valeur de l’expression constante se trouve dans la plage du type de destination.</span><span class="sxs-lookup"><span data-stu-id="406a1-130">A constant expression of type `int` can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided the value of the constant expression is within the range of the destination type.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="406a1-131">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="406a1-131">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="406a1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="406a1-132">See Also</span></span>  
 [<span data-ttu-id="406a1-133">Référence C#</span><span class="sxs-lookup"><span data-stu-id="406a1-133">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="406a1-134">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="406a1-134">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="406a1-135">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="406a1-135">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
 [<span data-ttu-id="406a1-136">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="406a1-136">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
 [<span data-ttu-id="406a1-137">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="406a1-137">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  
 [<span data-ttu-id="406a1-138">Cast et conversions de types</span><span class="sxs-lookup"><span data-stu-id="406a1-138">Casting and Type Conversions</span></span>](../../../csharp/programming-guide/types/casting-and-type-conversions.md)
