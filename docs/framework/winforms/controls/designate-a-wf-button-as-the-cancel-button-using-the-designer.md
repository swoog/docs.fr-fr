---
title: "Comment : désigner un bouton Windows Forms comme bouton Annuler à l'aide du concepteur"
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: e94553a31ecdbf325c12815aa7a782cb68b95f19
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a>Comment : désigner un bouton Windows Forms comme bouton Annuler à l'aide du concepteur
Sur un Windows Form, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle soit le bouton Annuler. Un bouton cancel chaque fois que l’utilisateur appuie sur la touche ÉCHAP, quels que soient les autres contrôles du formulaire a le focus. Ce bouton est généralement programmé pour permettre à l’utilisateur de quitter rapidement une opération sans valider aucune action.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnalisation des paramètres de développement dans Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-designate-the-cancel-button"></a>Pour désigner le bouton Annuler  
  
1.  Sélectionnez le formulaire sur lequel se trouve le bouton.  
  
2.  Dans le **propriétés** , configurez du formulaire <xref:System.Windows.Forms.Form.CancelButton%2A> propriété le <xref:System.Windows.Forms.Button> nom du contrôle.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Form.CancelButton%2A>  
 [Vue d'ensemble du contrôle Button](../../../../docs/framework/winforms/controls/button-control-overview-windows-forms.md)  
 [Méthodes de sélection du contrôle Button Windows Forms](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)  
 [Guide pratique pour répondre à un clic du contrôle Button Windows Forms](../../../../docs/framework/winforms/controls/how-to-respond-to-windows-forms-button-clicks.md)  
 [Guide pratique pour désigner un bouton Windows Forms comme bouton Accepter à l’aide du concepteur](../../../../docs/framework/winforms/controls/designate-a-wf-button-as-the-accept-button-using-the-designer.md)  
 [Button, contrôle](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
