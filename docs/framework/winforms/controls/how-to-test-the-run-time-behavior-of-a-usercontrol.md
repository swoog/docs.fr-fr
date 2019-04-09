---
title: 'Procédure : tester le comportement au moment de l’exécution d’un UserControl'
ms.date: 03/30/2017
helpviewer_keywords:
- UserControl class [Windows Forms], testing
- user controls [Windows Forms], testing
- composite controls [Windows Forms], testing
- UserControl Test Container
- UserControl class [Windows Forms], run-time behavior
ms.assetid: 4e4d5c49-1346-40ac-9d96-40211b573583
ms.openlocfilehash: 1719d0461fbb582a1486dcc0726253ec97a07ac6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59116491"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a><span data-ttu-id="b65a3-102">Procédure : tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="b65a3-102">How to: Test the Run-Time Behavior of a UserControl</span></span>
<span data-ttu-id="b65a3-103">Lorsque vous développez un <xref:System.Windows.Forms.UserControl>, vous devez tester son comportement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b65a3-103">When you develop a <xref:System.Windows.Forms.UserControl>, you need to test its run-time behavior.</span></span> <span data-ttu-id="b65a3-104">Vous pouvez créer un projet d’application Windows séparé et placer votre contrôle sur un formulaire de test, mais cette procédure n’est pas pratique.</span><span class="sxs-lookup"><span data-stu-id="b65a3-104">You can create a separate Windows-based application project and place your control on a test form, but this procedure is inconvenient.</span></span> <span data-ttu-id="b65a3-105">Un moyen plus rapide et plus facile consiste à utiliser le **conteneur de Test UserControl** fournis par Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b65a3-105">A faster and easier way is to use the **UserControl Test Container** provided by Visual Studio.</span></span> <span data-ttu-id="b65a3-106">Ce conteneur de test démarre directement à partir de votre projet de bibliothèque de contrôles Windows.</span><span class="sxs-lookup"><span data-stu-id="b65a3-106">This test container starts directly from your Windows control library project.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b65a3-107">Le conteneur de test charger votre <xref:System.Windows.Forms.UserControl>, le contrôle doit avoir au moins un constructeur public.</span><span class="sxs-lookup"><span data-stu-id="b65a3-107">For the test container to load your <xref:System.Windows.Forms.UserControl>, the control must have at least one public constructor.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b65a3-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="b65a3-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="b65a3-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="b65a3-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="b65a3-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="b65a3-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b65a3-111">Un contrôle Visual C++ ne peuvent pas être testé à l’aide de la **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="b65a3-111">A Visual C++ control cannot be tested using the **UserControl Test Container**.</span></span>  
  
### <a name="to-test-the-run-time-behavior-of-a-usercontrol"></a><span data-ttu-id="b65a3-112">Pour tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="b65a3-112">To test the run-time behavior of a UserControl</span></span>  
  
1.  <span data-ttu-id="b65a3-113">Créer un projet de bibliothèque de contrôles Windows appelé **TestContainerExample**.</span><span class="sxs-lookup"><span data-stu-id="b65a3-113">Create a Windows control library project called **TestContainerExample**.</span></span> <span data-ttu-id="b65a3-114">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="b65a3-114">For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="b65a3-115">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Label> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b65a3-115">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Label> control from the **Toolbox** onto the control's design surface.</span></span>  
  
3.  <span data-ttu-id="b65a3-116">Appuyez sur F5 pour générer le projet et exécuter le **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="b65a3-116">Press F5 to build the project and run the **UserControl Test Container**.</span></span> <span data-ttu-id="b65a3-117">Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-117">The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.</span></span>  
  
4.  <span data-ttu-id="b65a3-118">Sélectionnez le <xref:System.Windows.Forms.Control.BackColor%2A> propriété affichée dans le <xref:System.Windows.Forms.PropertyGrid> contrôle situé à droite de la **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-118">Select the <xref:System.Windows.Forms.Control.BackColor%2A> property displayed in the <xref:System.Windows.Forms.PropertyGrid> control to the right of the **Preview** pane.</span></span> <span data-ttu-id="b65a3-119">Modifiez sa valeur en `ControlDark`.</span><span class="sxs-lookup"><span data-stu-id="b65a3-119">Change its value to `ControlDark`.</span></span> <span data-ttu-id="b65a3-120">Observez que le contrôle passe à une couleur plus sombre.</span><span class="sxs-lookup"><span data-stu-id="b65a3-120">Observe that the control changes to a darker color.</span></span> <span data-ttu-id="b65a3-121">Essayez de modifier d’autres valeurs de propriété et observer l’effet sur votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="b65a3-121">Try changing other property values and observe the effect on your control.</span></span>  
  
