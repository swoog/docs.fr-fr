---
title: Utilisation de foreach avec des tableaux (Guide de programmation C#)
ms.date: 05/23/2018
helpviewer_keywords:
- arrays [C#], foreach
- foreach statement [C#], using with arrays
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
ms.openlocfilehash: 298ee915bbe11313f3b33ea7dae9353ef956a231
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43509533"
---
# <a name="using-foreach-with-arrays-c-programming-guide"></a><span data-ttu-id="a1f57-102">Utilisation de foreach avec des tableaux (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="a1f57-102">Using foreach with Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="a1f57-103">L’instruction [foreach](../../language-reference/keywords/foreach-in.md) offre une méthode simple et appropriée pour itérer au sein des éléments d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="a1f57-103">The [foreach](../../language-reference/keywords/foreach-in.md) statement provides a simple, clean way to iterate through the elements of an array.</span></span>

<span data-ttu-id="a1f57-104">Pour les tableaux unidimensionnels, l’instruction `foreach` traite les éléments dans l’ordre croissant des index, en commençant par l’index 0 et en terminant par l’index `Length - 1` :</span><span class="sxs-lookup"><span data-stu-id="a1f57-104">For single-dimensional arrays, the `foreach` statement processes elements in increasing index order, starting with index 0 and ending with index `Length - 1`:</span></span>

[!code-csharp[csProgGuideArrays#28](./codesnippet/CSharp/using-foreach-with-arrays_1.cs)]

<span data-ttu-id="a1f57-105">Pour les tableaux multidimensionnels, les éléments sont traités de sorte que les index de la dimension la plus à droite sont incrémentés en premier, puis la dimension immédiatement à gauche, et ainsi de suite vers la gauche :</span><span class="sxs-lookup"><span data-stu-id="a1f57-105">For multi-dimensional arrays, elements are traversed such that the indices of the rightmost dimension are increased first, then the next left dimension, and so on to the left:</span></span>

[!code-csharp[csProgGuideArrays#29](./codesnippet/CSharp/using-foreach-with-arrays_2.cs)]

<span data-ttu-id="a1f57-106">Cependant, dans le cas de tableaux multidimensionnels, l’utilisation d’une boucle [for](../../language-reference/keywords/for.md) imbriquée vous permet de mieux contrôler l’ordre dans lequel les éléments du tableau sont traités.</span><span class="sxs-lookup"><span data-stu-id="a1f57-106">However, with multidimensional arrays, using a nested [for](../../language-reference/keywords/for.md) loop gives you more control over the order in which to process the array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1f57-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1f57-107">See Also</span></span>

- <xref:System.Array>  
- [<span data-ttu-id="a1f57-108">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a1f57-108">C# Programming Guide</span></span>](../index.md)  
- [<span data-ttu-id="a1f57-109">Tableaux</span><span class="sxs-lookup"><span data-stu-id="a1f57-109">Arrays</span></span>](index.md)  
- [<span data-ttu-id="a1f57-110">Tableaux unidimensionnels</span><span class="sxs-lookup"><span data-stu-id="a1f57-110">Single-Dimensional Arrays</span></span>](single-dimensional-arrays.md)  
- [<span data-ttu-id="a1f57-111">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="a1f57-111">Multidimensional Arrays</span></span>](multidimensional-arrays.md)  
- [<span data-ttu-id="a1f57-112">Tableaux en escalier</span><span class="sxs-lookup"><span data-stu-id="a1f57-112">Jagged Arrays</span></span>](jagged-arrays.md)
