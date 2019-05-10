---
title: 'Procédure pas à pas : création d’un formulaire MDI avec la fusion des menus et des contrôles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- MDI [Windows Forms], creating forms
- multiple document interface forms
- MDI forms
- ToolStrip control [Windows Forms]
- MDI forms [Windows Forms], creating
- MDI forms [Windows Forms], walkthroughs
ms.assetid: fbab4221-74af-42d0-bbf4-3c97f7b2e544
ms.openlocfilehash: 5853760231cbece27805923c009d83e16c9b0a5e
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211557"
---
# <a name="walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a><span data-ttu-id="e3109-102">Procédure pas à pas : création d’un formulaire MDI avec la fusion des menus et des contrôles ToolStrip</span><span class="sxs-lookup"><span data-stu-id="e3109-102">Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls</span></span>

<span data-ttu-id="e3109-103">L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> prend en charge plusieurs applications MDI (Multiple Document Interface) et le contrôle <xref:System.Windows.Forms.MenuStrip> prend en charge la fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="e3109-103">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace supports multiple document interface (MDI) applications, and the <xref:System.Windows.Forms.MenuStrip> control supports menu merging.</span></span> <span data-ttu-id="e3109-104">Les formulaires MDI peuvent également contenir des contrôles <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="e3109-104">MDI forms can also <xref:System.Windows.Forms.ToolStrip> controls.</span></span>

<span data-ttu-id="e3109-105">Cette procédure pas à pas montre comment utiliser <xref:System.Windows.Forms.ToolStripPanel> contrôles avec un formulaire MDI.</span><span class="sxs-lookup"><span data-stu-id="e3109-105">This walkthrough demonstrates how to use <xref:System.Windows.Forms.ToolStripPanel> controls with an MDI form.</span></span> <span data-ttu-id="e3109-106">Le formulaire prend également en charge la fusion de menus avec les menus enfants.</span><span class="sxs-lookup"><span data-stu-id="e3109-106">The form also supports menu merging with child menus.</span></span> <span data-ttu-id="e3109-107">Les tâches suivantes sont illustrées dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="e3109-107">The following tasks are illustrated in this walkthrough:</span></span>

- <span data-ttu-id="e3109-108">Création d’un projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e3109-108">Creating a Windows Forms project.</span></span>

- <span data-ttu-id="e3109-109">Création du menu principal pour votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-109">Creating the main menu for your form.</span></span> <span data-ttu-id="e3109-110">Le nom réel du menu varient.</span><span class="sxs-lookup"><span data-stu-id="e3109-110">The actual name of the menu will vary.</span></span>

- <span data-ttu-id="e3109-111">Ajout de la <xref:System.Windows.Forms.ToolStripPanel> le contrôle à la **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="e3109-111">Adding the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox**.</span></span>

- <span data-ttu-id="e3109-112">Création d’un formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="e3109-112">Creating a child form.</span></span>

- <span data-ttu-id="e3109-113">Réorganisation <xref:System.Windows.Forms.ToolStripPanel> par ordre de plan des contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-113">Arranging <xref:System.Windows.Forms.ToolStripPanel> controls by z-order.</span></span>

<span data-ttu-id="e3109-114">Lorsque vous avez terminé, avoir un formulaire MDI qui prend en charge la fusion de menus et movable <xref:System.Windows.Forms.ToolStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-114">When you are finished, you will have an MDI form that supports menu merging and movable <xref:System.Windows.Forms.ToolStrip> controls.</span></span>

<span data-ttu-id="e3109-115">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e3109-115">To copy the code in this topic as a single listing, see [How to: Create an MDI Form with Menu Merging and ToolStrip Controls](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3109-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e3109-116">Prerequisites</span></span>

<span data-ttu-id="e3109-117">Vous aurez besoin de Visual Studio pour effectuer cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="e3109-117">You'll need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="e3109-118">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="e3109-118">Create the project</span></span>

