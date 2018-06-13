---
title: Capture de la souris dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- mouse [Windows Forms], capture
ms.assetid: 8911d4b0-a4f8-4f93-8246-371aebd27d0c
ms.openlocfilehash: dfe983b9e407eddb9bed3bcc1a767cdeff38f2ab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33538406"
---
# <a name="mouse-capture-in-windows-forms"></a><span data-ttu-id="03cb4-102">Capture de la souris dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="03cb4-102">Mouse Capture in Windows Forms</span></span>
<span data-ttu-id="03cb4-103">*Capture de souris* signifie qu’un contrôle prend de toutes les entrées de souris.</span><span class="sxs-lookup"><span data-stu-id="03cb4-103">*Mouse capture* refers to when a control takes command of all mouse input.</span></span> <span data-ttu-id="03cb4-104">Lorsqu’un contrôle a capturé la souris, il reçoit l’entrée de la souris ou non le pointeur se trouve dans ses limites.</span><span class="sxs-lookup"><span data-stu-id="03cb4-104">When a control has captured the mouse, it receives mouse input whether or not the pointer is within its borders.</span></span>  
  
## <a name="setting-mouse-capture"></a><span data-ttu-id="03cb4-105">Définition de Capture de la souris</span><span class="sxs-lookup"><span data-stu-id="03cb4-105">Setting Mouse Capture</span></span>  
 <span data-ttu-id="03cb4-106">Dans les Windows Forms, la souris est capturée par le contrôle lorsque l’utilisateur appuie sur le bouton de la souris sur un contrôle, et la souris est relâchée par le contrôle lorsque l’utilisateur relâche le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="03cb4-106">In Windows Forms the mouse is captured by the control when the user presses a mouse button on a control, and the mouse is released by the control when the user releases the mouse button.</span></span>  
  
 <span data-ttu-id="03cb4-107">Le <xref:System.Windows.Forms.Control.Capture%2A> propriété de la <xref:System.Windows.Forms.Control> classe spécifie si un contrôle a capturé la souris.</span><span class="sxs-lookup"><span data-stu-id="03cb4-107">The <xref:System.Windows.Forms.Control.Capture%2A> property of the <xref:System.Windows.Forms.Control> class specifies whether a control has captured the mouse.</span></span> <span data-ttu-id="03cb4-108">Pour déterminer quand un contrôle perd la capture de la souris, gérez le <xref:System.Windows.Forms.Control.MouseCaptureChanged> événement.</span><span class="sxs-lookup"><span data-stu-id="03cb4-108">To determine when a control loses mouse capture, handle the <xref:System.Windows.Forms.Control.MouseCaptureChanged> event.</span></span>  
  
 <span data-ttu-id="03cb4-109">Seule la fenêtre de premier plan peut capturer la souris.</span><span class="sxs-lookup"><span data-stu-id="03cb4-109">Only the foreground window can capture the mouse.</span></span> <span data-ttu-id="03cb4-110">Lorsqu’une fenêtre d’arrière-plan tente de capturer la souris, la fenêtre reçoit des messages uniquement pour les événements de souris qui se produisent lorsque le pointeur de la souris se trouve dans la partie visible de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="03cb4-110">When a background window attempts to capture the mouse, the window receives messages only for mouse events that occur when the mouse pointer is within the visible portion of the window.</span></span> <span data-ttu-id="03cb4-111">En outre, même si la fenêtre de premier plan a capturé la souris, l’utilisateur peut toujours cliquer sur une autre fenêtre, mettre au premier plan.</span><span class="sxs-lookup"><span data-stu-id="03cb4-111">Also, even if the foreground window has captured the mouse, the user can still click another window, bringing it to the foreground.</span></span> <span data-ttu-id="03cb4-112">Lorsque la souris est capturée, les touches de raccourci ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="03cb4-112">When the mouse is captured, shortcut keys do not work.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03cb4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03cb4-113">See Also</span></span>  
 [<span data-ttu-id="03cb4-114">Entrée de la souris dans une application Windows Forms</span><span class="sxs-lookup"><span data-stu-id="03cb4-114">Mouse Input in a Windows Forms Application</span></span>](../../../docs/framework/winforms/mouse-input-in-a-windows-forms-application.md)
