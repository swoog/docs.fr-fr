---
title: 'Procédure : déclencher des événements de menu pour des boutons de barre d’outils'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], toolbars
- ToolBar control [Windows Forms], click event handlers
- ToolBar control [Windows Forms], coding button click events
- toolbars [Windows Forms], click event handlers
ms.assetid: 98374f70-993d-4ca4-89fb-48fea6ce5b45
ms.openlocfilehash: 0f5afde1cc0be772baff373c84c82f81df284b9b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785825"
---
# <a name="how-to-trigger-menu-events-for-toolbar-buttons"></a><span data-ttu-id="28625-102">Procédure : déclencher des événements de menu pour des boutons de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="28625-102">How to: Trigger Menu Events for Toolbar Buttons</span></span>
> [!NOTE]
>  <span data-ttu-id="28625-103">Le contrôle <xref:System.Windows.Forms.ToolStrip> remplace le contrôle <xref:System.Windows.Forms.ToolBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.ToolBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="28625-103">The <xref:System.Windows.Forms.ToolStrip> control replaces and adds functionality to the <xref:System.Windows.Forms.ToolBar> control; however, the <xref:System.Windows.Forms.ToolBar> control is retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="28625-104">Si votre Windows Form contient un <xref:System.Windows.Forms.ToolBar> contrôle avec des boutons de barre d’outils, vous devez savoir sur quel bouton l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="28625-104">If your Windows Form features a <xref:System.Windows.Forms.ToolBar> control with toolbar buttons, you will want to know which button the user clicks.</span></span>  
  
 <span data-ttu-id="28625-105">Sur le <xref:System.Windows.Forms.ToolBar.ButtonClick> événements de la <xref:System.Windows.Forms.ToolBar> contrôle, vous pouvez évaluer le <xref:System.Windows.Forms.ToolBarButtonClickEventArgs.Button%2A> propriété de la <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> classe.</span><span class="sxs-lookup"><span data-stu-id="28625-105">On the <xref:System.Windows.Forms.ToolBar.ButtonClick> event of the <xref:System.Windows.Forms.ToolBar> control, you can evaluate the <xref:System.Windows.Forms.ToolBarButtonClickEventArgs.Button%2A> property of the <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> class.</span></span> <span data-ttu-id="28625-106">Dans l’exemple ci-dessous, une boîte de message s’affiche, indiquant sur quel bouton l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="28625-106">In the example below, a message box is shown, indicating which button was clicked.</span></span> <span data-ttu-id="28625-107">Pour plus d'informations, consultez <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="28625-107">For details, see <xref:System.Windows.Forms.MessageBox>.</span></span>  
  
 <span data-ttu-id="28625-108">L’exemple suivant suppose un <xref:System.Windows.Forms.ToolBar> contrôle a été ajouté à un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="28625-108">The example below assumes a <xref:System.Windows.Forms.ToolBar> control has been added to a Windows Form.</span></span>  
  
### <a name="to-handle-the-click-event-on-a-toolbar"></a><span data-ttu-id="28625-109">Pour gérer l’événement de clic sur une barre d’outils</span><span class="sxs-lookup"><span data-stu-id="28625-109">To handle the Click event on a toolbar</span></span>  
  
1. <span data-ttu-id="28625-110">Dans une procédure, ajoutez des boutons de barre d’outils à la <xref:System.Windows.Forms.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="28625-110">In a procedure, add toolbar buttons to the <xref:System.Windows.Forms.ToolBar> control.</span></span>  
  
    ```vb  
    Public Sub ToolBarConfig()  
    ' Instantiate the toolbar buttons, set their Text properties  
    ' and add them to the ToolBar control.  
       ToolBar1.Buttons.Add(New ToolBarButton("One"))  
       ToolBar1.Buttons.Add(New ToolBarButton("Two"))  
       ToolBar1.Buttons.Add(New ToolBarButton("Three"))  
    ' Add the event handler delegate.  
       AddHandler ToolBar1.ButtonClick, AddressOf Me.ToolBar1_ButtonClick  
    End Sub  
    ```  
  
    ```csharp  
    public void ToolBarConfig()   
    {  
       toolBar1.Buttons.Add(new ToolBarButton("One"));  
       toolBar1.Buttons.Add(new ToolBarButton("Two"));  
       toolBar1.Buttons.Add(new ToolBarButton("Three"));  
  
       toolBar1.ButtonClick +=   
          new ToolBarButtonClickEventHandler(this.toolBar1_ButtonClick);  
    }  
    ```  
  
    ```cpp  
    public:  
       void ToolBarConfig()  
       {  
          toolBar1->Buttons->Add(gcnew ToolBarButton("One"));  
          toolBar1->Buttons->Add(gcnew ToolBarButton("Two"));  
          toolBar1->Buttons->Add(gcnew ToolBarButton("Three"));  
  
          toolBar1->ButtonClick +=   
             gcnew ToolBarButtonClickEventHandler(this,  
             &Form1::toolBar1_ButtonClick);  
       }  
    ```  
  
