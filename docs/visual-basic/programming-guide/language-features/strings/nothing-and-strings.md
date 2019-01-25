---
title: Nothing et les chaînes en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], Nothing
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
ms.openlocfilehash: 65a69861c2a74a3191a45eb782a97f289b0c0726
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574168"
---
# <a name="nothing-and-strings-in-visual-basic"></a><span data-ttu-id="62454-102">Nothing et les chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62454-102">Nothing and Strings in Visual Basic</span></span>
<span data-ttu-id="62454-103">Le runtime Visual Basic et le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] évaluer `Nothing` différemment lorsqu’il s’agit de chaînes.</span><span class="sxs-lookup"><span data-stu-id="62454-103">The Visual Basic runtime and the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] evaluate `Nothing` differently when it comes to strings.</span></span>  
  
## <a name="visual-basic-runtime-and-the-net-framework"></a><span data-ttu-id="62454-104">Runtime Visual Basic et .NET Framework</span><span class="sxs-lookup"><span data-stu-id="62454-104">Visual Basic Runtime and the .NET Framework</span></span>  
 <span data-ttu-id="62454-105">Prenons l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="62454-105">Consider the following example:</span></span>  
  
 [!code-vb[VbVbalrStrings#47](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/nothing-and-strings_1.vb)]  
  
 <span data-ttu-id="62454-106">Le runtime Visual Basic prend généralement la valeur `Nothing` comme une chaîne vide ( » »).</span><span class="sxs-lookup"><span data-stu-id="62454-106">The Visual Basic runtime usually evaluates `Nothing` as an empty string ("").</span></span> <span data-ttu-id="62454-107">Le [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] est pas le cas, toutefois et lève une exception chaque fois qu’une tentative est effectuée pour effectuer une opération de chaîne sur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="62454-107">The [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] does not, however, and throws an exception whenever an attempt is made to perform a string operation on `Nothing`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62454-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62454-108">See also</span></span>
- [<span data-ttu-id="62454-109">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="62454-109">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)
