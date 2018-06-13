---
title: Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: 68217023a980891200c18b5536ef902574d36257
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33638510"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="c66d7-102">Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source</span><span class="sxs-lookup"><span data-stu-id="c66d7-102">Could not complete operation since target directory is under source directory</span></span>
<span data-ttu-id="c66d7-103">Une opération cyclique a échoué.</span><span class="sxs-lookup"><span data-stu-id="c66d7-103">A cyclic operation has failed.</span></span> <span data-ttu-id="c66d7-104">Les opérations cycliques se répètent et, par conséquent, ne peuvent pas s’achever.</span><span class="sxs-lookup"><span data-stu-id="c66d7-104">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="c66d7-105">Par exemple, l’objet A peut essayer d’hériter de l’objet B qui hérite, à son tour, de l’objet A.</span><span class="sxs-lookup"><span data-stu-id="c66d7-105">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="c66d7-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="c66d7-106">To correct this error</span></span>  
  
-   <span data-ttu-id="c66d7-107">Lors d’un héritage, vérifiez qu’il n’existe aucune référence cyclique.</span><span class="sxs-lookup"><span data-stu-id="c66d7-107">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c66d7-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c66d7-108">See Also</span></span>  
 [<span data-ttu-id="c66d7-109">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="c66d7-109">Error Types</span></span>](../../visual-basic/programming-guide/language-features/error-types.md)  
 [<span data-ttu-id="c66d7-110">Éléments fondamentaux du débogage : points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="c66d7-110">Debugging Basics: Breakpoints</span></span>](http://msdn.microsoft.com/library/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)
