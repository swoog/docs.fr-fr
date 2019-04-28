---
title: Les événements des variables WithEvents partagées ne peuvent pas être gérés par des méthodes non partagées
ms.date: 07/20/2015
f1_keywords:
- bc30594
- vbc30594
helpviewer_keywords:
- BC30594
ms.assetid: 5b9fceb4-ab11-41bb-ad3b-6f1a9da8ae7e
ms.openlocfilehash: 2b32043898986b3e3e68fab18c5f907843d7691c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61803252"
---
# <a name="events-of-shared-withevents-variables-cannot-be-handled-by-non-shared-methods"></a><span data-ttu-id="f19d6-102">Les événements des variables WithEvents partagées ne peuvent pas être gérés par des méthodes non partagées</span><span class="sxs-lookup"><span data-stu-id="f19d6-102">Events of shared WithEvents variables cannot be handled by non-shared methods</span></span>
<span data-ttu-id="f19d6-103">Une variable déclarée avec le `Shared` modificateur est une variable partagée.</span><span class="sxs-lookup"><span data-stu-id="f19d6-103">A variable declared with the `Shared` modifier is a shared variable.</span></span> <span data-ttu-id="f19d6-104">Une variable partagée identifie exactement un emplacement de stockage.</span><span class="sxs-lookup"><span data-stu-id="f19d6-104">A shared variable identifies exactly one storage location.</span></span> <span data-ttu-id="f19d6-105">Une variable déclarée avec le `WithEvents` modificateur garantit que le type auquel appartient la variable gère l’ensemble de la variable déclenche des événements.</span><span class="sxs-lookup"><span data-stu-id="f19d6-105">A variable declared with the `WithEvents` modifier asserts that the type to which the variable belongs handles the set of events the variable raises.</span></span> <span data-ttu-id="f19d6-106">Lorsqu’une valeur est attribuée à la variable, la propriété créée par le `WithEvents` déclaration déconnecte tout gestionnaire d’événements existant et raccorde le nouveau gestionnaire d’événements via le `Add` (méthode).</span><span class="sxs-lookup"><span data-stu-id="f19d6-106">When a value is assigned to the variable, the property created by the `WithEvents` declaration unhooks any existing event handler and hooks up the new event handler via the `Add` method.</span></span>  
  
 <span data-ttu-id="f19d6-107">**ID d’erreur :** BC30594</span><span class="sxs-lookup"><span data-stu-id="f19d6-107">**Error ID:** BC30594</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f19d6-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f19d6-108">To correct this error</span></span>  
  
- <span data-ttu-id="f19d6-109">Déclarez votre gestionnaire d’événements `Shared`.</span><span class="sxs-lookup"><span data-stu-id="f19d6-109">Declare your event handler `Shared`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f19d6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f19d6-110">See also</span></span>

- [<span data-ttu-id="f19d6-111">Shared</span><span class="sxs-lookup"><span data-stu-id="f19d6-111">Shared</span></span>](../../../visual-basic/language-reference/modifiers/shared.md)
- [<span data-ttu-id="f19d6-112">WithEvents</span><span class="sxs-lookup"><span data-stu-id="f19d6-112">WithEvents</span></span>](../../../visual-basic/language-reference/modifiers/withevents.md)
