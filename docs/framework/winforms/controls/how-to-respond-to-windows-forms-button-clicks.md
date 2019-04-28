---
title: 'Procédure : répondre aux clics de bouton Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], responding to Click events
- events [Windows Forms], Click events
- Click event [Windows Forms], Button control
- MouseDown event
- Button control [Windows Forms], click response
- double-clicks
- examples [Windows Forms], controls
- Click event [Windows Forms], responding to
ms.assetid: 7a4951bd-369c-4662-b246-28ad83eda484
ms.openlocfilehash: a10eaa3ea62df9301a53f5609b503bfabcb50a46
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913079"
---
# <a name="how-to-respond-to-windows-forms-button-clicks"></a><span data-ttu-id="9cd69-102">Procédure : répondre aux clics de bouton Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9cd69-102">How to: Respond to Windows Forms Button Clicks</span></span>
<span data-ttu-id="9cd69-103">L’utilisation la plus élémentaire d’un formulaire Windows <xref:System.Windows.Forms.Button> contrôle consiste à exécuter du code lorsque le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="9cd69-103">The most basic use of a Windows Forms <xref:System.Windows.Forms.Button> control is to run some code when the button is clicked.</span></span>  
  
 <span data-ttu-id="9cd69-104">En cliquant sur un <xref:System.Windows.Forms.Button> contrôle génère également un nombre d’événements, tels que le <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseDown>, et <xref:System.Windows.Forms.Control.MouseUp> événements.</span><span class="sxs-lookup"><span data-stu-id="9cd69-104">Clicking a <xref:System.Windows.Forms.Button> control also generates a number of other events, such as the <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseDown>, and <xref:System.Windows.Forms.Control.MouseUp> events.</span></span> <span data-ttu-id="9cd69-105">Si vous avez l’intention d’attacher des gestionnaires d’événements pour ces événements connexes, veillez à ce que leurs actions ne sont pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="9cd69-105">If you intend to attach event handlers for these related events, be sure that their actions do not conflict.</span></span> <span data-ttu-id="9cd69-106">Par exemple, si vous cliquez sur le bouton efface les informations que l’utilisateur a tapé dans une zone de texte, suspendant le pointeur de la souris sur le bouton ne doit pas afficher une info-bulle contenant ces informations inexistante pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="9cd69-106">For example, if clicking the button clears information that the user has typed in a text box, pausing the mouse pointer over the button should not display a tool tip with that now-nonexistent information.</span></span>  
  
 <span data-ttu-id="9cd69-107">Si l’utilisateur tente de double-cliquer sur le <xref:System.Windows.Forms.Button> contrôle, chaque clic sera traité séparément ; autrement dit, le contrôle ne prend pas en charge l’événement de double-clic.</span><span class="sxs-lookup"><span data-stu-id="9cd69-107">If the user attempts to double-click the <xref:System.Windows.Forms.Button> control, each click will be processed separately; that is, the control does not support the double-click event.</span></span>  
  
### <a name="to-respond-to-a-button-click"></a><span data-ttu-id="9cd69-108">Pour répondre à un clic de bouton</span><span class="sxs-lookup"><span data-stu-id="9cd69-108">To respond to a button click</span></span>  
  
- <span data-ttu-id="9cd69-109">Dans le bouton `Click` <xref:System.EventHandler> écrire le code à exécuter.</span><span class="sxs-lookup"><span data-stu-id="9cd69-109">In the button's `Click` <xref:System.EventHandler> write the code to run.</span></span> <span data-ttu-id="9cd69-110">`Button1_Click` doit être lié au contrôle.</span><span class="sxs-lookup"><span data-stu-id="9cd69-110">`Button1_Click` must be bound to the control.</span></span> <span data-ttu-id="9cd69-111">Pour plus d'informations, voir [Procédure : Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="9cd69-111">For more information, see [How to: Create Event Handlers at Run Time for Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       MessageBox.Show("Button1 was clicked")  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       MessageBox.Show("button1 was clicked");  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          MessageBox::Show("button1 was clicked");  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="9cd69-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cd69-112">See also</span></span>

- [<span data-ttu-id="9cd69-113">Vue d'ensemble du contrôle Button</span><span class="sxs-lookup"><span data-stu-id="9cd69-113">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="9cd69-114">Méthodes de sélection du contrôle Button Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9cd69-114">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="9cd69-115">Button, contrôle</span><span class="sxs-lookup"><span data-stu-id="9cd69-115">Button Control</span></span>](button-control-windows-forms.md)
