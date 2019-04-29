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
ms.openlocfilehash: b4957a3f2efcb31594806a188e3d3bb10c2dac09
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61792208"
---
# <a name="walkthrough-providing-standard-menu-items-to-a-form"></a><span data-ttu-id="e9c30-102">Procédure pas à pas : fourniture d’éléments de menu standard à un formulaire</span><span class="sxs-lookup"><span data-stu-id="e9c30-102">Walkthrough: Providing Standard Menu Items to a Form</span></span>
<span data-ttu-id="e9c30-103">Vous pouvez fournir un menu standard pour vos formulaires avec le contrôle <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="e9c30-103">You can provide a standard menu for your forms with the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
 <span data-ttu-id="e9c30-104">Cette procédure pas à pas montre comment utiliser un <xref:System.Windows.Forms.MenuStrip> contrôle pour créer un menu standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-104">This walkthrough demonstrates how to use a <xref:System.Windows.Forms.MenuStrip> control to create a standard menu.</span></span> <span data-ttu-id="e9c30-105">Le formulaire répond également lorsqu’un utilisateur sélectionne un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e9c30-105">The form also responds when a user selects a menu item.</span></span> <span data-ttu-id="e9c30-106">Les tâches suivantes sont illustrées dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="e9c30-106">The following tasks are illustrated in this walkthrough:</span></span>  
  
- <span data-ttu-id="e9c30-107">Création d’un projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e9c30-107">Creating a Windows Forms project.</span></span>  
  
- <span data-ttu-id="e9c30-108">Création d’un menu standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-108">Creating a standard menu.</span></span>  
  
