---
title: Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source
ms.date: 07/20/2015
f1_keywords:
- vbrIO_CyclicOperation
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
ms.openlocfilehash: f53ad664b341d4db803dee1f0f008c3918d13d93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61970116"
---
# <a name="could-not-complete-operation-since-target-directory-is-under-source-directory"></a><span data-ttu-id="97774-102">Impossible d’achever l’opération, car le répertoire cible se situe sous le répertoire source</span><span class="sxs-lookup"><span data-stu-id="97774-102">Could not complete operation since target directory is under source directory</span></span>
<span data-ttu-id="97774-103">Une opération cyclique a échoué.</span><span class="sxs-lookup"><span data-stu-id="97774-103">A cyclic operation has failed.</span></span> <span data-ttu-id="97774-104">Les opérations cycliques se répètent et, par conséquent, ne peuvent pas s’achever.</span><span class="sxs-lookup"><span data-stu-id="97774-104">Cyclic operations cycle and therefore cannot complete.</span></span> <span data-ttu-id="97774-105">Par exemple, l’objet A peut essayer d’hériter de l’objet B qui hérite, à son tour, de l’objet A.</span><span class="sxs-lookup"><span data-stu-id="97774-105">For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="97774-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="97774-106">To correct this error</span></span>  
  
- <span data-ttu-id="97774-107">Lors d’un héritage, vérifiez qu’il n’existe aucune référence cyclique.</span><span class="sxs-lookup"><span data-stu-id="97774-107">When inheriting, make sure that there are no cyclic references.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97774-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97774-108">See also</span></span>

- [<span data-ttu-id="97774-109">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="97774-109">Error Types</span></span>](../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="97774-110">Utilisez des points d’arrêt dans le débogueur Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97774-110">Use breakpoints in the Visual Studio debugger</span></span>](/visualstudio/debugger/using-breakpoints)
