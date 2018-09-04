---
title: Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: b821034731514362a3725c390e02542b536f0a59
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43542217"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="bb0e5-102">Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source</span><span class="sxs-lookup"><span data-stu-id="bb0e5-102">Could not complete operation since target directory is under source directory</span></span>
<span data-ttu-id="bb0e5-103">Une opération cyclique a échoué.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-103">A cyclic operation has failed.</span></span> <span data-ttu-id="bb0e5-104">Les opérations cycliques se répètent et, par conséquent, ne peuvent pas s’achever.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-104">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="bb0e5-105">Par exemple, l’objet A peut essayer d’hériter de l’objet B qui hérite, à son tour, de l’objet A.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-105">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bb0e5-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="bb0e5-106">To correct this error</span></span>  
  
-   <span data-ttu-id="bb0e5-107">Lors d’un héritage, vérifiez qu’il n’existe aucune référence cyclique.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-107">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb0e5-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb0e5-108">See Also</span></span>  
 [<span data-ttu-id="bb0e5-109">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="bb0e5-109">Error Types</span></span>](../../visual-basic/programming-guide/language-features/error-types.md)  
 [<span data-ttu-id="bb0e5-110">Éléments fondamentaux du débogage : points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="bb0e5-110">Debugging Basics: Breakpoints</span></span>](https://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
