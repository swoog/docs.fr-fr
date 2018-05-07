---
title: Vue d'ensemble du contrôle CheckBox (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- CheckBox
helpviewer_keywords:
- CheckBox control [Windows Forms], about CheckBox control
- data binding [Windows Forms], checkbox controls
- check boxes [Windows Forms], about check boxes
ms.assetid: 085a4e0b-9046-473f-b141-d0edddfb2ebb
ms.openlocfilehash: 54a0bba3923626398fb4d1b0af753177dfaa09a5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="checkbox-control-overview-windows-forms"></a>Vue d'ensemble du contrôle CheckBox (Windows Forms)
Le contrôle <xref:System.Windows.Forms.CheckBox> Windows Forms indique si une condition particulière est activée ou désactivée. Il est couramment utilisé pour présenter une sélection Oui/Non ou Vrai/Faux à l'utilisateur. Vous pouvez utiliser des contrôles de case à cocher dans des groupes pour afficher plusieurs choix à partir desquels l'utilisateur peut sélectionner un ou plusieurs éléments.  
  
 Le contrôle de case à cocher est similaire au contrôle de bouton radio, car chacun est utilisé pour indiquer une sélection est effectuée par l’utilisateur. Elles diffèrent dans ce qu’une case d’option dans un groupe peut être sélectionnée à la fois. Avec le contrôle de case à cocher, toutefois, un nombre quelconque de cases à cocher peut être sélectionné.  
  
 Une case à cocher peut être connecté aux éléments d’une base de données à l’aide de la liaison de données simple. Plusieurs cases à cocher peuvent être regroupées à l’aide de la <xref:System.Windows.Forms.GroupBox> contrôle. Cela est utile pour l’apparence visuelle et également pour la conception de l’interface utilisateur, dans la mesure où les contrôles groupés peuvent être déplacés ensemble dans le Concepteur de formulaires. Pour plus d’informations, consultez [une liaison de données Windows Forms](../../../../docs/framework/winforms/windows-forms-data-binding.md) et [du contrôle GroupBox](../../../../docs/framework/winforms/controls/groupbox-control-windows-forms.md).  
  
 Le <xref:System.Windows.Forms.CheckBox> contrôle possède deux propriétés importantes, <xref:System.Windows.Forms.CheckBox.Checked%2A> et <xref:System.Windows.Forms.CheckBox.CheckState%2A>. Le <xref:System.Windows.Forms.CheckBox.Checked%2A> propriété retourne `true` ou `false`. Le <xref:System.Windows.Forms.CheckBox.CheckState%2A> propriété retourne <xref:System.Windows.Forms.CheckState.Checked> ou <xref:System.Windows.Forms.CheckState.Unchecked>; ou, si le <xref:System.Windows.Forms.CheckBox.ThreeState%2A> est définie sur `true`, <xref:System.Windows.Forms.CheckBox.CheckState%2A> peut également retourner <xref:System.Windows.Forms.CheckState.Indeterminate>. Dans un état indéterminé, la zone s’affiche avec une apparence estompée pour indiquer que l’option n’est pas disponible.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.CheckBox>  
 [Guide pratique pour définir des options avec les contrôles CheckBox Windows Forms](../../../../docs/framework/winforms/controls/how-to-set-options-with-windows-forms-checkbox-controls.md)  
 [Guide pratique pour répondre à un clic du contrôle CheckBox Windows Forms](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-checkbox-clicks.md)  
 [CheckBox, contrôle](../../../../docs/framework/winforms/controls/checkbox-control-windows-forms.md)
