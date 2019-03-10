---
title: Événements dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: dfbac71335615af52de3b5862c4058981f965654
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720792"
---
# <a name="events-in-windows-forms-controls"></a><span data-ttu-id="27143-102">Événements dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="27143-102">Events in Windows Forms Controls</span></span>
<span data-ttu-id="27143-103">Un contrôle Windows Forms hérite plus de soixante événements de <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="27143-103">A Windows Forms control inherits more than sixty events from <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="27143-104">Ceux-ci incluent le <xref:System.Windows.Forms.Control.Paint> événement, ce qui provoque un contrôle est dessiné, les événements liés à l’affichage d’une fenêtre, comme le <xref:System.Windows.Forms.Control.Resize> et <xref:System.Windows.Forms.Control.Layout> événements et les événements de souris et clavier de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="27143-104">These include the <xref:System.Windows.Forms.Control.Paint> event, which causes a control to be drawn, events related to displaying a window, such as the <xref:System.Windows.Forms.Control.Resize> and <xref:System.Windows.Forms.Control.Layout> events, and low-level mouse and keyboard events.</span></span> <span data-ttu-id="27143-105">Certains événements de bas niveau sont synthétisés par <xref:System.Windows.Forms.Control> en événements de sémantique comme <xref:System.Windows.Forms.Control.Click> et <xref:System.Windows.Forms.Control.DoubleClick>.</span><span class="sxs-lookup"><span data-stu-id="27143-105">Some low-level events are synthesized by <xref:System.Windows.Forms.Control> into semantic events such as <xref:System.Windows.Forms.Control.Click> and <xref:System.Windows.Forms.Control.DoubleClick>.</span></span> <span data-ttu-id="27143-106">Pour plus d’informations sur les événements hérités, consultez <xref:System.Windows.Forms.Control>.</span><span class="sxs-lookup"><span data-stu-id="27143-106">For details about inherited events, see <xref:System.Windows.Forms.Control>.</span></span>  
  
 <span data-ttu-id="27143-107">Si votre contrôle personnalisé doit remplacer des fonctionnalités d’événements héritées, remplacez la méthode `On`*EventName* plutôt que d’attacher un délégué.</span><span class="sxs-lookup"><span data-stu-id="27143-107">If your custom control needs to override inherited event functionality, override the inherited `On`*EventName* method instead of attaching a delegate.</span></span> <span data-ttu-id="27143-108">Si le modèle d’événement dans le .NET Framework ne vous est pas familier, consultez la page [Déclencher des événements à partir d’un composant](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="27143-108">If you are not familiar with the event model in the .NET Framework, see [Raising Events from a Component](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27143-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27143-109">See also</span></span>
- [<span data-ttu-id="27143-110">Remplacer la méthode OnPaint</span><span class="sxs-lookup"><span data-stu-id="27143-110">Overriding the OnPaint Method</span></span>](overriding-the-onpaint-method.md)
- [<span data-ttu-id="27143-111">Gestion des entrées utilisateur</span><span class="sxs-lookup"><span data-stu-id="27143-111">Handling User Input</span></span>](handling-user-input.md)
- [<span data-ttu-id="27143-112">Définition d’un événement</span><span class="sxs-lookup"><span data-stu-id="27143-112">Defining an Event</span></span>](defining-an-event-in-windows-forms-controls.md)
- [<span data-ttu-id="27143-113">Événements</span><span class="sxs-lookup"><span data-stu-id="27143-113">Events</span></span>](../../../standard/events/index.md)
