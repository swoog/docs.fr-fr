---
title: "Comment : afficher une palette de couleurs à l'aide du composant ColorDialog"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- palettes [Windows Forms], showing color
- color dialog box [Windows Forms], showing color palettes
- colors [Windows Forms], allowing users to select
- color palettes [Windows Forms], dialog box
- ColorDialog component [Windows Forms], showing color palettes
- color palettes [Windows Forms], showing in ColorDialog component
- colors [Windows Forms], showing palettes
ms.assetid: ee050f61-dbc8-4436-ba22-51360981ab48
ms.openlocfilehash: ea12fe19b6c8c7464f0820267face8a1d66de784
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33536925"
---
# <a name="how-to-show-a-color-palette-with-the-colordialog-component"></a>Comment : afficher une palette de couleurs à l'aide du composant ColorDialog
Le [ColorDialog](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md) composant affiche une palette de couleurs et retourne une propriété contenant la couleur sélectionnée par l’utilisateur.  
  
### <a name="to-choose-a-color-using-the-colordialog-component"></a>Pour choisir une couleur à l’aide du composant ColorDialog  
  
1.  Afficher la boîte de dialogue à l’aide de la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).  
  
2.  Utilisez le <xref:System.Windows.Forms.DialogResult> propriété pour déterminer comment la boîte de dialogue a été fermée.  
  
3.  Utilisez le <xref:System.Windows.Forms.ColorDialog.Color%2A> propriété de la <xref:System.Windows.Forms.ColorDialog> composant pour définir la couleur choisie.  
  
     Dans l’exemple ci-dessous, le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements ouvre un <xref:System.Windows.Forms.ColorDialog> composant. Lorsqu’une couleur est choisie et l’utilisateur clique sur **OK**, le <xref:System.Windows.Forms.Button> couleur d’arrière-plan du contrôle est défini sur la couleur choisie. L’exemple suppose que votre formulaire contient un <xref:System.Windows.Forms.Button> contrôle et un <xref:System.Windows.Forms.ColorDialog> composant.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles Button1.Click  
       If ColorDialog1.ShowDialog() = DialogResult.OK Then  
          Button1.BackColor = ColorDialog1.Color  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       if(colorDialog1.ShowDialog() == DialogResult.OK)  
       {  
          button1.BackColor = colorDialog1.Color;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,   
          System::EventArgs ^ e)  
       {  
          if(colorDialog1->ShowDialog() == DialogResult::OK)  
          {  
             button1->BackColor = colorDialog1->Color;  
          }  
       }  
    ```  
  
     (Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click +=   
       gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.ColorDialog>  
 [ColorDialog, composant](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md)
