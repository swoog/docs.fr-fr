---
title: Gestion des entrées utilisateur
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user input using code
- custom controls [Windows Forms], keyboard events using code
- custom controls [Windows Forms], mouse events using code
ms.assetid: d9b12787-86f6-4022-8e0f-e12d312c4af2
ms.openlocfilehash: a230611bfbb0a7f21a96de22674377887cc93c2d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33527798"
---
# <a name="handling-user-input"></a><span data-ttu-id="0eb0b-102">Gestion des entrées utilisateur</span><span class="sxs-lookup"><span data-stu-id="0eb0b-102">Handling User Input</span></span>
<span data-ttu-id="0eb0b-103">Cette rubrique décrit les principaux événements de clavier et souris fournis par <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-103">This topic describes the main keyboard and mouse events provided by <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="0eb0b-104">Lors de la gestion d’un événement, les auteurs de contrôle doivent substituer la méthode protégée `On`*EventName* au lieu d’attacher un délégué à l’événement.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-104">When handling an event, control authors should override the protected `On`*EventName* method rather than attaching a delegate to the event.</span></span> <span data-ttu-id="0eb0b-105">Pour un examen des événements, consultez [Déclenchement d’événements à partir d’un composant](http://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0).</span><span class="sxs-lookup"><span data-stu-id="0eb0b-105">For a review of events, see [Raising Events from a Component](http://msdn.microsoft.com/library/9aebf605-a87d-470b-b7c8-f9abfc8360a0).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0eb0b-106">Si aucune donnée associée à un événement, une instance de la classe de base <xref:System.EventArgs> est passé comme argument à la `On` *EventName* (méthode).</span><span class="sxs-lookup"><span data-stu-id="0eb0b-106">If there is no data associated with an event, an instance of the base class <xref:System.EventArgs> is passed as an argument to the `On`*EventName* method.</span></span>  
  
## <a name="keyboard-events"></a><span data-ttu-id="0eb0b-107">Événements de clavier</span><span class="sxs-lookup"><span data-stu-id="0eb0b-107">Keyboard Events</span></span>  
 <span data-ttu-id="0eb0b-108">Les événements de clavier courants que votre contrôle peut gérer sont <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, et <xref:System.Windows.Forms.Control.KeyUp>.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-108">The common keyboard events that your control can handle are <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, and <xref:System.Windows.Forms.Control.KeyUp>.</span></span>  
  
|<span data-ttu-id="0eb0b-109">Nom de l'événement</span><span class="sxs-lookup"><span data-stu-id="0eb0b-109">Event Name</span></span>|<span data-ttu-id="0eb0b-110">Méthode à substituer</span><span class="sxs-lookup"><span data-stu-id="0eb0b-110">Method to Override</span></span>|<span data-ttu-id="0eb0b-111">Description de l’événement</span><span class="sxs-lookup"><span data-stu-id="0eb0b-111">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|<span data-ttu-id="0eb0b-112">Déclenché uniquement lorsque l’utilisateur appuie initialement sur une touche.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-112">Raised only when a key is initially pressed.</span></span>|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|<span data-ttu-id="0eb0b-113">Déclenché à chaque fois que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-113">Raised every time a key is pressed.</span></span> <span data-ttu-id="0eb0b-114">Si une touche est maintenue enfoncée, un <xref:System.Windows.Forms.Control.KeyPress> événement est déclenché à la fréquence de répétition définie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-114">If a key is held down, a <xref:System.Windows.Forms.Control.KeyPress> event is raised at the repeat rate defined by the operating system.</span></span>|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|<span data-ttu-id="0eb0b-115">Déclenché lors du relâchement d’une touche.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-115">Raised when a key is released.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="0eb0b-116">La gestion des entrées sur le clavier est considérablement plus complexe que la substitution des événements dans le tableau précédent. Ce thème dépasse le cadre de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-116">Handling keyboard input is considerably more complex than overriding the events in the preceding table and is beyond the scope of this topic.</span></span> <span data-ttu-id="0eb0b-117">Pour plus d’informations, consultez [Entrée d’utilisateur dans Windows Forms](../../../../docs/framework/winforms/user-input-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="0eb0b-117">For more information, see [User Input in Windows Forms](../../../../docs/framework/winforms/user-input-in-windows-forms.md).</span></span>  
  
## <a name="mouse-events"></a><span data-ttu-id="0eb0b-118">Événements de souris</span><span class="sxs-lookup"><span data-stu-id="0eb0b-118">Mouse Events</span></span>  
 <span data-ttu-id="0eb0b-119">Les événements de souris que votre contrôle peut gérer sont <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseHover>, <xref:System.Windows.Forms.Control.MouseLeave>, <xref:System.Windows.Forms.Control.MouseMove>, et <xref:System.Windows.Forms.Control.MouseUp>.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-119">The mouse events that your control can handle are <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseHover>, <xref:System.Windows.Forms.Control.MouseLeave>, <xref:System.Windows.Forms.Control.MouseMove>, and <xref:System.Windows.Forms.Control.MouseUp>.</span></span>  
  
|<span data-ttu-id="0eb0b-120">Nom de l'événement</span><span class="sxs-lookup"><span data-stu-id="0eb0b-120">Event Name</span></span>|<span data-ttu-id="0eb0b-121">Méthode à substituer</span><span class="sxs-lookup"><span data-stu-id="0eb0b-121">Method to Override</span></span>|<span data-ttu-id="0eb0b-122">Description de l’événement</span><span class="sxs-lookup"><span data-stu-id="0eb0b-122">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|<span data-ttu-id="0eb0b-123">Déclenché quand le bouton de la souris est enfoncé alors que le pointeur se trouve sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-123">Raised when the mouse button is pressed while the pointer is over the control.</span></span>|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|<span data-ttu-id="0eb0b-124">Déclenché lorsque le pointeur pénètre la première fois dans la zone du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-124">Raised when the pointer first enters the region of the control.</span></span>|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|<span data-ttu-id="0eb0b-125">Déclenché lorsque le pointeur pointe sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-125">Raised when the pointer hovers over the control.</span></span>|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|<span data-ttu-id="0eb0b-126">Déclenché lorsque le pointeur quitte la zone du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-126">Raised when the pointer leaves the region of the control.</span></span>|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|<span data-ttu-id="0eb0b-127">Déclenché lorsque le pointeur se déplace dans la zone du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-127">Raised when the pointer moves in the region of the control.</span></span>|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|<span data-ttu-id="0eb0b-128">Déclenché lorsque le bouton de la souris est relâché alors que le pointeur se trouve sur le contrôle ou quitte la zone du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-128">Raised when the mouse button is released while the pointer is over the control or the pointer leaves the region of the control.</span></span>|  
  
 <span data-ttu-id="0eb0b-129">Le fragment de code suivant montre un exemple de substitution de la <xref:System.Windows.Forms.Control.MouseDown> événement.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-129">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseDown> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 <span data-ttu-id="0eb0b-130">Le fragment de code suivant montre un exemple de substitution de la <xref:System.Windows.Forms.Control.MouseMove> événement.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-130">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseMove> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 <span data-ttu-id="0eb0b-131">Le fragment de code suivant montre un exemple de substitution de la <xref:System.Windows.Forms.Control.MouseUp> événement.</span><span class="sxs-lookup"><span data-stu-id="0eb0b-131">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseUp> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 <span data-ttu-id="0eb0b-132">Pour obtenir le code source complet pour l’exemple `FlashTrackBar`, consultez [Comment : créer un contrôle Windows Forms qui affiche la progression](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span><span class="sxs-lookup"><span data-stu-id="0eb0b-132">For the complete source code for the `FlashTrackBar` sample, see [How to: Create a Windows Forms Control That Shows Progress](../../../../docs/framework/winforms/controls/how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0eb0b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eb0b-133">See Also</span></span>  
 [<span data-ttu-id="0eb0b-134">Événements dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0eb0b-134">Events in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/events-in-windows-forms-controls.md)  
 [<span data-ttu-id="0eb0b-135">Définition d’un événement</span><span class="sxs-lookup"><span data-stu-id="0eb0b-135">Defining an Event</span></span>](../../../../docs/framework/winforms/controls/defining-an-event-in-windows-forms-controls.md)  
 [<span data-ttu-id="0eb0b-136">Événements</span><span class="sxs-lookup"><span data-stu-id="0eb0b-136">Events</span></span>](../../../../docs/standard/events/index.md)  
 [<span data-ttu-id="0eb0b-137">Entrées d’utilisateur dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0eb0b-137">User Input in Windows Forms</span></span>](../../../../docs/framework/winforms/user-input-in-windows-forms.md)
