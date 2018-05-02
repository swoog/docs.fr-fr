---
title: Tableau des valeurs par défaut (référence C#)
descripton: Learn what are the default values of value types returned by the default constructors.
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- constructors [C#], return values
- keywords [C#], new
- default constructor [C#]
- defaults [C#]
- value types [C#], initializing
- variables [C#], value types
- constructors [C#], default constructor
- types [C#], default constructor return values
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e249dd2f352fe6177f3afbfd089fc4dc9b1b7798
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="default-values-table-c-reference"></a><span data-ttu-id="903a1-102">Tableau des valeurs par défaut (référence C#)</span><span class="sxs-lookup"><span data-stu-id="903a1-102">Default values table (C# Reference)</span></span>

<span data-ttu-id="903a1-103">Le tableau suivant indique les valeurs par défaut de types valeur qui sont retournées par les constructeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="903a1-103">The following table shows the default values of value types returned by the default constructors.</span></span> <span data-ttu-id="903a1-104">Les constructeurs par défaut sont appelés au moyen de l’opérateur `new`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="903a1-104">Default constructors are invoked by using the `new` operator, as follows:</span></span>

```csharp
int myInt = new int();
```

<span data-ttu-id="903a1-105">L’instruction qui précède produit le même résultat que la suivante :</span><span class="sxs-lookup"><span data-stu-id="903a1-105">The preceding statement has the same effect as the following statement:</span></span>

```csharp
int myInt = 0;
```

<span data-ttu-id="903a1-106">Pour rappel, il n’est pas possible d’utiliser en C# des variables qui n’ont pas été initialisées.</span><span class="sxs-lookup"><span data-stu-id="903a1-106">Remember that using uninitialized variables in C# is not allowed.</span></span>

|<span data-ttu-id="903a1-107">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="903a1-107">Value type</span></span>|<span data-ttu-id="903a1-108">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="903a1-108">Default value</span></span>|
|----------------|-------------------|
|[<span data-ttu-id="903a1-109">bool</span><span class="sxs-lookup"><span data-stu-id="903a1-109">bool</span></span>](bool.md)|`false`|
|[<span data-ttu-id="903a1-110">byte</span><span class="sxs-lookup"><span data-stu-id="903a1-110">byte</span></span>](byte.md)|<span data-ttu-id="903a1-111">0</span><span class="sxs-lookup"><span data-stu-id="903a1-111">0</span></span>|
|[<span data-ttu-id="903a1-112">char</span><span class="sxs-lookup"><span data-stu-id="903a1-112">char</span></span>](char.md)|<span data-ttu-id="903a1-113">'\0'</span><span class="sxs-lookup"><span data-stu-id="903a1-113">'\0'</span></span>|
|[<span data-ttu-id="903a1-114">decimal</span><span class="sxs-lookup"><span data-stu-id="903a1-114">decimal</span></span>](decimal.md)|<span data-ttu-id="903a1-115">0M</span><span class="sxs-lookup"><span data-stu-id="903a1-115">0M</span></span>|
|[<span data-ttu-id="903a1-116">double</span><span class="sxs-lookup"><span data-stu-id="903a1-116">double</span></span>](double.md)|<span data-ttu-id="903a1-117">0.0D</span><span class="sxs-lookup"><span data-stu-id="903a1-117">0.0D</span></span>|
|[<span data-ttu-id="903a1-118">enum</span><span class="sxs-lookup"><span data-stu-id="903a1-118">enum</span></span>](enum.md)|<span data-ttu-id="903a1-119">Valeur produite par l’expression (E)0, où E est l’identificateur de l’enum.</span><span class="sxs-lookup"><span data-stu-id="903a1-119">The value produced by the expression (E)0, where E is the enum identifier.</span></span>|
|[<span data-ttu-id="903a1-120">float</span><span class="sxs-lookup"><span data-stu-id="903a1-120">float</span></span>](float.md)|<span data-ttu-id="903a1-121">0.0F</span><span class="sxs-lookup"><span data-stu-id="903a1-121">0.0F</span></span>|
|[<span data-ttu-id="903a1-122">int</span><span class="sxs-lookup"><span data-stu-id="903a1-122">int</span></span>](int.md)|<span data-ttu-id="903a1-123">0</span><span class="sxs-lookup"><span data-stu-id="903a1-123">0</span></span>|
|[<span data-ttu-id="903a1-124">long</span><span class="sxs-lookup"><span data-stu-id="903a1-124">long</span></span>](long.md)|<span data-ttu-id="903a1-125">0L</span><span class="sxs-lookup"><span data-stu-id="903a1-125">0L</span></span>|
|[<span data-ttu-id="903a1-126">sbyte</span><span class="sxs-lookup"><span data-stu-id="903a1-126">sbyte</span></span>](sbyte.md)|<span data-ttu-id="903a1-127">0</span><span class="sxs-lookup"><span data-stu-id="903a1-127">0</span></span>|
|[<span data-ttu-id="903a1-128">short</span><span class="sxs-lookup"><span data-stu-id="903a1-128">short</span></span>](short.md)|<span data-ttu-id="903a1-129">0</span><span class="sxs-lookup"><span data-stu-id="903a1-129">0</span></span>|
|[<span data-ttu-id="903a1-130">struct</span><span class="sxs-lookup"><span data-stu-id="903a1-130">struct</span></span>](struct.md)|<span data-ttu-id="903a1-131">Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="903a1-131">The value produced by setting all value-type fields to their default values and all reference-type fields to `null`.</span></span>|
|[<span data-ttu-id="903a1-132">uint</span><span class="sxs-lookup"><span data-stu-id="903a1-132">uint</span></span>](uint.md)|<span data-ttu-id="903a1-133">0</span><span class="sxs-lookup"><span data-stu-id="903a1-133">0</span></span>|
|[<span data-ttu-id="903a1-134">ulong</span><span class="sxs-lookup"><span data-stu-id="903a1-134">ulong</span></span>](ulong.md)|<span data-ttu-id="903a1-135">0</span><span class="sxs-lookup"><span data-stu-id="903a1-135">0</span></span>|
|[<span data-ttu-id="903a1-136">ushort</span><span class="sxs-lookup"><span data-stu-id="903a1-136">ushort</span></span>](ushort.md)|<span data-ttu-id="903a1-137">0</span><span class="sxs-lookup"><span data-stu-id="903a1-137">0</span></span>|

## <a name="see-also"></a><span data-ttu-id="903a1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="903a1-138">See also</span></span>
 [<span data-ttu-id="903a1-139">Référence C#</span><span class="sxs-lookup"><span data-stu-id="903a1-139">C# Reference</span></span>](../index.md)  
 [<span data-ttu-id="903a1-140">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="903a1-140">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="903a1-141">Tableau des types valeur</span><span class="sxs-lookup"><span data-stu-id="903a1-141">Value Types Table</span></span>](value-types-table.md)  
 [<span data-ttu-id="903a1-142">Types valeur</span><span class="sxs-lookup"><span data-stu-id="903a1-142">Value Types</span></span>](value-types.md)  
 [<span data-ttu-id="903a1-143">Tableau des types intégrés</span><span class="sxs-lookup"><span data-stu-id="903a1-143">Built-In Types Table</span></span>](built-in-types-table.md)  
 [<span data-ttu-id="903a1-144">Tableaux de référence des types</span><span class="sxs-lookup"><span data-stu-id="903a1-144">Reference Tables for Types</span></span>](reference-tables-for-types.md)
