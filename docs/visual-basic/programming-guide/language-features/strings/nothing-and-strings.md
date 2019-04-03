---
title: Nothing et les chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], Nothing
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
ms.openlocfilehash: 5fbcf86261892e3eb8e43ee8eaa3728cd8e42ced
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841886"
---
# <a name="nothing-and-strings-in-visual-basic"></a><span data-ttu-id="6cac0-102">Nothing et les chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6cac0-102">Nothing and Strings in Visual Basic</span></span>
<span data-ttu-id="6cac0-103">Le runtime Visual Basic et le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] évaluer `Nothing` différemment lorsqu’il s’agit de chaînes.</span><span class="sxs-lookup"><span data-stu-id="6cac0-103">The Visual Basic runtime and the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] evaluate `Nothing` differently when it comes to strings.</span></span>  
  
## <a name="visual-basic-runtime-and-the-net-framework"></a><span data-ttu-id="6cac0-104">Runtime Visual Basic et .NET Framework</span><span class="sxs-lookup"><span data-stu-id="6cac0-104">Visual Basic Runtime and the .NET Framework</span></span>  
 <span data-ttu-id="6cac0-105">Prenons l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6cac0-105">Consider the following example:</span></span>  
  
 [!code-vb[VbVbalrStrings#47](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#47)]  
  
 <span data-ttu-id="6cac0-106">Le runtime Visual Basic prend généralement la valeur `Nothing` comme une chaîne vide ( » »).</span><span class="sxs-lookup"><span data-stu-id="6cac0-106">The Visual Basic runtime usually evaluates `Nothing` as an empty string ("").</span></span> <span data-ttu-id="6cac0-107">Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] est pas le cas, toutefois et lève une exception chaque fois qu’une tentative est effectuée pour effectuer une opération de chaîne sur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="6cac0-107">The [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] does not, however, and throws an exception whenever an attempt is made to perform a string operation on `Nothing`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cac0-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cac0-108">See also</span></span>

- [<span data-ttu-id="6cac0-109">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6cac0-109">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
