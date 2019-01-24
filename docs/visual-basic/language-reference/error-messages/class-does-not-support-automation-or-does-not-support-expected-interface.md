---
title: La classe ne prend pas en charge Automation ou l'interface attendue
ms.date: 07/20/2015
f1_keywords:
- vbrID430
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
ms.openlocfilehash: d5b47b39742a995be6076ddc0edc17f1ec94dade
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54534162"
---
# <a name="class-does-not-support-automation-or-does-not-support-expected-interface"></a><span data-ttu-id="0308e-102">La classe ne prend pas en charge Automation ou l'interface attendue</span><span class="sxs-lookup"><span data-stu-id="0308e-102">Class does not support Automation or does not support expected interface</span></span>
<span data-ttu-id="0308e-103">La classe que vous avez spécifiée dans l'appel de fonction `GetObject` ou `CreateObject` n'a exposé aucune interface programmable, ou vous avez modifié un projet .dll en .exe, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="0308e-103">Either the class you specified in the `GetObject` or `CreateObject` function call has not exposed a programmability interface, or you changed a project from .dll to .exe, or vice versa.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0308e-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0308e-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="0308e-105">Vérifiez la documentation de l'application qui a créé l'objet pour connaître les limitations relatives à l'utilisation de l'automatisation avec cette classe d'objet.</span><span class="sxs-lookup"><span data-stu-id="0308e-105">Check the documentation of the application that created the object for limitations on the use of automation with this class of object.</span></span>  
  
2.  <span data-ttu-id="0308e-106">Si vous avez modifié un projet .dll en .exe ou vice versa, vous devez annuler manuellement l'inscription de l'ancien projet .dll ou .exe.</span><span class="sxs-lookup"><span data-stu-id="0308e-106">If you changed a project from .dll to .exe or vice versa, you must manually unregister the old .dll or .exe.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0308e-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0308e-107">See also</span></span>
- [<span data-ttu-id="0308e-108">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="0308e-108">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="0308e-109">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="0308e-109">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
