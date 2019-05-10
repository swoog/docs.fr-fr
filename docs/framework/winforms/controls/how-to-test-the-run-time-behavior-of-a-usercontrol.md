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
ms.openlocfilehash: 48531ab1ef3b30b6516e3f2e7b5858a8884cbfe8
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211717"
---
# <a name="how-to-test-the-run-time-behavior-of-a-usercontrol"></a><span data-ttu-id="f8c8d-102">Procédure : Tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="f8c8d-102">How to: Test the run-time behavior of a UserControl</span></span>

<span data-ttu-id="f8c8d-103">Lorsque vous développez un <xref:System.Windows.Forms.UserControl>, vous devez tester son comportement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-103">When you develop a <xref:System.Windows.Forms.UserControl>, you need to test its run-time behavior.</span></span> <span data-ttu-id="f8c8d-104">Vous pouvez créer un projet d’application Windows séparé et placer votre contrôle sur un formulaire de test, mais cette procédure n’est pas pratique.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-104">You can create a separate Windows-based application project and place your control on a test form, but this procedure is inconvenient.</span></span> <span data-ttu-id="f8c8d-105">Un moyen plus rapide et plus facile consiste à utiliser le **conteneur de Test UserControl** fournis par Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-105">A faster and easier way is to use the **UserControl Test Container** provided by Visual Studio.</span></span> <span data-ttu-id="f8c8d-106">Ce conteneur de test démarre directement à partir de votre projet de bibliothèque de contrôles Windows.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-106">This test container starts directly from your Windows control library project.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8c8d-107">Le conteneur de test charger votre <xref:System.Windows.Forms.UserControl>, le contrôle doit avoir au moins un constructeur public.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-107">For the test container to load your <xref:System.Windows.Forms.UserControl>, the control must have at least one public constructor.</span></span>

> [!NOTE]
> <span data-ttu-id="f8c8d-108">Un contrôle Visual C++ ne peuvent pas être testé à l’aide de la **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-108">A Visual C++ control cannot be tested using the **UserControl Test Container**.</span></span>

## <a name="test-the-run-time-behavior-of-a-usercontrol"></a><span data-ttu-id="f8c8d-109">Tester le comportement au moment de l’exécution d’un UserControl</span><span class="sxs-lookup"><span data-stu-id="f8c8d-109">Test the run-time behavior of a UserControl</span></span>

1. <span data-ttu-id="f8c8d-110">Dans Visual Studio, créez un projet de bibliothèque de contrôles Windows appelé **TestContainerExample**.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-110">In Visual Studio, create a Windows control library project called **TestContainerExample**.</span></span> <span data-ttu-id="f8c8d-111">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f8c8d-111">For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span></span>

2. <span data-ttu-id="f8c8d-112">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Label> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-112">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Label> control from the **Toolbox** onto the control's design surface.</span></span>

3. <span data-ttu-id="f8c8d-113">Appuyez sur **F5** pour générer le projet et exécuter le **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-113">Press **F5** to build the project and run the **UserControl Test Container**.</span></span> <span data-ttu-id="f8c8d-114">Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-114">The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.</span></span>

4. <span data-ttu-id="f8c8d-115">Sélectionnez le <xref:System.Windows.Forms.Control.BackColor%2A> propriété affichée dans le <xref:System.Windows.Forms.PropertyGrid> contrôle situé à droite de la **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-115">Select the <xref:System.Windows.Forms.Control.BackColor%2A> property displayed in the <xref:System.Windows.Forms.PropertyGrid> control to the right of the **Preview** pane.</span></span> <span data-ttu-id="f8c8d-116">Modifiez sa valeur en `ControlDark`.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-116">Change its value to `ControlDark`.</span></span> <span data-ttu-id="f8c8d-117">Observez que le contrôle passe à une couleur plus sombre.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-117">Observe that the control changes to a darker color.</span></span> <span data-ttu-id="f8c8d-118">Essayez de modifier d’autres valeurs de propriété et observer l’effet sur votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-118">Try changing other property values and observe the effect on your control.</span></span>

5. <span data-ttu-id="f8c8d-119">Cliquez sur le **ancrer le contrôle utilisateur remplir** case à cocher ci-dessous le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-119">Click the **Dock Fill User Control** check box below the **Preview** pane.</span></span> <span data-ttu-id="f8c8d-120">Observez que le contrôle est redimensionné pour remplir le volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-120">Observe that the control is resized to fill the pane.</span></span> <span data-ttu-id="f8c8d-121">Redimensionner le conteneur de test et observez que le contrôle est redimensionné avec le volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-121">Resize the test container and observe that the control is resized with the pane.</span></span>

6. <span data-ttu-id="f8c8d-122">Fermez le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-122">Close the test container.</span></span>

