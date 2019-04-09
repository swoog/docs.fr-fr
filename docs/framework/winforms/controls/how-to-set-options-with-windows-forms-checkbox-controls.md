---
title: 'Procédure : définir des options avec des contrôles CheckBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- checked
helpviewer_keywords:
- CheckBox control [Windows Forms], checked state
- check boxes [Windows Forms], using to set options
- CheckBox control [Windows Forms], using to set options
ms.assetid: 2ac70498-7e3e-4e07-8901-ccabaeb5fd3e
ms.openlocfilehash: 926e89272e9ebedb0668b26b96b1614e85e637ea
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59095917"
---
# <a name="how-to-set-options-with-windows-forms-checkbox-controls"></a>Procédure : définir des options avec des contrôles CheckBox Windows Forms
Un formulaire Windows <xref:System.Windows.Forms.CheckBox> contrôle est utilisé pour permettre aux utilisateurs vrai/faux ou Oui/non. Le contrôle affiche une coche lorsqu’il est sélectionné.  
  
### <a name="to-set-options-with-checkbox-controls"></a>Pour définir les options avec les contrôles de case à cocher  
  
1.  Examinez la valeur de la <xref:System.Windows.Forms.CheckBox.Checked%2A> propriété pour déterminer son état et utilise cette valeur pour définir une option.  
  
     Dans l’exemple de code ci-dessous, lorsque le <xref:System.Windows.Forms.CheckBox> du contrôle <xref:System.Windows.Forms.CheckBox.CheckedChanged> événement est déclenché, le formulaire <xref:System.Windows.Forms.Control.AllowDrop%2A> propriété est définie sur `false` si la case à cocher est activée. Cela est utile pour les situations où vous souhaitez limiter l’interaction de l’utilisateur.  
  
    ```vb  
    Private Sub CheckBox1_CheckedChanged(ByVal sender As System.Object, _  
       ByVal e As System.EventArgs) Handles CheckBox1.CheckedChanged  
       ' Determine the CheckState of the check box.  
       If CheckBox1.CheckState = CheckState.Checked Then  
          ' If checked, do not allow items to be dragged onto the form.  
          Me.AllowDrop = False  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_CheckedChanged(object sender, System.EventArgs e)  
    {  
       // Determine the CheckState of the check box.  
       if (checkBox1.CheckState == CheckState.Checked)   
       {  
          // If checked, do not allow items to be dragged onto the form.  
          this.AllowDrop = false;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          // Determine the CheckState of the check box.  
          if (checkBox1->CheckState == CheckState::Checked)   
          {  
             // If checked, do not allow items to be dragged onto the form.  
             this->AllowDrop = false;  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.CheckBox>
- [Vue d’ensemble du contrôle CheckBox](checkbox-control-overview-windows-forms.md)
- [Procédure : répondre aux clics sur des contrôles Checkbox Windows Forms](how-to-respond-to-windows-forms-checkbox-clicks.md)
- [CheckBox, contrôle](checkbox-control-windows-forms.md)
