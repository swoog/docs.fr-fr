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
ms.openlocfilehash: 881996563acef36a1981ca6236c155b8fc56ef0a
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59307307"
---
# <a name="how-to-set-options-with-windows-forms-checkbox-controls"></a><span data-ttu-id="5491f-102">Procédure : définir des options avec des contrôles CheckBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5491f-102">How to: Set Options with Windows Forms CheckBox Controls</span></span>
<span data-ttu-id="5491f-103">Un formulaire Windows <xref:System.Windows.Forms.CheckBox> contrôle est utilisé pour permettre aux utilisateurs vrai/faux ou Oui/non.</span><span class="sxs-lookup"><span data-stu-id="5491f-103">A Windows Forms <xref:System.Windows.Forms.CheckBox> control is used to give users True/False or Yes/No options.</span></span> <span data-ttu-id="5491f-104">Le contrôle affiche une coche lorsqu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5491f-104">The control displays a check mark when it is selected.</span></span>  
  
### <a name="to-set-options-with-checkbox-controls"></a><span data-ttu-id="5491f-105">Pour définir les options avec les contrôles de case à cocher</span><span class="sxs-lookup"><span data-stu-id="5491f-105">To set options with CheckBox controls</span></span>  
  
1. <span data-ttu-id="5491f-106">Examinez la valeur de la <xref:System.Windows.Forms.CheckBox.Checked%2A> propriété pour déterminer son état et utilise cette valeur pour définir une option.</span><span class="sxs-lookup"><span data-stu-id="5491f-106">Examine the value of the <xref:System.Windows.Forms.CheckBox.Checked%2A> property to determine its state, and use that value to set an option.</span></span>  
  
     <span data-ttu-id="5491f-107">Dans l’exemple de code ci-dessous, lorsque le <xref:System.Windows.Forms.CheckBox> du contrôle <xref:System.Windows.Forms.CheckBox.CheckedChanged> événement est déclenché, le formulaire <xref:System.Windows.Forms.Control.AllowDrop%2A> propriété est définie sur `false` si la case à cocher est activée.</span><span class="sxs-lookup"><span data-stu-id="5491f-107">In the code sample below, when the <xref:System.Windows.Forms.CheckBox> control's <xref:System.Windows.Forms.CheckBox.CheckedChanged> event is raised, the form's <xref:System.Windows.Forms.Control.AllowDrop%2A> property is set to `false` if the check box is checked.</span></span> <span data-ttu-id="5491f-108">Cela est utile pour les situations où vous souhaitez limiter l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5491f-108">This is useful for situations where you want to restrict user interaction.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="5491f-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5491f-109">See also</span></span>

- <xref:System.Windows.Forms.CheckBox>
- [<span data-ttu-id="5491f-110">Vue d’ensemble du contrôle CheckBox</span><span class="sxs-lookup"><span data-stu-id="5491f-110">CheckBox Control Overview</span></span>](checkbox-control-overview-windows-forms.md)
- [<span data-ttu-id="5491f-111">Procédure : répondre aux clics sur des contrôles Checkbox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5491f-111">How to: Respond to Windows Forms CheckBox Clicks</span></span>](how-to-respond-to-windows-forms-checkbox-clicks.md)
- [<span data-ttu-id="5491f-112">CheckBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="5491f-112">CheckBox Control</span></span>](checkbox-control-windows-forms.md)
