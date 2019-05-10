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
ms.openlocfilehash: 329060e0c53178a9320be9a7cdff492d69917782
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211248"
---
# <a name="creating-event-handlers-in-windows-forms"></a><span data-ttu-id="0dcd2-102">Création de gestionnaires d'événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0dcd2-102">Creating Event Handlers in Windows Forms</span></span>

<span data-ttu-id="0dcd2-103">Un gestionnaire d'événements est une procédure de votre code qui détermine les actions à effectuer quand un événement se produit, par exemple, quand un utilisateur clique sur un bouton ou une file d'attente reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-103">An event handler is a procedure in your code that determines what actions are performed when an event occurs, such as when the user clicks a button or a message queue receives a message.</span></span> <span data-ttu-id="0dcd2-104">Au déclenchement de l'événement, le ou les gestionnaires d'événements qui reçoivent l'événement sont exécutés.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-104">When an event is raised, the event handler or handlers that receive the event are executed.</span></span> <span data-ttu-id="0dcd2-105">Des événements peuvent être affectés à plusieurs gestionnaires et les méthodes qui gèrent des événements particuliers peuvent être modifiées de façon dynamique.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-105">Events can be assigned to multiple handlers, and the methods that handle particular events can be changed dynamically.</span></span> <span data-ttu-id="0dcd2-106">Vous pouvez également utiliser le Concepteur de formulaires Windows dans Visual Studio pour créer des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-106">You can also use the Windows Forms Designer in Visual Studio to create event handlers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0dcd2-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0dcd2-107">In This Section</span></span>

 <span data-ttu-id="0dcd2-108">[Vue d’ensemble des événements](events-overview-windows-forms.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-108">[Events Overview](events-overview-windows-forms.md)\\</span></span>
 <span data-ttu-id="0dcd2-109">Présente le modèle d'événement et explique le rôle des délégués.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-109">Explains the event model and the role of delegates.</span></span>

 <span data-ttu-id="0dcd2-110">[Vue d’ensemble des gestionnaires d’événements](event-handlers-overview-windows-forms.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-110">[Event Handlers Overview](event-handlers-overview-windows-forms.md)\\</span></span>
 <span data-ttu-id="0dcd2-111">Explique comment gérer les événements.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-111">Describes how to handle events.</span></span>

 <span data-ttu-id="0dcd2-112">[Guide pratique pour Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](how-to-create-event-handlers-at-run-time-for-windows-forms.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-112">[How to: Create Event Handlers at Run Time for Windows Forms](how-to-create-event-handlers-at-run-time-for-windows-forms.md)\\</span></span>
 <span data-ttu-id="0dcd2-113">Explique comment répondre dynamiquement aux événements système ou utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-113">Gives directions for responding to system or user events dynamically.</span></span>

 <span data-ttu-id="0dcd2-114">[Guide pratique pour Connecter plusieurs événements à un seul gestionnaire d’événements dans les Windows Forms](how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-114">[How to: Connect Multiple Events to a Single Event Handler in Windows Forms](how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md)\\</span></span>
 <span data-ttu-id="0dcd2-115">Explique comment assigner la même fonctionnalité à plusieurs contrôles par le biais d'événements.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-115">Gives directions for assigning the same functionality to multiple controls through events.</span></span>

 <span data-ttu-id="0dcd2-116">[Ordre des événements dans les Windows Forms](order-of-events-in-windows-forms.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-116">[Order of Events in Windows Forms](order-of-events-in-windows-forms.md)\\</span></span>
 <span data-ttu-id="0dcd2-117">Décrit l'ordre dans lequel les événements sont déclenchés dans les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-117">Describes the order in which events are raised in Windows Forms controls.</span></span>

 <span data-ttu-id="0dcd2-118">[Guide pratique pour Créer des gestionnaires d’événements à l’aide du concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)) explique comment utiliser le Concepteur de formulaires Windows pour créer des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-118">[How to: Create Event Handlers Using the Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)) Describes how to use the Windows Forms Designer to create event handlers.</span></span>

## <a name="related-sections"></a><span data-ttu-id="0dcd2-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0dcd2-119">Related Sections</span></span>

 <span data-ttu-id="0dcd2-120">[Événements](../../standard/events/index.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-120">[Events](../../standard/events/index.md)\\</span></span>
 <span data-ttu-id="0dcd2-121">Fournit des liens vers des rubriques sur la gestion et déclenchement d’événements à l’aide du [!INCLUDE [dnprdnshort](../../../includes/dnprdnshort-md.md)\].</span><span class="sxs-lookup"><span data-stu-id="0dcd2-121">Provides links to topics on handling and raising events using the [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)\].</span></span>

 <span data-ttu-id="0dcd2-122">[Dépannage des gestionnaires d’événements hérités en Visual Basic](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)\\</span><span class="sxs-lookup"><span data-stu-id="0dcd2-122">[Troubleshooting Inherited Event Handlers in Visual Basic](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)\\</span></span>
 <span data-ttu-id="0dcd2-123">Répertorie les problèmes courants qui surviennent avec les gestionnaires d'événements dans les composants hérités.</span><span class="sxs-lookup"><span data-stu-id="0dcd2-123">Lists common issues that occur with event handlers in inherited components.</span></span>
