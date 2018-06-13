---
title: 'Comment : déterminer le moment où les attributs de mise en forme changent dans le contrôle RichTextBox Windows Forms'
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
ms.openlocfilehash: 789a0a25c65185b101ef427ff62871fa490c7f1d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33525212"
---
# <a name="how-to-determine-when-formatting-attributes-change-in-the-windows-forms-richtextbox-control"></a><span data-ttu-id="6641a-102">Comment : déterminer le moment où les attributs de mise en forme changent dans le contrôle RichTextBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6641a-102">How to: Determine When Formatting Attributes Change in the Windows Forms RichTextBox Control</span></span>
<span data-ttu-id="6641a-103">Une utilisation courante de Windows Forms <xref:System.Windows.Forms.RichTextBox> est mise en forme du texte avec des attributs, tels que les options de police ou des styles de paragraphe.</span><span class="sxs-lookup"><span data-stu-id="6641a-103">A common use of the Windows Forms <xref:System.Windows.Forms.RichTextBox> control is formatting text with attributes such as font options or paragraph styles.</span></span> <span data-ttu-id="6641a-104">Votre application peut besoin suivre les modifications apportées à la mise en forme en vue d’afficher une barre d’outils, comme dans nombreuses applications de traitement de texte.</span><span class="sxs-lookup"><span data-stu-id="6641a-104">Your application may need to keep track of any changes in text formatting for the purpose of displaying a toolbar, as in many word-processing applications.</span></span>  
  
### <a name="to-respond-to-changes-in-formatting-attributes"></a><span data-ttu-id="6641a-105">Pour répondre aux modifications apportées aux attributs de mise en forme</span><span class="sxs-lookup"><span data-stu-id="6641a-105">To respond to changes in formatting attributes</span></span>  
  
1.  <span data-ttu-id="6641a-106">Écrire du code dans le <xref:System.Windows.Forms.RichTextBox.SelectionChanged> Gestionnaire d’événements pour effectuer une action appropriée en fonction de la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="6641a-106">Write code in the <xref:System.Windows.Forms.RichTextBox.SelectionChanged> event handler to perform an appropriate action depending on the value of the attribute.</span></span> <span data-ttu-id="6641a-107">L’exemple suivant modifie l’apparence d’un bouton de barre d’outils en fonction de la valeur de la <xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="6641a-107">The following example changes the appearance of a toolbar button depending on the value of the <xref:System.Windows.Forms.RichTextBox.SelectionBullet%2A> property.</span></span> <span data-ttu-id="6641a-108">Le bouton de barre d’outils est actualisé seulement lorsque le point d’insertion est placé dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="6641a-108">The toolbar button will only be updated when the insertion point is moved in the control.</span></span>  
  
     <span data-ttu-id="6641a-109">L’exemple ci-dessous illustre un formulaire avec un <xref:System.Windows.Forms.RichTextBox> contrôle et un <xref:System.Windows.Forms.ToolBar> contrôle qui contient un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="6641a-109">The example below assumes a form with a <xref:System.Windows.Forms.RichTextBox> control and a <xref:System.Windows.Forms.ToolBar> control that contains a toolbar button.</span></span> <span data-ttu-id="6641a-110">Pour plus d’informations sur les barres d’outils et des boutons de barre d’outils, consultez [Comment : ajouter des boutons à un contrôle de barre d’outils](../../../../docs/framework/winforms/controls/how-to-add-buttons-to-a-toolbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="6641a-110">For more information about toolbars and toolbar buttons, see [How to: Add Buttons to a ToolBar Control](../../../../docs/framework/winforms/controls/how-to-add-buttons-to-a-toolbar-control.md).</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="6641a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6641a-111">See Also</span></span>  
 <xref:System.Windows.Forms.RichTextBox.SelectionChanged>  
 <xref:System.Windows.Forms.RichTextBox>  
 [<span data-ttu-id="6641a-112">RichTextBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="6641a-112">RichTextBox Control</span></span>](../../../../docs/framework/winforms/controls/richtextbox-control-windows-forms.md)  
 [<span data-ttu-id="6641a-113">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6641a-113">Controls to Use on Windows Forms</span></span>](../../../../docs/framework/winforms/controls/controls-to-use-on-windows-forms.md)