5.  <span data-ttu-id="b65a3-122">Cliquez sur le **ancrer le contrôle utilisateur remplir** case à cocher ci-dessous le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-122">Click the **Dock Fill User Control** check box below the **Preview** pane.</span></span> <span data-ttu-id="b65a3-123">Observez que le contrôle est redimensionné pour remplir le volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-123">Observe that the control is resized to fill the pane.</span></span> <span data-ttu-id="b65a3-124">Redimensionner le conteneur de test et observez que le contrôle est redimensionné avec le volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-124">Resize the test container and observe that the control is resized with the pane.</span></span>  
  
6.  <span data-ttu-id="b65a3-125">Fermez le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="b65a3-125">Close the test container.</span></span>  
  
7.  <span data-ttu-id="b65a3-126">Ajoutez un autre contrôle utilisateur à la **TestContainerExample** projet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-126">Add another user control to the **TestContainerExample** project.</span></span> <span data-ttu-id="b65a3-127">Pour plus d’informations, consultez [Guide pratique pour Ajouter des éléments existants à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="b65a3-127">For details, see [How to: Add Existing Items to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).</span></span>  
  
8.  <span data-ttu-id="b65a3-128">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b65a3-128">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** onto the control's design surface.</span></span>  
  
9. <span data-ttu-id="b65a3-129">Appuyez sur F5 pour générer le projet et exécuter le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="b65a3-129">Press F5 to build the project and run the test container.</span></span>  
  
10. <span data-ttu-id="b65a3-130">Cliquez sur le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b65a3-130">Click the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls.</span></span>  
  
## <a name="testing-user-controls-from-another-project"></a><span data-ttu-id="b65a3-131">Test des contrôles utilisateur à partir d’un autre projet</span><span class="sxs-lookup"><span data-stu-id="b65a3-131">Testing User Controls from Another Project</span></span>  
 <span data-ttu-id="b65a3-132">Vous pouvez tester les contrôles utilisateur à partir d’autres projets dans le conteneur de test de votre projet actuel.</span><span class="sxs-lookup"><span data-stu-id="b65a3-132">You can test user controls from other projects in your current project's test container.</span></span>  
  
#### <a name="to-test-user-controls-from-another-project"></a><span data-ttu-id="b65a3-133">Pour tester les contrôles utilisateur à partir d’un autre projet</span><span class="sxs-lookup"><span data-stu-id="b65a3-133">To test user controls from another project</span></span>  
  
1.  <span data-ttu-id="b65a3-134">Créer un projet de bibliothèque de contrôles Windows appelé **TestContainerExample2**.</span><span class="sxs-lookup"><span data-stu-id="b65a3-134">Create a Windows control library project called **TestContainerExample2**.</span></span> <span data-ttu-id="b65a3-135">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="b65a3-135">For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="b65a3-136">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.RadioButton> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b65a3-136">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.RadioButton> control from the **Toolbox** onto the control's design surface.</span></span>  
  
3.  <span data-ttu-id="b65a3-137">Appuyez sur F5 pour générer le projet et exécuter le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="b65a3-137">Press F5 to build the project and run the test container.</span></span> <span data-ttu-id="b65a3-138">Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-138">The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.</span></span>  
  
4.  <span data-ttu-id="b65a3-139">Cliquez sur le **charge** bouton.</span><span class="sxs-lookup"><span data-stu-id="b65a3-139">Click the **Load** button.</span></span>  
  
5.  <span data-ttu-id="b65a3-140">Dans le **Open** boîte de dialogue, accédez à **TestContainerExample**.dll que vous avez créé dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="b65a3-140">In the **Open** dialog box, navigate to **TestContainerExample**.dll, which you built in the previous procedure.</span></span> <span data-ttu-id="b65a3-141">Sélectionnez **TestContainerExample**.dll et cliquez sur le **Open** bouton pour charger les contrôles utilisateur</span><span class="sxs-lookup"><span data-stu-id="b65a3-141">Select **TestContainerExample**.dll and click the **Open** button to load the user controls</span></span>  
  
6.  <span data-ttu-id="b65a3-142">Utilisez le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur à partir de la **TestContainerExample** projet.</span><span class="sxs-lookup"><span data-stu-id="b65a3-142">Use the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls from the **TestContainerExample** project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b65a3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b65a3-143">See also</span></span>

- <xref:System.Windows.Forms.UserControl>
- [<span data-ttu-id="b65a3-144">Procédure : créer des contrôles composites</span><span class="sxs-lookup"><span data-stu-id="b65a3-144">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)
- [<span data-ttu-id="b65a3-145">Procédure pas à pas : création d’un contrôle composite avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b65a3-145">Walkthrough: Authoring a Composite Control with Visual Basic</span></span>](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [<span data-ttu-id="b65a3-146">Procédure pas à pas : Création d'un contrôle composite à l'aide de Visual C#</span><span class="sxs-lookup"><span data-stu-id="b65a3-146">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- [<span data-ttu-id="b65a3-147">Concepteur de contrôles utilisateur</span><span class="sxs-lookup"><span data-stu-id="b65a3-147">User Control Designer</span></span>](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))
