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
ms.openlocfilehash: 703f60f48e1e569e0ffcab66ff7ccc91d4a49514
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093552"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="88664-102">Tableau des conversions numériques implicites (référence C#)</span><span class="sxs-lookup"><span data-stu-id="88664-102">Implicit numeric conversions table (C# Reference)</span></span>

<span data-ttu-id="88664-103">Le tableau suivant montre les conversions implicites prédéfinies entre les types numériques .NET.</span><span class="sxs-lookup"><span data-stu-id="88664-103">The following table shows the predefined implicit conversions between .NET numeric types.</span></span>
  
|<span data-ttu-id="88664-104">From</span><span class="sxs-lookup"><span data-stu-id="88664-104">From</span></span>|<span data-ttu-id="88664-105">À</span><span class="sxs-lookup"><span data-stu-id="88664-105">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="88664-106">sbyte</span><span class="sxs-lookup"><span data-stu-id="88664-106">sbyte</span></span>](sbyte.md)|<span data-ttu-id="88664-107">`short`, `int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-107">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-108">byte</span><span class="sxs-lookup"><span data-stu-id="88664-108">byte</span></span>](byte.md)|<span data-ttu-id="88664-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-109">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-110">char</span><span class="sxs-lookup"><span data-stu-id="88664-110">char</span></span>](char.md)|<span data-ttu-id="88664-111">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-111">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-112">short</span><span class="sxs-lookup"><span data-stu-id="88664-112">short</span></span>](short.md)|<span data-ttu-id="88664-113">`int`, `long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-113">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-114">ushort</span><span class="sxs-lookup"><span data-stu-id="88664-114">ushort</span></span>](ushort.md)|<span data-ttu-id="88664-115">`int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-115">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-116">int</span><span class="sxs-lookup"><span data-stu-id="88664-116">int</span></span>](int.md)|<span data-ttu-id="88664-117">`long`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-117">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-118">uint</span><span class="sxs-lookup"><span data-stu-id="88664-118">uint</span></span>](uint.md)|<span data-ttu-id="88664-119">`long`, `ulong`, `float`, `double` ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-119">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-120">long</span><span class="sxs-lookup"><span data-stu-id="88664-120">long</span></span>](long.md)|<span data-ttu-id="88664-121">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-121">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-122">ulong</span><span class="sxs-lookup"><span data-stu-id="88664-122">ulong</span></span>](ulong.md)|<span data-ttu-id="88664-123">`float`, `double`ou `decimal`</span><span class="sxs-lookup"><span data-stu-id="88664-123">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="88664-124">float</span><span class="sxs-lookup"><span data-stu-id="88664-124">float</span></span>](float.md)|`double`|  
  
## <a name="remarks"></a><span data-ttu-id="88664-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="88664-125">Remarks</span></span>  

- <span data-ttu-id="88664-126">Un [type intégral](integral-types-table.md) est implicitement convertible en [type à virgule flottante](floating-point-types-table.md).</span><span class="sxs-lookup"><span data-stu-id="88664-126">Any [integral type](integral-types-table.md) is implicitly convertible to any [floating-point type](floating-point-types-table.md).</span></span>

- <span data-ttu-id="88664-127">La précision, et non la magnitude, peut être perdue dans les conversions de `int`, `uint`, `long` ou `ulong` à `float`, et de `long` ou `ulong` à `double`.</span><span class="sxs-lookup"><span data-stu-id="88664-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`, `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
- <span data-ttu-id="88664-128">Il n’existe aucune conversion implicite vers les types `char`, `byte` et `sbyte`.</span><span class="sxs-lookup"><span data-stu-id="88664-128">There are no implicit conversions to the `char`, `byte`, and `sbyte` types.</span></span>  

- <span data-ttu-id="88664-129">Il n’existe aucune conversion implicite à partir des types `double` et `decimal`.</span><span class="sxs-lookup"><span data-stu-id="88664-129">There are no implicit conversions from the `double` and `decimal` types.</span></span>
  
- <span data-ttu-id="88664-130">Il n’existe aucune conversion implicite entre le type `decimal` et le type `float` ou `double`.</span><span class="sxs-lookup"><span data-stu-id="88664-130">There are no implicit conversions between the `decimal` type and the `float` or `double` types.</span></span>  
  
- <span data-ttu-id="88664-131">La valeur d’une expression constante de type `int` (par exemple, une valeur représentée par un littéral intégral) peut être convertie en `sbyte`, `byte`, `short`, `ushort`, `uint` ou `ulong`, à condition qu’elle se trouve dans la plage du type de destination :</span><span class="sxs-lookup"><span data-stu-id="88664-131">A value of a constant expression of type `int` (for example, a value represented by an integral literal) can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided it's within the range of the destination type:</span></span>

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

<span data-ttu-id="88664-132">Pour plus d’informations sur les conversions implicites, consultez la section [Conversions implicites](~/_csharplang/spec/conversions.md#implicit-conversions) de la [Spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="88664-132">For more information about implicit conversions, see the [Implicit conversions](~/_csharplang/spec/conversions.md#implicit-conversions) section of the [C# language specification](../language-specification/index.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88664-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88664-133">See also</span></span>

- [<span data-ttu-id="88664-134">Référence C#</span><span class="sxs-lookup"><span data-stu-id="88664-134">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="88664-135">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="88664-135">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="88664-136">Tableau des types intégraux</span><span class="sxs-lookup"><span data-stu-id="88664-136">Integral types table</span></span>](integral-types-table.md)
- [<span data-ttu-id="88664-137">Tableau des types à virgule flottante</span><span class="sxs-lookup"><span data-stu-id="88664-137">Floating-point types table</span></span>](floating-point-types-table.md)
- [<span data-ttu-id="88664-138">Tableaux des types intégrés</span><span class="sxs-lookup"><span data-stu-id="88664-138">Built-in types table</span></span>](built-in-types-table.md)
- [<span data-ttu-id="88664-139">Tableau des conversions numériques explicites</span><span class="sxs-lookup"><span data-stu-id="88664-139">Explicit numeric conversions table</span></span>](explicit-numeric-conversions-table.md)
- [<span data-ttu-id="88664-140">Cast et conversions de types</span><span class="sxs-lookup"><span data-stu-id="88664-140">Casting and type conversions</span></span>](../../programming-guide/types/casting-and-type-conversions.md)
