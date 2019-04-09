---
title: 'Procédure : désigner un bouton Windows Forms comme bouton Annuler à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: be0847d1837ec85ed9d82dc7cc879d0cffa19cd6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59156219"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a>Procédure : désigner un bouton Windows Forms comme bouton Annuler à l’aide du concepteur
Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle soit le bouton Annuler. Un bouton Annuler est activé chaque fois que l’utilisateur appuie sur la touche ÉCHAP, quels que soient les autres contrôles du formulaire a le focus. Ce bouton est généralement programmé pour permettre à l’utilisateur à quitter rapidement une opération sans effectuer d’action.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-designate-the-cancel-button"></a>Pour désigner le bouton Annuler  
  
1.  Sélectionnez le formulaire sur lequel réside le bouton.  
  
2.  Dans le **propriétés** fenêtre, définissez le formulaire <xref:System.Windows.Forms.Form.CancelButton%2A> propriété le <xref:System.Windows.Forms.Button> nom du contrôle.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [Vue d’ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Méthodes de sélection du contrôle Button Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Procédure : répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Procédure : désigner un bouton Windows Forms comme bouton Accepter à l’aide du concepteur](designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [Button, contrôle](button-control-windows-forms.md)
