---
title: 'Procédure : Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], entering passwords
- password boxes [Windows Forms], creating
- PasswordChar property in text boxes
- passwords [Windows Forms], input mask
- passwords [Windows Forms], password text box
ms.assetid: d105d6b9-3d50-44cd-80d8-2c0e2f486727
ms.openlocfilehash: 93be2378e812ce909adaf9b640b37f8056fc09c3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710808"
---
# <a name="how-to-create-a-password-text-box-with-the-windows-forms-textbox-control"></a>Procédure : Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms
Une zone de mot de passe est une zone de texte Windows Forms qui affiche les caractères d’espace réservé pendant qu’un utilisateur tape une chaîne.  
  
### <a name="to-create-a-password-text-box"></a>Pour créer une zone de texte mot de passe  
  
1.  Définir le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété de la <xref:System.Windows.Forms.TextBox> contrôle à un caractère spécifique.  
  
     Le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété spécifie le caractère affiché dans la zone de texte. Par exemple, si vous souhaitez que des astérisques s’affichent dans la zone de mot de passe, spécifiez * pour le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété dans la fenêtre Propriétés. Ensuite, indépendamment du caractère qu’un utilisateur tape dans la zone de texte, un astérisque est affiché.  
  
2.  (Facultatif) Définir le <xref:System.Windows.Forms.TextBoxBase.MaxLength%2A> propriété. La propriété détermine le nombre de caractères peut être tapé dans la zone de texte. Si la longueur maximale est dépassée, le système émet un signal sonore et la zone de texte n’accepte pas plus de caractères. Notez que vous ne pouvez pas effectuer cette opération car la longueur maximale d’un mot de passe peut-être être utiles aux pirates informatiques qui tentent de deviner le mot de passe.  
  
     L’exemple de code suivant montre comment initialiser une zone de texte qui acceptent une chaîne de 14 caractères au maximum et affichera des astérisques à la place de la chaîne. Le `InitializeMyControl` procédure s’exécutera pas automatiquement ; il doit être appelé.  
  
    > [!IMPORTANT]
    >  À l’aide de la <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété sur une zone de texte permet de garantir que les autres personnes ne sera pas en mesure de déterminer un mot de passe utilisateur observant l’entrer. Cette mesure de sécurité ne couvre pas une forme quelconque de stockage ou transmission du mot de passe qui peut se produire en raison de votre logique d’application. Étant donné que le texte entré n’est pas chiffré en aucune façon, vous devez le considérer comme vous le feriez pour d’autres données confidentielles. Même si elle n’apparaît pas en tant que tel, le mot de passe est toujours traité comme une chaîne de texte brut (sauf si vous avez implémenté certaines mesures de sécurité supplémentaires).  
  
    ```vb  
    Private Sub InitializeMyControl()  
       ' Set to no text.  
       TextBox1.Text = ""  
       ' The password character is an asterisk.  
       TextBox1.PasswordChar = "*"  
       ' The control will allow no more than 14 characters.  
       TextBox1.MaxLength = 14  
    End Sub  
    ```  
  
    ```csharp  
    private void InitializeMyControl()  
    {  
       // Set to no text.  
       textBox1.Text = "";  
       // The password character is an asterisk.  
       textBox1.PasswordChar = '*';  
       // The control will allow no more than 14 characters.  
       textBox1.MaxLength = 14;  
    }  
    ```  
  
    ```cpp  
    private:  
       void InitializeMyControl()  
       {  
          // Set to no text.  
          textBox1->Text = "";  
          // The password character is an asterisk.  
          textBox1->PasswordChar = '*';  
          // The control will allow no more than 14 characters.  
          textBox1->MaxLength = 14;  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TextBox>
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
- [Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte en lecture seule](how-to-create-a-read-only-text-box-windows-forms.md)
- [Guide pratique pour Placez des guillemets doubles dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
