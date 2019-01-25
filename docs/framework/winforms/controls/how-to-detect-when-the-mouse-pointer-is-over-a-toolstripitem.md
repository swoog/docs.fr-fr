---
title: 'Procédure : Détecter lorsque le pointeur de la souris est sur un ToolStripItem'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], detecting mouse movement
- ToolStrip control [Windows Forms], detecting mouse movement
- ToolStripItem class [Windows Forms], detecting mouse movement
- mouse [Windows Forms], detecting movement on toolbars
ms.assetid: d38b5082-aba7-4f6c-841b-bd9714e307fd
ms.openlocfilehash: 20fbc91773f431fc68f606f8aa9f24f4c0cc06bf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539595"
---
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a>Procédure : Détecter lorsque le pointeur de la souris est sur un ToolStripItem
Utilisez la procédure suivante pour détecter lorsque le pointeur de la souris est positionnée sur un <xref:System.Windows.Forms.ToolStripItem>.  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a>Pour détecter lorsque le pointeur se trouve sur un ToolStripItem  
  
-   Utilisez le <xref:System.Windows.Forms.ToolStripItem.Selected%2A> propriété pour les éléments dans lequel <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> est `true`.  
  
     Cela vous empêche d’avoir à synchroniser le <xref:System.Windows.Forms.ToolStripItem.MouseEnter> et <xref:System.Windows.Forms.ToolStripItem.MouseLeave> événements.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripItem.Selected%2A>
- [Vue d’ensemble du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
