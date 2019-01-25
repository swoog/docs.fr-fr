---
title: 'Procédure : Utiliser des info-bulles dans les contrôles ToolStrip'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], adding tooltips
- toolbars [Windows Forms], adding tooltips
- tooltips [Windows Forms], adding
ms.assetid: c5d86024-a7c5-44ee-8b3f-2daf53d80d3e
ms.openlocfilehash: 60d024dcb023b3d6cfafb68263291acefb38e14a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54519158"
---
# <a name="how-to-use-tooltips-in-toolstrip-controls"></a>Procédure : Utiliser des info-bulles dans les contrôles ToolStrip
Vous pouvez afficher un <xref:System.Windows.Forms.ToolTip> pour le <xref:System.Windows.Forms.ToolStrip> contrôle souhaité en définissant le contrôle <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> propriété `true`.  
  
### <a name="to-display-a-tooltip"></a>Pour afficher une info-bulle  
  
-   Définir le <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> propriété du contrôle à `true`.  
  
     La valeur par défaut <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A?displayProperty=nameWithType> est `true`et la valeur par défaut de <xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A?displayProperty=nameWithType> et <xref:System.Windows.Forms.StatusStrip.ShowItemToolTips%2A?displayProperty=nameWithType> est `false`.  
  
### <a name="to-use-the-tooltiptext-property-for-the-tooltip-text-of-a-toolstripbutton"></a>Pour utiliser la propriété ToolTipText pour le texte d’info-bulle d’un ToolStripButton  
  
1.  Définir le <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A> propriété du bouton `true`.  
  
2.  Définir le <xref:System.Windows.Forms.ToolStripButton.AutoToolTip%2A?displayProperty=nameWithType> propriété du bouton `false`.  
  
     Le `AutoToolTip` propriété est `true` par défaut pour <xref:System.Windows.Forms.ToolStripButton>, <xref:System.Windows.Forms.ToolStripDropDownButton>, et <xref:System.Windows.Forms.ToolStripSplitButton>.  
  
     Un <xref:System.Windows.Forms.ToolStripButton> utilise son `Text` propriété pour la <xref:System.Windows.Forms.ToolTip> texte par défaut. Utilisez cette procédure pour afficher un texte personnalisé dans un <xref:System.Windows.Forms.ToolStripButton> <xref:System.Windows.Forms.ToolTip>.  
  
> [!NOTE]
>  Si vous définissez <xref:System.Windows.Forms.ToolStripItemDisplayStyle> à <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None> ou <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Image>, aucun texte n’apparaît sur le bouton, mais l’info-bulle apparaît toujours.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ToolStrip.ShowItemToolTips%2A>
- <xref:System.Windows.Forms.ToolStripButton>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- <xref:System.Windows.Forms.ToolStripSplitButton>
- [Vue d’ensemble du contrôle ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
