---
title: Comparaison de pointeurs - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], comparison
ms.assetid: fcafd514-7405-4deb-8490-cc58efda5495
ms.openlocfilehash: 5185bd5e1686858452efcc7c89e2c1977e094386
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969204"
---
# <a name="pointer-comparison-c-programming-guide"></a><span data-ttu-id="2bcef-102">Comparaison de pointeurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="2bcef-102">Pointer Comparison (C# Programming Guide)</span></span>
<span data-ttu-id="2bcef-103">Vous pouvez appliquer les opérateurs suivants pour comparer des pointeurs de tout type :</span><span class="sxs-lookup"><span data-stu-id="2bcef-103">You can apply the following operators to compare pointers of any type:</span></span>  
  
 <span data-ttu-id="2bcef-104">**==   !=   \<   >   \<=   >=**</span><span class="sxs-lookup"><span data-stu-id="2bcef-104">**==   !=   \<   >   \<=   >=**</span></span>  
  
 <span data-ttu-id="2bcef-105">Les opérateurs de comparaison comparent les adresses des deux opérandes comme s’il s’agissait d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="2bcef-105">The comparison operators compare the addresses of the two operands as if they are unsigned integers.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2bcef-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="2bcef-106">Example</span></span>  
 [!code-csharp[csProgGuidePointers#16](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers2.cs#16)]  
  
 [!code-csharp[csProgGuidePointers#17](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#17)]  
  
## <a name="sample-output"></a><span data-ttu-id="2bcef-107">Résultat de l'exemple</span><span class="sxs-lookup"><span data-stu-id="2bcef-107">Sample Output</span></span>  
 `True`  
  
 `False`  
  
## <a name="see-also"></a><span data-ttu-id="2bcef-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bcef-108">See also</span></span>

- [<span data-ttu-id="2bcef-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2bcef-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="2bcef-110">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="2bcef-110">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="2bcef-111">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="2bcef-111">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
- [<span data-ttu-id="2bcef-112">Manipulation de pointeurs</span><span class="sxs-lookup"><span data-stu-id="2bcef-112">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)
- [<span data-ttu-id="2bcef-113">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="2bcef-113">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="2bcef-114">Types</span><span class="sxs-lookup"><span data-stu-id="2bcef-114">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="2bcef-115">unsafe</span><span class="sxs-lookup"><span data-stu-id="2bcef-115">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="2bcef-116">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="2bcef-116">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="2bcef-117">stackalloc</span><span class="sxs-lookup"><span data-stu-id="2bcef-117">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
