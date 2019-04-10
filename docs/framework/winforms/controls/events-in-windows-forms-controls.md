---
title: Événements dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: 41ad95de7a65dbd0cb3a0d1af8f5c8cb00c1ccdd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59215884"
---
# <a name="events-in-windows-forms-controls"></a><span data-ttu-id="38420-102">Événements dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="38420-102">Events in Windows Forms Controls</span></span>
<span data-ttu-id="38420-103">Un contrôle Windows Forms hérite plus de soixante événements de <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="38420-103">A Windows Forms control inherits more than sixty events from <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="38420-104">Ceux-ci incluent le <xref:System.Windows.Forms.Control.Paint> événement, ce qui provoque un contrôle est dessiné, les événements liés à l’affichage d’une fenêtre, comme le <xref:System.Windows.Forms.Control.Resize> et <xref:System.Windows.Forms.Control.Layout> événements et les événements de souris et clavier de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="38420-104">These include the <xref:System.Windows.Forms.Control.Paint> event, which causes a control to be drawn, events related to displaying a window, such as the <xref:System.Windows.Forms.Control.Resize> and <xref:System.Windows.Forms.Control.Layout> events, and low-level mouse and keyboard events.</span></span> <span data-ttu-id="38420-105">Certains événements de bas niveau sont synthétisés par <xref:System.Windows.Forms.Control> en événements de sémantique comme <xref:System.Windows.Forms.Control.Click> et <xref:System.Windows.Forms.Control.DoubleClick>.</span><span class="sxs-lookup"><span data-stu-id="38420-105">Some low-level events are synthesized by <xref:System.Windows.Forms.Control> into semantic events such as <xref:System.Windows.Forms.Control.Click> and <xref:System.Windows.Forms.Control.DoubleClick>.</span></span> <span data-ttu-id="38420-106">Pour plus d’informations sur les événements hérités, consultez <xref:System.Windows.Forms.Control>.</span><span class="sxs-lookup"><span data-stu-id="38420-106">For details about inherited events, see <xref:System.Windows.Forms.Control>.</span></span>  
  
 <span data-ttu-id="38420-107">Si votre contrôle personnalisé doit remplacer des fonctionnalités d’événements héritées, remplacez la méthode `On`*EventName* plutôt que d’attacher un délégué.</span><span class="sxs-lookup"><span data-stu-id="38420-107">If your custom control needs to override inherited event functionality, override the inherited `On`*EventName* method instead of attaching a delegate.</span></span> <span data-ttu-id="38420-108">Si le modèle d’événement dans le .NET Framework ne vous est pas familier, consultez la page [Déclencher des événements à partir d’un composant](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="38420-108">If you are not familiar with the event model in the .NET Framework, see [Raising Events from a Component](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38420-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38420-109">See also</span></span>

- [<span data-ttu-id="38420-110">Substitution de la méthode OnPaint</span><span class="sxs-lookup"><span data-stu-id="38420-110">Overriding the OnPaint Method</span></span>](overriding-the-onpaint-method.md)
- [<span data-ttu-id="38420-111">Gestion des entrées utilisateur</span><span class="sxs-lookup"><span data-stu-id="38420-111">Handling User Input</span></span>](handling-user-input.md)
- [<span data-ttu-id="38420-112">Définition d’un événement</span><span class="sxs-lookup"><span data-stu-id="38420-112">Defining an Event</span></span>](defining-an-event-in-windows-forms-controls.md)
- [<span data-ttu-id="38420-113">Événements</span><span class="sxs-lookup"><span data-stu-id="38420-113">Events</span></span>](../../../standard/events/index.md)
