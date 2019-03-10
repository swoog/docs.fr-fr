---
title: 'Procédure : Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], insertion point
- insertion points [Windows Forms], TextBox controls
- text boxes [Windows Forms], controlling insertion point
ms.assetid: 5bee7d34-5121-429e-ab1f-d8ff67bc74c1
ms.openlocfilehash: cb3e7e7a44391ec7ee34ad0659f4185bd2304d26
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57714890"
---
# <a name="how-to-control-the-insertion-point-in-a-windows-forms-textbox-control"></a>Procédure : Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms
Lorsqu’un formulaire Windows <xref:System.Windows.Forms.TextBox> contrôle reçoit tout d’abord le focus, l’insertion de la valeur par défaut dans la zone de texte est à gauche du texte existant. L’utilisateur peut déplacer le point d’insertion avec le clavier ou la souris. Si la zone de texte perd, puis reprend le focus, le point d’insertion sera, là où l’utilisateur a placé en dernier.  
  
 Dans certains cas, ce comportement peut être déconcertant pour l’utilisateur. Dans un traitement de texte, l’utilisateur peut attendre de nouveaux caractères apparaissent après le texte existant. Dans une application de saisie de données, l’utilisateur peut attendre de nouveaux caractères à remplacer l’entrée existante. Le <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> et <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriétés vous permettent de modifier le comportement selon vos besoins.  
  
### <a name="to-control-the-insertion-point-in-a-textbox-control"></a>Pour contrôler le point d’insertion dans un contrôle TextBox  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.TextBoxBase.SelectionStart%2A> une valeur appropriée. Zéro place le point d’insertion immédiatement à gauche du premier caractère.  
  
2.  (Facultatif) Définir le <xref:System.Windows.Forms.TextBoxBase.SelectionLength%2A> propriété à la longueur du texte que vous souhaitez sélectionner.  
  
     Le code ci-dessous retourne toujours le point d’insertion à 0. Le `TextBox1_Enter` Gestionnaire d’événements doit être lié au contrôle ; pour plus d’informations, consultez [création de gestionnaires d’événements dans les Windows Forms](../creating-event-handlers-in-windows-forms.md).  
  
    ```vb  
    Private Sub TextBox1_Enter(ByVal sender As Object, ByVal e As System.EventArgs) Handles TextBox1.Enter  
       TextBox1.SelectionStart = 0  
       TextBox1.SelectionLength = 0  
    End Sub  
    ```  
  
    ```csharp  
    private void textBox1_Enter(Object sender, System.EventArgs e) {  
       textBox1.SelectionStart = 0;  
       textBox1.SelectionLength = 0;  
    }  
    ```  
  
    ```cpp  
    private:  
       void textBox1_Enter(System::Object ^  sender,  
          System::EventArgs ^  e)  
       {  
          textBox1->SelectionStart = 0;  
          textBox1->SelectionLength = 0;  
       }  
    ```  
  
## <a name="making-the-insertion-point-visible-by-default"></a>Le fait de rendre le Point d’Insertion Visible par défaut  
 Le <xref:System.Windows.Forms.TextBox> point d’insertion est visible par défaut dans un nouveau formulaire uniquement si le <xref:System.Windows.Forms.TextBox> contrôle apparaît en premier dans l’ordre de tabulation. Sinon, le point d’insertion s’affiche uniquement si vous donnez le <xref:System.Windows.Forms.TextBox> le focus du clavier ou la souris.  
  
#### <a name="to-make-the-text-box-insertion-point-visible-by-default-on-a-new-form"></a>Pour que l’insertion de zone de texte pointent visible par défaut sur un nouveau formulaire  
  
-   Définir le <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.Control.TabIndex%2A> propriété `0`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TextBox>
- [Vue d’ensemble du contrôle TextBox](textbox-control-overview-windows-forms.md)
- [Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [Guide pratique pour Créer une zone de texte en lecture seule](how-to-create-a-read-only-text-box-windows-forms.md)
- [Guide pratique pour Placez des guillemets doubles dans une chaîne](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [TextBox, contrôle](textbox-control-windows-forms.md)
