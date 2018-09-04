---
title: Tableaux (guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#]
- C# language, arrays
ms.assetid: bb79bdde-e570-4c30-adb0-1dd5759ae041
ms.openlocfilehash: 1469336bf034fd22c9d7355b2f8dd8be32721fdf
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510636"
---
# <a name="arrays-c-programming-guide"></a><span data-ttu-id="04a33-102">Tableaux (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="04a33-102">Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="04a33-103">Vous pouvez stocker plusieurs variables du même type dans une structure de données de type tableau.</span><span class="sxs-lookup"><span data-stu-id="04a33-103">You can store multiple variables of the same type in an array data structure.</span></span> <span data-ttu-id="04a33-104">Vous déclarez un tableau en spécifiant le type de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="04a33-104">You declare an array by specifying the type of its elements.</span></span>  
  
 `type[] arrayName;`  
  
 <span data-ttu-id="04a33-105">Les exemples suivants créent des tableaux unidimensionnels, multidimensionnels et en escalier :</span><span class="sxs-lookup"><span data-stu-id="04a33-105">The following examples create single-dimensional, multidimensional, and jagged arrays:</span></span>  
  
 [!code-csharp[csProgGuideArrays#1](../../../csharp/programming-guide/arrays/codesnippet/CSharp/index_1.cs)]  
  
## <a name="array-overview"></a><span data-ttu-id="04a33-106">Vue d’ensemble du tableau</span><span class="sxs-lookup"><span data-stu-id="04a33-106">Array Overview</span></span>

 <span data-ttu-id="04a33-107">Un tableau possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="04a33-107">An array has the following properties:</span></span>  
  
-   <span data-ttu-id="04a33-108">Un tableau peut être [unidimensionnel](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [multidimensionnel](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) ou [en escalier](../../../csharp/programming-guide/arrays/jagged-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="04a33-108">An array can be [Single-Dimensional](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [Multidimensional](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) or [Jagged](../../../csharp/programming-guide/arrays/jagged-arrays.md).</span></span>  
  
-   <span data-ttu-id="04a33-109">Le nombre de dimensions et la longueur de chaque dimension sont établis lors de la création de l’instance de tableau.</span><span class="sxs-lookup"><span data-stu-id="04a33-109">The number of dimensions and the length of each dimension are established when the array instance is created.</span></span> <span data-ttu-id="04a33-110">Ces valeurs ne peuvent pas être modifiées pendant la durée de vie de l’instance.</span><span class="sxs-lookup"><span data-stu-id="04a33-110">These values can't be changed during the lifetime of the instance.</span></span>  
  
-   <span data-ttu-id="04a33-111">Les valeurs par défaut des éléments de tableau numériques sont définies sur zéro et les éléments de référence sont définis sur Null.</span><span class="sxs-lookup"><span data-stu-id="04a33-111">The default values of numeric array elements are set to zero, and reference elements are set to null.</span></span>  
  
-   <span data-ttu-id="04a33-112">Un tableau en escalier est un tableau de tableaux, et par conséquent ses éléments sont des types référence et sont initialisés sur `null`.</span><span class="sxs-lookup"><span data-stu-id="04a33-112">A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.</span></span>  
  
-   <span data-ttu-id="04a33-113">Les tableaux sont indexés sur zéro : un tableau avec `n` éléments est indexée de `0` à `n-1`.</span><span class="sxs-lookup"><span data-stu-id="04a33-113">Arrays are zero indexed: an array with `n` elements is indexed from `0` to `n-1`.</span></span>  
  
-   <span data-ttu-id="04a33-114">Les éléments de tableau peuvent être de n’importe quel type, y compris un type tableau.</span><span class="sxs-lookup"><span data-stu-id="04a33-114">Array elements can be of any type, including an array type.</span></span>  
  
-   <span data-ttu-id="04a33-115">Les types tableau sont des [types référence](../../../csharp/language-reference/keywords/reference-types.md) dérivés du type de base abstrait <xref:System.Array>.</span><span class="sxs-lookup"><span data-stu-id="04a33-115">Array types are [reference types](../../../csharp/language-reference/keywords/reference-types.md) derived from the abstract base type <xref:System.Array>.</span></span> <span data-ttu-id="04a33-116">Étant donné que ce type implémente <xref:System.Collections.IEnumerable> et <xref:System.Collections.Generic.IEnumerable%601>, vous pouvez utiliser l’itération [foreach](../../../csharp/language-reference/keywords/foreach-in.md) sur tous les tableaux en C#.</span><span class="sxs-lookup"><span data-stu-id="04a33-116">Since this type implements <xref:System.Collections.IEnumerable> and <xref:System.Collections.Generic.IEnumerable%601>, you can use [foreach](../../../csharp/language-reference/keywords/foreach-in.md) iteration on all arrays in C#.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="04a33-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04a33-117">Related Sections</span></span>  
  
-   [<span data-ttu-id="04a33-118">Tableaux comme objets</span><span class="sxs-lookup"><span data-stu-id="04a33-118">Arrays as Objects</span></span>](../../../csharp/programming-guide/arrays/arrays-as-objects.md)  
  
-   [<span data-ttu-id="04a33-119">Utilisation de foreach avec des tableaux</span><span class="sxs-lookup"><span data-stu-id="04a33-119">Using foreach with Arrays</span></span>](../../../csharp/programming-guide/arrays/using-foreach-with-arrays.md)  
  
-   [<span data-ttu-id="04a33-120">Passage de tableaux en tant qu’arguments</span><span class="sxs-lookup"><span data-stu-id="04a33-120">Passing Arrays as Arguments</span></span>](../../../csharp/programming-guide/arrays/passing-arrays-as-arguments.md)  
  
-   [<span data-ttu-id="04a33-121">Passage de tableaux à l’aide de paramètres ref et out</span><span class="sxs-lookup"><span data-stu-id="04a33-121">Passing Arrays Using ref and out</span></span>](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md)   
  
## <a name="c-language-specification"></a><span data-ttu-id="04a33-122">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="04a33-122">C# Language Specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="04a33-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04a33-123">See Also</span></span>

- [<span data-ttu-id="04a33-124">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="04a33-124">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="04a33-125">Collections</span><span class="sxs-lookup"><span data-stu-id="04a33-125">Collections</span></span>](https://msdn.microsoft.com/library/e76533a9-5033-4a0b-b003-9c2be60d185b)  
- [<span data-ttu-id="04a33-126">Type de collection Array</span><span class="sxs-lookup"><span data-stu-id="04a33-126">Array Collection Type</span></span>](https://msdn.microsoft.com/library/8a9964de-8941-47b1-a3cf-a01bc88db9e8)
