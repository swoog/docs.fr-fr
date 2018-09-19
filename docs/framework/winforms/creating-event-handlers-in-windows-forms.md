---
title: Création de gestionnaires d'événements dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- event handling [Windows Forms]
- Windows Forms controls, event handling
- Windows Forms, event handling
- events [Windows Forms], event handlers
- event handlers [Windows Forms]
ms.assetid: 6514e530-c6b8-489c-a8d2-eda7b7072701
ms.openlocfilehash: 9095946d52360c69fd6c4dd6285039fb3e1874d5
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45994596"
---
# <a name="creating-event-handlers-in-windows-forms"></a><span data-ttu-id="e8ff9-102">Création de gestionnaires d'événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e8ff9-102">Creating Event Handlers in Windows Forms</span></span>
<span data-ttu-id="e8ff9-103">Un gestionnaire d'événements est une procédure de votre code qui détermine les actions à effectuer quand un événement se produit, par exemple, quand un utilisateur clique sur un bouton ou une file d'attente reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-103">An event handler is a procedure in your code that determines what actions are performed when an event occurs, such as when the user clicks a button or a message queue receives a message.</span></span> <span data-ttu-id="e8ff9-104">Au déclenchement de l'événement, le ou les gestionnaires d'événements qui reçoivent l'événement sont exécutés.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-104">When an event is raised, the event handler or handlers that receive the event are executed.</span></span> <span data-ttu-id="e8ff9-105">Des événements peuvent être affectés à plusieurs gestionnaires et les méthodes qui gèrent des événements particuliers peuvent être modifiées de façon dynamique.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-105">Events can be assigned to multiple handlers, and the methods that handle particular events can be changed dynamically.</span></span> <span data-ttu-id="e8ff9-106">Vous pouvez également utiliser le Concepteur Windows Forms pour créer des gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-106">You can also use the Windows Forms Designer to create event handlers.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e8ff9-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e8ff9-107">In This Section</span></span>  
 [<span data-ttu-id="e8ff9-108">Vue d'ensemble des événements</span><span class="sxs-lookup"><span data-stu-id="e8ff9-108">Events Overview</span></span>](../../../docs/framework/winforms/events-overview-windows-forms.md)  
 <span data-ttu-id="e8ff9-109">Présente le modèle d'événement et explique le rôle des délégués.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-109">Explains the event model and the role of delegates.</span></span>  
  
 [<span data-ttu-id="e8ff9-110">Vue d'ensemble des gestionnaires d'événements</span><span class="sxs-lookup"><span data-stu-id="e8ff9-110">Event Handlers Overview</span></span>](../../../docs/framework/winforms/event-handlers-overview-windows-forms.md)  
 <span data-ttu-id="e8ff9-111">Explique comment gérer les événements.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-111">Describes how to handle events.</span></span>  
  
 [<span data-ttu-id="e8ff9-112">Comment : créer des gestionnaires d'événements pour les Windows Forms au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="e8ff9-112">How to: Create Event Handlers at Run Time for Windows Forms</span></span>](../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md)  
 <span data-ttu-id="e8ff9-113">Explique comment répondre dynamiquement aux événements système ou utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-113">Gives directions for responding to system or user events dynamically.</span></span>  
  
 [<span data-ttu-id="e8ff9-114">Comment : connecter plusieurs événements à un même gestionnaire d'événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e8ff9-114">How to: Connect Multiple Events to a Single Event Handler in Windows Forms</span></span>](../../../docs/framework/winforms/how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md)  
 <span data-ttu-id="e8ff9-115">Explique comment assigner la même fonctionnalité à plusieurs contrôles par le biais d'événements.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-115">Gives directions for assigning the same functionality to multiple controls through events.</span></span>  
  
 [<span data-ttu-id="e8ff9-116">Ordre des événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e8ff9-116">Order of Events in Windows Forms</span></span>](../../../docs/framework/winforms/order-of-events-in-windows-forms.md)  
 <span data-ttu-id="e8ff9-117">Décrit l'ordre dans lequel les événements sont déclenchés dans les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-117">Describes the order in which events are raised in Windows Forms controls.</span></span>  
  
 [<span data-ttu-id="e8ff9-118">Comment : créer des gestionnaires d'événements à l'aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="e8ff9-118">How to: Create Event Handlers Using the Designer</span></span>](https://msdn.microsoft.com/library/8461e9b8-14e8-406f-936e-3726732b23d2)  
 <span data-ttu-id="e8ff9-119">Décrit comment utiliser le Concepteur Windows Forms pour créer des gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-119">Describes how to use the Windows Forms Designer to create event handlers.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="e8ff9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8ff9-120">Related Sections</span></span>  
 [<span data-ttu-id="e8ff9-121">Événements</span><span class="sxs-lookup"><span data-stu-id="e8ff9-121">Events</span></span>](../../../docs/standard/events/index.md)  
 <span data-ttu-id="e8ff9-122">Fournit des liens vers les rubriques sur la gestion et le déclenchement des événements à l'aide du [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e8ff9-122">Provides links to topics on handling and raising events using the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)].</span></span>  
  
 [<span data-ttu-id="e8ff9-123">Dépannage des gestionnaires d’événements hérités en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e8ff9-123">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)  
 <span data-ttu-id="e8ff9-124">Répertorie les problèmes courants qui surviennent avec les gestionnaires d'événements dans les composants hérités.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-124">Lists common issues that occur with event handlers in inherited components.</span></span>
