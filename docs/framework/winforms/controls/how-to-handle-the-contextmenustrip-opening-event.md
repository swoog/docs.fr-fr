---
title: 'Procédure : Gérer l’événement d’ouverture ContextMenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- context menus [Windows Forms], event handling
- ToolStrip control [Windows Forms]
- event handling [Windows Forms], context menus
- shortcut menus [Windows Forms], event handling
ms.assetid: b661b3dd-7815-4cc2-a1aa-a9a391ab3427
ms.openlocfilehash: 179411da96362fd9ba42e2b97682f335beb894c1
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715449"
---
# <a name="how-to-handle-the-contextmenustrip-opening-event"></a><span data-ttu-id="58217-102">Procédure : Gérer l’événement d’ouverture ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="58217-102">How to: Handle the ContextMenuStrip Opening Event</span></span>
<span data-ttu-id="58217-103">Vous pouvez personnaliser le comportement de votre <xref:System.Windows.Forms.ContextMenuStrip> contrôle en gérant la <xref:System.Windows.Forms.ToolStripDropDown.Opening> événement.</span><span class="sxs-lookup"><span data-stu-id="58217-103">You can customize the behavior of your <xref:System.Windows.Forms.ContextMenuStrip> control by handling the <xref:System.Windows.Forms.ToolStripDropDown.Opening> event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58217-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="58217-104">Example</span></span>  
 <span data-ttu-id="58217-105">L’exemple de code suivant montre comment gérer les <xref:System.Windows.Forms.ToolStripDropDown.Opening> événement.</span><span class="sxs-lookup"><span data-stu-id="58217-105">The following code example demonstrates how to handle the <xref:System.Windows.Forms.ToolStripDropDown.Opening> event.</span></span> <span data-ttu-id="58217-106">Le Gestionnaire d’événements ajoute des éléments dynamiquement à un <xref:System.Windows.Forms.ContextMenuStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="58217-106">The event handler adds items dynamically to a <xref:System.Windows.Forms.ContextMenuStrip> control.</span></span> <span data-ttu-id="58217-107">Pour l’exemple de code complet, consultez [Comment : Ajouter dynamiquement des éléments ToolStrip](how-to-add-toolstrip-items-dynamically.md).</span><span class="sxs-lookup"><span data-stu-id="58217-107">For the complete code example, see [How to: Add ToolStrip Items Dynamically](how-to-add-toolstrip-items-dynamically.md).</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#42)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#42)]  
  
 <span data-ttu-id="58217-108">Définir le <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> propriété `true` pour empêcher l’ouverture du menu.</span><span class="sxs-lookup"><span data-stu-id="58217-108">Set the <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> property to `true` to prevent the menu from opening.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58217-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58217-109">See also</span></span>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [<span data-ttu-id="58217-110">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="58217-110">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
