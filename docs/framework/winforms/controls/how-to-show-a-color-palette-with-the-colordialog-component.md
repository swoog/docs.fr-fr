---
title: 'Procédure : Afficher une Palette de couleurs avec le composant ColorDialog'
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
ms.openlocfilehash: 34da70280ff6e5b850469e7ba041cc7c7aaf1f47
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54637123"
---
# <a name="how-to-show-a-color-palette-with-the-colordialog-component"></a><span data-ttu-id="7acf4-102">Procédure : Afficher une Palette de couleurs avec le composant ColorDialog</span><span class="sxs-lookup"><span data-stu-id="7acf4-102">How to: Show a Color Palette with the ColorDialog Component</span></span>
<span data-ttu-id="7acf4-103">Le [ColorDialog](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md) composant affiche une palette de couleurs et retourne une propriété contenant la couleur sélectionnée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7acf4-103">The [ColorDialog](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md) component displays a palette of colors and returns a property containing the color the user has selected.</span></span>  
  
### <a name="to-choose-a-color-using-the-colordialog-component"></a><span data-ttu-id="7acf4-104">Pour choisir une couleur à l’aide du composant ColorDialog</span><span class="sxs-lookup"><span data-stu-id="7acf4-104">To choose a color using the ColorDialog component</span></span>  
  
1.  <span data-ttu-id="7acf4-105">Afficher la boîte de dialogue à l’aide de la <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="7acf4-105">Display the dialog box using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
2.  <span data-ttu-id="7acf4-106">Utilisez le <xref:System.Windows.Forms.DialogResult> propriété afin de déterminer comment la boîte de dialogue a été fermée.</span><span class="sxs-lookup"><span data-stu-id="7acf4-106">Use the <xref:System.Windows.Forms.DialogResult> property to determine how the dialog box was closed.</span></span>  
  
3.  <span data-ttu-id="7acf4-107">Utilisez le <xref:System.Windows.Forms.ColorDialog.Color%2A> propriété de la <xref:System.Windows.Forms.ColorDialog> composant pour définir la couleur choisie.</span><span class="sxs-lookup"><span data-stu-id="7acf4-107">Use the <xref:System.Windows.Forms.ColorDialog.Color%2A> property of the <xref:System.Windows.Forms.ColorDialog> component to set the chosen color.</span></span>  
  
     <span data-ttu-id="7acf4-108">Dans l’exemple ci-dessous, le <xref:System.Windows.Forms.Button> du contrôle <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements ouvre un <xref:System.Windows.Forms.ColorDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="7acf4-108">In the example below, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens a <xref:System.Windows.Forms.ColorDialog> component.</span></span> <span data-ttu-id="7acf4-109">Quand une couleur est choisie et l’utilisateur clique sur **OK**, le <xref:System.Windows.Forms.Button> couleur d’arrière-plan du contrôle est défini sur la couleur choisie.</span><span class="sxs-lookup"><span data-stu-id="7acf4-109">When a color is chosen and the user clicks **OK**, the <xref:System.Windows.Forms.Button> control's background color is set to the chosen color.</span></span> <span data-ttu-id="7acf4-110">L’exemple suppose que votre formulaire contient un <xref:System.Windows.Forms.Button> contrôle et un <xref:System.Windows.Forms.ColorDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="7acf4-110">The example assumes your form has a <xref:System.Windows.Forms.Button> control and a <xref:System.Windows.Forms.ColorDialog> component.</span></span>  
  
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
  
     <span data-ttu-id="7acf4-111">(Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="7acf4-111">(Visual C#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click +=   
       gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="7acf4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7acf4-112">See also</span></span>
- <xref:System.Windows.Forms.ColorDialog>
- [<span data-ttu-id="7acf4-113">ColorDialog, composant</span><span class="sxs-lookup"><span data-stu-id="7acf4-113">ColorDialog Component</span></span>](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md)
