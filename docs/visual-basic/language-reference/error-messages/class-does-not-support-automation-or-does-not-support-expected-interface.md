---
title: La classe ne prend pas en charge Automation ou l'interface attendue
ms.date: 07/20/2015
f1_keywords:
- vbrID430
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
ms.openlocfilehash: 4545c6d3bc302dba0c37e5ae6ebefa8939b0cff9
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59305921"
---
# <a name="class-does-not-support-automation-or-does-not-support-expected-interface"></a><span data-ttu-id="1c20c-102">La classe ne prend pas en charge Automation ou l'interface attendue</span><span class="sxs-lookup"><span data-stu-id="1c20c-102">Class does not support Automation or does not support expected interface</span></span>
<span data-ttu-id="1c20c-103">La classe que vous avez spécifiée dans l'appel de fonction `GetObject` ou `CreateObject` n'a exposé aucune interface programmable, ou vous avez modifié un projet .dll en .exe, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="1c20c-103">Either the class you specified in the `GetObject` or `CreateObject` function call has not exposed a programmability interface, or you changed a project from .dll to .exe, or vice versa.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1c20c-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1c20c-104">To correct this error</span></span>  
  
1. <span data-ttu-id="1c20c-105">Vérifiez la documentation de l'application qui a créé l'objet pour connaître les limitations relatives à l'utilisation de l'automatisation avec cette classe d'objet.</span><span class="sxs-lookup"><span data-stu-id="1c20c-105">Check the documentation of the application that created the object for limitations on the use of automation with this class of object.</span></span>  
  
2. <span data-ttu-id="1c20c-106">Si vous avez modifié un projet .dll en .exe ou vice versa, vous devez annuler manuellement l'inscription de l'ancien projet .dll ou .exe.</span><span class="sxs-lookup"><span data-stu-id="1c20c-106">If you changed a project from .dll to .exe or vice versa, you must manually unregister the old .dll or .exe.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c20c-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c20c-107">See also</span></span>

- [<span data-ttu-id="1c20c-108">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="1c20c-108">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
- [<span data-ttu-id="1c20c-109">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="1c20c-109">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
