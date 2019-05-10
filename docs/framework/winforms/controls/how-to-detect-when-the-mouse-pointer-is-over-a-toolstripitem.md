---
title: 'Procédure : détecter le moment auquel le pointeur de la souris est au-dessus d’un ToolStripItem'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], detecting mouse movement
- ToolStrip control [Windows Forms], detecting mouse movement
- ToolStripItem class [Windows Forms], detecting mouse movement
- mouse [Windows Forms], detecting movement on toolbars
ms.assetid: d38b5082-aba7-4f6c-841b-bd9714e307fd
ms.openlocfilehash: f01a9acb3a566be40d65fb075c8487d4e9cb6e73
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64623640"
---
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="bbad7-102">Procédure : détecter le moment auquel le pointeur de la souris est au-dessus d’un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="bbad7-102">How to: Detect When the Mouse Pointer Is Over a ToolStripItem</span></span>
<span data-ttu-id="bbad7-103">Utilisez la procédure suivante pour détecter lorsque le pointeur de la souris est positionnée sur un <xref:System.Windows.Forms.ToolStripItem>.</span><span class="sxs-lookup"><span data-stu-id="bbad7-103">Use the following procedure to detect when the mouse pointer is over a <xref:System.Windows.Forms.ToolStripItem>.</span></span>  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="bbad7-104">Pour détecter lorsque le pointeur se trouve sur un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="bbad7-104">To detect when the pointer is over a ToolStripItem</span></span>  
  
- <span data-ttu-id="bbad7-105">Utilisez le <xref:System.Windows.Forms.ToolStripItem.Selected%2A> propriété pour les éléments dans lequel <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> est `true`.</span><span class="sxs-lookup"><span data-stu-id="bbad7-105">Use the <xref:System.Windows.Forms.ToolStripItem.Selected%2A> property for items in which <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> is `true`.</span></span>  
  
     <span data-ttu-id="bbad7-106">Cela vous empêche d’avoir à synchroniser le <xref:System.Windows.Forms.ToolStripItem.MouseEnter> et <xref:System.Windows.Forms.ToolStripItem.MouseLeave> événements.</span><span class="sxs-lookup"><span data-stu-id="bbad7-106">This will prevent you from having to synchronize the <xref:System.Windows.Forms.ToolStripItem.MouseEnter> and <xref:System.Windows.Forms.ToolStripItem.MouseLeave> events.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbad7-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbad7-107">See also</span></span>

- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripItem.Selected%2A>
- [<span data-ttu-id="bbad7-108">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="bbad7-108">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
