---
title: L'instruction ne peut pas terminer un bloc en dehors d'une instruction 'If' d'une ligne
ms.date: 07/20/2015
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords:
- BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
ms.openlocfilehash: 85573099ec0a3f8a23c17bdf384c4c105f9157df
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58825792"
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-if-statement"></a><span data-ttu-id="0f2d1-102">L'instruction ne peut pas terminer un bloc en dehors d'une instruction 'If' d'une ligne</span><span class="sxs-lookup"><span data-stu-id="0f2d1-102">Statement cannot end a block outside of a line 'If' statement</span></span>
<span data-ttu-id="0f2d1-103">Une seule ligne `If` instruction contient plusieurs instructions séparées par le signe deux-points ( :),) d'entre eux étant un `End` instruction pour un bloc de contrôle en dehors de la ligne unique `If`.</span><span class="sxs-lookup"><span data-stu-id="0f2d1-103">A single-line `If` statement contains several statements separated by colons (:), one of which is an `End` statement for a control block outside the single-line `If`.</span></span> <span data-ttu-id="0f2d1-104">Une ligne `If` instructions n’utilisent pas la `End If` instruction.</span><span class="sxs-lookup"><span data-stu-id="0f2d1-104">Single-line `If` statements do not use the `End If` statement.</span></span>  
  
 <span data-ttu-id="0f2d1-105">**ID d’erreur :** BC32005</span><span class="sxs-lookup"><span data-stu-id="0f2d1-105">**Error ID:** BC32005</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0f2d1-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0f2d1-106">To correct this error</span></span>  
  
-   <span data-ttu-id="0f2d1-107">Déplacer la ligne unique `If` instruction en dehors du bloc de contrôle qui contient le `End If` instruction.</span><span class="sxs-lookup"><span data-stu-id="0f2d1-107">Move the single-line `If` statement outside the control block that contains the `End If` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f2d1-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f2d1-108">See also</span></span>

- [<span data-ttu-id="0f2d1-109">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="0f2d1-109">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
