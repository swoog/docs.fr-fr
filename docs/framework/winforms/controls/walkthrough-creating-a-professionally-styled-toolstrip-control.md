---
title: 'Procédure pas à pas : création d’un contrôle ToolStrip de style professionnel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- toolbars [Windows Forms], walkthroughs
- ToolStrip control [Windows Forms], creating professionally styled controls
ms.assetid: b52339ae-f1d3-494e-996e-eb455614098a
ms.openlocfilehash: 226e805d0240236899ee0cc290f1060a3b0aa391
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211772"
---
# <a name="walkthrough-creating-a-professionally-styled-toolstrip-control"></a><span data-ttu-id="0de4f-102">Procédure pas à pas : création d’un contrôle ToolStrip de style professionnel</span><span class="sxs-lookup"><span data-stu-id="0de4f-102">Walkthrough: Creating a Professionally Styled ToolStrip Control</span></span>

<span data-ttu-id="0de4f-103">Vous pouvez donner à votre application <xref:System.Windows.Forms.ToolStrip> un aspect professionnel et un comportement de contrôles en écrivant votre propre classe dérivée de la <xref:System.Windows.Forms.ToolStripProfessionalRenderer> type.</span><span class="sxs-lookup"><span data-stu-id="0de4f-103">You can give your application’s <xref:System.Windows.Forms.ToolStrip> controls a professional appearance and behavior by writing your own class derived from the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> type.</span></span>

<span data-ttu-id="0de4f-104">Cette procédure pas à pas montre comment utiliser <xref:System.Windows.Forms.ToolStrip> contrôles pour créer un contrôle composite qui ressemble à la **volet de Navigation** fourni par Microsoft® Outlook®.</span><span class="sxs-lookup"><span data-stu-id="0de4f-104">This walkthrough demonstrates how to use <xref:System.Windows.Forms.ToolStrip> controls to create a composite control that resembles the **Navigation Pane** provided by Microsoft® Outlook®.</span></span> <span data-ttu-id="0de4f-105">Les tâches suivantes sont illustrées dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="0de4f-105">The following tasks are illustrated in this walkthrough:</span></span>

- <span data-ttu-id="0de4f-106">Création d’un projet de bibliothèque de contrôles Windows.</span><span class="sxs-lookup"><span data-stu-id="0de4f-106">Creating a Windows Control Library project.</span></span>

- <span data-ttu-id="0de4f-107">Conception du contrôle StackView.</span><span class="sxs-lookup"><span data-stu-id="0de4f-107">Designing the StackView Control.</span></span>

- <span data-ttu-id="0de4f-108">Implémentation d’un convertisseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0de4f-108">Implementing a Custom Renderer.</span></span>

<span data-ttu-id="0de4f-109">Lorsque vous avez terminé, avoir un contrôle client personnalisé réutilisable avec l’aspect d’un contrôle Microsoft Office® XP Professionnel.</span><span class="sxs-lookup"><span data-stu-id="0de4f-109">When you are finished, you will have a reusable custom client control with the professional appearance of a Microsoft Office® XP control.</span></span>