- <span data-ttu-id="e9c30-109">Création d’un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e9c30-109">Creating a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
- <span data-ttu-id="e9c30-110">Gérer la sélection d’éléments de menu.</span><span class="sxs-lookup"><span data-stu-id="e9c30-110">Handling menu item selection.</span></span>  
  
 <span data-ttu-id="e9c30-111">Lorsque vous avez terminé, vous disposerez d’un formulaire avec un menu standard qui affiche les sélections d’élément de menu dans un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e9c30-111">When you are finished, you will have a form with a standard menu that displays menu item selections in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
 <span data-ttu-id="e9c30-112">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Fournir des éléments de Menu Standard à un formulaire](how-to-provide-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="e9c30-112">To copy the code in this topic as a single listing, see [How to: Provide Standard Menu Items to a Form](how-to-provide-standard-menu-items-to-a-form.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e9c30-113">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="e9c30-113">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="e9c30-114">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="e9c30-114">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="e9c30-115">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="e9c30-115">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="e9c30-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e9c30-116">Prerequisites</span></span>  
 <span data-ttu-id="e9c30-117">Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e9c30-117">In order to complete this walkthrough, you will need:</span></span>  
  
- <span data-ttu-id="e9c30-118">Autorisations suffisantes pour pouvoir créer et exécuter des projets d’application Windows Forms sur l’ordinateur où Visual Studio est installé.</span><span class="sxs-lookup"><span data-stu-id="e9c30-118">Sufficient permissions to be able to create and run Windows Forms application projects on the computer where Visual Studio is installed.</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="e9c30-119">Création du projet</span><span class="sxs-lookup"><span data-stu-id="e9c30-119">Creating the Project</span></span>  
 <span data-ttu-id="e9c30-120">La première étape consiste à créer le projet et à configurer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-120">The first step is to create the project and set up the form.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="e9c30-121">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="e9c30-121">To create the project</span></span>  
  
1. <span data-ttu-id="e9c30-122">Créez un projet d’application Windows appelé **StandardMenuForm** (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="e9c30-122">Create a Windows application project called **StandardMenuForm** (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2. <span data-ttu-id="e9c30-123">Dans le Concepteur Windows Forms, sélectionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-123">In the Windows Forms Designer, select the form.</span></span>  
  
## <a name="creating-a-standard-menu"></a><span data-ttu-id="e9c30-124">Création d’un Menu Standard</span><span class="sxs-lookup"><span data-stu-id="e9c30-124">Creating a Standard Menu</span></span>  
 <span data-ttu-id="e9c30-125">Le Concepteur de formulaires Windows peut remplir automatiquement un <xref:System.Windows.Forms.MenuStrip> contrôle avec les éléments de menu standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-125">The Windows Forms Designer can automatically populate a <xref:System.Windows.Forms.MenuStrip> control with standard menu items.</span></span>  
  
#### <a name="to-create-a-standard-menu"></a><span data-ttu-id="e9c30-126">Pour créer un menu standard</span><span class="sxs-lookup"><span data-stu-id="e9c30-126">To create a standard menu</span></span>  
  
1. <span data-ttu-id="e9c30-127">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-127">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto your form.</span></span>  
  
2. <span data-ttu-id="e9c30-128">Cliquez sur le <xref:System.Windows.Forms.MenuStrip> glyphe de balise active du contrôle (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) et sélectionnez **insérer des éléments Standard**.</span><span class="sxs-lookup"><span data-stu-id="e9c30-128">Click the <xref:System.Windows.Forms.MenuStrip> control's smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) and select **Insert Standard Items**.</span></span>  
  
     <span data-ttu-id="e9c30-129">Le <xref:System.Windows.Forms.MenuStrip> contrôle soit rempli avec les éléments de menu standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-129">The <xref:System.Windows.Forms.MenuStrip> control is populated with the standard menu items.</span></span>  
  
3. <span data-ttu-id="e9c30-130">Cliquez sur le **fichier** élément de menu pour afficher ses éléments de menu par défaut et les icônes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="e9c30-130">Click the **File** menu item to see its default menu items and corresponding icons.</span></span>  
  
## <a name="creating-a-statusstrip-control"></a><span data-ttu-id="e9c30-131">Création d’un contrôle StatusStrip</span><span class="sxs-lookup"><span data-stu-id="e9c30-131">Creating a StatusStrip Control</span></span>  
 <span data-ttu-id="e9c30-132">Utilisez le <xref:System.Windows.Forms.StatusStrip> contrôle pour afficher l’état de vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="e9c30-132">Use the <xref:System.Windows.Forms.StatusStrip> control to display status for your Windows Forms applications.</span></span> <span data-ttu-id="e9c30-133">Dans l’exemple actuel, les éléments de menu sélectionnés par l’utilisateur sont affichés dans un <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e9c30-133">In the current example, menu items selected by the user are displayed in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
#### <a name="to-create-a-statusstrip-control"></a><span data-ttu-id="e9c30-134">Pour créer un contrôle StatusStrip</span><span class="sxs-lookup"><span data-stu-id="e9c30-134">To create a StatusStrip control</span></span>  
  
1. <span data-ttu-id="e9c30-135">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.StatusStrip> contrôle vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-135">From the **Toolbox**, drag a <xref:System.Windows.Forms.StatusStrip> control onto your form.</span></span>  
  
     <span data-ttu-id="e9c30-136">Le <xref:System.Windows.Forms.StatusStrip> contrôle s’ancre automatiquement vers le bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-136">The <xref:System.Windows.Forms.StatusStrip> control automatically docks to the bottom of the form.</span></span>  
  
2. <span data-ttu-id="e9c30-137">Cliquez sur le <xref:System.Windows.Forms.StatusStrip> du contrôle bouton de liste déroulante et sélectionnez **StatusLabel** pour ajouter un <xref:System.Windows.Forms.ToolStripStatusLabel> le contrôle à la <xref:System.Windows.Forms.StatusStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="e9c30-137">Click the <xref:System.Windows.Forms.StatusStrip> control's drop-down button and select **StatusLabel** to add a <xref:System.Windows.Forms.ToolStripStatusLabel> control to the <xref:System.Windows.Forms.StatusStrip> control.</span></span>  
  
## <a name="handling-item-selection"></a><span data-ttu-id="e9c30-138">Sélection d’éléments de gestion</span><span class="sxs-lookup"><span data-stu-id="e9c30-138">Handling Item Selection</span></span>  
 <span data-ttu-id="e9c30-139">Gérer le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement répondre quand l’utilisateur sélectionne un élément de menu.</span><span class="sxs-lookup"><span data-stu-id="e9c30-139">Handle the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event to respond when the user selects a menu item.</span></span>  
  
#### <a name="to-handle-item-selection"></a><span data-ttu-id="e9c30-140">Pour gérer la sélection d’éléments</span><span class="sxs-lookup"><span data-stu-id="e9c30-140">To handle item selection</span></span>  
  
1. <span data-ttu-id="e9c30-141">Cliquez sur le **fichier** élément de menu que vous avez créé dans la création une section de Menu Standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-141">Click the **File** menu item that you created in the Creating a Standard Menu section.</span></span>  
  
2. <span data-ttu-id="e9c30-142">Dans la fenêtre **Propriétés**, cliquez sur **Événements**.</span><span class="sxs-lookup"><span data-stu-id="e9c30-142">In the **Properties** window, click **Events**.</span></span>  
  
3. <span data-ttu-id="e9c30-143">Double-cliquez sur le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.</span><span class="sxs-lookup"><span data-stu-id="e9c30-143">Double-click the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event.</span></span>  
  
     <span data-ttu-id="e9c30-144">Le Concepteur de formulaires Windows génère un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.</span><span class="sxs-lookup"><span data-stu-id="e9c30-144">The Windows Forms Designer generates an event handler for the <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> event.</span></span>  
  
4. <span data-ttu-id="e9c30-145">Insérez le code suivant dans le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="e9c30-145">Insert the following code into the event handler.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#3)]  
  
5. <span data-ttu-id="e9c30-146">Insérer le `UpdateStatus` définition de méthode d’utilitaire dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-146">Insert the `UpdateStatus` utility method definition into the form.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#2)]  
  
## <a name="checkpoint"></a><span data-ttu-id="e9c30-147">Point de contrôle</span><span class="sxs-lookup"><span data-stu-id="e9c30-147">Checkpoint</span></span>  
  
#### <a name="to-test-your-form"></a><span data-ttu-id="e9c30-148">Pour tester votre formulaire</span><span class="sxs-lookup"><span data-stu-id="e9c30-148">To test your form</span></span>  
  
1. <span data-ttu-id="e9c30-149">Appuyez sur F5 pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e9c30-149">Press F5 to compile and run your form.</span></span>  
  
2. <span data-ttu-id="e9c30-150">Cliquez sur le **fichier** élément de menu pour ouvrir le menu.</span><span class="sxs-lookup"><span data-stu-id="e9c30-150">Click the **File** menu item to open the menu.</span></span>  
  
3. <span data-ttu-id="e9c30-151">Sur le **fichier** menu, cliquez sur un des éléments pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="e9c30-151">On the **File** menu, click one of the items to select it.</span></span>  
  
     <span data-ttu-id="e9c30-152">Le <xref:System.Windows.Forms.StatusStrip> contrôle affiche l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e9c30-152">The <xref:System.Windows.Forms.StatusStrip> control displays the selected item.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="e9c30-153">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e9c30-153">Next Steps</span></span>  
 <span data-ttu-id="e9c30-154">Dans cette procédure pas à pas, vous avez créé un formulaire avec un menu standard.</span><span class="sxs-lookup"><span data-stu-id="e9c30-154">In this walkthrough, you have created a form with a standard menu.</span></span> <span data-ttu-id="e9c30-155">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :</span><span class="sxs-lookup"><span data-stu-id="e9c30-155">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>  
  
- <span data-ttu-id="e9c30-156">Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="e9c30-156">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="e9c30-157">Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="e9c30-157">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>  
  
- <span data-ttu-id="e9c30-158">Créer un formulaire d’interface (multidocument MDI) document avec l’ancrage <xref:System.Windows.Forms.ToolStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="e9c30-158">Create a multiple document interface (MDI) form with docking <xref:System.Windows.Forms.ToolStrip> controls.</span></span> <span data-ttu-id="e9c30-159">Pour plus d’informations, consultez [Procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e9c30-159">For more information, see [Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>  
  
- <span data-ttu-id="e9c30-160">Donnez à votre <xref:System.Windows.Forms.ToolStrip> contrôle un aspect professionnel.</span><span class="sxs-lookup"><span data-stu-id="e9c30-160">Give your <xref:System.Windows.Forms.ToolStrip> controls a professional appearance.</span></span> <span data-ttu-id="e9c30-161">Pour plus d'informations, voir [Procédure : Définir le convertisseur ToolStrip pour une Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="e9c30-161">For more information, see [How to: Set the ToolStrip Renderer for an Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9c30-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c30-162">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="e9c30-163">MenuStrip, contrôle</span><span class="sxs-lookup"><span data-stu-id="e9c30-163">MenuStrip Control</span></span>](menustrip-control-windows-forms.md)
