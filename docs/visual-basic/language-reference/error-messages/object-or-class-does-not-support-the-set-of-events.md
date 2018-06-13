---
title: L'objet ou la classe ne prend pas en charge le jeu d'événements
ms.date: 07/20/2015
f1_keywords:
- vbrID459
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
ms.openlocfilehash: 4a6f1f59f43cdb351d49fbcbfd18362db888586e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593202"
---
# <a name="object-or-class-does-not-support-the-set-of-events"></a><span data-ttu-id="2d147-102">L'objet ou la classe ne prend pas en charge le jeu d'événements</span><span class="sxs-lookup"><span data-stu-id="2d147-102">Object or class does not support the set of events</span></span>
<span data-ttu-id="2d147-103">Vous avez essayé d’utiliser un `WithEvents` variable avec un composant qui ne peut pas fonctionner en tant que source d’événements pour le jeu d’événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d147-103">You tried to use a `WithEvents` variable with a component that cannot work as an event source for the specified set of events.</span></span> <span data-ttu-id="2d147-104">Par exemple, vous souhaitez recevoir les événements d’un objet, puis créer un autre objet qui `Implements` le premier objet.</span><span class="sxs-lookup"><span data-stu-id="2d147-104">For example, you wanted to sink the events of an object, then create another object that `Implements` the first object.</span></span> <span data-ttu-id="2d147-105">Même si vous pensez que vous pouvez recevoir les événements de l’objet implémenté, ce n’est pas toujours le cas.</span><span class="sxs-lookup"><span data-stu-id="2d147-105">Although you might think you could sink the events from the implemented object, this is not always the case.</span></span> <span data-ttu-id="2d147-106">`Implements` implémente uniquement une interface pour les méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="2d147-106">`Implements` only implements an interface for methods and properties.</span></span> <span data-ttu-id="2d147-107">`WithEvents` n’est pas prise en charge privé `UserControls`, car les informations de type nécessaires pour déclencher le `ObjectEvent` n’est pas disponible au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d147-107">`WithEvents` is not supported for private `UserControls`, because the type info needed to raise the `ObjectEvent` is not available at run time.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2d147-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="2d147-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="2d147-109">Vous ne pouvez pas recevoir d’événements pour un composant qui ne fournit pas d’événements.</span><span class="sxs-lookup"><span data-stu-id="2d147-109">You cannot sink events for a component that does not source events.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d147-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d147-110">See Also</span></span>  
 [<span data-ttu-id="2d147-111">WithEvents</span><span class="sxs-lookup"><span data-stu-id="2d147-111">WithEvents</span></span>](../../../visual-basic/language-reference/modifiers/withevents.md)  
 [<span data-ttu-id="2d147-112">Implements (instruction)</span><span class="sxs-lookup"><span data-stu-id="2d147-112">Implements Statement</span></span>](../../../visual-basic/language-reference/statements/implements-statement.md)
