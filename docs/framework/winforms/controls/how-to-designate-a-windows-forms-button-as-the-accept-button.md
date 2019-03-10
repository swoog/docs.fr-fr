---
title: 'Procédure : Désigner un contrôle Button Windows Forms comme bouton Accepter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], default on Windows Forms
- Accept button on Windows Forms
- Button control [Windows Forms], designating as default
- Windows Forms controls, default button on form
ms.assetid: 22cc9da6-b913-4e04-9554-dee443ac5c3a
ms.openlocfilehash: 00d9f4acffb88b5047b40df91799cea1caaf2cf2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57714695"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-accept-button"></a>Procédure : Désigner un contrôle Button Windows Forms comme bouton Accepter
Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle de bouton Accepter, également connu sous le bouton par défaut. Chaque fois que l’utilisateur appuie sur la touche entrée, le bouton par défaut un clic sur quel autre contrôle sur le formulaire a le focus.  
  
> [!NOTE]
>  Les exceptions sont lorsque le contrôle ayant le focus est un autre bouton, dans ce cas, un clic sur le bouton qui a le focus, ou une zone de texte multiligne ou un contrôle personnalisé qui intercepte la touche ENTRÉE.  
  
### <a name="to-designate-the-accept-button"></a>Pour désigner le bouton Accepter  
  
1.  Définir le formulaire <xref:System.Windows.Forms.Form.AcceptButton%2A> propriété appropriés <xref:System.Windows.Forms.Button> contrôle.  
  
    ```vb  
    Private Sub SetDefault(ByVal myDefaultBtn As Button)  
      Me.AcceptButton = myDefaultBtn   
    End Sub  
    ```  
  
    ```csharp  
    private void SetDefault(Button myDefaultBtn)  
    {  
       this.AcceptButton = myDefaultBtn;  
    }  
    ```  
  
    ```cpp  
    private:  
       void SetDefault(Button ^ myDefaultBtn)  
       {  
          this->AcceptButton = myDefaultBtn;  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Form.AcceptButton%2A>
- [Vue d'ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Méthodes de sélection du contrôle Button Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Guide pratique pour Répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Guide pratique pour Désigner un contrôle Button Windows Forms comme bouton Annuler](how-to-designate-a-windows-forms-button-as-the-cancel-button.md)
- [Button, contrôle](button-control-windows-forms.md)
