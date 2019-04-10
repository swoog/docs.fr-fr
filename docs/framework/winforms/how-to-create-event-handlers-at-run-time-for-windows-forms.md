---
title: 'Procédure : créer des gestionnaires d’événements au moment de l’exécution pour Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, event handling
- event handlers [Windows Forms], creating
- run time [Windows Forms], creating event handlers at
- examples [Windows Forms], event handling
- Button control [Windows Forms], event handlers
ms.assetid: 2e7c9e1a-61fe-444d-8113-3c5bacf1c8cb
ms.openlocfilehash: 09f090c6267093e3ad59266d8c77ea13b13b63d3
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59343261"
---
# <a name="how-to-create-event-handlers-at-run-time-for-windows-forms"></a><span data-ttu-id="0e9e3-102">Procédure : créer des gestionnaires d’événements au moment de l’exécution pour Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0e9e3-102">How to: Create Event Handlers at Run Time for Windows Forms</span></span>
<span data-ttu-id="0e9e3-103">Outre la création d’événements à l’aide du Concepteur Windows Forms, vous pouvez créer un gestionnaire d’événements au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-103">In addition to creating events using the Windows Forms Designer, you can also create an event handler at run time.</span></span> <span data-ttu-id="0e9e3-104">Cette action vous permet de connecter des gestionnaires d’événements en fonction de conditions spécifiées dans le code lors de l’exécution au lieu de les connecter au premier démarrage du programme.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-104">This action allows you to connect event handlers based on conditions in code at run time as opposed to having them connected when the program initially starts.</span></span>  
  
### <a name="to-create-an-event-handler-at-run-time"></a><span data-ttu-id="0e9e3-105">Pour créer un gestionnaire d’événements au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="0e9e3-105">To create an event handler at run time</span></span>  
  
1. <span data-ttu-id="0e9e3-106">Ouvrez le formulaire auquel vous souhaitez ajouter un gestionnaire d’événements dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-106">Open the form in the Code Editor that you want to add an event handler to.</span></span>  
  
2. <span data-ttu-id="0e9e3-107">Ajoutez une méthode à votre formulaire avec la signature de méthode pour l’événement que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-107">Add a method to your form with the method signature for the event that you want to handle.</span></span>  
  
     <span data-ttu-id="0e9e3-108">Par exemple, si vous gérez le <xref:System.Windows.Forms.Control.Click> événement d’un <xref:System.Windows.Forms.Button> contrôle, vous pouvez créer une méthode telle que la suivante :</span><span class="sxs-lookup"><span data-stu-id="0e9e3-108">For example, if you were handling the <xref:System.Windows.Forms.Control.Click> event of a <xref:System.Windows.Forms.Button> control, you would create a method such as the following:</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As Object, ByVal e As EventArgs)  
       ' Add event handler code here.  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)   
    {  
    // Add event handler code here.  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,   
          System::EventArgs ^ e)  
       {  
          // Add event handler code here.  
       }  
    ```  
  
3. <span data-ttu-id="0e9e3-109">Ajoutez le code au gestionnaire d’événements en fonction de votre application.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-109">Add code to the event handler as appropriate to your application.</span></span>  
  
4. <span data-ttu-id="0e9e3-110">Déterminez le formulaire ou le contrôle pour lequel vous souhaitez créer un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-110">Determine which form or control you want to create an event handler for.</span></span>  
  
5. <span data-ttu-id="0e9e3-111">Dans une méthode de classe de votre formulaire, ajoutez le code qui spécifie au gestionnaire d’événements de gérer l’événement.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-111">In a method within your form's class, add code that specifies the event handler to handle the event.</span></span> <span data-ttu-id="0e9e3-112">Par exemple, le code suivant spécifie le Gestionnaire d’événements `button1_Click` gère la <xref:System.Windows.Forms.Control.Click> événement d’un <xref:System.Windows.Forms.Button> contrôle :</span><span class="sxs-lookup"><span data-stu-id="0e9e3-112">For example, the following code specifies the event handler `button1_Click` handles the <xref:System.Windows.Forms.Control.Click> event of a <xref:System.Windows.Forms.Button> control:</span></span>  
  
    ```vb  
    AddHandler Button1.Click, AddressOf Button1_Click  
    ```  
  
    ```csharp  
    button1.Click += new EventHandler(button1_Click);  
    ```  
  
    ```cpp  
    button1->Click += gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
     <span data-ttu-id="0e9e3-113">Le <xref:System.ComponentModel.EventHandlerList.AddHandler%2A> méthode présentée dans le code Visual Basic ci-dessus établit un gestionnaire d’événements click du bouton.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-113">The <xref:System.ComponentModel.EventHandlerList.AddHandler%2A> method demonstrated in the Visual Basic code above establishes a click event handler for the button.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e9e3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e9e3-114">See also</span></span>

- [<span data-ttu-id="0e9e3-115">Création de gestionnaires d'événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0e9e3-115">Creating Event Handlers in Windows Forms</span></span>](creating-event-handlers-in-windows-forms.md)
- [<span data-ttu-id="0e9e3-116">Vue d’ensemble des gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="0e9e3-116">Event Handlers Overview</span></span>](event-handlers-overview-windows-forms.md)
- [<span data-ttu-id="0e9e3-117">Dépannage des gestionnaires d'événements hérités dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0e9e3-117">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](~/docs/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers.md)
