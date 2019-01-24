---
title: 'Procédure : Activer la réorganisation des éléments ToolStrip au moment de l’exécution dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], examples
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], rearranging controls
- ToolStrip control [Windows Forms], reordering items
ms.assetid: 8480b69a-379f-4dc2-8dcf-365ed93692b2
ms.openlocfilehash: 0b3662a700d897607780e8d5032c498faff97753
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577017"
---
# <a name="how-to-enable-reordering-of-toolstrip-items-at-run-time-in-windows-forms"></a>Procédure : Activer la réorganisation des éléments ToolStrip au moment de l’exécution dans les Windows Forms
Vous pouvez autoriser l’utilisateur à réorganiser <xref:System.Windows.Forms.ToolStripItem> contrôle sur le <xref:System.Windows.Forms.ToolStrip>.  
  
### <a name="to-enable-toolstripitem-rearrangement-at-run-time"></a>Pour activer la réorganisation ToolStripItem au moment de l’exécution  
  
-   Affectez à la propriété <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> la valeur `true`. Par défaut, <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> est `false`.  
  
     Au moment de l’exécution, l’utilisateur maintient enfoncée la touche ALT et le bouton gauche de la souris pour faire glisser un <xref:System.Windows.Forms.ToolStripItem> vers un autre emplacement sur le <xref:System.Windows.Forms.ToolStrip>.  
  
    ```vb  
    toolStrip1.AllowItemReorder = True  
    ```  
  
    ```csharp  
    toolStrip1.AllowItemReorder = true;  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>
- [Vue d’ensemble du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
- [Architecture du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)
- [Résumé de la technologie ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
