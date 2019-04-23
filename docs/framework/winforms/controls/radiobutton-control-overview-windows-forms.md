---
title: Vue d'ensemble du contrôle RadioButton (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- RadioButton
helpviewer_keywords:
- RadioButton control [Windows Forms], about RadioButton control
- RadioButton control [Windows Forms], determining state
- radio buttons [Windows Forms], determining state
- radio buttons [Windows Forms], about radio buttons
ms.assetid: cd11f0c2-d098-4022-adf9-1455bc166a13
ms.openlocfilehash: 1210658226d9bcacbf4904fdc90a9908c34f5b73
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59129114"
---
# <a name="radiobutton-control-overview-windows-forms"></a>Vue d'ensemble du contrôle RadioButton (Windows Forms)
Windows Forms <xref:System.Windows.Forms.RadioButton> contrôle présente un ensemble de deux ou plusieurs choix qui s’excluent mutuellement à l’utilisateur. Tandis que les cases à cocher et des boutons radio peuvent sembler fonctionner de la même façon, il existe une différence importante : lorsqu’un utilisateur sélectionne un bouton radio, les autres cases d’option dans le même groupe ne peut pas être également sélectionnée. En revanche, un nombre quelconque de cases à cocher peut être sélectionné. Définition d’un groupe de cases d’option indique à l’utilisateur, « Voici un ensemble de choix à partir de laquelle vous pouvez choisir un seul et unique. »  
  
## <a name="using-the-control"></a>Utilisation du contrôle  
 Quand un <xref:System.Windows.Forms.RadioButton> clic sur le contrôle, son <xref:System.Windows.Forms.RadioButton.Checked%2A> propriété est définie sur `true` et le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements est appelé. Le <xref:System.Windows.Forms.RadioButton.CheckedChanged> événement est déclenché lorsque la valeur de la <xref:System.Windows.Forms.RadioButton.Checked%2A> les modifications de propriété. Si le <xref:System.Windows.Forms.RadioButton.AutoCheck%2A> propriété est définie sur `true` (la valeur par défaut), la case d’option est sélectionnée désactiver toutes les autres dans le groupe sont automatiquement. Cette propriété est généralement uniquement défini sur `false` lorsque le code de validation est utilisé s’assurer que la case d’option sélectionnée est une option autorisée. Le texte affiché dans le contrôle est défini avec la <xref:System.Windows.Forms.Control.Text%2A> propriété, qui peut contenir des raccourcis de touches d’accès. Une clé d’accès permet à un utilisateur de « click » sur le contrôle en appuyant sur la touche ALT et la clé d’accès. Pour plus d'informations, voir [Procédure : Créer des clés d’accès pour les contrôles de Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md) et [Comment : Définir le texte affiché par un Windows Forms contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control.md).  
  
 Le <xref:System.Windows.Forms.RadioButton> contrôle l’aspect d’un bouton de commande, ce qui semble avoir été sélectionné, si le <xref:System.Windows.Forms.RadioButton.Appearance%2A> propriété est définie sur <xref:System.Windows.Forms.Appearance.Button>. Cases d’option peuvent également afficher des images à l’aide de la <xref:System.Windows.Forms.ButtonBase.Image%2A> et <xref:System.Windows.Forms.ButtonBase.ImageList%2A> propriétés. Pour plus d'informations, voir [Procédure : Définir l’Image affichée par un Windows Forms contrôle](how-to-set-the-image-displayed-by-a-windows-forms-control.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RadioButton>
- [Vue d’ensemble du contrôle Panel](panel-control-overview-windows-forms.md)
- [Vue d’ensemble du contrôle GroupBox](groupbox-control-overview-windows-forms.md)
- [Vue d'ensemble du contrôle CheckBox](checkbox-control-overview-windows-forms.md)
- [Guide pratique pour Créer des clés d’accès pour les contrôles Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md)
- [Guide pratique pour Définir le texte affiché par un Windows Forms de contrôle](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [Guide pratique pour Groupe Windows Forms contrôles RadioButton en tant qu’ensemble](how-to-group-windows-forms-radiobutton-controls-to-function-as-a-set.md)
- [RadioButton, contrôle](radiobutton-control-windows-forms.md)
