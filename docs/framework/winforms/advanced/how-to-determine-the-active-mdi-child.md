---
title: 'Procédure : déterminer l’enfant MDI actif'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Clipboard [Windows Forms], copying data to
- MDI [Windows Forms], child windows
- child forms
- MDI [Windows Forms], activating forms
- MDI [Windows Forms], locating focus
ms.assetid: 33880ec3-0207-4c2b-a616-ff140443cc0f
ms.openlocfilehash: 9b70824670b8f47a2346135cb31ad39bd55694d1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59300604"
---
# <a name="how-to-determine-the-active-mdi-child"></a>Procédure : déterminer l’enfant MDI actif
Parfois, vous devez fournir une commande qui fonctionne sur le contrôle qui a le focus sur le formulaire enfant actif. Par exemple, supposons que vous souhaitez copier le texte sélectionné dans le Presse-papiers à partir de la zone de texte du formulaire enfant. Vous devez créer une procédure qui copie le texte sélectionné dans le Presse-papiers à l’aide de la <xref:System.Windows.Forms.Control.Click> événements de l’élément de menu Copier dans le menu Edition standard.  
  
 Comme une application MDI peut avoir plusieurs instances de la même forme enfant, la procédure doit connaître le formulaire à utiliser. Pour spécifier la forme correcte, utilisez le <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> propriété, qui retourne le formulaire enfant qui a le focus ou qui a été actif récemment.  
  
 Lorsque vous avez plusieurs contrôles sur un formulaire, vous devez également spécifier quel contrôle est actif. Comme le <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> propriété, le <xref:System.Windows.Forms.ContainerControl.ActiveControl%2A> propriété retourne le contrôle qui a le focus sur le formulaire enfant actif. La procédure ci-dessous illustre une procédure de copie qui peut être appelée à partir d’un menu de formulaire enfant, un menu sur le formulaire MDI ou un bouton de barre d’outils.  
  
### <a name="to-determine-the-active-mdi-child-to-copy-its-text-to-the-clipboard"></a>Pour déterminer l’enfant MDI actif (pour copier son texte dans le Presse-papiers)  
  
1. Dans une méthode, copiez le texte du contrôle actif du formulaire enfant active dans le Presse-papiers.  
  
    > [!NOTE]
    >  Cet exemple suppose il existe un formulaire MDI parent (`Form1`) qui a une ou plusieurs fenêtres MDI enfants contenant un <xref:System.Windows.Forms.RichTextBox> contrôle. Pour plus d’informations, consultez [création de formulaires MDI parents](how-to-create-mdi-parent-forms.md).  
  
    ```vb  
    Public Sub mniCopy_Click(ByVal sender As Object, _  
       ByVal e As System.EventArgs) Handles mniCopy.Click  
  
       ' Determine the active child form.  
       Dim activeChild As Form = Me.ActiveMDIChild  
  
       ' If there is an active child form, find the active control, which  
       ' in this example should be a RichTextBox.  
       If (Not activeChild Is Nothing) Then  
          Dim theBox As RichTextBox = _  
            TryCast(activeChild.ActiveControl, RichTextBox)  
  
          If (Not theBox Is Nothing) Then  
             'Put selected text on Clipboard.  
             Clipboard.SetDataObject(theBox.SelectedText)  
          Else  
             MessageBox.Show("You need to select a RichTextBox.")  
          End If  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    protected void mniCopy_Click (object sender, System.EventArgs e)  
    {  
       // Determine the active child form.  
       Form activeChild = this.ActiveMdiChild;  
  
       // If there is an active child form, find the active control, which  
       // in this example should be a RichTextBox.  
       if (activeChild != null)  
       {    
          try  
          {  
             RichTextBox theBox = (RichTextBox)activeChild.ActiveControl;  
             if (theBox != null)  
             {  
                // Put the selected text on the Clipboard.  
                Clipboard.SetDataObject(theBox.SelectedText);  
  
             }  
          }  
          catch  
          {  
             MessageBox.Show("You need to select a RichTextBox.");  
          }  
       }  
    }  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Applications d’interface multidocument (MDI, Multiple Document Interface)](multiple-document-interface-mdi-applications.md)
- [Guide pratique pour Créer des formulaires MDI parents](how-to-create-mdi-parent-forms.md)
- [Guide pratique pour Créer des formulaires MDI enfants](how-to-create-mdi-child-forms.md)
- [Guide pratique pour Envoyer des données à l’enfant MDI actif](how-to-send-data-to-the-active-mdi-child.md)
- [Guide pratique pour Réorganiser des formulaires MDI enfants](how-to-arrange-mdi-child-forms.md)