1. <span data-ttu-id="e3109-119">Dans Visual Studio, créez un projet d’Application de Windows appelé **MdiForm** (**fichier** > **New** > **projet**  >  **Visual C#**  ou **Visual Basic** > **bureau classique**  >   **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="e3109-119">In Visual Studio, create a Windows Application project called **MdiForm** (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="e3109-120">Dans le Concepteur Windows Forms, sélectionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-120">In the Windows Forms Designer, select the form.</span></span>

3. <span data-ttu-id="e3109-121">Dans la fenêtre Propriétés, définissez la valeur de la <xref:System.Windows.Forms.Form.IsMdiContainer%2A> à `true`.</span><span class="sxs-lookup"><span data-stu-id="e3109-121">In the Properties window, set the value of the <xref:System.Windows.Forms.Form.IsMdiContainer%2A> to `true`.</span></span>

## <a name="create-the-main-menu"></a><span data-ttu-id="e3109-122">Créer le menu principal</span><span class="sxs-lookup"><span data-stu-id="e3109-122">Create the main menu</span></span>

<span data-ttu-id="e3109-123">Le formulaire MDI parent contient le menu principal.</span><span class="sxs-lookup"><span data-stu-id="e3109-123">The parent MDI form contains the main menu.</span></span> <span data-ttu-id="e3109-124">Le menu principal possède un élément de menu nommé **fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="e3109-124">The main menu has one menu item named **Window**.</span></span> <span data-ttu-id="e3109-125">Avec le **fenêtre** élément de menu, vous pouvez créer des formulaires enfants.</span><span class="sxs-lookup"><span data-stu-id="e3109-125">With the **Window** menu item, you can create child forms.</span></span> <span data-ttu-id="e3109-126">Éléments de menu à partir de formulaires enfants sont fusionnés dans le menu principal.</span><span class="sxs-lookup"><span data-stu-id="e3109-126">Menu items from child forms are merged into the main menu.</span></span>

1. <span data-ttu-id="e3109-127">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-127">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the form.</span></span>

2. <span data-ttu-id="e3109-128">Ajouter un <xref:System.Windows.Forms.ToolStripMenuItem> à la <xref:System.Windows.Forms.MenuStrip> contrôler et nommez-le **fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="e3109-128">Add a <xref:System.Windows.Forms.ToolStripMenuItem> to the <xref:System.Windows.Forms.MenuStrip> control and name it **Window**.</span></span>

3. <span data-ttu-id="e3109-129">Sélectionnez le contrôle <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="e3109-129">Select the <xref:System.Windows.Forms.MenuStrip> control.</span></span>

4. <span data-ttu-id="e3109-130">Dans la fenêtre Propriétés, définissez la valeur de la <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> propriété `ToolStripMenuItem1`.</span><span class="sxs-lookup"><span data-stu-id="e3109-130">In the Properties window, set the value of the <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property to `ToolStripMenuItem1`.</span></span>

5. <span data-ttu-id="e3109-131">Ajouter un sous-élément à la **fenêtre** élément de menu, puis nommez le sous-élément **New**.</span><span class="sxs-lookup"><span data-stu-id="e3109-131">Add a subitem to the **Window** menu item, and then name the subitem **New**.</span></span>

6. <span data-ttu-id="e3109-132">Dans la fenêtre Propriétés, cliquez sur **événements**.</span><span class="sxs-lookup"><span data-stu-id="e3109-132">In the Properties window, click **Events**.</span></span>

7. <span data-ttu-id="e3109-133">Double-cliquez sur le <xref:System.Windows.Forms.ToolStripItem.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="e3109-133">Double-click the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>

     <span data-ttu-id="e3109-134">Le Concepteur de formulaires Windows génère un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="e3109-134">The Windows Forms Designer generates an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>

8. <span data-ttu-id="e3109-135">Insérez le code suivant dans le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="e3109-135">Insert the following code into the event handler.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#2)]

## <a name="add-the-toolstrippanel-control-to-the-toolbox"></a><span data-ttu-id="e3109-136">Ajouter le contrôle ToolStripPanel à la boîte à outils</span><span class="sxs-lookup"><span data-stu-id="e3109-136">Add the ToolStripPanel control to the Toolbox</span></span>

<span data-ttu-id="e3109-137">Lorsque vous utilisez <xref:System.Windows.Forms.MenuStrip> contrôles avec un formulaire MDI doit avoir le <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3109-137">When you use <xref:System.Windows.Forms.MenuStrip> controls with an MDI form you must have the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="e3109-138">Vous devez ajouter le <xref:System.Windows.Forms.ToolStripPanel> le contrôle à la **boîte à outils** pour générer votre formulaire MDI dans le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="e3109-138">You must add the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox** to build your MDI form in the Windows Forms Designer.</span></span>

1. <span data-ttu-id="e3109-139">Ouvrez le **boîte à outils**, puis cliquez sur le **tous les Windows Forms** onglet pour afficher les contrôles Windows Forms disponibles.</span><span class="sxs-lookup"><span data-stu-id="e3109-139">Open the **Toolbox**, and then click the **All Windows Forms** tab to show the available Windows Forms controls.</span></span>

2. <span data-ttu-id="e3109-140">Avec le bouton droit pour ouvrir le menu contextuel, puis sélectionnez **choisir des éléments de**.</span><span class="sxs-lookup"><span data-stu-id="e3109-140">Right-click to open the shortcut menu, and select **Choose Items**.</span></span>

3. <span data-ttu-id="e3109-141">Dans le **Choose Toolbox Items** boîte de dialogue, faites défiler vers le bas le **nom** colonne jusqu'à ce que vous trouviez **ToolStripPanel**.</span><span class="sxs-lookup"><span data-stu-id="e3109-141">In the **Choose Toolbox Items** dialog box, scroll down the **Name** column until you find **ToolStripPanel**.</span></span>

4. <span data-ttu-id="e3109-142">Sélectionnez la case à cocher par **ToolStripPanel**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3109-142">Select the check box by **ToolStripPanel**, and then click **OK**.</span></span>

     <span data-ttu-id="e3109-143">Le <xref:System.Windows.Forms.ToolStripPanel> contrôle s’affiche dans le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="e3109-143">The <xref:System.Windows.Forms.ToolStripPanel> control appears in the **Toolbox**.</span></span>

## <a name="create-a-child-form"></a><span data-ttu-id="e3109-144">Créer un formulaire enfant</span><span class="sxs-lookup"><span data-stu-id="e3109-144">Create a child form</span></span>

<span data-ttu-id="e3109-145">Dans cette procédure, vous allez définir une classe de formulaire enfant distincte qui possède son propre <xref:System.Windows.Forms.MenuStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3109-145">In this procedure, you will define a separate child form class that has its own <xref:System.Windows.Forms.MenuStrip> control.</span></span> <span data-ttu-id="e3109-146">Les éléments de menu pour ce formulaire sont fusionnés avec ceux du formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="e3109-146">The menu items for this form are merged with those of the parent form.</span></span>

1. <span data-ttu-id="e3109-147">Ajoutez un nouveau formulaire nommé `ChildForm` au projet.</span><span class="sxs-lookup"><span data-stu-id="e3109-147">Add a new form named `ChildForm` to the project.</span></span>

     <span data-ttu-id="e3109-148">Pour plus d'informations, voir [Procédure : Ajouter des Windows Forms à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e3109-148">For more information, see [How to: Add Windows Forms to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span></span>

2. <span data-ttu-id="e3109-149">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers le formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="e3109-149">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the child form.</span></span>

3. <span data-ttu-id="e3109-150">Cliquez sur le <xref:System.Windows.Forms.MenuStrip> glyphe de balise active du contrôle (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")), puis sélectionnez **modifier les éléments**.</span><span class="sxs-lookup"><span data-stu-id="e3109-150">Click the <xref:System.Windows.Forms.MenuStrip> control's smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")), and then select **Edit Items**.</span></span>

