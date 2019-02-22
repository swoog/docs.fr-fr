---
title: 'Procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip'
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
ms.openlocfilehash: f4e6bc0faf0dc088d919ee929a7bf320d6e169c4
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56664950"
---
# <a name="walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a><span data-ttu-id="4c659-102">Procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip</span><span class="sxs-lookup"><span data-stu-id="4c659-102">Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls</span></span>
<span data-ttu-id="4c659-103">L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> prend en charge plusieurs applications MDI (Multiple Document Interface) et le contrôle <xref:System.Windows.Forms.MenuStrip> prend en charge la fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="4c659-103">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace supports multiple document interface (MDI) applications, and the <xref:System.Windows.Forms.MenuStrip> control supports menu merging.</span></span> <span data-ttu-id="4c659-104">Les formulaires MDI peuvent également contenir des contrôles <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="4c659-104">MDI forms can also <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="4c659-105">Cette procédure pas à pas montre comment utiliser <xref:System.Windows.Forms.ToolStripPanel> contrôles avec un formulaire MDI.</span><span class="sxs-lookup"><span data-stu-id="4c659-105">This walkthrough demonstrates how to use <xref:System.Windows.Forms.ToolStripPanel> controls with an MDI form.</span></span> <span data-ttu-id="4c659-106">Le formulaire prend également en charge la fusion de menus avec les menus enfants.</span><span class="sxs-lookup"><span data-stu-id="4c659-106">The form also supports menu merging with child menus.</span></span> <span data-ttu-id="4c659-107">Les tâches suivantes sont illustrées dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="4c659-107">The following tasks are illustrated in this walkthrough:</span></span>  
  
-   <span data-ttu-id="4c659-108">Création d’un projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="4c659-108">Creating a Windows Forms project.</span></span>  
  
-   <span data-ttu-id="4c659-109">Création du menu principal pour votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-109">Creating the main menu for your form.</span></span> <span data-ttu-id="4c659-110">Le nom réel du menu varient.</span><span class="sxs-lookup"><span data-stu-id="4c659-110">The actual name of the menu will vary.</span></span>  
  
-   <span data-ttu-id="4c659-111">Ajout de la <xref:System.Windows.Forms.ToolStripPanel> le contrôle à la **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="4c659-111">Adding the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox**.</span></span>  
  
-   <span data-ttu-id="4c659-112">Création d’un formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="4c659-112">Creating a child form.</span></span>  
  
