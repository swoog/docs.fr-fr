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
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a>Procédure : Détecter lorsque le pointeur de la souris est sur un ToolStripItem
Utilisez la procédure suivante pour détecter lorsque le pointeur de la souris est positionnée sur un <xref:System.Windows.Forms.ToolStripItem>.  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a>Pour détecter lorsque le pointeur se trouve sur un ToolStripItem  
  
-   Utilisez le <xref:System.Windows.Forms.ToolStripItem.Selected%2A> propriété pour les éléments dans lequel <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> est `true`.  
  
     Cela vous empêche d’avoir à synchroniser le <xref:System.Windows.Forms.ToolStripItem.MouseEnter> et <xref:System.Windows.Forms.ToolStripItem.MouseLeave> événements.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripItem.Selected%2A>
- [Vue d’ensemble du contrôle ToolStrip](toolstrip-control-overview-windows-forms.md)
