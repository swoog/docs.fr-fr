---
title: 'Procédure : connecter plusieurs événements à un seul gestionnaire d’événements dans Windows Forms'
ms.date: 03/30/2017
dev_langs:
- vb
helpviewer_keywords:
- events [Windows Forms], connecting multiple to single event handler
- event handlers [Windows Forms], connecting events to
- menus [Windows Forms], event-handling methods for multiple menu items
- Windows Forms controls, events
- menu items [Windows Forms], multicasting event-handling methods
ms.assetid: 5a20749a-41b5-4acc-8eb1-9e5040b0a2c4
ms.openlocfilehash: eec6a754b885cd169e5542221caefb3233c4c8af
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59300721"
---
# <a name="how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms"></a><span data-ttu-id="94898-102">Procédure : connecter plusieurs événements à un seul gestionnaire d’événements dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="94898-102">How to: Connect Multiple Events to a Single Event Handler in Windows Forms</span></span>
<span data-ttu-id="94898-103">Conception de votre application, vous pouvez s’avérer nécessaire pour utiliser un seul gestionnaire d’événements pour plusieurs événements ou d’avoir plusieurs événements à effectuer la même procédure.</span><span class="sxs-lookup"><span data-stu-id="94898-103">In your application design, you may find it necessary to use a single event handler for multiple events or have multiple events perform the same procedure.</span></span> <span data-ttu-id="94898-104">Par exemple, il est souvent un temps précieux pour avoir une commande de menu à déclencher l’événement de même qu’un bouton sur votre formulaire peut si elles exposent les mêmes fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="94898-104">For example, it is often a powerful time-saver to have a menu command raise the same event as a button on your form does if they expose the same functionality.</span></span> <span data-ttu-id="94898-105">Vous pouvez faire à l’aide de l’affichage des événements de la fenêtre Propriétés dans C# ou à l’aide de la `Handles` mot clé et le **nom de la classe** et **nom de la méthode** listes déroulantes dans l’éditeur de Code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="94898-105">You can do this by using the Events view of the Properties window in C# or using the `Handles` keyword and the **Class Name** and **Method Name** drop-down boxes in the Visual Basic Code Editor.</span></span>  
  
### <a name="to-connect-multiple-events-to-a-single-event-handler-in-visual-basic"></a><span data-ttu-id="94898-106">Pour connecter plusieurs événements à un seul gestionnaire d’événements en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="94898-106">To connect multiple events to a single event handler in Visual Basic</span></span>  
  
1. <span data-ttu-id="94898-107">Avec le bouton droit de la forme et choisissez **afficher le Code**.</span><span class="sxs-lookup"><span data-stu-id="94898-107">Right-click the form and choose **View Code**.</span></span>  
  
2. <span data-ttu-id="94898-108">À partir de la **nom de la classe** zone de liste déroulante, sélectionnez un des contrôles que vous souhaitez associer le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="94898-108">From the **Class Name** drop-down box, select one of the controls that you want to have the event handler handle.</span></span>  
  
3. <span data-ttu-id="94898-109">À partir de la **nom de la méthode** zone de liste déroulante, sélectionnez un des événements que vous souhaitez que le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="94898-109">From the **Method Name** drop-down box, select one of the events that you want the event handler to handle.</span></span>  
  
4. <span data-ttu-id="94898-110">L’éditeur de Code insère le Gestionnaire d’événements approprié et place le point d’insertion dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="94898-110">The Code Editor inserts the appropriate event handler and positions the insertion point within the method.</span></span> <span data-ttu-id="94898-111">Dans l’exemple ci-dessous, il est le <xref:System.Windows.Forms.Control.Click> événement pour le <xref:System.Windows.Forms.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="94898-111">In the example below, it is the <xref:System.Windows.Forms.Control.Click> event for the <xref:System.Windows.Forms.Button> control.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
    ' Add event-handler code here.  
    End Sub  
    ```  
  
5. <span data-ttu-id="94898-112">Ajoutez éventuellement les autres événements que vous souhaitez que gérées à le `Handles` clause.</span><span class="sxs-lookup"><span data-stu-id="94898-112">Append the other events you would like handled to the `Handles` clause.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click, Button2.Click  
    ' Add event-handler code here.  
    End Sub  
    ```  
  
6. <span data-ttu-id="94898-113">Ajoutez le code approprié au gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="94898-113">Add the appropriate code to the event handler.</span></span>  
  
### <a name="to-connect-multiple-events-to-a-single-event-handler-in-c"></a><span data-ttu-id="94898-114">Pour connecter plusieurs événements à un seul gestionnaire d’événements en C\#</span><span class="sxs-lookup"><span data-stu-id="94898-114">To connect multiple events to a single event handler in C\#</span></span>
  
1. <span data-ttu-id="94898-115">Sélectionnez le contrôle auquel vous souhaitez vous connecter à un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="94898-115">Select the control to which you want to connect an event handler.</span></span>  
  
2. <span data-ttu-id="94898-116">Dans la fenêtre Propriétés, cliquez sur le **événements** bouton (![bouton événements](./media/vxeventsbutton-propertieswindow.png "vxEventsButton_PropertiesWindow")).</span><span class="sxs-lookup"><span data-stu-id="94898-116">In the Properties window, click the **Events** button (![Events Button](./media/vxeventsbutton-propertieswindow.png "vxEventsButton_PropertiesWindow")).</span></span>  
  
3. <span data-ttu-id="94898-117">Cliquez sur le nom de l’événement que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="94898-117">Click the name of the event that you want to handle.</span></span>  
  
4. <span data-ttu-id="94898-118">Dans la section valeur en regard du nom de l’événement, cliquez sur le bouton de liste déroulante pour afficher une liste des gestionnaires d’événements qui correspondent à la signature de méthode de l’événement que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="94898-118">In the value section next to the event name, click the drop-down button to display a list of existing event handlers that match the method signature of the event you want to handle.</span></span>  
  
5. <span data-ttu-id="94898-119">Sélectionnez le Gestionnaire d’événements appropriée dans la liste.</span><span class="sxs-lookup"><span data-stu-id="94898-119">Select the appropriate event handler from the list.</span></span>  
  
     <span data-ttu-id="94898-120">Code sera ajouté au formulaire pour lier l’événement au gestionnaire d’événements existant.</span><span class="sxs-lookup"><span data-stu-id="94898-120">Code will be added to the form to bind the event to the existing event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94898-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94898-121">See also</span></span>

- [<span data-ttu-id="94898-122">Création de gestionnaires d’événements dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="94898-122">Creating Event Handlers in Windows Forms</span></span>](creating-event-handlers-in-windows-forms.md)
- [<span data-ttu-id="94898-123">Vue d'ensemble des gestionnaires d'événements</span><span class="sxs-lookup"><span data-stu-id="94898-123">Event Handlers Overview</span></span>](event-handlers-overview-windows-forms.md)
