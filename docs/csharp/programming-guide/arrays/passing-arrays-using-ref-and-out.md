---
title: Passage de tableaux à l'aide de paramètres ref et out (guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [C#], passing using ref and out
ms.assetid: 6a2b261e-a1cc-49a6-b4f0-6cacae385a1e
ms.openlocfilehash: a186399125e01bb2535f3a8b488c6fbd85932246
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33313568"
---
# <a name="passing-arrays-using-ref-and-out-c-programming-guide"></a><span data-ttu-id="b23d7-102">Passage de tableaux à l'aide de paramètres ref et out (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b23d7-102">Passing Arrays Using ref and out (C# Programming Guide)</span></span>
<span data-ttu-id="b23d7-103">Comme tous les paramètres [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), un paramètre `out` d’un type tableau doit être assigné avant d’être utilisé ; c’est-à-dire qu’il doit être assigné par l’appelé.</span><span class="sxs-lookup"><span data-stu-id="b23d7-103">Like all [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) parameters, an `out` parameter of an array type must be assigned before it is used; that is, it must be assigned by the callee.</span></span> <span data-ttu-id="b23d7-104">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b23d7-104">For example:</span></span>  
  
 [!code-csharp[csProgGuideArrays#39](../../../csharp/programming-guide/arrays/codesnippet/CSharp/passing-arrays-using-ref-and-out_1.cs)]  
  
 <span data-ttu-id="b23d7-105">Comme tous les paramètres [ref](../../../csharp/language-reference/keywords/ref.md), un paramètre `ref` d’un type tableau doit absolument être assigné par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b23d7-105">Like all [ref](../../../csharp/language-reference/keywords/ref.md) parameters, a `ref` parameter of an array type must be definitely assigned by the caller.</span></span> <span data-ttu-id="b23d7-106">Par conséquent, il n'a pas besoin d'être assigné par l'appelé.</span><span class="sxs-lookup"><span data-stu-id="b23d7-106">Therefore, there is no need to be definitely assigned by the callee.</span></span> <span data-ttu-id="b23d7-107">Un paramètre `ref` d'un type tableau peut être modifié à la suite de l'appel.</span><span class="sxs-lookup"><span data-stu-id="b23d7-107">A `ref` parameter of an array type may be altered as a result of the call.</span></span> <span data-ttu-id="b23d7-108">Par exemple, la valeur [null](../../../csharp/language-reference/keywords/null.md) peut être assignée au tableau ou ce dernier peut être initialisé sur un tableau différent.</span><span class="sxs-lookup"><span data-stu-id="b23d7-108">For example, the array can be assigned the [null](../../../csharp/language-reference/keywords/null.md) value or can be initialized to a different array.</span></span> <span data-ttu-id="b23d7-109">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b23d7-109">For example:</span></span>  
  
 [!code-csharp[csProgGuideArrays#40](../../../csharp/programming-guide/arrays/codesnippet/CSharp/passing-arrays-using-ref-and-out_2.cs)]  
  
 <span data-ttu-id="b23d7-110">Les deux exemples suivants illustrent la différence entre les paramètres `out` et `ref` lorsqu'ils sont utilisés pour le passage de tableaux à des méthodes.</span><span class="sxs-lookup"><span data-stu-id="b23d7-110">The following two examples demonstrate the difference between `out` and `ref` when used in passing arrays to methods.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b23d7-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="b23d7-111">Example</span></span>  
 <span data-ttu-id="b23d7-112">Dans cet exemple, le tableau `theArray` est déclaré dans l'appelant (la méthode `Main`) et initialisé dans la méthode `FillArray`.</span><span class="sxs-lookup"><span data-stu-id="b23d7-112">In this example, the array `theArray` is declared in the caller (the `Main` method), and initialized in the `FillArray` method.</span></span> <span data-ttu-id="b23d7-113">Ensuite, les éléments du tableau sont retournés à l'appelant puis affichés.</span><span class="sxs-lookup"><span data-stu-id="b23d7-113">Then, the array elements are returned to the caller and displayed.</span></span>  
  
 [!code-csharp[csProgGuideArrays#37](../../../csharp/programming-guide/arrays/codesnippet/CSharp/passing-arrays-using-ref-and-out_3.cs)]  
  
## <a name="example"></a><span data-ttu-id="b23d7-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="b23d7-114">Example</span></span>  
 <span data-ttu-id="b23d7-115">Dans cet exemple, le tableau `theArray` est initialisé dans l'appelant (la méthode `Main`) et passé à la méthode `FillArray` à l'aide du paramètre `ref`.</span><span class="sxs-lookup"><span data-stu-id="b23d7-115">In this example, the array `theArray` is initialized in the caller (the `Main` method), and passed to the `FillArray` method by using the `ref` parameter.</span></span> <span data-ttu-id="b23d7-116">Certains des éléments du tableau sont mis à jour dans la méthode `FillArray`.</span><span class="sxs-lookup"><span data-stu-id="b23d7-116">Some of the array elements are updated in the `FillArray` method.</span></span> <span data-ttu-id="b23d7-117">Ensuite, les éléments du tableau sont retournés à l'appelant puis affichés.</span><span class="sxs-lookup"><span data-stu-id="b23d7-117">Then, the array elements are returned to the caller and displayed.</span></span>  
  
 [!code-csharp[csProgGuideArrays#38](../../../csharp/programming-guide/arrays/codesnippet/CSharp/passing-arrays-using-ref-and-out_4.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b23d7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b23d7-118">See Also</span></span>  
 [<span data-ttu-id="b23d7-119">ref</span><span class="sxs-lookup"><span data-stu-id="b23d7-119">ref</span></span>](../../../csharp/language-reference/keywords/ref.md)  
 [<span data-ttu-id="b23d7-120">out, modificateur de paramètre</span><span class="sxs-lookup"><span data-stu-id="b23d7-120">out parameter modifier</span></span>](../../../csharp/language-reference/keywords/out-parameter-modifier.md)  
 [<span data-ttu-id="b23d7-121">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b23d7-121">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b23d7-122">Tableaux</span><span class="sxs-lookup"><span data-stu-id="b23d7-122">Arrays</span></span>](../../../csharp/programming-guide/arrays/index.md)  
 [<span data-ttu-id="b23d7-123">Tableaux unidimensionnels</span><span class="sxs-lookup"><span data-stu-id="b23d7-123">Single-Dimensional Arrays</span></span>](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)  
 [<span data-ttu-id="b23d7-124">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="b23d7-124">Multidimensional Arrays</span></span>](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)  
 [<span data-ttu-id="b23d7-125">Tableaux en escalier</span><span class="sxs-lookup"><span data-stu-id="b23d7-125">Jagged Arrays</span></span>](../../../csharp/programming-guide/arrays/jagged-arrays.md)
