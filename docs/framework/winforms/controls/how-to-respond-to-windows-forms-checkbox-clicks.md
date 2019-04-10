---
title: 'Procédure : répondre aux clics sur des contrôles Checkbox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Click event [Windows Forms], CheckBox control
- CheckBox control [Windows Forms], Click events
- events [Windows Forms], Click events
- double-clicks
- check boxes [Windows Forms], responding to events
ms.assetid: c39f901e-8899-43b6-aa31-939cbf7089fb
ms.openlocfilehash: 77f93dae2a91f282c6746c3fec3fb5f567cae2e3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211983"
---
# <a name="how-to-respond-to-windows-forms-checkbox-clicks"></a>Procédure : répondre aux clics sur des contrôles Checkbox Windows Forms
Chaque fois qu’un utilisateur clique sur un formulaire Windows <xref:System.Windows.Forms.CheckBox> contrôle, le <xref:System.Windows.Forms.Control.Click> événement se produit. Vous pouvez programmer votre application pour effectuer une action en fonction de l’état de la case à cocher.  
  
### <a name="to-respond-to-checkbox-clicks"></a>Pour répondre à un clic du contrôle CheckBox  
  
1.  Dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements, utilisez le <xref:System.Windows.Forms.CheckBox.Checked%2A> propriété pour déterminer l’état du contrôle et effectuer toute action requise.  
  
    ```vb  
    Private Sub CheckBox1_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles CheckBox1.Click  
       ' The CheckBox control's Text property is changed each time the   
       ' control is clicked, indicating a checked or unchecked state.  
       If CheckBox1.Checked = True Then  
          CheckBox1.Text = "Checked"  
       Else  
          CheckBox1.Text = "Unchecked"  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_Click(object sender, System.EventArgs e)  
    {  
       // The CheckBox control's Text property is changed each time the   
       // control is clicked, indicating a checked or unchecked state.  
       if (checkBox1.Checked)  
       {  
          checkBox1.Text = "Checked";  
       }  
       else  
       {  
          checkBox1.Text = "Unchecked";  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          if (checkBox1->Checked)  
          {  
             checkBox1->Text = "Checked";  
          }  
          else  
          {  
             checkBox1->Text = "Unchecked";  
          }  
       }  
    ```  
  
    > [!NOTE]
    >  Si l’utilisateur tente de double-cliquer sur le <xref:System.Windows.Forms.CheckBox> contrôle, chaque clic sera traité séparément ; autrement dit, la <xref:System.Windows.Forms.CheckBox> contrôle ne prend pas en charge l’événement de double-clic.  
  
    > [!NOTE]
    >  Lorsque le <xref:System.Windows.Forms.CheckBox.AutoCheck%2A> propriété est `true` (la valeur par défaut), le <xref:System.Windows.Forms.CheckBox> est automatiquement sélectionné ou effacé lorsque vous cliquez dessus. Sinon, vous devez définir manuellement le <xref:System.Windows.Forms.CheckBox.Checked%2A> propriété lorsque le <xref:System.Windows.Forms.Control.Click> événement se produit.  
  
     Vous pouvez également utiliser le <xref:System.Windows.Forms.CheckBox> contrôle pour déterminer l’action.  
  
### <a name="to-determine-a-course-of-action-when-a-check-box-is-clicked"></a>Pour déterminer l’action quand une case à cocher est cliqué.  
  
1.  Utilisez une instruction case pour interroger la valeur de la <xref:System.Windows.Forms.CheckBox.CheckState%2A> propriété afin de déterminer un plan d’action. Lorsque le <xref:System.Windows.Forms.CheckBox.ThreeState%2A> propriété est définie sur `true`, le <xref:System.Windows.Forms.CheckBox.CheckState%2A> propriété peut retourner trois valeurs possibles, qui représentent la case est cochée, la case désactivée ou un troisième état indéterminé dans lequel la zone est affichée avec un texte estompé apparence pour indiquer l’option n’est pas disponible.  
  
    ```vb  
    Private Sub CheckBox1_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles CheckBox1.Click  
       Select Case CheckBox1.CheckState  
          Case CheckState.Checked  
             ' Code for checked state.  
          Case CheckState.Unchecked  
             ' Code for unchecked state.  
          Case CheckState.Indeterminate  
             ' Code for indeterminate state.  
       End Select   
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_Click(object sender, System.EventArgs e)  
    {  
       switch(checkBox1.CheckState)  
       {  
          case CheckState.Checked:  
             // Code for checked state.  
             break;  
          case CheckState.Unchecked:  
             // Code for unchecked state.  
             break;  
          case CheckState.Indeterminate:  
             // Code for indeterminate state.  
             break;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          switch(checkBox1->CheckState) {  
             case CheckState::Checked:  
                // Code for checked state.  
                break;  
             case CheckState::Unchecked:  
                // Code for unchecked state.  
                break;  
             case CheckState::Indeterminate:  
                // Code for indeterminate state.  
                break;  
          }  
       }  
    ```  
  
    > [!NOTE]
    >  Lorsque le <xref:System.Windows.Forms.CheckBox.ThreeState%2A> propriété est définie sur `true`, le <xref:System.Windows.Forms.CheckBox.Checked%2A> retourne de la propriété `true` pour les deux <xref:System.Windows.Forms.CheckState.Checked> et <xref:System.Windows.Forms.CheckState.Indeterminate>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.CheckBox>
- [Vue d’ensemble du contrôle CheckBox](checkbox-control-overview-windows-forms.md)
- [Procédure : définir des options avec des contrôles CheckBox Windows Forms](how-to-set-options-with-windows-forms-checkbox-controls.md)
- [CheckBox, contrôle](checkbox-control-windows-forms.md)
