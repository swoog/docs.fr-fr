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
ms.openlocfilehash: fe4c8fc3d2446b09add7336fa11670ff9ca8fed2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532111"
---
# <a name="how-to-handle-the-contextmenustrip-opening-event"></a>Procédure : Gérer l’événement d’ouverture ContextMenuStrip
Vous pouvez personnaliser le comportement de votre <xref:System.Windows.Forms.ContextMenuStrip> contrôle en gérant la <xref:System.Windows.Forms.ToolStripDropDown.Opening> événement.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment gérer les <xref:System.Windows.Forms.ToolStripDropDown.Opening> événement. Le Gestionnaire d’événements ajoute des éléments dynamiquement à un <xref:System.Windows.Forms.ContextMenuStrip> contrôle. Pour l’exemple de code complet, consultez [Comment : Ajouter dynamiquement des éléments ToolStrip](../../../../docs/framework/winforms/controls/how-to-add-toolstrip-items-dynamically.md).  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#42)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#42)]  
  
 Définir le <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> propriété `true` pour empêcher l’ouverture du menu.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [Contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
