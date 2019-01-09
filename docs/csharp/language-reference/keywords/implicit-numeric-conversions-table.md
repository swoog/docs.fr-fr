---
title: Tableau des conversions numériques implicites - Référence C#
ms.custom: seodec18
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: ab6506e619c675ddd68237c4ddca870e9e14098f
ms.sourcegitcommit: deb9225a55485a5a6e6c7914deb30ccfceb69d3f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2019
ms.locfileid: "54058462"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="a83a6-102">Tableau des conversions numériques implicites (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a83a6-102">Implicit numeric conversions table (C# Reference)</span></span>

<span data-ttu-id="a83a6-103">Le tableau suivant montre les conversions implicites prédéfinies entre les types numériques .NET.</span><span class="sxs-lookup"><span data-stu-id="a83a6-103">The following table shows the predefined implicit conversions between .NET numeric types.</span></span>
  
|<span data-ttu-id="a83a6-104">From</span><span class="sxs-lookup"><span data-stu-id="a83a6-104">From</span></span>|<span data-ttu-id="a83a6-105">À</span><span class="sxs-lookup"><span data-stu-id="a83a6-105">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="a83a6-106">sbyte</span><span class="sxs-lookup"><span data-stu-id="a83a6-106">sbyte</span></span>](sbyte.md)|<span data-ttu-id="a83a6-107">`short`, `int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-107">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-108">byte</span><span class="sxs-lookup"><span data-stu-id="a83a6-108">byte</span></span>](byte.md)|<span data-ttu-id="a83a6-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-110">char</span><span class="sxs-lookup"><span data-stu-id="a83a6-110">char</span></span>](char.md)|<span data-ttu-id="a83a6-111">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-111">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-112">short</span><span class="sxs-lookup"><span data-stu-id="a83a6-112">short</span></span>](short.md)|<span data-ttu-id="a83a6-113">`int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-113">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-114">ushort</span><span class="sxs-lookup"><span data-stu-id="a83a6-114">ushort</span></span>](ushort.md)|<span data-ttu-id="a83a6-115">`int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-115">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-116">int</span><span class="sxs-lookup"><span data-stu-id="a83a6-116">int</span></span>](int.md)|<span data-ttu-id="a83a6-117">`long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-117">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-118">uint</span><span class="sxs-lookup"><span data-stu-id="a83a6-118">uint</span></span>](uint.md)|<span data-ttu-id="a83a6-119">`long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-119">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-120">long</span><span class="sxs-lookup"><span data-stu-id="a83a6-120">long</span></span>](long.md)|<span data-ttu-id="a83a6-121">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-121">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-122">ulong</span><span class="sxs-lookup"><span data-stu-id="a83a6-122">ulong</span></span>](ulong.md)|<span data-ttu-id="a83a6-123">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="a83a6-123">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="a83a6-124">float</span><span class="sxs-lookup"><span data-stu-id="a83a6-124">float</span></span>](float.md)|`double`|  
  
## <a name="remarks"></a><span data-ttu-id="a83a6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a83a6-125">Remarks</span></span>  

- <span data-ttu-id="a83a6-126">Un [type intégral](integral-types-table.md) est implicitement convertible en [type à virgule flottante](floating-point-types-table.md).</span><span class="sxs-lookup"><span data-stu-id="a83a6-126">Any [integral type](integral-types-table.md) is implicitly convertible to any [floating-point type](floating-point-types-table.md).</span></span>

- <span data-ttu-id="a83a6-127">La précision, et non la magnitude, peut être perdue dans les conversions de `int`, `uint`, `long` ou `ulong` à `float`, et de `long` ou `ulong` à `double`.</span><span class="sxs-lookup"><span data-stu-id="a83a6-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`, `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
- <span data-ttu-id="a83a6-128">Il n’existe aucune conversion implicite vers les types `char`, `byte` et `sbyte`.</span><span class="sxs-lookup"><span data-stu-id="a83a6-128">There are no implicit conversions to the `char`, `byte` and `sbyte` types.</span></span>  

- <span data-ttu-id="a83a6-129">Il n’existe aucune conversion implicite à partir des types `char`, `double` et `decimal`.</span><span class="sxs-lookup"><span data-stu-id="a83a6-129">There are no implicit conversions from the `char`, `double` and `decimal` types.</span></span>
  
- <span data-ttu-id="a83a6-130">Il n’existe aucune conversion implicite entre le type `decimal` et le type `float` ou `double`.</span><span class="sxs-lookup"><span data-stu-id="a83a6-130">There are no implicit conversions between the `decimal` type and the `float` or `double` types.</span></span>  
  
- <span data-ttu-id="a83a6-131">La valeur d’une expression constante de type `int` (par exemple, une valeur représentée par un littéral intégral) peut être convertie en `sbyte`, `byte`, `short`, `ushort`, `uint` ou `ulong`, à condition qu’elle se trouve dans la plage du type de destination :</span><span class="sxs-lookup"><span data-stu-id="a83a6-131">A value of a constant expression of type `int` (for example, a value represented by an integral literal) can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided it's within the range of the destination type:</span></span>

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

<span data-ttu-id="a83a6-132">Pour plus d’informations sur les conversions implicites, consultez la section [Conversions implicites](~/_csharplang/spec/conversions.md#implicit-conversions) de la [Spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="a83a6-132">For more information about implicit conversions, see the [Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions) section of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a83a6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a83a6-133">See also</span></span>

- [<span data-ttu-id="a83a6-134">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a83a6-134">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a83a6-135">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a83a6-135">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a83a6-136">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="a83a6-136">Integral types table</span></span>](integral-types-table.md)
- [<span data-ttu-id="a83a6-137">Tableau des types à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="a83a6-137">Floating-point types table</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="a83a6-138">Tableaux des types intégrés</span><span class="sxs-lookup"><span data-stu-id="a83a6-138">Built-in types table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="a83a6-139">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="a83a6-139">Explicit numeric conversions table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="a83a6-140">Cast et conversions de types</span><span class="sxs-lookup"><span data-stu-id="a83a6-140">Casting and type conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
