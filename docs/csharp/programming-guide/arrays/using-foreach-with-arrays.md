---
title: Utiliser foreach avec des tableaux - Guide de programmation C#
ms.custom: seodec18
ms.date: 05/23/2018
helpviewer_keywords:
- arrays [C#], foreach
- foreach statement [C#], using with arrays
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
ms.openlocfilehash: a22cb939370b38780881eca0d9585a14002c8250
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966409"
---
# <a name="using-foreach-with-arrays-c-programming-guide"></a><span data-ttu-id="5efde-102">Utiliser foreach avec des tableaux (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="5efde-102">Using foreach with arrays (C# Programming Guide)</span></span>

<span data-ttu-id="5efde-103">L’instruction [foreach](../../language-reference/keywords/foreach-in.md) offre une méthode simple et appropriée pour itérer au sein des éléments d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="5efde-103">The [foreach](../../language-reference/keywords/foreach-in.md) statement provides a simple, clean way to iterate through the elements of an array.</span></span>

<span data-ttu-id="5efde-104">Pour les tableaux unidimensionnels, l’instruction `foreach` traite les éléments dans l’ordre croissant des index, en commençant par l’index 0 et en terminant par l’index `Length - 1` :</span><span class="sxs-lookup"><span data-stu-id="5efde-104">For single-dimensional arrays, the `foreach` statement processes elements in increasing index order, starting with index 0 and ending with index `Length - 1`:</span></span>

 [!code-csharp[csProgGuideArrays#28](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#28)]

<span data-ttu-id="5efde-105">Pour les tableaux multidimensionnels, les éléments sont traités de sorte que les index de la dimension la plus à droite sont incrémentés en premier, puis la dimension immédiatement à gauche, et ainsi de suite vers la gauche :</span><span class="sxs-lookup"><span data-stu-id="5efde-105">For multi-dimensional arrays, elements are traversed such that the indices of the rightmost dimension are increased first, then the next left dimension, and so on to the left:</span></span>

 [!code-csharp[csProgGuideArrays#29](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#29)]

<span data-ttu-id="5efde-106">Cependant, dans le cas de tableaux multidimensionnels, l’utilisation d’une boucle [for](../../language-reference/keywords/for.md) imbriquée vous permet de mieux contrôler l’ordre dans lequel les éléments du tableau sont traités.</span><span class="sxs-lookup"><span data-stu-id="5efde-106">However, with multidimensional arrays, using a nested [for](../../language-reference/keywords/for.md) loop gives you more control over the order in which to process the array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="5efde-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5efde-107">See also</span></span>

- <xref:System.Array>
- [<span data-ttu-id="5efde-108">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5efde-108">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="5efde-109">Tableaux</span><span class="sxs-lookup"><span data-stu-id="5efde-109">Arrays</span></span>](index.md)
- [<span data-ttu-id="5efde-110">Tableaux unidimensionnels</span><span class="sxs-lookup"><span data-stu-id="5efde-110">Single-Dimensional Arrays</span></span>](single-dimensional-arrays.md)
- [<span data-ttu-id="5efde-111">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="5efde-111">Multidimensional Arrays</span></span>](multidimensional-arrays.md)
- [<span data-ttu-id="5efde-112">Tableaux en escalier</span><span class="sxs-lookup"><span data-stu-id="5efde-112">Jagged Arrays</span></span>](jagged-arrays.md)