-   <span data-ttu-id="4c659-113">Réorganisation <xref:System.Windows.Forms.ToolStripPanel> par ordre de plan des contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-113">Arranging <xref:System.Windows.Forms.ToolStripPanel> controls by z-order.</span></span>  
  
 <span data-ttu-id="4c659-114">Lorsque vous avez terminé, avoir un formulaire MDI qui prend en charge la fusion de menus et movable <xref:System.Windows.Forms.ToolStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-114">When you are finished, you will have an MDI form that supports menu merging and movable <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="4c659-115">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Créer un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](../../../../docs/framework/winforms/controls/how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4c659-115">To copy the code in this topic as a single listing, see [How to: Create an MDI Form with Menu Merging and ToolStrip Controls](../../../../docs/framework/winforms/controls/how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4c659-116">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="4c659-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="4c659-117">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="4c659-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="4c659-118">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="4c659-118">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="4c659-119">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4c659-119">Prerequisites</span></span>  
 <span data-ttu-id="4c659-120">Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4c659-120">In order to complete this walkthrough, you will need:</span></span>  
  
-   <span data-ttu-id="4c659-121">Autorisations suffisantes pour pouvoir créer et exécuter des projets d’application Windows Forms sur l’ordinateur où Visual Studio est installé.</span><span class="sxs-lookup"><span data-stu-id="4c659-121">Sufficient permissions to be able to create and run Windows Forms application projects on the computer where Visual Studio is installed.</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="4c659-122">Création du projet</span><span class="sxs-lookup"><span data-stu-id="4c659-122">Creating the Project</span></span>  
 <span data-ttu-id="4c659-123">La première étape consiste à créer le projet et à configurer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-123">The first step is to create the project and set up the form.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="4c659-124">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="4c659-124">To create the project</span></span>  
  
1.  <span data-ttu-id="4c659-125">Créez un projet Windows Application appelé **MdiForm** (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="4c659-125">Create a Windows Application project called **MdiForm** (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2.  <span data-ttu-id="4c659-126">Dans le Concepteur Windows Forms, sélectionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-126">In the Windows Forms Designer, select the form.</span></span>  
  
3.  <span data-ttu-id="4c659-127">Dans la fenêtre Propriétés, définissez la valeur de la <xref:System.Windows.Forms.Form.IsMdiContainer%2A> à `true`.</span><span class="sxs-lookup"><span data-stu-id="4c659-127">In the Properties window, set the value of the <xref:System.Windows.Forms.Form.IsMdiContainer%2A> to `true`.</span></span>  
  
## <a name="creating-the-main-menu"></a><span data-ttu-id="4c659-128">Création du Menu principal</span><span class="sxs-lookup"><span data-stu-id="4c659-128">Creating the Main Menu</span></span>  
 <span data-ttu-id="4c659-129">Le formulaire MDI parent contient le menu principal.</span><span class="sxs-lookup"><span data-stu-id="4c659-129">The parent MDI form contains the main menu.</span></span> <span data-ttu-id="4c659-130">Le menu principal possède un élément de menu nommé **fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="4c659-130">The main menu has one menu item named **Window**.</span></span> <span data-ttu-id="4c659-131">Avec le **fenêtre** élément de menu, vous pouvez créer des formulaires enfants.</span><span class="sxs-lookup"><span data-stu-id="4c659-131">With the **Window** menu item, you can create child forms.</span></span> <span data-ttu-id="4c659-132">Éléments de menu à partir de formulaires enfants sont fusionnés dans le menu principal.</span><span class="sxs-lookup"><span data-stu-id="4c659-132">Menu items from child forms are merged into the main menu.</span></span>  
  
#### <a name="to-create-the-main-menu"></a><span data-ttu-id="4c659-133">Pour créer le menu principal</span><span class="sxs-lookup"><span data-stu-id="4c659-133">To create the Main menu</span></span>  
  
1.  <span data-ttu-id="4c659-134">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-134">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the form.</span></span>  
  
2.  <span data-ttu-id="4c659-135">Ajouter un <xref:System.Windows.Forms.ToolStripMenuItem> à la <xref:System.Windows.Forms.MenuStrip> contrôler et nommez-le **fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="4c659-135">Add a <xref:System.Windows.Forms.ToolStripMenuItem> to the <xref:System.Windows.Forms.MenuStrip> control and name it **Window**.</span></span>  
  
3.  <span data-ttu-id="4c659-136">Sélectionnez le contrôle <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="4c659-136">Select the <xref:System.Windows.Forms.MenuStrip> control.</span></span>  
  
4.  <span data-ttu-id="4c659-137">Dans la fenêtre Propriétés, définissez la valeur de la <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> propriété `ToolStripMenuItem1`.</span><span class="sxs-lookup"><span data-stu-id="4c659-137">In the Properties window, set the value of the <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property to `ToolStripMenuItem1`.</span></span>  
  
5.  <span data-ttu-id="4c659-138">Ajouter un sous-élément à la **fenêtre** élément de menu, puis nommez le sous-élément **New**.</span><span class="sxs-lookup"><span data-stu-id="4c659-138">Add a subitem to the **Window** menu item, and then name the subitem **New**.</span></span>  
  
6.  <span data-ttu-id="4c659-139">Dans la fenêtre Propriétés, cliquez sur **événements**.</span><span class="sxs-lookup"><span data-stu-id="4c659-139">In the Properties window, click **Events**.</span></span>  
  
7.  <span data-ttu-id="4c659-140">Double-cliquez sur le <xref:System.Windows.Forms.ToolStripItem.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="4c659-140">Double-click the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>  
  
     <span data-ttu-id="4c659-141">Le Concepteur de formulaires Windows génère un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événement.</span><span class="sxs-lookup"><span data-stu-id="4c659-141">The Windows Forms Designer generates an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>  
  
8.  <span data-ttu-id="4c659-142">Insérez le code suivant dans le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="4c659-142">Insert the following code into the event handler.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#2)]  
  
## <a name="adding-the-toolstrippanel-control-to-the-toolbox"></a><span data-ttu-id="4c659-143">Ajout du contrôle ToolStripPanel à la boîte à outils</span><span class="sxs-lookup"><span data-stu-id="4c659-143">Adding the ToolStripPanel Control to the Toolbox</span></span>  
 <span data-ttu-id="4c659-144">Lorsque vous utilisez <xref:System.Windows.Forms.MenuStrip> contrôles avec un formulaire MDI doit avoir le <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c659-144">When you use <xref:System.Windows.Forms.MenuStrip> controls with an MDI form you must have the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="4c659-145">Vous devez ajouter le <xref:System.Windows.Forms.ToolStripPanel> le contrôle à la **boîte à outils** pour générer votre formulaire MDI dans le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="4c659-145">You must add the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox** to build your MDI form in the Windows Forms Designer.</span></span>  
  
#### <a name="to-add-the-toolstrippanel-control-to-the-toolbox"></a><span data-ttu-id="4c659-146">Pour ajouter le contrôle ToolStripPanel à la boîte à outils</span><span class="sxs-lookup"><span data-stu-id="4c659-146">To add the ToolStripPanel control to the Toolbox</span></span>  
  
1.  <span data-ttu-id="4c659-147">Ouvrez le **boîte à outils**, puis cliquez sur le **tous les Windows Forms** onglet pour afficher les contrôles Windows Forms disponibles.</span><span class="sxs-lookup"><span data-stu-id="4c659-147">Open the **Toolbox**, and then click the **All Windows Forms** tab to show the available Windows Forms controls.</span></span>  
  
2.  <span data-ttu-id="4c659-148">Avec le bouton droit pour ouvrir le menu contextuel, puis sélectionnez **choisir des éléments de**.</span><span class="sxs-lookup"><span data-stu-id="4c659-148">Right-click to open the shortcut menu, and select **Choose Items**.</span></span>  
  
3.  <span data-ttu-id="4c659-149">Dans le **Choose Toolbox Items** boîte de dialogue, faites défiler vers le bas le **nom** colonne jusqu'à ce que vous trouviez **ToolStripPanel**.</span><span class="sxs-lookup"><span data-stu-id="4c659-149">In the **Choose Toolbox Items** dialog box, scroll down the **Name** column until you find **ToolStripPanel**.</span></span>  
  
4.  <span data-ttu-id="4c659-150">Sélectionnez la case à cocher par **ToolStripPanel**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c659-150">Select the check box by **ToolStripPanel**, and then click **OK**.</span></span>  
  
     <span data-ttu-id="4c659-151">Le <xref:System.Windows.Forms.ToolStripPanel> contrôle s’affiche dans le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="4c659-151">The <xref:System.Windows.Forms.ToolStripPanel> control appears in the **Toolbox**.</span></span>  
  
## <a name="creating-a-child-form"></a><span data-ttu-id="4c659-152">Création d’un formulaire enfant</span><span class="sxs-lookup"><span data-stu-id="4c659-152">Creating a Child Form</span></span>  
 <span data-ttu-id="4c659-153">Dans cette procédure, vous allez définir une classe de formulaire enfant distincte qui possède son propre <xref:System.Windows.Forms.MenuStrip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c659-153">In this procedure, you will define a separate child form class that has its own <xref:System.Windows.Forms.MenuStrip> control.</span></span> <span data-ttu-id="4c659-154">Les éléments de menu pour ce formulaire sont fusionnés avec ceux du formulaire parent.</span><span class="sxs-lookup"><span data-stu-id="4c659-154">The menu items for this form are merged with those of the parent form.</span></span>  
  
#### <a name="to-define-a-child-form"></a><span data-ttu-id="4c659-155">Pour définir un formulaire enfant</span><span class="sxs-lookup"><span data-stu-id="4c659-155">To define a child form</span></span>  
  
1.  <span data-ttu-id="4c659-156">Ajoutez un nouveau formulaire nommé `ChildForm` au projet.</span><span class="sxs-lookup"><span data-stu-id="4c659-156">Add a new form named `ChildForm` to the project.</span></span>  
  
     <span data-ttu-id="4c659-157">Pour plus d'informations, voir [Procédure : Ajouter des Windows Forms à un projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4c659-157">For more information, see [How to: Add Windows Forms to a Project](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span></span>  
  
2.  <span data-ttu-id="4c659-158">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers le formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="4c659-158">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the child form.</span></span>  
  
3.  <span data-ttu-id="4c659-159">Cliquez sur le <xref:System.Windows.Forms.MenuStrip> glyphe de balise active du contrôle (![glyphe de balise active](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")), puis sélectionnez **modifier les éléments**.</span><span class="sxs-lookup"><span data-stu-id="4c659-159">Click the <xref:System.Windows.Forms.MenuStrip> control's smart tag glyph (![Smart Tag Glyph](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")), and then select **Edit Items**.</span></span>  
  
4.  <span data-ttu-id="4c659-160">Dans le **éditeur de collections Items** boîte de dialogue zone, ajoutez une nouvelle <xref:System.Windows.Forms.ToolStripMenuItem> nommé **ChildMenuItem** au menu enfant.</span><span class="sxs-lookup"><span data-stu-id="4c659-160">In the **Items Collection Editor** dialog box, add a new <xref:System.Windows.Forms.ToolStripMenuItem> named **ChildMenuItem** to the child menu.</span></span>  
  
     <span data-ttu-id="4c659-161">Pour plus d’informations, consultez [éditeur de collections d’éléments ToolStrip](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4c659-161">For more information, see [ToolStrip Items Collection Editor](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100)).</span></span>  
  
## <a name="testing-the-form"></a><span data-ttu-id="4c659-162">Test du formulaire</span><span class="sxs-lookup"><span data-stu-id="4c659-162">Testing the Form</span></span>  
  
#### <a name="to-test-your-form"></a><span data-ttu-id="4c659-163">Pour tester votre formulaire</span><span class="sxs-lookup"><span data-stu-id="4c659-163">To test your form</span></span>  
  
1.  <span data-ttu-id="4c659-164">Appuyez sur F5 pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-164">Press F5 to compile and run your form.</span></span>  
  
2.  <span data-ttu-id="4c659-165">Cliquez sur le **fenêtre** élément de menu pour ouvrir le menu, puis cliquez sur **New**.</span><span class="sxs-lookup"><span data-stu-id="4c659-165">Click the **Window** menu item to open the menu, and then click **New**.</span></span>  
  
     <span data-ttu-id="4c659-166">Un nouveau formulaire enfant est créé dans la zone du formulaire MDI client.</span><span class="sxs-lookup"><span data-stu-id="4c659-166">A new child form is created in the form's MDI client area.</span></span> <span data-ttu-id="4c659-167">Les menus du formulaire enfant sont fusionné avec le menu principal.</span><span class="sxs-lookup"><span data-stu-id="4c659-167">The child form's menu is merged with the main menu.</span></span>  
  
3.  <span data-ttu-id="4c659-168">Fermez le formulaire enfant.</span><span class="sxs-lookup"><span data-stu-id="4c659-168">Close the child form.</span></span>  
  
     <span data-ttu-id="4c659-169">Les menus du formulaire enfant sont supprimé dans le menu principal.</span><span class="sxs-lookup"><span data-stu-id="4c659-169">The child form's menu is removed from the main menu.</span></span>  
  
4.  <span data-ttu-id="4c659-170">Cliquez sur **New** plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="4c659-170">Click **New** several times.</span></span>  
  
     <span data-ttu-id="4c659-171">Les formulaires enfants sont automatiquement répertoriés sous la **fenêtre** élément de menu, car le <xref:System.Windows.Forms.MenuStrip> du contrôle <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> propriété est affectée.</span><span class="sxs-lookup"><span data-stu-id="4c659-171">The child forms are automatically listed under the **Window** menu item because the <xref:System.Windows.Forms.MenuStrip> control's <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property is assigned.</span></span>  
  
## <a name="adding-toolstrip-support"></a><span data-ttu-id="4c659-172">Ajout de prise en charge de ToolStrip</span><span class="sxs-lookup"><span data-stu-id="4c659-172">Adding ToolStrip Support</span></span>  
 <span data-ttu-id="4c659-173">Dans cette procédure, vous allez ajouter quatre <xref:System.Windows.Forms.ToolStrip> contrôles au formulaire parent MDI.</span><span class="sxs-lookup"><span data-stu-id="4c659-173">In this procedure, you will add four <xref:System.Windows.Forms.ToolStrip> controls to the MDI parent form.</span></span> <span data-ttu-id="4c659-174">Chaque <xref:System.Windows.Forms.ToolStrip> contrôle est ajouté à l’intérieur d’un <xref:System.Windows.Forms.ToolStripPanel> contrôle, qui est ancré au bord du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-174">Each <xref:System.Windows.Forms.ToolStrip> control is added inside a <xref:System.Windows.Forms.ToolStripPanel> control, which is docked to the edge of the form.</span></span>  
  
#### <a name="to-add-toolstrip-controls-to-the-mdi-parent-form"></a><span data-ttu-id="4c659-175">Pour ajouter des contrôles ToolStrip au formulaire parent MDI</span><span class="sxs-lookup"><span data-stu-id="4c659-175">To add ToolStrip controls to the MDI parent form</span></span>  
  
1.  <span data-ttu-id="4c659-176">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.ToolStripPanel> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-176">From the **Toolbox**, drag a <xref:System.Windows.Forms.ToolStripPanel> control onto the form.</span></span>  
  
2.  <span data-ttu-id="4c659-177">Avec le <xref:System.Windows.Forms.ToolStripPanel> contrôle sélectionné, double-cliquez sur le <xref:System.Windows.Forms.ToolStrip> dans contrôler le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="4c659-177">With the <xref:System.Windows.Forms.ToolStripPanel> control selected, double-click the <xref:System.Windows.Forms.ToolStrip> control in the **Toolbox**.</span></span>  
  
     <span data-ttu-id="4c659-178">Un <xref:System.Windows.Forms.ToolStrip> contrôle est créé dans le <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c659-178">A <xref:System.Windows.Forms.ToolStrip> control is created in the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>  
  
3.  <span data-ttu-id="4c659-179">Sélectionnez le contrôle <xref:System.Windows.Forms.ToolStripPanel>.</span><span class="sxs-lookup"><span data-stu-id="4c659-179">Select the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>  
  
4.  <span data-ttu-id="4c659-180">Dans la fenêtre Propriétés, modifiez la valeur du contrôle <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Left>.</span><span class="sxs-lookup"><span data-stu-id="4c659-180">In the Properties window, change the value of the control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Left>.</span></span>  
  
     <span data-ttu-id="4c659-181">Le <xref:System.Windows.Forms.ToolStripPanel> contrôler s’ancre sur le côté gauche du formulaire, sous le menu principal.</span><span class="sxs-lookup"><span data-stu-id="4c659-181">The <xref:System.Windows.Forms.ToolStripPanel> control docks to the left side of the form, underneath the main menu.</span></span> <span data-ttu-id="4c659-182">La zone cliente MDI est redimensionné pour s’ajuster à la <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c659-182">The MDI client area resizes to fit the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>  
  
5.  <span data-ttu-id="4c659-183">Répétez les étapes 1 à 4.</span><span class="sxs-lookup"><span data-stu-id="4c659-183">Repeat steps 1 through 4.</span></span>  
  
     <span data-ttu-id="4c659-184">Ancrer la nouvelle <xref:System.Windows.Forms.ToolStripPanel> contrôle vers le haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-184">Dock the new <xref:System.Windows.Forms.ToolStripPanel> control to the top of the form.</span></span>  
  
     <span data-ttu-id="4c659-185">Le <xref:System.Windows.Forms.ToolStripPanel> contrôle est ancré sous le menu principal, mais à droite de la première <xref:System.Windows.Forms.ToolStripPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c659-185">The <xref:System.Windows.Forms.ToolStripPanel> control is docked underneath the main menu, but to the right of the first <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="4c659-186">Cette étape illustre l’importance de l’ordre de plan positionner correctement <xref:System.Windows.Forms.ToolStripPanel> contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-186">This step illustrates the importance of z-order in correctly positioning <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>  
  
6.  <span data-ttu-id="4c659-187">Répétez les étapes 1 à 4 pour deux autres <xref:System.Windows.Forms.ToolStripPanel> contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-187">Repeat steps 1 through 4 for two more <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>  
  
     <span data-ttu-id="4c659-188">Ancrer la nouvelle <xref:System.Windows.Forms.ToolStripPanel> contrôles vers la droite et le bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-188">Dock the new <xref:System.Windows.Forms.ToolStripPanel> controls to the right and bottom of the form.</span></span>  
  
## <a name="arranging-toolstrippanel-controls-by-z-order"></a><span data-ttu-id="4c659-189">Organisation des contrôles ToolStripPanel par ordre de plan</span><span class="sxs-lookup"><span data-stu-id="4c659-189">Arranging ToolStripPanel Controls by Z-order</span></span>  
 <span data-ttu-id="4c659-190">La position d’une fenêtre fixe <xref:System.Windows.Forms.ToolStripPanel> contrôle sur votre formulaire MDI est déterminée par la position du contrôle dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="4c659-190">The position of a docked <xref:System.Windows.Forms.ToolStripPanel> control on your MDI form is determined by the control's position in the z-order.</span></span> <span data-ttu-id="4c659-191">Vous pouvez facilement réorganiser l’ordre de plan de vos contrôles dans la fenêtre Structure du Document.</span><span class="sxs-lookup"><span data-stu-id="4c659-191">You can easily arrange the z-order of your controls in the Document Outline window.</span></span>  
  
#### <a name="to-arrange-toolstrippanel-controls-by-z-order"></a><span data-ttu-id="4c659-192">Pour réorganiser des contrôles ToolStripPanel suivant l’ordre de plan</span><span class="sxs-lookup"><span data-stu-id="4c659-192">To arrange ToolStripPanel controls by Z-order</span></span>  
  
1.  <span data-ttu-id="4c659-193">Dans le **vue** menu, cliquez sur **Windows autres**, puis cliquez sur **structure du Document**.</span><span class="sxs-lookup"><span data-stu-id="4c659-193">In the **View** menu, click **Other Windows**, and then click **Document Outline**.</span></span>  
  
     <span data-ttu-id="4c659-194">La disposition de votre <xref:System.Windows.Forms.ToolStripPanel> contrôles à partir de la procédure précédente n’est pas standard.</span><span class="sxs-lookup"><span data-stu-id="4c659-194">The arrangement of your <xref:System.Windows.Forms.ToolStripPanel> controls from the previous procedure is nonstandard.</span></span> <span data-ttu-id="4c659-195">Il s’agit, car l’ordre de plan n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="4c659-195">This is because the z-order is not correct.</span></span> <span data-ttu-id="4c659-196">Utilisez la fenêtre Structure du Document pour modifier l’ordre de plan des contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-196">Use the Document Outline window to change the z-order of the controls.</span></span>  
  
2.  <span data-ttu-id="4c659-197">Dans la fenêtre Structure du Document, sélectionnez **ToolStripPanel4**.</span><span class="sxs-lookup"><span data-stu-id="4c659-197">In the Document Outline window, select **ToolStripPanel4**.</span></span>  
  
3.  <span data-ttu-id="4c659-198">Cliquez sur le bouton de flèche vers le bas à plusieurs reprises, jusqu'à ce que **ToolStripPanel4** figure au bas de la liste.</span><span class="sxs-lookup"><span data-stu-id="4c659-198">Click the down-arrow button repeatedly, until **ToolStripPanel4** is at the bottom of the list.</span></span>  
  
     <span data-ttu-id="4c659-199">Le **ToolStripPanel4** contrôle est ancré en bas du formulaire, sous les autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-199">The **ToolStripPanel4** control is docked to the bottom of the form, underneath the other controls.</span></span>  
  
4.  <span data-ttu-id="4c659-200">Sélectionnez **ToolStripPanel2**.</span><span class="sxs-lookup"><span data-stu-id="4c659-200">Select **ToolStripPanel2**.</span></span>  
  
5.  <span data-ttu-id="4c659-201">Cliquez sur le bouton de flèche vers le bas une fois pour positionner le troisième contrôle dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4c659-201">Click the down-arrow button one time to position the control third in the list.</span></span>  
  
     <span data-ttu-id="4c659-202">Le **ToolStripPanel2** contrôle est ancré en haut du formulaire, sous le menu principal et au-dessus des autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c659-202">The **ToolStripPanel2** control is docked to the top of the form, underneath the main menu and above the other controls.</span></span>  
  
6.  <span data-ttu-id="4c659-203">Sélectionnez différents contrôles dans le **structure du Document** fenêtre et de les déplacer à différents endroits dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="4c659-203">Select various controls in the **Document Outline** window and move them to different positions in the z-order.</span></span> <span data-ttu-id="4c659-204">Notez l’effet de l’ordre de plan sur la position des contrôles ancrés.</span><span class="sxs-lookup"><span data-stu-id="4c659-204">Note the effect of the z-order on the placement of docked controls.</span></span> <span data-ttu-id="4c659-205">Utilisez CTRL + Z ou **Annuler** sur le **modifier** menu Annuler vos modifications.</span><span class="sxs-lookup"><span data-stu-id="4c659-205">Use CTRL-Z or **Undo** on the **Edit** menu to undo your changes.</span></span>  
  
## <a name="checkpoint"></a><span data-ttu-id="4c659-206">Point de contrôle</span><span class="sxs-lookup"><span data-stu-id="4c659-206">Checkpoint</span></span>  
  
#### <a name="to-test-your-form"></a><span data-ttu-id="4c659-207">Pour tester votre formulaire</span><span class="sxs-lookup"><span data-stu-id="4c659-207">To test your form</span></span>  
  
1.  <span data-ttu-id="4c659-208">Appuyez sur F5 pour compiler et exécuter votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-208">Press F5 to compile and run your form.</span></span>  
  
2.  <span data-ttu-id="4c659-209">Cliquez sur la poignée d’un <xref:System.Windows.Forms.ToolStrip> contrôler et faites glisser le contrôle à des positions différentes dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4c659-209">Click the grip of a <xref:System.Windows.Forms.ToolStrip> control and drag the control to different positions on the form.</span></span>  
  
     <span data-ttu-id="4c659-210">Vous pouvez faire glisser un <xref:System.Windows.Forms.ToolStrip> contrôle à partir d’un <xref:System.Windows.Forms.ToolStripPanel> contrôle vers un autre.</span><span class="sxs-lookup"><span data-stu-id="4c659-210">You can drag a <xref:System.Windows.Forms.ToolStrip> control from one <xref:System.Windows.Forms.ToolStripPanel> control to another.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="4c659-211">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4c659-211">Next Steps</span></span>  
 <span data-ttu-id="4c659-212">Dans cette procédure pas à pas, vous avez créé un formulaire MDI parent avec <xref:System.Windows.Forms.ToolStrip> de contrôles et de fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="4c659-212">In this walkthrough, you have created an MDI parent form with <xref:System.Windows.Forms.ToolStrip> controls and menu merging.</span></span> <span data-ttu-id="4c659-213">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :</span><span class="sxs-lookup"><span data-stu-id="4c659-213">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>  
  
-   <span data-ttu-id="4c659-214">Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="4c659-214">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="4c659-215">Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](../../../../docs/framework/winforms/controls/contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="4c659-215">For more information, see [ContextMenu Component Overview](../../../../docs/framework/winforms/controls/contextmenu-component-overview-windows-forms.md).</span></span>  
  
-   <span data-ttu-id="4c659-216">Créé un formulaire avec un menu standard automatiquement rempli.</span><span class="sxs-lookup"><span data-stu-id="4c659-216">Created a form with an automatically populated standard menu.</span></span> <span data-ttu-id="4c659-217">Pour plus d’informations, consultez [Procédure pas à pas : En fournissant des éléments de Menu Standard à un formulaire](../../../../docs/framework/winforms/controls/walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="4c659-217">For more information, see [Walkthrough: Providing Standard Menu Items to a Form](../../../../docs/framework/winforms/controls/walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>  
  
-   <span data-ttu-id="4c659-218">Donnez à votre <xref:System.Windows.Forms.ToolStrip> contrôle un aspect professionnel.</span><span class="sxs-lookup"><span data-stu-id="4c659-218">Give your <xref:System.Windows.Forms.ToolStrip> controls a professional appearance.</span></span> <span data-ttu-id="4c659-219">Pour plus d'informations, voir [Procédure : Définir le convertisseur ToolStrip pour une Application](../../../../docs/framework/winforms/controls/how-to-set-the-toolstrip-renderer-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="4c659-219">For more information, see [How to: Set the ToolStrip Renderer for an Application](../../../../docs/framework/winforms/controls/how-to-set-the-toolstrip-renderer-for-an-application.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c659-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c659-220">See also</span></span>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="4c659-221">Guide pratique pour Créer des formulaires MDI parents</span><span class="sxs-lookup"><span data-stu-id="4c659-221">How to: Create MDI Parent Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="4c659-222">Guide pratique pour Créer des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="4c659-222">How to: Create MDI Child Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="4c659-223">Guide pratique pour Insérer un MenuStrip dans un Menu du menu déroulant MDI</span><span class="sxs-lookup"><span data-stu-id="4c659-223">How to: Insert a MenuStrip into an MDI Drop-Down Menu</span></span>](../../../../docs/framework/winforms/controls/how-to-insert-a-menustrip-into-an-mdi-drop-down-menu-windows-forms.md)
- [<span data-ttu-id="4c659-224">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="4c659-224">ToolStrip Control</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
