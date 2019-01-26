---
title: Tableaux - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#]
- C# language, arrays
ms.assetid: bb79bdde-e570-4c30-adb0-1dd5759ae041
ms.openlocfilehash: 1b1a3d2e61507a497349deeb857e4333356f66a5
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857799"
---
# <a name="arrays-c-programming-guide"></a><span data-ttu-id="e3ba4-102">Tableaux (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="e3ba4-102">Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="e3ba4-103">Vous pouvez stocker plusieurs variables du même type dans une structure de données de type tableau.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-103">You can store multiple variables of the same type in an array data structure.</span></span> <span data-ttu-id="e3ba4-104">Vous déclarez un tableau en spécifiant le type de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-104">You declare an array by specifying the type of its elements.</span></span>  
  
 `type[] arrayName;`  
  
 <span data-ttu-id="e3ba4-105">L’exemple suivant crée des tableaux unidimensionnels, multidimensionnels et en escalier :</span><span class="sxs-lookup"><span data-stu-id="e3ba4-105">The following example creates single-dimensional, multidimensional, and jagged arrays:</span></span>  
  
 [!code-csharp[csProgGuideArrays#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#1)]  
  
## <a name="array-overview"></a><span data-ttu-id="e3ba4-106">Vue d’ensemble du tableau</span><span class="sxs-lookup"><span data-stu-id="e3ba4-106">Array Overview</span></span>

 <span data-ttu-id="e3ba4-107">Un tableau possède les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3ba4-107">An array has the following properties:</span></span>  
  
-   <span data-ttu-id="e3ba4-108">Un tableau peut être [unidimensionnel](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [multidimensionnel](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) ou [en escalier](../../../csharp/programming-guide/arrays/jagged-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="e3ba4-108">An array can be [Single-Dimensional](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md), [Multidimensional](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) or [Jagged](../../../csharp/programming-guide/arrays/jagged-arrays.md).</span></span>  
  
-   <span data-ttu-id="e3ba4-109">Le nombre de dimensions et la longueur de chaque dimension sont établis lors de la création de l’instance de tableau.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-109">The number of dimensions and the length of each dimension are established when the array instance is created.</span></span> <span data-ttu-id="e3ba4-110">Ces valeurs ne peuvent pas être modifiées pendant la durée de vie de l’instance.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-110">These values can't be changed during the lifetime of the instance.</span></span>  
  
-   <span data-ttu-id="e3ba4-111">Les valeurs par défaut des éléments de tableau numériques sont définies sur zéro et les éléments de référence sont définis sur Null.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-111">The default values of numeric array elements are set to zero, and reference elements are set to null.</span></span>  
  
-   <span data-ttu-id="e3ba4-112">Un tableau en escalier est un tableau de tableaux, et par conséquent ses éléments sont des types référence et sont initialisés sur `null`.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-112">A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.</span></span>  
  
-   <span data-ttu-id="e3ba4-113">Les tableaux sont indexés sur zéro : un tableau avec `n` éléments est indexée de `0` à `n-1`.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-113">Arrays are zero indexed: an array with `n` elements is indexed from `0` to `n-1`.</span></span>  
  
-   <span data-ttu-id="e3ba4-114">Les éléments de tableau peuvent être de n’importe quel type, y compris un type tableau.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-114">Array elements can be of any type, including an array type.</span></span>  
  
-   <span data-ttu-id="e3ba4-115">Les types tableau sont des [types référence](../../../csharp/language-reference/keywords/reference-types.md) dérivés du type de base abstrait <xref:System.Array>.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-115">Array types are [reference types](../../../csharp/language-reference/keywords/reference-types.md) derived from the abstract base type <xref:System.Array>.</span></span> <span data-ttu-id="e3ba4-116">Étant donné que ce type implémente <xref:System.Collections.IEnumerable> et <xref:System.Collections.Generic.IEnumerable%601>, vous pouvez utiliser l’itération [foreach](../../../csharp/language-reference/keywords/foreach-in.md) sur tous les tableaux en C#.</span><span class="sxs-lookup"><span data-stu-id="e3ba4-116">Since this type implements <xref:System.Collections.IEnumerable> and <xref:System.Collections.Generic.IEnumerable%601>, you can use [foreach](../../../csharp/language-reference/keywords/foreach-in.md) iteration on all arrays in C#.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="e3ba4-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3ba4-117">Related Sections</span></span>  
  
-   [<span data-ttu-id="e3ba4-118">Tableaux comme objets</span><span class="sxs-lookup"><span data-stu-id="e3ba4-118">Arrays as Objects</span></span>](../../../csharp/programming-guide/arrays/arrays-as-objects.md)  
  
-   [<span data-ttu-id="e3ba4-119">Utilisation de foreach avec des tableaux</span><span class="sxs-lookup"><span data-stu-id="e3ba4-119">Using foreach with Arrays</span></span>](../../../csharp/programming-guide/arrays/using-foreach-with-arrays.md)  
  
-   [<span data-ttu-id="e3ba4-120">Passage de tableaux en tant qu’arguments</span><span class="sxs-lookup"><span data-stu-id="e3ba4-120">Passing Arrays as Arguments</span></span>](../../../csharp/programming-guide/arrays/passing-arrays-as-arguments.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="e3ba4-121">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="e3ba4-121">C# Language Specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e3ba4-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ba4-122">See also</span></span>

- [<span data-ttu-id="e3ba4-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e3ba4-123">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="e3ba4-124">Collections</span><span class="sxs-lookup"><span data-stu-id="e3ba4-124">Collections</span></span>](../../../csharp/programming-guide/concepts/collections.md)
