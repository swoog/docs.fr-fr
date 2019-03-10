---
title: 'Procédure : Groupe Windows Forms contrôles RadioButton en tant qu’ensemble'
ms.date: 03/30/2017
helpviewer_keywords:
- radio buttons [Windows Forms], grouping
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
- RadioButton control [Windows Forms], grouping
ms.assetid: 58f8fe34-50b7-49d8-a2be-c271be3c6b32
ms.openlocfilehash: 2d0f32c506025c2d7f302bca67aa20e24d71a865
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723294"
---
# <a name="how-to-group-windows-forms-radiobutton-controls-to-function-as-a-set"></a>Procédure : Groupe Windows Forms contrôles RadioButton en tant qu’ensemble
Windows Forms <xref:System.Windows.Forms.RadioButton> contrôles sont conçus pour donner aux utilisateurs un choix parmi deux ou plusieurs paramètres, dont une seule peut être assignée à une procédure ou un objet. Par exemple, un groupe de <xref:System.Windows.Forms.RadioButton> contrôles peuvent afficher une liste d’opérateurs de package pour une commande, mais uniquement des transporteurs sera utilisé. Par conséquent seul <xref:System.Windows.Forms.RadioButton> à la fois peut être sélectionné, même s’il fait partie d’un groupe fonctionnel.  
  
 Groupe de cases d’option en dessinant comme à l’intérieur d’un conteneur un <xref:System.Windows.Forms.Panel> contrôle, un <xref:System.Windows.Forms.GroupBox> contrôle ou un formulaire. Toutes les cases d’option qui sont ajoutés directement à un formulaire devient un groupe. Pour ajouter des groupes distincts, vous devez les placer à l’intérieur de panneaux ou zones de groupe. Pour plus d’informations sur les panneaux ou zones de groupe, consultez [vue d’ensemble du contrôle de panneau](panel-control-overview-windows-forms.md) ou [vue d’ensemble du contrôle GroupBox](groupbox-control-overview-windows-forms.md).  
  
### <a name="to-group-radiobutton-controls-as-a-set-to-function-independently-of-other-sets"></a>Pour regrouper des contrôles RadioButton en tant qu’ensemble de la fonction indépendamment des autres jeux  
  
1.  Faites glisser un <xref:System.Windows.Forms.GroupBox> ou <xref:System.Windows.Forms.Panel> contrôler à partir de la **Windows Forms** onglet sur le **boîte à outils** vers le formulaire.  
  
2.  Dessiner <xref:System.Windows.Forms.RadioButton> contrôle sur le <xref:System.Windows.Forms.GroupBox> ou <xref:System.Windows.Forms.Panel> contrôle.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.RadioButton>
- [Vue d’ensemble du contrôle RadioButton](radiobutton-control-overview-windows-forms.md)
- [Vue d’ensemble du contrôle Panel](panel-control-overview-windows-forms.md)
- [Vue d’ensemble du contrôle GroupBox](groupbox-control-overview-windows-forms.md)
- [Vue d'ensemble du contrôle CheckBox](checkbox-control-overview-windows-forms.md)
- [RadioButton, contrôle](radiobutton-control-windows-forms.md)
