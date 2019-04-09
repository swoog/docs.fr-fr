---
title: 'Procédure : déterminer à quel moment les attributs de mise en forme changent dans le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], text boxes
- RichTextBox control [Windows Forms], determining font changes
- text boxes [Windows Forms], determining font changes
- SelChange event
ms.assetid: bdfed015-f77a-41e5-b38f-f8629b2fa166
ms.openlocfilehash: e35ebb7c90be00a814d465af3546de2bcd11c5de
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59183939"
---
# <a name="how-to-determine-when-formatting-attributes-change-in-the-windows-forms-richtextbox-control"></a>Procédure : déterminer à quel moment les attributs de mise en forme changent dans le contrôle RichTextBox Windows Forms
Une utilisation courante des formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle est mise en forme de texte avec des attributs tels que les options de police ou des styles de paragraphe. Votre application peut avoir besoin d’effectuer le suivi de toutes les modifications de texte mise en forme en vue d’afficher une barre d’outils, comme dans nombreuses applications de traitement de texte.  
  
### <a name="to-respond-to-changes-in-formatting-attributes"></a>Pour répondre aux modifications de mise en forme des attributs  
  
1.  Écrire du code dans le <xref:System.Windows.Forms.RichTextBox.SelectionChanged> Gestionnaire d’événements pour effectuer une action appropriée selon la valeur de l’attribut. L’exemple suivant change l’apparence d’un bouton de barre d’outils en fonction de la valeur de la <xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A> propriété. Le bouton de barre d’outils est actualisé seulement lorsque le point d’insertion est déplacé dans le contrôle.  
  
     L’exemple suivant suppose un formulaire avec un <xref:System.Windows.Forms.RichTextBox> contrôle et un <xref:System.Windows.Forms.ToolBar> contrôle qui contient un bouton de barre d’outils. Pour plus d’informations sur les barres d’outils et boutons de barre d’outils, consultez [Comment : Ajouter des boutons à un contrôle de barre d’outils](how-to-add-buttons-to-a-toolbar-control.md).  
  
    ```vb  
    ' The following code assumes the existence of a toolbar control  
    ' with at least one toolbar button.  
    Private Sub RichTextBox1_SelectionChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles RichTextBox1.SelectionChanged  
       If RichTextBox1.SelectionBullet = True Then  
          ' Bullet button on toolbar should appear pressed  
          ToolBarButton1.Pushed = True  
       Else  
           ' Bullet button on toolbar should appear unpressed  
           ToolBarButton1.Pushed = False  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    // The following code assumes the existence of a toolbar control  
    // with at least one toolbar button.  
    private void richTextBox1_SelectionChanged(object sender,  
    System.EventArgs e)  
    {  
       if (richTextBox1.SelectionBullet == true)   
       {  
          // Bullet button on toolbar should appear pressed  
          toolBarButton1.Pushed = true;  
       }  
       else   
       {  
          // Bullet button on toolbar should appear unpressed  
          toolBarButton1.Pushed = false;  
       }  
    }  
    ```  
  
    ```cpp  
    // The following code assumes the existence of a toolbar control  
    // with at least one toolbar button.  
    private:  
       System::Void richTextBox1_SelectionChanged(  
          System::Object ^  sender, System::EventArgs ^  e)  
       {  
          if (richTextBox1->SelectionBullet == true)  
          {  
             // Bullet button on toolbar should appear pressed  
             toolBarButton1->Pushed = true;  
          }  
          else  
          {  
             // Bullet button on toolbar should appear unpressed  
             toolBarButton1->Pushed = false;  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.RichTextBox.SelectionChanged>
- <xref:System.Windows.Forms.RichTextBox>
- [RichTextBox, contrôle](richtextbox-control-windows-forms.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
