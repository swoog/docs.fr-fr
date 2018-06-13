---
title: Vue d'ensemble du contrôle Button (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Button
helpviewer_keywords:
- Button control [Windows Forms], about Button control
- buttons [Windows Forms], about buttons
ms.assetid: 255b291b-51a9-4a92-a1a4-2400cd82443f
ms.openlocfilehash: 88255882d3255eff112b9048a906182b64d75084
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33526020"
---
# <a name="button-control-overview-windows-forms"></a>Vue d'ensemble du contrôle Button (Windows Forms)
Le contrôle Windows Forms <xref:System.Windows.Forms.Button> permet à l'utilisateur d'effectuer une action en cliquant dessus. Quand le bouton est activé, il donne l'impression d'être enfoncé puis relâché. Chaque fois que l’utilisateur clique sur un bouton, le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements est appelé. Vous placez le code dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour exécuter toute action que vous choisissez.  
  
 Le texte affiché sur le bouton est contenu dans le <xref:System.Windows.Forms.Control.Text%2A> propriété. Si votre texte dépasse la largeur du bouton, il encapsule à la ligne suivante. Toutefois, il apparaît découpé si le contrôle ne peut pas prendre en charge sa hauteur totale. Pour plus d’informations, consultez [Comment : définir le texte affiché par un contrôle Windows Forms](../../../../docs/framework/winforms/controls/how-to-set-the-text-displayed-by-a-windows-forms-control.md). Le <xref:System.Windows.Forms.Control.Text%2A> propriété peut contenir une clé d’accès, ce qui permet à un utilisateur « sur « le contrôle en appuyant sur la touche ALT et la clé d’accès. Pour plus d’informations, consultez [Comment : créer de touches d’accès rapide pour les contrôles Windows Forms](../../../../docs/framework/winforms/controls/how-to-create-access-keys-for-windows-forms-controls.md). L’apparence du texte est contrôlée par le <xref:System.Windows.Forms.Control.Font%2A> propriété et le <xref:System.Windows.Forms.ButtonBase.TextAlign%2A> propriété.  
  
 Le <xref:System.Windows.Forms.Button> contrôle peut également afficher des images à l’aide de la <xref:System.Windows.Forms.ButtonBase.Image%2A> et <xref:System.Windows.Forms.ButtonBase.ImageList%2A> propriétés. Pour plus d’informations, consultez [Comment : définir l’Image affichée par un contrôle Windows Forms](../../../../docs/framework/winforms/controls/how-to-set-the-image-displayed-by-a-windows-forms-control.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Button>  
 [Guide pratique pour répondre à un clic du contrôle Button Windows Forms](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)  
 [Méthodes de sélection du contrôle Button Windows Forms](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)  
 [Guide pratique pour désigner un bouton Windows Forms comme bouton Accepter à l’aide du concepteur](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-accept-button-using-the-designer.md)  
 [Guide pratique pour désigner un bouton Windows Forms comme bouton Annuler à l’aide du concepteur](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-cancel-button-using-the-designer.md)  
 [Button, contrôle](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
