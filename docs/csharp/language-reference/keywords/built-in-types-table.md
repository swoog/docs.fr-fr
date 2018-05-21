---
title: Tableau des types intégrés (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- types [C#], built-in
- built-in C# types
ms.assetid: 54f901f2-bf2f-472c-ae8d-73e8ecfc57fe
ms.openlocfilehash: 120347e5bff7f0d6c7120af0cb250936ca39ea16
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
---
# <a name="built-in-types-table-c-reference"></a><span data-ttu-id="1948a-102">Tableau des types intégrés (référence C#)</span><span class="sxs-lookup"><span data-stu-id="1948a-102">Built-In Types Table (C# Reference)</span></span>
<span data-ttu-id="1948a-103">Le tableau suivant liste les mots clés des types C# intégrés, qui sont des alias des types prédéfinis de l’espace de noms <xref:System>.</span><span class="sxs-lookup"><span data-stu-id="1948a-103">The following table shows the keywords for built-in C# types, which are aliases of predefined types in the <xref:System> namespace.</span></span>  
  
|<span data-ttu-id="1948a-104">Type C#</span><span class="sxs-lookup"><span data-stu-id="1948a-104">C# Type</span></span>|<span data-ttu-id="1948a-105">Type .NET Framework</span><span class="sxs-lookup"><span data-stu-id="1948a-105">.NET Framework Type</span></span>|  
|--------------|-------------------------|  
|[<span data-ttu-id="1948a-106">bool</span><span class="sxs-lookup"><span data-stu-id="1948a-106">bool</span></span>](../../../csharp/language-reference/keywords/bool.md)|`System.Boolean`|  
|[<span data-ttu-id="1948a-107">byte</span><span class="sxs-lookup"><span data-stu-id="1948a-107">byte</span></span>](../../../csharp/language-reference/keywords/byte.md)|`System.Byte`|  
|[<span data-ttu-id="1948a-108">sbyte</span><span class="sxs-lookup"><span data-stu-id="1948a-108">sbyte</span></span>](../../../csharp/language-reference/keywords/sbyte.md)|`System.SByte`|  
|[<span data-ttu-id="1948a-109">char</span><span class="sxs-lookup"><span data-stu-id="1948a-109">char</span></span>](../../../csharp/language-reference/keywords/char.md)|`System.Char`|  
|[<span data-ttu-id="1948a-110">decimal</span><span class="sxs-lookup"><span data-stu-id="1948a-110">decimal</span></span>](../../../csharp/language-reference/keywords/decimal.md)|`System.Decimal`|  
|[<span data-ttu-id="1948a-111">double</span><span class="sxs-lookup"><span data-stu-id="1948a-111">double</span></span>](../../../csharp/language-reference/keywords/double.md)|`System.Double`|  
|[<span data-ttu-id="1948a-112">float</span><span class="sxs-lookup"><span data-stu-id="1948a-112">float</span></span>](../../../csharp/language-reference/keywords/float.md)|`System.Single`|  
|[<span data-ttu-id="1948a-113">int</span><span class="sxs-lookup"><span data-stu-id="1948a-113">int</span></span>](../../../csharp/language-reference/keywords/int.md)|`System.Int32`|  
|[<span data-ttu-id="1948a-114">uint</span><span class="sxs-lookup"><span data-stu-id="1948a-114">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)|`System.UInt32`|  
|[<span data-ttu-id="1948a-115">long</span><span class="sxs-lookup"><span data-stu-id="1948a-115">long</span></span>](../../../csharp/language-reference/keywords/long.md)|`System.Int64`|  
|[<span data-ttu-id="1948a-116">ulong</span><span class="sxs-lookup"><span data-stu-id="1948a-116">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md)|`System.UInt64`|  
|[<span data-ttu-id="1948a-117">object</span><span class="sxs-lookup"><span data-stu-id="1948a-117">object</span></span>](../../../csharp/language-reference/keywords/object.md)|`System.Object`|  
|[<span data-ttu-id="1948a-118">short</span><span class="sxs-lookup"><span data-stu-id="1948a-118">short</span></span>](../../../csharp/language-reference/keywords/short.md)|`System.Int16`|  
|[<span data-ttu-id="1948a-119">ushort</span><span class="sxs-lookup"><span data-stu-id="1948a-119">ushort</span></span>](../../../csharp/language-reference/keywords/ushort.md)|`System.UInt16`|  
|[<span data-ttu-id="1948a-120">string</span><span class="sxs-lookup"><span data-stu-id="1948a-120">string</span></span>](../../../csharp/language-reference/keywords/string.md)|`System.String`|  
  
## <a name="remarks"></a><span data-ttu-id="1948a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1948a-121">Remarks</span></span>  
 <span data-ttu-id="1948a-122">Hormis les types `object` et `string`, tous les types listés dans le tableau sont considérés comme des types simples.</span><span class="sxs-lookup"><span data-stu-id="1948a-122">All of the types in the table, except `object` and `string`, are referred to as simple types.</span></span>  
  
 <span data-ttu-id="1948a-123">Les mots clés des types C# et leurs alias sont interchangeables.</span><span class="sxs-lookup"><span data-stu-id="1948a-123">The C# type keywords and their aliases are interchangeable.</span></span> <span data-ttu-id="1948a-124">Par exemple, vous pouvez déclarer une variable de type entier à l’aide de l’une des deux déclarations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1948a-124">For example, you can declare an integer variable by using either of the following declarations:</span></span>  
  
```csharp  
int x = 123;  
System.Int32 x = 123;  
```  
  
 <span data-ttu-id="1948a-125">Pour afficher le type réel d’un type C#, utilisez la méthode système `GetType()`.</span><span class="sxs-lookup"><span data-stu-id="1948a-125">To display the actual type for any C# type, use the system method `GetType()`.</span></span> <span data-ttu-id="1948a-126">Par exemple, l’instruction ci-après affiche l’alias système qui représente le type de `myVariable` :</span><span class="sxs-lookup"><span data-stu-id="1948a-126">For example, the following statement displays the system alias that represents the type of `myVariable`:</span></span>  
  
```csharp  
Console.WriteLine(myVariable.GetType());  
```  
  
 <span data-ttu-id="1948a-127">Vous pouvez également utiliser l’opérateur [typeof](../../../csharp/language-reference/keywords/typeof.md).</span><span class="sxs-lookup"><span data-stu-id="1948a-127">You can also use the [typeof](../../../csharp/language-reference/keywords/typeof.md) operator.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1948a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1948a-128">See Also</span></span>  
 [<span data-ttu-id="1948a-129">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1948a-129">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="1948a-130">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1948a-130">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="1948a-131">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="1948a-131">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="1948a-132">Types valeur</span><span class="sxs-lookup"><span data-stu-id="1948a-132">Value Types</span></span>](../../../csharp/language-reference/keywords/value-types.md)  
 [<span data-ttu-id="1948a-133">Tableau des valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="1948a-133">Default Values Table</span></span>](../../../csharp/language-reference/keywords/default-values-table.md)  
 [<span data-ttu-id="1948a-134">Tableau des formats des résultats numériques</span><span class="sxs-lookup"><span data-stu-id="1948a-134">Formatting Numeric Results Table</span></span>](../../../csharp/language-reference/keywords/formatting-numeric-results-table.md)  
 [<span data-ttu-id="1948a-135">dynamic</span><span class="sxs-lookup"><span data-stu-id="1948a-135">dynamic</span></span>](../../../csharp/language-reference/keywords/dynamic.md)  
 [<span data-ttu-id="1948a-136">Tableaux de référence des types</span><span class="sxs-lookup"><span data-stu-id="1948a-136">Reference Tables for Types</span></span>](../../../csharp/language-reference/keywords/reference-tables-for-types.md)