<span data-ttu-id="0de4f-110">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Créer un contrôle ToolStrip de style professionnel](how-to-create-a-professionally-styled-toolstrip-control.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-110">To copy the code in this topic as a single listing, see [How to: Create a Professionally Styled ToolStrip Control](how-to-create-a-professionally-styled-toolstrip-control.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0de4f-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0de4f-111">Prerequisites</span></span>

<span data-ttu-id="0de4f-112">Vous aurez besoin de Visual Studio pour effectuer cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="0de4f-112">You'll need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-control-library-project"></a><span data-ttu-id="0de4f-113">Créer le projet de bibliothèque de contrôles</span><span class="sxs-lookup"><span data-stu-id="0de4f-113">Create the control library project</span></span>

1. <span data-ttu-id="0de4f-114">Dans Visual Studio, créez un nouveau projet de bibliothèque de contrôles Windows nommé `StackViewLibrary`.</span><span class="sxs-lookup"><span data-stu-id="0de4f-114">In Visual Studio, create a new Windows Control Library project named `StackViewLibrary`.</span></span>

2. <span data-ttu-id="0de4f-115">Dans **l’Explorateur de solutions**, supprimer le contrôle du projet par défaut en supprimant le fichier source nommé « UserControl1.cs » ou « UserControl1.vb », en fonction de la langue de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0de4f-115">In **Solution Explorer**, delete the project's default control by deleting the source file named "UserControl1.cs" or "UserControl1.vb", depending on your language of choice.</span></span>

     <span data-ttu-id="0de4f-116">Pour plus d'informations, voir [Procédure : Supprimer, suppression et exclure des éléments](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="0de4f-116">For more information, see [How to: Remove, Delete, and Exclude Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span></span>

3. <span data-ttu-id="0de4f-117">Ajouter un nouveau <xref:System.Windows.Forms.UserControl> d’élément à la **StackViewLibrary** projet.</span><span class="sxs-lookup"><span data-stu-id="0de4f-117">Add a new <xref:System.Windows.Forms.UserControl> item to the **StackViewLibrary** project.</span></span> <span data-ttu-id="0de4f-118">Nommez le nouveau fichier source une base de `StackView`.</span><span class="sxs-lookup"><span data-stu-id="0de4f-118">Give the new source file a base name of `StackView`.</span></span>

## <a name="design-the-stackview-control"></a><span data-ttu-id="0de4f-119">Concevoir le contrôle StackView</span><span class="sxs-lookup"><span data-stu-id="0de4f-119">Design the StackView control</span></span>

<span data-ttu-id="0de4f-120">Le `StackView` contrôle est un contrôle composite avec un seul enfant <xref:System.Windows.Forms.ToolStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-120">The `StackView` control is a composite control with one child <xref:System.Windows.Forms.ToolStrip> control.</span></span> <span data-ttu-id="0de4f-121">Pour plus d’informations sur les contrôles composites, consultez [variétés de contrôles personnalisés](varieties-of-custom-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-121">For more information about composite controls, see [Varieties of Custom Controls](varieties-of-custom-controls.md).</span></span>

1. <span data-ttu-id="0de4f-122">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.ToolStrip> contrôle à l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="0de4f-122">From the **Toolbox**, drag a <xref:System.Windows.Forms.ToolStrip> control to the design surface.</span></span>

2. <span data-ttu-id="0de4f-123">Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.ToolStrip> propriétés de contrôle conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0de4f-123">In the **Properties** window, set the <xref:System.Windows.Forms.ToolStrip> control's properties according to the following table.</span></span>

    |<span data-ttu-id="0de4f-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="0de4f-124">Property</span></span>|<span data-ttu-id="0de4f-125">Value</span><span class="sxs-lookup"><span data-stu-id="0de4f-125">Value</span></span>|
    |--------------|-----------|
    |<span data-ttu-id="0de4f-126">Nom</span><span class="sxs-lookup"><span data-stu-id="0de4f-126">Name</span></span>|`stackStrip`|
    |<span data-ttu-id="0de4f-127">CanOverflow</span><span class="sxs-lookup"><span data-stu-id="0de4f-127">CanOverflow</span></span>|`false`|
    |<span data-ttu-id="0de4f-128">Station d' accueil</span><span class="sxs-lookup"><span data-stu-id="0de4f-128">Dock</span></span>|<xref:System.Windows.Forms.DockStyle.Bottom>|
    |<span data-ttu-id="0de4f-129">Police</span><span class="sxs-lookup"><span data-stu-id="0de4f-129">Font</span></span>|`Tahoma, 10pt, style=Bold`|
    |<span data-ttu-id="0de4f-130">GripStyle</span><span class="sxs-lookup"><span data-stu-id="0de4f-130">GripStyle</span></span>|<xref:System.Windows.Forms.ToolStripGripStyle.Hidden>|
    |<span data-ttu-id="0de4f-131">LayoutStyle</span><span class="sxs-lookup"><span data-stu-id="0de4f-131">LayoutStyle</span></span>|<xref:System.Windows.Forms.ToolStripLayoutStyle.VerticalStackWithOverflow>|
    |<span data-ttu-id="0de4f-132">Padding</span><span class="sxs-lookup"><span data-stu-id="0de4f-132">Padding</span></span>|`0, 7, 0, 0`|
    |<span data-ttu-id="0de4f-133">RenderMode</span><span class="sxs-lookup"><span data-stu-id="0de4f-133">RenderMode</span></span>|<xref:System.Windows.Forms.ToolStripRenderMode.Professional>|

3. <span data-ttu-id="0de4f-134">Dans le Concepteur de formulaires Windows, cliquez sur le <xref:System.Windows.Forms.ToolStrip> du contrôle **ajouter** bouton et ajoutez un <xref:System.Windows.Forms.ToolStripButton> à la `stackStrip` contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-134">In the Windows Forms Designer, click the <xref:System.Windows.Forms.ToolStrip> control's **Add** button and add a <xref:System.Windows.Forms.ToolStripButton> to the `stackStrip` control.</span></span>

4. <span data-ttu-id="0de4f-135">Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.ToolStripButton> propriétés de contrôle conformément au tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0de4f-135">In the **Properties** window, set the <xref:System.Windows.Forms.ToolStripButton> control's properties according to the following table.</span></span>

    |<span data-ttu-id="0de4f-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="0de4f-136">Property</span></span>|<span data-ttu-id="0de4f-137">Value</span><span class="sxs-lookup"><span data-stu-id="0de4f-137">Value</span></span>|
    |--------------|-----------|
    |<span data-ttu-id="0de4f-138">Nom</span><span class="sxs-lookup"><span data-stu-id="0de4f-138">Name</span></span>|`mailStackButton`|
    |<span data-ttu-id="0de4f-139">CheckOnClick</span><span class="sxs-lookup"><span data-stu-id="0de4f-139">CheckOnClick</span></span>|<span data-ttu-id="0de4f-140">true</span><span class="sxs-lookup"><span data-stu-id="0de4f-140">true</span></span>|
    |<span data-ttu-id="0de4f-141">CheckState</span><span class="sxs-lookup"><span data-stu-id="0de4f-141">CheckState</span></span>|<xref:System.Windows.Forms.CheckState.Checked>|
    |<span data-ttu-id="0de4f-142">Propriété DisplayStyle</span><span class="sxs-lookup"><span data-stu-id="0de4f-142">DisplayStyle</span></span>|<xref:System.Windows.Forms.ToolStripItemDisplayStyle.ImageAndText>|
    |<span data-ttu-id="0de4f-143">ImageAlign</span><span class="sxs-lookup"><span data-stu-id="0de4f-143">ImageAlign</span></span>|<xref:System.Drawing.ContentAlignment.MiddleLeft>|
    |<span data-ttu-id="0de4f-144">ImageScaling</span><span class="sxs-lookup"><span data-stu-id="0de4f-144">ImageScaling</span></span>|<xref:System.Windows.Forms.ToolStripItemImageScaling.None>|
    |<span data-ttu-id="0de4f-145">ImageTransparentColor</span><span class="sxs-lookup"><span data-stu-id="0de4f-145">ImageTransparentColor</span></span>|`238, 238, 238`|
    |<span data-ttu-id="0de4f-146">Marge</span><span class="sxs-lookup"><span data-stu-id="0de4f-146">Margin</span></span>|`0, 0, 0, 0`|
    |<span data-ttu-id="0de4f-147">Padding</span><span class="sxs-lookup"><span data-stu-id="0de4f-147">Padding</span></span>|`3, 3, 3, 3`|
    |<span data-ttu-id="0de4f-148">Texte</span><span class="sxs-lookup"><span data-stu-id="0de4f-148">Text</span></span>|<span data-ttu-id="0de4f-149">**Messagerie**</span><span class="sxs-lookup"><span data-stu-id="0de4f-149">**Mail**</span></span>|
    |<span data-ttu-id="0de4f-150">TextAlign</span><span class="sxs-lookup"><span data-stu-id="0de4f-150">TextAlign</span></span>|<xref:System.Drawing.ContentAlignment.MiddleLeft>|

5. <span data-ttu-id="0de4f-151">Répétez l’étape 7 pour les trois autres <xref:System.Windows.Forms.ToolStripButton> contrôles.</span><span class="sxs-lookup"><span data-stu-id="0de4f-151">Repeat step 7 for three more <xref:System.Windows.Forms.ToolStripButton> controls.</span></span>

     <span data-ttu-id="0de4f-152">Nommez les contrôles `calendarStackButton`, `contactsStackButton`, et `tasksStackButton`.</span><span class="sxs-lookup"><span data-stu-id="0de4f-152">Name the controls `calendarStackButton`, `contactsStackButton`, and `tasksStackButton`.</span></span> <span data-ttu-id="0de4f-153">Définissez la valeur de la <xref:System.Windows.Forms.Control.Text%2A> propriété **calendrier**, **Contacts**, et **tâches**, respectivement.</span><span class="sxs-lookup"><span data-stu-id="0de4f-153">Set the value of the <xref:System.Windows.Forms.Control.Text%2A> property to **Calendar**, **Contacts**, and **Tasks**, respectively.</span></span>

## <a name="handle-events"></a><span data-ttu-id="0de4f-154">Gérer les événements</span><span class="sxs-lookup"><span data-stu-id="0de4f-154">Handle events</span></span>

<span data-ttu-id="0de4f-155">Deux événements sont importantes pour rendre le `StackView` contrôle se comporte correctement.</span><span class="sxs-lookup"><span data-stu-id="0de4f-155">Two events are important to make the `StackView` control behave correctly.</span></span> <span data-ttu-id="0de4f-156">Gérer le <xref:System.Windows.Forms.UserControl.Load> événement pour positionner le contrôle correctement.</span><span class="sxs-lookup"><span data-stu-id="0de4f-156">Handle the <xref:System.Windows.Forms.UserControl.Load> event to position the control correctly.</span></span> <span data-ttu-id="0de4f-157">Gérer le <xref:System.Windows.Forms.ToolStripItem.Click> événement pour chaque <xref:System.Windows.Forms.ToolStripButton> pour donner le `StackView` contrôler le comportement d’état semblable à la <xref:System.Windows.Forms.RadioButton> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-157">Handle the <xref:System.Windows.Forms.ToolStripItem.Click> event for each <xref:System.Windows.Forms.ToolStripButton> to give the `StackView` control state behavior similar to the <xref:System.Windows.Forms.RadioButton> control.</span></span>

1. <span data-ttu-id="0de4f-158">Dans le Concepteur Windows Forms, sélectionnez le `StackView` contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-158">In the Windows Forms Designer, select the `StackView` control.</span></span>

2. <span data-ttu-id="0de4f-159">Dans la fenêtre **Propriétés**, cliquez sur **Événements**.</span><span class="sxs-lookup"><span data-stu-id="0de4f-159">In the **Properties** window, click **Events**.</span></span>

3. <span data-ttu-id="0de4f-160">Double-cliquez sur l’événement Load pour générer le `StackView_Load` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0de4f-160">Double-click the Load event to generate the `StackView_Load` event handler.</span></span>

4. <span data-ttu-id="0de4f-161">Dans la méthode de gestionnaire d'événements `StackView_Load`, copiez et collez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="0de4f-161">In the `StackView_Load` event handler, copy and paste the following code.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#3)]

5. <span data-ttu-id="0de4f-162">Dans le Concepteur Windows Forms, sélectionnez le `mailStackButton` contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-162">In the Windows Forms Designer, select the `mailStackButton` control.</span></span>

6. <span data-ttu-id="0de4f-163">Dans la fenêtre **Propriétés**, cliquez sur **Événements**.</span><span class="sxs-lookup"><span data-stu-id="0de4f-163">In the **Properties** window, click **Events**.</span></span>

7. <span data-ttu-id="0de4f-164">Double-cliquez sur l’événement Click.</span><span class="sxs-lookup"><span data-stu-id="0de4f-164">Double-click the Click event.</span></span>

     <span data-ttu-id="0de4f-165">Le Concepteur de formulaires Windows génère le `mailStackButton_Click` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0de4f-165">The Windows Forms Designer generates the `mailStackButton_Click` event handler.</span></span>

8. <span data-ttu-id="0de4f-166">Renommer le `mailStackButton_Click` Gestionnaire d’événements à `stackButton_Click`.</span><span class="sxs-lookup"><span data-stu-id="0de4f-166">Rename the `mailStackButton_Click` event handler to `stackButton_Click`.</span></span>

     <span data-ttu-id="0de4f-167">Pour plus d’informations, consultez [renommer un symbole de code (refactorisation)](/visualstudio/ide/reference/rename).</span><span class="sxs-lookup"><span data-stu-id="0de4f-167">For more information, see [Rename a code symbol refactoring](/visualstudio/ide/reference/rename).</span></span>

9. <span data-ttu-id="0de4f-168">Insérez le code suivant dans le `stackButton_Click` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0de4f-168">Insert the following code into the `stackButton_Click` event handler.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#4)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#4)]

10. <span data-ttu-id="0de4f-169">Dans le Concepteur Windows Forms, sélectionnez le `calendarStackButton` contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-169">In the Windows Forms Designer, select the `calendarStackButton` control.</span></span>

11. <span data-ttu-id="0de4f-170">Dans le **propriétés** , configurez l’événement Click pour le `stackButton_Click` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0de4f-170">In the **Properties** window, set the Click event to the `stackButton_Click` event handler.</span></span>

12. <span data-ttu-id="0de4f-171">Répétez les étapes 10 et 11 pour les `contactsStackButton` et `tasksStackButton` contrôles.</span><span class="sxs-lookup"><span data-stu-id="0de4f-171">Repeat steps 10 and 11 for the `contactsStackButton` and `tasksStackButton` controls.</span></span>

## <a name="define-icons"></a><span data-ttu-id="0de4f-172">Définir des icônes</span><span class="sxs-lookup"><span data-stu-id="0de4f-172">Define icons</span></span>

<span data-ttu-id="0de4f-173">Chaque `StackView` bouton a une icône associée.</span><span class="sxs-lookup"><span data-stu-id="0de4f-173">Each `StackView` button has an associated icon.</span></span> <span data-ttu-id="0de4f-174">Pour plus de commodité, chaque icône est représentée sous forme de chaîne codée en Base64, qui est désérialisé avant un <xref:System.Drawing.Bitmap> est créé à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0de4f-174">For convenience, each icon is represented as a Base64-encoded string, which is deserialized before a <xref:System.Drawing.Bitmap> is created from it.</span></span> <span data-ttu-id="0de4f-175">Dans un environnement de production, vous stockez des données bitmap en tant que ressource et vos icônes s’affichent dans le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="0de4f-175">In a production environment, you store bitmap data as a resource, and your icons appear in the Windows Forms Designer.</span></span> <span data-ttu-id="0de4f-176">Pour plus d'informations, voir [Procédure : Ajouter des Images d’arrière-plan à Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dff9f95f(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="0de4f-176">For more information, see [How to: Add Background Images to Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dff9f95f(v=vs.100)).</span></span>

1. <span data-ttu-id="0de4f-177">Dans l’éditeur de Code, insérez le code suivant dans le `StackView` définition de classe.</span><span class="sxs-lookup"><span data-stu-id="0de4f-177">In the Code Editor, insert the following code into the `StackView` class definition.</span></span> <span data-ttu-id="0de4f-178">Ce code initialise les bitmaps pour les <xref:System.Windows.Forms.ToolStripButton> icônes.</span><span class="sxs-lookup"><span data-stu-id="0de4f-178">This code initializes the bitmaps for the <xref:System.Windows.Forms.ToolStripButton> icons.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#2)]

2. <span data-ttu-id="0de4f-179">Ajoutez un appel à la `InitializeImages` méthode dans le `StackView` constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="0de4f-179">Add a call to the `InitializeImages` method in the `StackView` class constructor.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="implement-a-custom-renderer"></a><span data-ttu-id="0de4f-180">Implémenter un convertisseur personnalisé</span><span class="sxs-lookup"><span data-stu-id="0de4f-180">Implement a custom renderer</span></span>

<span data-ttu-id="0de4f-181">Vous pouvez personnaliser la plupart des éléments de la `StackView` contrôler en implémentant une classe qui dérive de la <xref:System.Windows.Forms.ToolStripRenderer> classe.</span><span class="sxs-lookup"><span data-stu-id="0de4f-181">You can customize most elements of the `StackView` control my implementing a class that derives from the <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span> <span data-ttu-id="0de4f-182">Dans cette procédure, vous allez implémenter un <xref:System.Windows.Forms.ToolStripProfessionalRenderer> classe qui personnalise la poignée et dessine des arrière-plans de dégradé pour le <xref:System.Windows.Forms.ToolStripButton> contrôles.</span><span class="sxs-lookup"><span data-stu-id="0de4f-182">In this procedure, you will implement a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class that customizes the grip and draws gradient backgrounds for the <xref:System.Windows.Forms.ToolStripButton> controls.</span></span>

1. <span data-ttu-id="0de4f-183">Insérez le code suivant dans le `StackView` définition du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0de4f-183">Insert the following code into the `StackView` control definition.</span></span>

     <span data-ttu-id="0de4f-184">La définition de la `StackRenderer` classe, qui remplace le <xref:System.Windows.Forms.ToolStripRenderer.RenderGrip>, <xref:System.Windows.Forms.ToolStripRenderer.RenderToolStripBorder>, et <xref:System.Windows.Forms.ToolStripRenderer.RenderButtonBackground> méthodes pour produire une apparence personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0de4f-184">This is the definition for the `StackRenderer` class, which overrides the <xref:System.Windows.Forms.ToolStripRenderer.RenderGrip>, <xref:System.Windows.Forms.ToolStripRenderer.RenderToolStripBorder>, and <xref:System.Windows.Forms.ToolStripRenderer.RenderButtonBackground> methods to produce a custom appearance.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#10)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#10)]

2. <span data-ttu-id="0de4f-185">Dans le `StackView` constructeur du contrôle, créer une nouvelle instance de la `StackRenderer` classe et assignez-la à la `stackStrip` du contrôle <xref:System.Windows.Forms.ToolStrip.Renderer%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="0de4f-185">In the `StackView` control's constructor, create a new instance of the `StackRenderer` class and assign this instance to the `stackStrip` control's <xref:System.Windows.Forms.ToolStrip.Renderer%2A> property.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="test-the-stackview-control"></a><span data-ttu-id="0de4f-186">Tester le contrôle StackView</span><span class="sxs-lookup"><span data-stu-id="0de4f-186">Test the StackView control</span></span>

<span data-ttu-id="0de4f-187">Le `StackView` contrôle dérive le <xref:System.Windows.Forms.UserControl> classe.</span><span class="sxs-lookup"><span data-stu-id="0de4f-187">The `StackView` control derives from the <xref:System.Windows.Forms.UserControl> class.</span></span> <span data-ttu-id="0de4f-188">Par conséquent, vous pouvez tester le contrôle avec le **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="0de4f-188">Therefore, you can test the control with the **UserControl Test Container**.</span></span> <span data-ttu-id="0de4f-189">Pour plus d'informations, voir [Procédure : Tester le comportement au moment de l’exécution d’un UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-189">For more information, see [How to: Test the Run-Time Behavior of a UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md).</span></span>

1. <span data-ttu-id="0de4f-190">Appuyez sur **F5** pour générer le projet et démarrer le **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="0de4f-190">Press **F5** to build the project and start the **UserControl Test Container**.</span></span>

2. <span data-ttu-id="0de4f-191">Déplacez le pointeur sur les boutons de la `StackView` contrôler, puis cliquez sur un bouton pour visualiser l’apparence de son état sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0de4f-191">Move the pointer over the buttons of the `StackView` control, and then click a button to see the appearance of its selected state.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0de4f-192">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0de4f-192">Next steps</span></span>

<span data-ttu-id="0de4f-193">Dans cette procédure pas à pas, vous avez créé un contrôle client personnalisé réutilisable avec l’apparence professionnelle d’un contrôle Office XP.</span><span class="sxs-lookup"><span data-stu-id="0de4f-193">In this walkthrough, you have created a reusable custom client control with the professional appearance of an Office XP control.</span></span> <span data-ttu-id="0de4f-194">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :</span><span class="sxs-lookup"><span data-stu-id="0de4f-194">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>

- <span data-ttu-id="0de4f-195">Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="0de4f-195">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="0de4f-196">Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-196">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

- <span data-ttu-id="0de4f-197">Créer un formulaire avec un menu standard automatiquement rempli.</span><span class="sxs-lookup"><span data-stu-id="0de4f-197">Create a form with an automatically populated standard menu.</span></span> <span data-ttu-id="0de4f-198">Pour plus d’informations, consultez [Procédure pas à pas : En fournissant des éléments de Menu Standard à un formulaire](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-198">For more information, see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>

- <span data-ttu-id="0de4f-199">Créer un formulaire d’interface (multidocument MDI) document avec l’ancrage <xref:System.Windows.Forms.ToolStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="0de4f-199">Create a multiple document interface (MDI) form with docking <xref:System.Windows.Forms.ToolStrip> controls.</span></span> <span data-ttu-id="0de4f-200">Pour plus d'informations, voir [Procédure : Créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-200">For more information, see [How to: Create an MDI Form with Menu Merging and ToolStrip Controls](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0de4f-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0de4f-201">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="0de4f-202">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="0de4f-202">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
- [<span data-ttu-id="0de4f-203">Guide pratique pour Fournir des éléments de Menu Standard à un formulaire</span><span class="sxs-lookup"><span data-stu-id="0de4f-203">How to: Provide Standard Menu Items to a Form</span></span>](how-to-provide-standard-menu-items-to-a-form.md)
