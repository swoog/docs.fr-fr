---
title: Vue d'ensemble du contrôle Panel (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Panel
helpviewer_keywords:
- grouping controls [Windows Forms], Panel control
- Panel control [Windows Forms], about Panel control
ms.assetid: b6b83636-2c39-4dad-89d6-f0fa41049a74
ms.openlocfilehash: d4976b3725d04162ac10242c486f57c4d2598769
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086362"
---
# <a name="panel-control-overview-windows-forms"></a>Vue d'ensemble du contrôle Panel (Windows Forms)
Windows Forms <xref:System.Windows.Forms.Panel> contrôles sont utilisés pour fournir un regroupement identifiable pour d’autres contrôles. En règle générale, vous utilisez pour diviser un formulaire par fonction. Par exemple, peut avoir un bon de commande qui spécifie des options de courrier de quels le lendemain à utiliser. Toutes les options dans un volet de regroupement donne à l’utilisateur un indice visuel logique. Au moment du design tous les contrôles peuvent être déplacés facilement — lorsque vous déplacez le <xref:System.Windows.Forms.Panel> contrôler, tous ses contrôles contenus déplacent, trop. Les contrôles regroupés dans un panneau sont accessibles via son <xref:System.Windows.Forms.Control.Controls%2A> propriété. Cette propriété retourne une collection de <xref:System.Windows.Forms.Control> instances, donc vous devrez généralement effectuer un cast d’un contrôle récupérées ainsi à son type spécifique.  
  
## <a name="panel-versus-groupbox"></a>Panneau par rapport à la zone de groupe  
 Le <xref:System.Windows.Forms.Panel> contrôle est similaire à la <xref:System.Windows.Forms.GroupBox> contrôler ; Toutefois, uniquement le <xref:System.Windows.Forms.Panel> contrôle peut avoir des barres de défilement et uniquement le <xref:System.Windows.Forms.GroupBox> contrôle affiche une légende.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Pour afficher les barres de défilement, définissez la <xref:System.Windows.Forms.ScrollableControl.AutoScroll%2A> propriété `true`. Vous pouvez également personnaliser l’apparence du panneau en définissant le <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.BackgroundImage%2A>, et <xref:System.Windows.Forms.Panel.BorderStyle%2A> propriétés. Pour plus d’informations sur la <xref:System.Windows.Forms.Control.BackColor%2A> et <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriétés, consultez [Comment : Définir l’arrière-plan d’un panneau](how-to-set-the-background-of-a-windows-forms-panel.md). Le <xref:System.Windows.Forms.Panel.BorderStyle%2A> propriété détermine si l’est entourée aucune bordure visible (<xref:System.Windows.Forms.BorderStyle.None>), une simple ligne (<xref:System.Windows.Forms.BorderStyle.FixedSingle>), ou d’une ligne ombrée (<xref:System.Windows.Forms.BorderStyle.Fixed3D>).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Panel>
- [GroupBox, contrôle](groupbox-control-windows-forms.md)
- [Guide pratique pour Contrôles de groupe avec le contrôle de panneau Windows Forms à l’aide du Concepteur](group-controls-with-wf-panel-control-using-the-designer.md)
- [Guide pratique pour Définir l’arrière-plan d’un contrôle Panel Windows Forms à l’aide du Concepteur](how-to-set-the-background-of-a-windows-forms-panel-using-the-designer.md)