4. <span data-ttu-id="e3109-151">Dans le **éditeur de collections Items** boîte de dialogue zone, ajoutez une nouvelle <xref:System.Windows.Forms.ToolStripMenuItem> nommé **ChildMenuItem** au menu enfant.</span><span class="sxs-lookup"><span data-stu-id="e3109-151">In the **Items Collection Editor** dialog box, add a new <xref:System.Windows.Forms.ToolStripMenuItem> named **ChildMenuItem** to the child menu.</span></span>

     <span data-ttu-id="e3109-152">Pour plus d’informations, consultez [éditeur de collections d’éléments ToolStrip](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e3109-152">For more information, see [ToolStrip Items Collection Editor](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100)).</span></span>

## <a name="test-the-form"></a><span data-ttu-id="e3109-153">Le formulaire de test</span><span class="sxs-lookup"><span data-stu-id="e3109-153">Test the form</span></span>

1. <span data-ttu-id="e3109-154">Appuyez sur **F5** pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-154">Press **F5** to compile and run your form.</span></span>

2. <span data-ttu-id="e3109-155">Cliquez sur le **fenêtre** élément de menu pour ouvrir le menu, puis cliquez sur **New**.</span><span class="sxs-lookup"><span data-stu-id="e3109-155">Click the **Window** menu item to open the menu, and then click **New**.</span></span>

     <span data-ttu-id="e3109-156">Un nouveau formulaire enfant est créé dans la zone du formulaire MDI client.</span><span class="sxs-lookup"><span data-stu-id="e3109-156">A new child form is created in the form's MDI client area.</span></span> <span data-ttu-id="e3109-157">Les menus du formulaire enfant sont fusionné avec le menu principal.</span><span class="sxs-lookup"><span data-stu-id="e3109-157">The child form's menu is merged with the main menu.</span></span>

3. <span data-ttu-id="e3109-158">Fermez le formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="e3109-158">Close the child form.</span></span>

     <span data-ttu-id="e3109-159">Les menus du formulaire enfant sont supprimé dans le menu principal.</span><span class="sxs-lookup"><span data-stu-id="e3109-159">The child form's menu is removed from the main menu.</span></span>

4. <span data-ttu-id="e3109-160">Cliquez sur **New** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="e3109-160">Click **New** several times.</span></span>

     <span data-ttu-id="e3109-161">Les formulaires enfants sont automatiquement répertoriés sous la **fenêtre** élément de menu, car le <xref:System.Windows.Forms.MenuStrip> du contrôle <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> propriété est affectée.</span><span class="sxs-lookup"><span data-stu-id="e3109-161">The child forms are automatically listed under the **Window** menu item because the <xref:System.Windows.Forms.MenuStrip> control's <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property is assigned.</span></span>

## <a name="add-toolstrip-support"></a><span data-ttu-id="e3109-162">Ajouter la prise en charge de ToolStrip</span><span class="sxs-lookup"><span data-stu-id="e3109-162">Add ToolStrip support</span></span>

<span data-ttu-id="e3109-163">Dans cette procédure, vous allez ajouter quatre <xref:System.Windows.Forms.ToolStrip> contrôles au formulaire parent MDI.</span><span class="sxs-lookup"><span data-stu-id="e3109-163">In this procedure, you will add four <xref:System.Windows.Forms.ToolStrip> controls to the MDI parent form.</span></span> <span data-ttu-id="e3109-164">Chaque <xref:System.Windows.Forms.ToolStrip> contrôle est ajouté à l’intérieur d’un <xref:System.Windows.Forms.ToolStripPanel> contrôle, qui est ancré au bord du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-164">Each <xref:System.Windows.Forms.ToolStrip> control is added inside a <xref:System.Windows.Forms.ToolStripPanel> control, which is docked to the edge of the form.</span></span>

1. <span data-ttu-id="e3109-165">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.ToolStripPanel> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-165">From the **Toolbox**, drag a <xref:System.Windows.Forms.ToolStripPanel> control onto the form.</span></span>

2. <span data-ttu-id="e3109-166">Avec le <xref:System.Windows.Forms.ToolStripPanel> contrôle sélectionné, double-cliquez sur le <xref:System.Windows.Forms.ToolStrip> dans contrôler le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="e3109-166">With the <xref:System.Windows.Forms.ToolStripPanel> control selected, double-click the <xref:System.Windows.Forms.ToolStrip> control in the **Toolbox**.</span></span>

     <span data-ttu-id="e3109-167">Un <xref:System.Windows.Forms.ToolStrip> contrôle est créé dans le <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3109-167">A <xref:System.Windows.Forms.ToolStrip> control is created in the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

3. <span data-ttu-id="e3109-168">Sélectionnez le contrôle <xref:System.Windows.Forms.ToolStripPanel>.</span><span class="sxs-lookup"><span data-stu-id="e3109-168">Select the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

4. <span data-ttu-id="e3109-169">Dans la fenêtre Propriétés, modifiez la valeur du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Left>.</span><span class="sxs-lookup"><span data-stu-id="e3109-169">In the Properties window, change the value of the control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Left>.</span></span>

     <span data-ttu-id="e3109-170">Le <xref:System.Windows.Forms.ToolStripPanel> contrôler s’ancre sur le côté gauche du formulaire, sous le menu principal.</span><span class="sxs-lookup"><span data-stu-id="e3109-170">The <xref:System.Windows.Forms.ToolStripPanel> control docks to the left side of the form, underneath the main menu.</span></span> <span data-ttu-id="e3109-171">La zone cliente MDI est redimensionné pour s’ajuster à la <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3109-171">The MDI client area resizes to fit the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

5. <span data-ttu-id="e3109-172">Répétez les étapes 1 à 4.</span><span class="sxs-lookup"><span data-stu-id="e3109-172">Repeat steps 1 through 4.</span></span>

     <span data-ttu-id="e3109-173">Ancrer la nouvelle <xref:System.Windows.Forms.ToolStripPanel> contrôle vers le haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-173">Dock the new <xref:System.Windows.Forms.ToolStripPanel> control to the top of the form.</span></span>

     <span data-ttu-id="e3109-174">Le <xref:System.Windows.Forms.ToolStripPanel> contrôle est ancré sous le menu principal, mais à droite de la première <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e3109-174">The <xref:System.Windows.Forms.ToolStripPanel> control is docked underneath the main menu, but to the right of the first <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="e3109-175">Cette étape illustre l’importance de l’ordre de plan positionner correctement <xref:System.Windows.Forms.ToolStripPanel> contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-175">This step illustrates the importance of z-order in correctly positioning <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>

6. <span data-ttu-id="e3109-176">Répétez les étapes 1 à 4 pour deux autres <xref:System.Windows.Forms.ToolStripPanel> contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-176">Repeat steps 1 through 4 for two more <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>

     <span data-ttu-id="e3109-177">Ancrer la nouvelle <xref:System.Windows.Forms.ToolStripPanel> contrôles vers la droite et le bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-177">Dock the new <xref:System.Windows.Forms.ToolStripPanel> controls to the right and bottom of the form.</span></span>

## <a name="arrange-toolstrippanel-controls-by-z-order"></a><span data-ttu-id="e3109-178">Organiser par ordre de plan des contrôles ToolStripPanel</span><span class="sxs-lookup"><span data-stu-id="e3109-178">Arrange ToolStripPanel controls by Z-order</span></span>

<span data-ttu-id="e3109-179">La position d’une fenêtre fixe <xref:System.Windows.Forms.ToolStripPanel> contrôle sur votre formulaire MDI est déterminée par la position du contrôle dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="e3109-179">The position of a docked <xref:System.Windows.Forms.ToolStripPanel> control on your MDI form is determined by the control's position in the z-order.</span></span> <span data-ttu-id="e3109-180">Vous pouvez facilement réorganiser l’ordre de plan de vos contrôles dans la fenêtre Structure du Document.</span><span class="sxs-lookup"><span data-stu-id="e3109-180">You can easily arrange the z-order of your controls in the Document Outline window.</span></span>

1. <span data-ttu-id="e3109-181">Dans le **vue** menu, cliquez sur **Windows autres**, puis cliquez sur **structure du Document**.</span><span class="sxs-lookup"><span data-stu-id="e3109-181">In the **View** menu, click **Other Windows**, and then click **Document Outline**.</span></span>

     <span data-ttu-id="e3109-182">La disposition de votre <xref:System.Windows.Forms.ToolStripPanel> contrôles à partir de la procédure précédente n’est pas standard.</span><span class="sxs-lookup"><span data-stu-id="e3109-182">The arrangement of your <xref:System.Windows.Forms.ToolStripPanel> controls from the previous procedure is nonstandard.</span></span> <span data-ttu-id="e3109-183">Il s’agit, car l’ordre de plan n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="e3109-183">This is because the z-order is not correct.</span></span> <span data-ttu-id="e3109-184">Utilisez la fenêtre Structure du Document pour modifier l’ordre de plan des contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-184">Use the Document Outline window to change the z-order of the controls.</span></span>

2. <span data-ttu-id="e3109-185">Dans la fenêtre Structure du Document, sélectionnez **ToolStripPanel4**.</span><span class="sxs-lookup"><span data-stu-id="e3109-185">In the Document Outline window, select **ToolStripPanel4**.</span></span>

3. <span data-ttu-id="e3109-186">Cliquez sur le bouton de flèche vers le bas à plusieurs reprises, jusqu'à ce que **ToolStripPanel4** figure au bas de la liste.</span><span class="sxs-lookup"><span data-stu-id="e3109-186">Click the down-arrow button repeatedly, until **ToolStripPanel4** is at the bottom of the list.</span></span>

     <span data-ttu-id="e3109-187">Le **ToolStripPanel4** contrôle est ancré en bas du formulaire, sous les autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-187">The **ToolStripPanel4** control is docked to the bottom of the form, underneath the other controls.</span></span>

4. <span data-ttu-id="e3109-188">Sélectionnez **ToolStripPanel2**.</span><span class="sxs-lookup"><span data-stu-id="e3109-188">Select **ToolStripPanel2**.</span></span>

5. <span data-ttu-id="e3109-189">Cliquez sur le bouton de flèche vers le bas une fois pour positionner le troisième contrôle dans la liste.</span><span class="sxs-lookup"><span data-stu-id="e3109-189">Click the down-arrow button one time to position the control third in the list.</span></span>

     <span data-ttu-id="e3109-190">Le **ToolStripPanel2** contrôle est ancré en haut du formulaire, sous le menu principal et au-dessus des autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="e3109-190">The **ToolStripPanel2** control is docked to the top of the form, underneath the main menu and above the other controls.</span></span>

6. <span data-ttu-id="e3109-191">Sélectionnez différents contrôles dans le **structure du Document** fenêtre et de les déplacer à différents endroits dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="e3109-191">Select various controls in the **Document Outline** window and move them to different positions in the z-order.</span></span> <span data-ttu-id="e3109-192">Notez l’effet de l’ordre de plan sur la position des contrôles ancrés.</span><span class="sxs-lookup"><span data-stu-id="e3109-192">Note the effect of the z-order on the placement of docked controls.</span></span> <span data-ttu-id="e3109-193">Utilisez CTRL + Z ou **Annuler** sur le **modifier** menu Annuler vos modifications.</span><span class="sxs-lookup"><span data-stu-id="e3109-193">Use CTRL-Z or **Undo** on the **Edit** menu to undo your changes.</span></span>

## <a name="checkpoint---test-your-form"></a><span data-ttu-id="e3109-194">Point de contrôle - tester votre formulaire</span><span class="sxs-lookup"><span data-stu-id="e3109-194">Checkpoint - test your form</span></span>

1. <span data-ttu-id="e3109-195">Appuyez sur **F5** pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-195">Press **F5** to compile and run your form.</span></span>

2. <span data-ttu-id="e3109-196">Cliquez sur la poignée d’un <xref:System.Windows.Forms.ToolStrip> contrôler et faites glisser le contrôle à des positions différentes dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e3109-196">Click the grip of a <xref:System.Windows.Forms.ToolStrip> control and drag the control to different positions on the form.</span></span>

     <span data-ttu-id="e3109-197">Vous pouvez faire glisser un <xref:System.Windows.Forms.ToolStrip> contrôle à partir d’un <xref:System.Windows.Forms.ToolStripPanel> contrôle vers un autre.</span><span class="sxs-lookup"><span data-stu-id="e3109-197">You can drag a <xref:System.Windows.Forms.ToolStrip> control from one <xref:System.Windows.Forms.ToolStripPanel> control to another.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e3109-198">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e3109-198">Next steps</span></span>

<span data-ttu-id="e3109-199">Dans cette procédure pas à pas, vous avez créé un formulaire MDI parent avec <xref:System.Windows.Forms.ToolStrip> de contrôles et de fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="e3109-199">In this walkthrough, you have created an MDI parent form with <xref:System.Windows.Forms.ToolStrip> controls and menu merging.</span></span> <span data-ttu-id="e3109-200">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :</span><span class="sxs-lookup"><span data-stu-id="e3109-200">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>

- <span data-ttu-id="e3109-201">Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="e3109-201">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="e3109-202">Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="e3109-202">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

- <span data-ttu-id="e3109-203">Créé un formulaire avec un menu standard automatiquement rempli.</span><span class="sxs-lookup"><span data-stu-id="e3109-203">Created a form with an automatically populated standard menu.</span></span> <span data-ttu-id="e3109-204">Pour plus d’informations, consultez [Procédure pas à pas : En fournissant des éléments de Menu Standard à un formulaire](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="e3109-204">For more information, see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>

- <span data-ttu-id="e3109-205">Donnez à votre <xref:System.Windows.Forms.ToolStrip> contrôle un aspect professionnel.</span><span class="sxs-lookup"><span data-stu-id="e3109-205">Give your <xref:System.Windows.Forms.ToolStrip> controls a professional appearance.</span></span> <span data-ttu-id="e3109-206">Pour plus d'informations, voir [Procédure : Définir le convertisseur ToolStrip pour une Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="e3109-206">For more information, see [How to: Set the ToolStrip Renderer for an Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e3109-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3109-207">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="e3109-208">Guide pratique pour Créer des formulaires MDI parents</span><span class="sxs-lookup"><span data-stu-id="e3109-208">How to: Create MDI Parent Forms</span></span>](../advanced/how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="e3109-209">Guide pratique pour Créer des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="e3109-209">How to: Create MDI Child Forms</span></span>](../advanced/how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="e3109-210">Guide pratique pour Insérer un MenuStrip dans un Menu du menu déroulant MDI</span><span class="sxs-lookup"><span data-stu-id="e3109-210">How to: Insert a MenuStrip into an MDI Drop-Down Menu</span></span>](how-to-insert-a-menustrip-into-an-mdi-drop-down-menu-windows-forms.md)
- [<span data-ttu-id="e3109-211">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="e3109-211">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
