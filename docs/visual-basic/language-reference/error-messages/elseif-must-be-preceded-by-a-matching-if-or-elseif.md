---
title: '&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30014
- bc30014
helpviewer_keywords:
- BC30014
ms.assetid: 5215585e-2efa-485a-9efe-9833a1cc83a0
ms.openlocfilehash: 1e63595ee573e9356f6870a02b2131897c725baf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505781"
---
# <a name="39elseif39-must-be-preceded-by-a-matching-39if39-or-39elseif39"></a><span data-ttu-id="66126-102">&#39;#ElseIf&#39; doit être précédé d’une mise en correspondance &#39;#If&#39; ou &#39;#ElseIf&#39;</span><span class="sxs-lookup"><span data-stu-id="66126-102">&#39;#ElseIf&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;</span></span>
<span data-ttu-id="66126-103">`#ElseIf` est une directive de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="66126-103">`#ElseIf` is a conditional compilation directive.</span></span> <span data-ttu-id="66126-104">Un `#ElseIf` clause doit être précédée d’une mise en correspondance `#If` ou `#ElseIf` clause.</span><span class="sxs-lookup"><span data-stu-id="66126-104">An `#ElseIf` clause must be preceded by a matching `#If` or `#ElseIf` clause.</span></span>  
  
 <span data-ttu-id="66126-105">**ID d’erreur :** BC30014</span><span class="sxs-lookup"><span data-stu-id="66126-105">**Error ID:** BC30014</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="66126-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="66126-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="66126-107">Vérifiez que précédente `#If` ou `#ElseIf` n’a pas été séparés à partir de ce `#ElseIf` par un bloc de compilation conditionnelle intermédiaire ou mal placé `#End If`.</span><span class="sxs-lookup"><span data-stu-id="66126-107">Check that a preceding `#If` or `#ElseIf` has not been separated from this `#ElseIf` by an intervening conditional compilation block or an incorrectly placed `#End If`.</span></span>  
  
2.  <span data-ttu-id="66126-108">Si le `#ElseIf` est précédé par un `#Else` directive, supprimez le `#Else` ou remplacez-le par un `#ElseIf`.</span><span class="sxs-lookup"><span data-stu-id="66126-108">If the `#ElseIf` is preceded by a `#Else` directive, either remove the `#Else` or change it to an `#ElseIf`.</span></span>  
  
3.  <span data-ttu-id="66126-109">Si tout le reste est en ordre, ajoutez une directive `#If` au début du bloc de compilation conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="66126-109">If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66126-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66126-110">See also</span></span>
- [<span data-ttu-id="66126-111">#If...Then...#Else, directives</span><span class="sxs-lookup"><span data-stu-id="66126-111">#If...Then...#Else Directives</span></span>](../../../visual-basic/language-reference/directives/if-then-else-directives.md)
