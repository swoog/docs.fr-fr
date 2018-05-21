---
title: Tableau des valeurs par défaut (référence C#)
description: Découvrez les valeurs par défaut des types valeur qui sont retournées par les constructeurs par défaut.
ms.date: 07/20/2015
helpviewer_keywords:
- constructors [C#], return values
- keywords [C#], new
- default constructor [C#]
- defaults [C#]
- value types [C#], initializing
- variables [C#], value types
- constructors [C#], default constructor
- types [C#], default constructor return values
ms.openlocfilehash: 634a55304534b4269487f29be1fbb4930f51d8ca
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="default-values-table-c-reference"></a><span data-ttu-id="23d2a-103">Tableau des valeurs par défaut (référence C#)</span><span class="sxs-lookup"><span data-stu-id="23d2a-103">Default values table (C# Reference)</span></span>

<span data-ttu-id="23d2a-104">Le tableau suivant indique les valeurs par défaut de types valeur qui sont retournées par les constructeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="23d2a-104">The following table shows the default values of value types returned by the default constructors.</span></span> <span data-ttu-id="23d2a-105">Les constructeurs par défaut sont appelés au moyen de l’opérateur `new`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="23d2a-105">Default constructors are invoked by using the `new` operator, as follows:</span></span>

```csharp
int myInt = new int();
```

<span data-ttu-id="23d2a-106">L’instruction qui précède produit le même résultat que la suivante :</span><span class="sxs-lookup"><span data-stu-id="23d2a-106">The preceding statement has the same effect as the following statement:</span></span>

```csharp
int myInt = 0;
```

<span data-ttu-id="23d2a-107">Pour rappel, il n’est pas possible d’utiliser en C# des variables qui n’ont pas été initialisées.</span><span class="sxs-lookup"><span data-stu-id="23d2a-107">Remember that using uninitialized variables in C# is not allowed.</span></span>

|<span data-ttu-id="23d2a-108">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="23d2a-108">Value type</span></span>|<span data-ttu-id="23d2a-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="23d2a-109">Default value</span></span>|
|----------------|-------------------|
|[<span data-ttu-id="23d2a-110">bool</span><span class="sxs-lookup"><span data-stu-id="23d2a-110">bool</span></span>](bool.md)|`false`|
|[<span data-ttu-id="23d2a-111">byte</span><span class="sxs-lookup"><span data-stu-id="23d2a-111">byte</span></span>](byte.md)|<span data-ttu-id="23d2a-112">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-112">0</span></span>|
|[<span data-ttu-id="23d2a-113">char</span><span class="sxs-lookup"><span data-stu-id="23d2a-113">char</span></span>](char.md)|<span data-ttu-id="23d2a-114">'\0'</span><span class="sxs-lookup"><span data-stu-id="23d2a-114">'\0'</span></span>|
|[<span data-ttu-id="23d2a-115">decimal</span><span class="sxs-lookup"><span data-stu-id="23d2a-115">decimal</span></span>](decimal.md)|<span data-ttu-id="23d2a-116">0M</span><span class="sxs-lookup"><span data-stu-id="23d2a-116">0M</span></span>|
|[<span data-ttu-id="23d2a-117">double</span><span class="sxs-lookup"><span data-stu-id="23d2a-117">double</span></span>](double.md)|<span data-ttu-id="23d2a-118">0.0D</span><span class="sxs-lookup"><span data-stu-id="23d2a-118">0.0D</span></span>|
|[<span data-ttu-id="23d2a-119">enum</span><span class="sxs-lookup"><span data-stu-id="23d2a-119">enum</span></span>](enum.md)|<span data-ttu-id="23d2a-120">Valeur produite par l’expression (E)0, où E est l’identificateur de l’enum.</span><span class="sxs-lookup"><span data-stu-id="23d2a-120">The value produced by the expression (E)0, where E is the enum identifier.</span></span>|
|[<span data-ttu-id="23d2a-121">float</span><span class="sxs-lookup"><span data-stu-id="23d2a-121">float</span></span>](float.md)|<span data-ttu-id="23d2a-122">0.0F</span><span class="sxs-lookup"><span data-stu-id="23d2a-122">0.0F</span></span>|
|[<span data-ttu-id="23d2a-123">int</span><span class="sxs-lookup"><span data-stu-id="23d2a-123">int</span></span>](int.md)|<span data-ttu-id="23d2a-124">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-124">0</span></span>|
|[<span data-ttu-id="23d2a-125">long</span><span class="sxs-lookup"><span data-stu-id="23d2a-125">long</span></span>](long.md)|<span data-ttu-id="23d2a-126">0L</span><span class="sxs-lookup"><span data-stu-id="23d2a-126">0L</span></span>|
|[<span data-ttu-id="23d2a-127">sbyte</span><span class="sxs-lookup"><span data-stu-id="23d2a-127">sbyte</span></span>](sbyte.md)|<span data-ttu-id="23d2a-128">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-128">0</span></span>|
|[<span data-ttu-id="23d2a-129">short</span><span class="sxs-lookup"><span data-stu-id="23d2a-129">short</span></span>](short.md)|<span data-ttu-id="23d2a-130">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-130">0</span></span>|
|[<span data-ttu-id="23d2a-131">struct</span><span class="sxs-lookup"><span data-stu-id="23d2a-131">struct</span></span>](struct.md)|<span data-ttu-id="23d2a-132">Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="23d2a-132">The value produced by setting all value-type fields to their default values and all reference-type fields to `null`.</span></span>|
|[<span data-ttu-id="23d2a-133">uint</span><span class="sxs-lookup"><span data-stu-id="23d2a-133">uint</span></span>](uint.md)|<span data-ttu-id="23d2a-134">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-134">0</span></span>|
|[<span data-ttu-id="23d2a-135">ulong</span><span class="sxs-lookup"><span data-stu-id="23d2a-135">ulong</span></span>](ulong.md)|<span data-ttu-id="23d2a-136">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-136">0</span></span>|
|[<span data-ttu-id="23d2a-137">ushort</span><span class="sxs-lookup"><span data-stu-id="23d2a-137">ushort</span></span>](ushort.md)|<span data-ttu-id="23d2a-138">0</span><span class="sxs-lookup"><span data-stu-id="23d2a-138">0</span></span>|

## <a name="see-also"></a><span data-ttu-id="23d2a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23d2a-139">See also</span></span>
 [<span data-ttu-id="23d2a-140">Référence C#</span><span class="sxs-lookup"><span data-stu-id="23d2a-140">C# Reference</span></span>](../index.md)  
 [<span data-ttu-id="23d2a-141">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="23d2a-141">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="23d2a-142">Tableau des types valeur</span><span class="sxs-lookup"><span data-stu-id="23d2a-142">Value Types Table</span></span>](value-types-table.md)  
 [<span data-ttu-id="23d2a-143">Types valeur</span><span class="sxs-lookup"><span data-stu-id="23d2a-143">Value Types</span></span>](value-types.md)  
 [<span data-ttu-id="23d2a-144">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="23d2a-144">Built-In Types Table</span></span>](built-in-types-table.md)  
 [<span data-ttu-id="23d2a-145">Tableaux de référence des types</span><span class="sxs-lookup"><span data-stu-id="23d2a-145">Reference Tables for Types</span></span>](reference-tables-for-types.md)
