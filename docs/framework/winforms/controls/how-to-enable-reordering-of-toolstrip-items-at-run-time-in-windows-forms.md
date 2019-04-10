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
ms.openlocfilehash: daff9d6d351db514d552225853f977775f8e3204
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59220400"
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
- [Vue d’ensemble du contrôle ToolStrip](toolstrip-control-overview-windows-forms.md)
- [Architecture du contrôle ToolStrip](toolstrip-control-architecture.md)
- [Résumé de la technologie ToolStrip](toolstrip-technology-summary.md)
