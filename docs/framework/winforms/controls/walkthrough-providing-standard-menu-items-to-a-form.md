---
title: 'Procédure pas à pas : fourniture d’éléments de menu standard à un formulaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], standard
- toolbars [Windows Forms], walkthroughs
- StatusStrip control [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: dac37d98-589e-4d6d-9673-6437e8943122
ms.openlocfilehash: ebfacadfee3ea069359a72ea0402751e9e6280d7
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211498"
---
# <a name="walkthrough-providing-standard-menu-items-to-a-form"></a><span data-ttu-id="17f97-102">Procédure pas à pas : fourniture d’éléments de menu standard à un formulaire</span><span class="sxs-lookup"><span data-stu-id="17f97-102">Walkthrough: Providing Standard Menu Items to a Form</span></span>

<span data-ttu-id="17f97-103">Vous pouvez fournir un menu standard pour vos formulaires avec le contrôle <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="17f97-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>

<span data-ttu-id="17f97-104">Cette procédure pas à pas montre comment utiliser un <xref:System.Windows.Forms.MenuStrip> contrôle pour créer un menu standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-104">This walkthrough demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a standard menu.</span></span> <span data-ttu-id="17f97-105">Le formulaire répond également lorsqu’un utilisateur sélectionne un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="17f97-105">The form also responds when a user selects a menu item.</span></span> <span data-ttu-id="17f97-106">Les tâches suivantes sont illustrées dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="17f97-106">The following tasks are illustrated in this walkthrough:</span></span>

- <span data-ttu-id="17f97-107">Création d’un projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="17f97-107">Creating a Windows Forms project.</span></span>

- <span data-ttu-id="17f97-108">Création d’un menu standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-108">Creating a standard menu.</span></span>

- <span data-ttu-id="17f97-109">Création d’un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="17f97-109">Creating a <xref:System.Windows.Forms.StatusStrip> control.</span></span>

- <span data-ttu-id="17f97-110">Gérer la sélection d’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="17f97-110">Handling menu item selection.</span></span>

<span data-ttu-id="17f97-111">Lorsque vous avez terminé, vous disposerez d’un formulaire avec un menu standard qui affiche les sélections d’élément de menu dans un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="17f97-111">When you are finished, you will have a form with a standard menu that displays menu item selections in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>

<span data-ttu-id="17f97-112">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Fournir des éléments de Menu Standard à un formulaire](how-to-provide-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="17f97-112">To copy the code in this topic as a single listing, see [How to: Provide Standard Menu Items to a Form](how-to-provide-standard-menu-items-to-a-form.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17f97-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="17f97-113">Prerequisites</span></span>

<span data-ttu-id="17f97-114">Vous aurez besoin de Visual Studio pour effectuer cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="17f97-114">You'll need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="17f97-115">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="17f97-115">Create the project</span></span>

1. <span data-ttu-id="17f97-116">Dans Visual Studio, créez un projet d’application Windows appelé **StandardMenuForm** (**fichier** > **New** > **projet**   >  **Visual C#**  ou **Visual Basic** > **bureau classique**  >  **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="17f97-116">In Visual Studio, create a Windows application project called **StandardMenuForm** (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="17f97-117">Dans le Concepteur Windows Forms, sélectionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-117">In the Windows Forms Designer, select the form.</span></span>

## <a name="create-a-standard-menu"></a><span data-ttu-id="17f97-118">Créer un menu standard</span><span class="sxs-lookup"><span data-stu-id="17f97-118">Create a standard menu</span></span>

<span data-ttu-id="17f97-119">Le Concepteur de formulaires Windows peut remplir automatiquement un <xref:System.Windows.Forms.MenuStrip> contrôle avec les éléments de menu standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-119">The Windows Forms Designer can automatically populate a <xref:System.Windows.Forms.MenuStrip> control with standard menu items.</span></span>

1. <span data-ttu-id="17f97-120">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-120">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto your form.</span></span>

2. <span data-ttu-id="17f97-121">Cliquez sur le <xref:System.Windows.Forms.MenuStrip> glyphe de balise active du contrôle (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) et sélectionnez **insérer des éléments Standard**.</span><span class="sxs-lookup"><span data-stu-id="17f97-121">Click the <xref:System.Windows.Forms.MenuStrip> control's smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) and select **Insert Standard Items**.</span></span>

     <span data-ttu-id="17f97-122">Le <xref:System.Windows.Forms.MenuStrip> contrôle soit rempli avec les éléments de menu standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-122">The <xref:System.Windows.Forms.MenuStrip> control is populated with the standard menu items.</span></span>

3. <span data-ttu-id="17f97-123">Cliquez sur le **fichier** élément de menu pour afficher ses éléments de menu par défaut et les icônes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="17f97-123">Click the **File** menu item to see its default menu items and corresponding icons.</span></span>

## <a name="create-a-statusstrip-control"></a><span data-ttu-id="17f97-124">Créer un contrôle StatusStrip</span><span class="sxs-lookup"><span data-stu-id="17f97-124">Create a StatusStrip control</span></span>

<span data-ttu-id="17f97-125">Utilisez le <xref:System.Windows.Forms.StatusStrip> contrôle pour afficher l’état de vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="17f97-125">Use the <xref:System.Windows.Forms.StatusStrip> control to display status for your Windows Forms applications.</span></span> <span data-ttu-id="17f97-126">Dans l’exemple actuel, les éléments de menu sélectionnés par l’utilisateur sont affichés dans un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="17f97-126">In the current example, menu items selected by the user are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>

1. <span data-ttu-id="17f97-127">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.StatusStrip> contrôle vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-127">From the **Toolbox**, drag a <xref:System.Windows.Forms.StatusStrip> control onto your form.</span></span>

     <span data-ttu-id="17f97-128">Le <xref:System.Windows.Forms.StatusStrip> contrôle s’ancre automatiquement vers le bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-128">The <xref:System.Windows.Forms.StatusStrip> control automatically docks to the bottom of the form.</span></span>

2. <span data-ttu-id="17f97-129">Cliquez sur le <xref:System.Windows.Forms.StatusStrip> du contrôle bouton de liste déroulante et sélectionnez **StatusLabel** pour ajouter un <xref:System.Windows.Forms.ToolStripStatusLabel> le contrôle à la <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="17f97-129">Click the <xref:System.Windows.Forms.StatusStrip> control's drop-down button and select **StatusLabel** to add a <xref:System.Windows.Forms.ToolStripStatusLabel> control to the <xref:System.Windows.Forms.StatusStrip> control.</span></span>

## <a name="handle-item-selection"></a><span data-ttu-id="17f97-130">Gérer la sélection d’éléments</span><span class="sxs-lookup"><span data-stu-id="17f97-130">Handle item selection</span></span>

<span data-ttu-id="17f97-131">Gérer le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement répondre quand l’utilisateur sélectionne un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="17f97-131">Handle the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event to respond when the user selects a menu item.</span></span>

1. <span data-ttu-id="17f97-132">Cliquez sur le **fichier** élément de menu que vous avez créé dans la création une section de Menu Standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-132">Click the **File** menu item that you created in the Creating a Standard Menu section.</span></span>

2. <span data-ttu-id="17f97-133">Dans la fenêtre **Propriétés**, cliquez sur **Événements**.</span><span class="sxs-lookup"><span data-stu-id="17f97-133">In the **Properties** window, click **Events**.</span></span>

3. <span data-ttu-id="17f97-134">Double-cliquez sur le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.</span><span class="sxs-lookup"><span data-stu-id="17f97-134">Double-click the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event.</span></span>

     <span data-ttu-id="17f97-135">Le Concepteur de formulaires Windows génère un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.</span><span class="sxs-lookup"><span data-stu-id="17f97-135">The Windows Forms Designer generates an event handler for the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event.</span></span>

4. <span data-ttu-id="17f97-136">Insérez le code suivant dans le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="17f97-136">Insert the following code into the event handler.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#3)]

5. <span data-ttu-id="17f97-137">Insérer le `UpdateStatus` définition de méthode d’utilitaire dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-137">Insert the `UpdateStatus` utility method definition into the form.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#2)]

## <a name="checkpoint--test-your-form"></a><span data-ttu-id="17f97-138">Point de contrôle-tester votre formulaire</span><span class="sxs-lookup"><span data-stu-id="17f97-138">Checkpoint -test your form</span></span>

1. <span data-ttu-id="17f97-139">Appuyez sur **F5** pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="17f97-139">Press **F5** to compile and run your form.</span></span>

2. <span data-ttu-id="17f97-140">Cliquez sur le **fichier** élément de menu pour ouvrir le menu.</span><span class="sxs-lookup"><span data-stu-id="17f97-140">Click the **File** menu item to open the menu.</span></span>

3. <span data-ttu-id="17f97-141">Sur le **fichier** menu, cliquez sur un des éléments pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="17f97-141">On the **File** menu, click one of the items to select it.</span></span>

     <span data-ttu-id="17f97-142">Le <xref:System.Windows.Forms.StatusStrip> contrôle affiche l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="17f97-142">The <xref:System.Windows.Forms.StatusStrip> control displays the selected item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="17f97-143">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="17f97-143">Next steps</span></span>

<span data-ttu-id="17f97-144">Dans cette procédure pas à pas, vous avez créé un formulaire avec un menu standard.</span><span class="sxs-lookup"><span data-stu-id="17f97-144">In this walkthrough, you have created a form with a standard menu.</span></span> <span data-ttu-id="17f97-145">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :</span><span class="sxs-lookup"><span data-stu-id="17f97-145">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>

- <span data-ttu-id="17f97-146">Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="17f97-146">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="17f97-147">Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="17f97-147">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

- <span data-ttu-id="17f97-148">Créer un formulaire d’interface (multidocument MDI) document avec l’ancrage <xref:System.Windows.Forms.ToolStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="17f97-148">Create a multiple document interface (MDI) form with docking <xref:System.Windows.Forms.ToolStrip> controls.</span></span> <span data-ttu-id="17f97-149">Pour plus d’informations, consultez [Procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="17f97-149">For more information, see [Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>

- <span data-ttu-id="17f97-150">Donnez à votre <xref:System.Windows.Forms.ToolStrip> contrôle un aspect professionnel.</span><span class="sxs-lookup"><span data-stu-id="17f97-150">Give your <xref:System.Windows.Forms.ToolStrip> controls a professional appearance.</span></span> <span data-ttu-id="17f97-151">Pour plus d'informations, voir [Procédure : Définir le convertisseur ToolStrip pour une Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="17f97-151">For more information, see [How to: Set the ToolStrip Renderer for an Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="17f97-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f97-152">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="17f97-153">MenuStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="17f97-153">MenuStrip Control</span></span>](menustrip-control-windows-forms.md)