2. <span data-ttu-id="28625-111">Ajouter un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolBar> du contrôle <xref:System.Windows.Forms.ToolBar.ButtonClick> événement.</span><span class="sxs-lookup"><span data-stu-id="28625-111">Add an event handler for the <xref:System.Windows.Forms.ToolBar> control's <xref:System.Windows.Forms.ToolBar.ButtonClick> event.</span></span> <span data-ttu-id="28625-112">Utilisez une instruction switch case et la <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> classe pour déterminer le bouton de barre d’outils qui a été cliqué.</span><span class="sxs-lookup"><span data-stu-id="28625-112">Use a case switching statement and the <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> class to determine the toolbar button that was clicked.</span></span> <span data-ttu-id="28625-113">Sur cette base, affichez une boîte de message appropriée.</span><span class="sxs-lookup"><span data-stu-id="28625-113">Based on this, show an appropriate message box.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="28625-114">Dans cet exemple, une boîte de message est utilisée seulement en tant qu’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="28625-114">A message box is being used solely as a placeholder in this example.</span></span> <span data-ttu-id="28625-115">Vous pouvez ajouter tout autre code à exécuter quand l’utilisateur clique sur les boutons de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="28625-115">Feel free to add other code to execute when the toolbar buttons are clicked.</span></span>  
  
    ```vb  
    Protected Sub ToolBar1_ButtonClick(ByVal sender As Object, _  
    ByVal e As ToolBarButtonClickEventArgs)  
    ' Evaluate the Button property of the ToolBarButtonClickEventArgs  
    ' to determine which button was clicked.  
       Select Case ToolBar1.Buttons.IndexOf(e.Button)  
         Case 0  
           MessageBox.Show("First toolbar button clicked")  
         Case 1  
           MessageBox.Show("Second toolbar button clicked")  
         Case 2  
           MessageBox.Show("Third toolbar button clicked")  
       End Select  
    End Sub  
    ```  
  
    ```csharp  
    protected void toolBar1_ButtonClick(object sender,  
    ToolBarButtonClickEventArgs e)  
    {  
       // Evaluate the Button property of the ToolBarButtonClickEventArgs  
       // to determine which button was clicked.  
       switch (toolBar1.Buttons.IndexOf(e.Button))  
       {  
          case 0 :  
             MessageBox.Show("First toolbar button clicked");  
             break;  
          case 1 :  
             MessageBox.Show("Second toolbar button clicked");  
             break;  
          case 2 :  
             MessageBox.Show("Third toolbar button clicked");  
             break;  
       }  
    }  
    ```  
  
    ```cpp  
    protected:  
       void toolBar1_ButtonClick(System::Object ^ sender,  
          ToolBarButtonClickEventArgs ^ e)  
       {  
         // Evaluate the Button property of the ToolBarButtonClickEventArgs  
         // to determine which button was clicked.  
          switch (toolBar1->Buttons->IndexOf(e->Button))  
          {  
             case 0 :  
                MessageBox::Show("First toolbar button clicked");  
                break;  
             case 1 :  
                MessageBox::Show("Second toolbar button clicked");  
                break;  
             case 2 :  
                MessageBox::Show("Third toolbar button clicked");  
                break;  
          }  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="28625-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28625-116">See also</span></span>

- <xref:System.Windows.Forms.ToolBar>
- [<span data-ttu-id="28625-117">Guide pratique pour Ajouter des boutons à un contrôle de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="28625-117">How to: Add Buttons to a ToolBar Control</span></span>](how-to-add-buttons-to-a-toolbar-control.md)
- [<span data-ttu-id="28625-118">Guide pratique pour Définir une icône pour un bouton de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="28625-118">How to: Define an Icon for a ToolBar Button</span></span>](how-to-define-an-icon-for-a-toolbar-button.md)
- [<span data-ttu-id="28625-119">ToolBar, contrôle</span><span class="sxs-lookup"><span data-stu-id="28625-119">ToolBar Control</span></span>](toolbar-control-windows-forms.md)