7. <span data-ttu-id="f8c8d-123">Ajoutez un autre contrôle utilisateur à la **TestContainerExample** projet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-123">Add another user control to the **TestContainerExample** project.</span></span> <span data-ttu-id="f8c8d-124">Pour plus d’informations, consultez [Guide pratique pour Ajouter des éléments existants à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f8c8d-124">For details, see [How to: Add Existing Items to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9f4t9t92(v=vs.100)).</span></span>

8. <span data-ttu-id="f8c8d-125">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.Button> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-125">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.Button> control from the **Toolbox** onto the control's design surface.</span></span>

9. <span data-ttu-id="f8c8d-126">Appuyez sur F5 pour générer le projet et exécuter le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-126">Press F5 to build the project and run the test container.</span></span>

10. <span data-ttu-id="f8c8d-127">Cliquez sur le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-127">Click the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls.</span></span>

## <a name="test-user-controls-from-another-project"></a><span data-ttu-id="f8c8d-128">Contrôles utilisateur de test à partir d’un autre projet</span><span class="sxs-lookup"><span data-stu-id="f8c8d-128">Test user controls from another project</span></span>

<span data-ttu-id="f8c8d-129">Vous pouvez tester les contrôles utilisateur à partir d’autres projets dans le conteneur de test de votre projet actuel.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-129">You can test user controls from other projects in your current project's test container.</span></span>

1. <span data-ttu-id="f8c8d-130">Créer un projet de bibliothèque de contrôles Windows appelé **TestContainerExample2**.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-130">Create a Windows control library project called **TestContainerExample2**.</span></span> <span data-ttu-id="f8c8d-131">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="f8c8d-131">For details, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span></span>

2. <span data-ttu-id="f8c8d-132">Dans le **Windows Forms Designer**, faites glisser un <xref:System.Windows.Forms.RadioButton> contrôle depuis la **boîte à outils** aire de conception du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-132">In the **Windows Forms Designer**, drag a <xref:System.Windows.Forms.RadioButton> control from the **Toolbox** onto the control's design surface.</span></span>

3. <span data-ttu-id="f8c8d-133">Appuyez sur F5 pour générer le projet et exécuter le conteneur de test.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-133">Press F5 to build the project and run the test container.</span></span> <span data-ttu-id="f8c8d-134">Le conteneur de test s’affiche avec votre <xref:System.Windows.Forms.UserControl> dans le **aperçu** volet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-134">The test container appears with your <xref:System.Windows.Forms.UserControl> in the **Preview** pane.</span></span>

4. <span data-ttu-id="f8c8d-135">Cliquez sur le **charge** bouton.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-135">Click the **Load** button.</span></span>

5. <span data-ttu-id="f8c8d-136">Dans le **Open** boîte de dialogue, accédez à **TestContainerExample**.dll que vous avez créé dans la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-136">In the **Open** dialog box, navigate to **TestContainerExample**.dll, which you built in the previous procedure.</span></span> <span data-ttu-id="f8c8d-137">Sélectionnez **TestContainerExample**.dll et cliquez sur le **Open** bouton pour charger les contrôles utilisateur</span><span class="sxs-lookup"><span data-stu-id="f8c8d-137">Select **TestContainerExample**.dll and click the **Open** button to load the user controls</span></span>

6. <span data-ttu-id="f8c8d-138">Utilisez le **sélectionner un contrôle utilisateur** <xref:System.Windows.Forms.ComboBox> pour basculer entre les deux contrôles utilisateur à partir de la **TestContainerExample** projet.</span><span class="sxs-lookup"><span data-stu-id="f8c8d-138">Use the **Select User Control**<xref:System.Windows.Forms.ComboBox> to switch between the two user controls from the **TestContainerExample** project.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8c8d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c8d-139">See also</span></span>

- <xref:System.Windows.Forms.UserControl>
- [<span data-ttu-id="f8c8d-140">Guide pratique pour Créer des contrôles composites</span><span class="sxs-lookup"><span data-stu-id="f8c8d-140">How to: Author Composite Controls</span></span>](how-to-author-composite-controls.md)
- [<span data-ttu-id="f8c8d-141">Procédure pas à pas : Création d’un contrôle Composite avec Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f8c8d-141">Walkthrough: Authoring a Composite Control with Visual Basic</span></span>](walkthrough-authoring-a-composite-control-with-visual-basic.md)
- [<span data-ttu-id="f8c8d-142">Procédure pas à pas : Création d’un contrôle Composite avec VisualC#</span><span class="sxs-lookup"><span data-stu-id="f8c8d-142">Walkthrough: Authoring a Composite Control with Visual C#</span></span>](walkthrough-authoring-a-composite-control-with-visual-csharp.md)
- <span data-ttu-id="f8c8d-143">[Concepteur de contrôles utilisateur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f8c8d-143">[User Control Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/183c3hth(v=vs.100))</span></span>
