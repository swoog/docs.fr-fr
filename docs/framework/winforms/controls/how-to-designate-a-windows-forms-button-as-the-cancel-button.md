---
title: 'Procédure : désigner un bouton Windows Forms comme bouton Annuler'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 252f0834-e54b-44d9-96f7-ee5f50e94f2c
ms.openlocfilehash: ad95a527ea72858cc106c87d8712110e018e97b2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231433"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button"></a>Procédure : désigner un bouton Windows Forms comme bouton Annuler
Sur n’importe quel formulaire Windows, vous pouvez désigner un <xref:System.Windows.Forms.Button> contrôle soit le bouton Annuler. Un bouton Annuler est activé chaque fois que l’utilisateur appuie sur la touche ÉCHAP, quels que soient les autres contrôles du formulaire a le focus. Ce bouton est généralement programmé pour permettre à l’utilisateur à quitter rapidement une opération sans effectuer d’action.  
  
### <a name="to-designate-the-cancel-button"></a>Pour désigner le bouton Annuler  
  
1.  Définir le formulaire <xref:System.Windows.Forms.Form.CancelButton%2A> propriété appropriés <xref:System.Windows.Forms.Button> contrôle.  
  
    ```vb  
    Private Sub SetCancelButton(ByVal myCancelBtn As Button)  
       Me.CancelButton = myCancelBtn  
    End Sub  
    ```  
  
    ```csharp  
    private void SetCancelButton(Button myCancelBtn)  
    {  
       this.CancelButton = myCancelBtn;  
    }  
    ```  
  
    ```cpp  
    private:  
       void SetCancelButton(Button ^ myCancelBtn)  
       {  
          this->CancelButton = myCancelBtn;  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [Vue d’ensemble du contrôle Button](button-control-overview-windows-forms.md)
- [Méthodes de sélection du contrôle Button Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Procédure : répondre aux clics de bouton Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Procédure : désigner un bouton Windows Forms comme bouton Accepter](how-to-designate-a-windows-forms-button-as-the-accept-button.md)
- [Button, contrôle](button-control-windows-forms.md)
