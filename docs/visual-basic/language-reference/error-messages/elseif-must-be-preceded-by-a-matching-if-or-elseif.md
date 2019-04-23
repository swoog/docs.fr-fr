---
title: "'#ElseIf' doit être précédé d'un '#If' ou '#ElseIf' correspondant"
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 4832fb80cfbe42c7a1303e0de69f36784711c05a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59311056"
---
# <a name="elseif-must-be-preceded-by-a-matching-if-or-elseif"></a><span data-ttu-id="863f2-102">'#ElseIf' doit être précédé d'un '#If' ou '#ElseIf' correspondant</span><span class="sxs-lookup"><span data-stu-id="863f2-102">'#ElseIf' must be preceded by a matching '#If' or '#ElseIf'</span></span>
<span data-ttu-id="863f2-103">`#ElseIf` est une directive de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="863f2-103">`#ElseIf` is a conditional compilation directive.</span></span> <span data-ttu-id="863f2-104">Un `#ElseIf` clause doit être précédée d’une mise en correspondance `#If` ou `#ElseIf` clause.</span><span class="sxs-lookup"><span data-stu-id="863f2-104">An `#ElseIf` clause must be preceded by a matching `#If` or `#ElseIf` clause.</span></span>  
  
 <span data-ttu-id="863f2-105">**ID d’erreur :** BC30014</span><span class="sxs-lookup"><span data-stu-id="863f2-105">**Error ID:** BC30014</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="863f2-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="863f2-106">To correct this error</span></span>  
  
1. <span data-ttu-id="863f2-107">Vérifiez que précédente `#If` ou `#ElseIf` n’a pas été séparés à partir de ce `#ElseIf` par un bloc de compilation conditionnelle intermédiaire ou mal placé `#End If`.</span><span class="sxs-lookup"><span data-stu-id="863f2-107">Check that a preceding `#If` or `#ElseIf` has not been separated from this `#ElseIf` by an intervening conditional compilation block or an incorrectly placed `#End If`.</span></span>  
  
2. <span data-ttu-id="863f2-108">Si le `#ElseIf` est précédé par un `#Else` directive, supprimez le `#Else` ou remplacez-le par un `#ElseIf`.</span><span class="sxs-lookup"><span data-stu-id="863f2-108">If the `#ElseIf` is preceded by a `#Else` directive, either remove the `#Else` or change it to an `#ElseIf`.</span></span>  
  
3. <span data-ttu-id="863f2-109">Si tout le reste est en ordre, ajoutez une directive `#If` au début du bloc de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="863f2-109">If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="863f2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="863f2-110">See also</span></span>

- [<span data-ttu-id="863f2-111">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="863f2-111">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
