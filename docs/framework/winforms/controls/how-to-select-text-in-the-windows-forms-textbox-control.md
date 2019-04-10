---
title: 'Procédure : sélectionner du texte dans le contrôle TextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], selecting text programmatically
- text boxes [Windows Forms], selecting text programmatically
- text [Windows Forms], selecting in text boxes programmatically
ms.assetid: 8c591546-6a01-45c7-8e03-f78431f903b1
ms.openlocfilehash: 3bb1245cd47084935d632ff345a32058db6074e1
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59321708"
---
# <a name="how-to-select-text-in-the-windows-forms-textbox-control"></a>Procédure : sélectionner du texte dans le contrôle TextBox Windows Forms
Vous pouvez sélectionner le texte par programmation dans les formulaires Windows <xref:System.Windows.Forms.TextBox> contrôle. Par exemple, si vous créez une fonction qui recherche du texte pour une chaîne particulière, vous pouvez sélectionner le texte afin d’alerter visuellement le lecteur de position de la chaîne trouvée.  
  
### <a name="to-select-text-programmatically"></a>Pour sélectionner le texte par programmation  
  
1. Définir le <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> propriété vers le début du texte que vous souhaitez sélectionner.  
  
     Le <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> propriété est un nombre qui indique le point d’insertion dans la chaîne de texte, 0 étant la position la plus à gauche. Si la <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> est définie sur une valeur égale ou supérieure au nombre de caractères dans la zone de texte, le point d’insertion est placé après le dernier caractère.  
  
2. Définir le <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriété à la longueur du texte que vous souhaitez sélectionner.  
  
     Le <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriété est une valeur numérique qui définit la largeur du point d’insertion. Définition de la <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> par un nombre supérieur à 0 ce nombre de caractères à sélectionner, en commençant à partir du point d’insertion actuel.  
  
3. (Facultatif) Accéder au texte sélectionné via la <xref:System.Windows.Forms.TextBoxBase.SelectedText%2A> propriété.  
  
     Le code ci-dessous sélectionne le contenu d’un texte boîte lorsque le contrôle <xref:System.Windows.Forms.Control.Enter> événement se produit. Cet exemple vérifie si la zone de texte a une valeur pour le <xref:System.Windows.Forms.TextBox.Text%2A> propriété qui n’est pas `null` ou une chaîne vide. Lorsque la zone de texte reçoit le focus, le texte actuel dans la zone de texte est sélectionné. Le `TextBox1_Enter` Gestionnaire d’événements doit être lié au contrôle ; pour plus d’informations, consultez [Comment : Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).  
  
     Pour tester cet exemple, appuyez sur la touche Tab jusqu'à ce que la zone de texte a le focus. Si vous cliquez dans la zone de texte, le texte est désélectionné.  
  
    ```vb  
    Private Sub TextBox1_Enter(ByVal sender As Object, ByVal e As System.EventArgs) Handles TextBox1.Enter  
       If (Not String.IsNullOrEmpty(TextBox1.Text)) Then  
          TextBox1.SelectionStart = 0  
          TextBox1.SelectionLength = TextBox1.Text.Length  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_Enter(object sender, System.EventArgs e){  
       if (!String.IsNullOrEmpty(textBox1.Text))  
       {  
          textBox1.SelectionStart = 0;  
          textBox1.SelectionLength = textBox1.Text.Length;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void textBox1_Enter(System::Object ^ sender,  
          System::EventArgs ^ e) {  
       if (!System::String::IsNullOrEmpty(textBox1->Text))  
       {  
          textBox1->SelectionStart = 0;  
          textBox1->SelectionLength = textBox1->Text->Length;  
       }  
    }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.TextBox>
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
- [Procédure : contrôler le point d’insertion dans un contrôle TextBox Windows Forms](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [Procédure : créer une zone de texte pour un mot de passe avec le contrôle TextBox Windows Forms](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [Procédure : créer une zone de texte en lecture seule](how-to-create-a-read-only-text-box-windows-forms.md)
- [Procédure : mettre des guillemets dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Procédure : voir plusieurs lignes dans le contrôle TextBox Windows Forms](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
