---
title: 'Procédure : Gérer le dépassement de capacité de ToolStrip dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], managing overflow
- toolbars [Windows Forms], managing overflow
- examples [Windows Forms], toolbars
- CanOverflow property
ms.assetid: fa10e0ad-4cbf-4c0d-9082-359c2f855d4e
ms.openlocfilehash: 5f26217c92aef1d568349aefb87dd5a882a0cf28
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541155"
---
# <a name="how-to-manage-toolstrip-overflow-in-windows-forms"></a>Procédure : Gérer le dépassement de capacité de ToolStrip dans les Windows Forms
Lorsque tous les éléments sur un <xref:System.Windows.Forms.ToolStrip> contrôle ne tiennent pas dans l’espace alloué, vous pouvez activer la fonctionnalité de dépassement de capacité sur le <xref:System.Windows.Forms.ToolStrip> et déterminer le comportement de dépassement de capacité de spécifiques <xref:System.Windows.Forms.ToolStripItem>s.  
  
 Lorsque vous ajoutez <xref:System.Windows.Forms.ToolStripItem>s qui nécessitent davantage d’espace est alloué à la <xref:System.Windows.Forms.ToolStrip> étant donné la taille du formulaire actuel, un <xref:System.Windows.Forms.ToolStripOverflowButton> apparaît automatiquement sur le <xref:System.Windows.Forms.ToolStrip>. Le <xref:System.Windows.Forms.ToolStripOverflowButton> s’affiche, et prenant en charge le dépassement de capacité des éléments sont déplacés dans le menu de dépassement de la liste déroulante. Cela vous permet de personnaliser les hiérarchiser comment votre <xref:System.Windows.Forms.ToolStrip> éléments s’ajustent aux différentes tailles de formulaire. Vous pouvez également modifier l’apparence de vos éléments lorsqu’elles se trouvent dans le dépassement de capacité à l’aide de la <xref:System.Windows.Forms.ToolStripItem.Placement%2A> et <xref:System.Windows.Forms.ToolStripOverflow.DisplayedItems%2A?displayProperty=nameWithType> propriétés et le <xref:System.Windows.Forms.ToolStrip.LayoutCompleted> événement. Si vous agrandissez le formulaire au moment du design ou au moment de l’exécution, plus <xref:System.Windows.Forms.ToolStripItem>s peuvent être affichées sur les principaux <xref:System.Windows.Forms.ToolStrip> et <xref:System.Windows.Forms.ToolStripOverflowButton> peut même disparaître jusqu'à ce que vous diminuez la taille du formulaire.  
  
### <a name="to-enable-overflow-on-a-toolstrip-control"></a>Pour activer le dépassement de capacité sur un contrôle ToolStrip  
  
-   Vérifiez que le <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> propriété n’est pas définie sur `false` pour le <xref:System.Windows.Forms.ToolStrip>. La valeur par défaut est `True`.  
  
     Lorsque <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A> est `True` (la valeur par défaut), un <xref:System.Windows.Forms.ToolStripItem> est envoyé au menu déroulant de dépassement de capacité lorsque le contenu de la <xref:System.Windows.Forms.ToolStripItem> dépasse la largeur d’un horizontal <xref:System.Windows.Forms.ToolStrip> ou la hauteur d’une verticale <xref:System.Windows.Forms.ToolStrip>.  
  
### <a name="to-specify-overflow-behavior-of-a-specific-toolstripitem"></a>Pour spécifier le comportement de dépassement de capacité d’un ToolStripItem spécifique  
  
-   Définir le <xref:System.Windows.Forms.ToolStripItem.Overflow%2A> propriété de la <xref:System.Windows.Forms.ToolStripItem> sur la valeur souhaitée. Les possibilités sont `Always`, `Never`, et `AsNeeded`. Le defaultis `AsNeeded`.  
  
    ```vb  
    toolStripTextBox1.Overflow = _  
    System.Windows.Forms.ToolStripItemOverflow.Never  
    ```  
  
    ```csharp  
    toolStripTextBox1.Overflow = _  
    System.Windows.Forms.ToolStripItemOverflow.Never;  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripOverflowButton>
- <xref:System.Windows.Forms.ToolStripItem.Overflow%2A>
- <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>
- [Vue d’ensemble du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
- [Architecture du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)
- [Résumé de la technologie ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
