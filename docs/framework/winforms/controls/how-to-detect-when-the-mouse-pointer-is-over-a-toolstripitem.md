---
title: 'Procédure : Détecter lorsque le pointeur de la souris est sur un ToolStripItem'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], detecting mouse movement
- ToolStrip control [Windows Forms], detecting mouse movement
- ToolStripItem class [Windows Forms], detecting mouse movement
- mouse [Windows Forms], detecting movement on toolbars
ms.assetid: d38b5082-aba7-4f6c-841b-bd9714e307fd
ms.openlocfilehash: 39173490c31711cca9f26f5f0cb2ab493546dda3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720810"
---
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="76161-102">Procédure : Détecter lorsque le pointeur de la souris est sur un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="76161-102">How to: Detect When the Mouse Pointer Is Over a ToolStripItem</span></span>
<span data-ttu-id="76161-103">Utilisez la procédure suivante pour détecter lorsque le pointeur de la souris est positionnée sur un <xref:System.Windows.Forms.ToolStripItem>.</span><span class="sxs-lookup"><span data-stu-id="76161-103">Use the following procedure to detect when the mouse pointer is over a <xref:System.Windows.Forms.ToolStripItem>.</span></span>  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="76161-104">Pour détecter lorsque le pointeur se trouve sur un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="76161-104">To detect when the pointer is over a ToolStripItem</span></span>  
  
-   <span data-ttu-id="76161-105">Utilisez le <xref:System.Windows.Forms.ToolStripItem.Selected%2A> propriété pour les éléments dans lequel <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> est `true`.</span><span class="sxs-lookup"><span data-stu-id="76161-105">Use the <xref:System.Windows.Forms.ToolStripItem.Selected%2A> property for items in which <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> is `true`.</span></span>  
  
     <span data-ttu-id="76161-106">Cela vous empêche d’avoir à synchroniser le <xref:System.Windows.Forms.ToolStripItem.MouseEnter> et <xref:System.Windows.Forms.ToolStripItem.MouseLeave> événements.</span><span class="sxs-lookup"><span data-stu-id="76161-106">This will prevent you from having to synchronize the <xref:System.Windows.Forms.ToolStripItem.MouseEnter> and <xref:System.Windows.Forms.ToolStripItem.MouseLeave> events.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76161-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76161-107">See also</span></span>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripItem.Selected%2A>
- [<span data-ttu-id="76161-108">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="76161-108">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
