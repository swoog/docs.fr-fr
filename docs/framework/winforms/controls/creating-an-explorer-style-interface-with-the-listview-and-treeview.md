---
title: 'Procédure pas à pas : création d’une interface de style explorateur avec les contrôles ListView et TreeView à l’aide du concepteur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Explorer-style applications [Windows Forms], walkthroughs
- TreeView control [Windows Forms], ListView controls used with
- ListView control [Windows Forms], TreeView controls used with
- Explorer-style applications
- TreeView control [Windows Forms], using for explorer-style interface
- ListView control [Windows Forms], explorer style interface
- ListView control [Windows Forms], explorer-style interface
ms.assetid: 9e5e7721-19e2-4890-b273-a43589fe99ff
ms.openlocfilehash: c8f6e51b5ab8242ba8253a04160c40e59fce0088
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64648204"
---
# <a name="walkthrough-creating-an-explorer-style-interface-with-the-listview-and-treeview-controls-using-the-designer"></a><span data-ttu-id="15bb0-102">Procédure pas à pas : création d’une interface de style explorateur avec les contrôles ListView et TreeView à l’aide du concepteur</span><span class="sxs-lookup"><span data-stu-id="15bb0-102">Walkthrough: Creating an Explorer Style Interface with the ListView and TreeView Controls Using the Designer</span></span>
<span data-ttu-id="15bb0-103">Un des avantages de Visual Studio est la capacité de créer des applications Windows Forms de qualité professionnelle en un court laps de temps.</span><span class="sxs-lookup"><span data-stu-id="15bb0-103">One of the benefits of Visual Studio is the ability to create professional-looking Windows Forms applications in a short of amount of time.</span></span> <span data-ttu-id="15bb0-104">Un scénario courant est création d’une interface utilisateur (IU) avec <xref:System.Windows.Forms.ListView> et <xref:System.Windows.Forms.TreeView> contrôles qui ressemble à la fonctionnalité de l’Explorateur Windows des systèmes d’exploitation de Windows.</span><span class="sxs-lookup"><span data-stu-id="15bb0-104">A common scenario is creating a user interface (UI) with <xref:System.Windows.Forms.ListView> and <xref:System.Windows.Forms.TreeView> controls that resembles the Windows Explorer feature of Windows operating systems.</span></span> <span data-ttu-id="15bb0-105">L’Explorateur Windows affiche une structure hiérarchique des fichiers et dossiers sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15bb0-105">Windows Explorer displays a hierarchical structure of the files and folders on a user's computer.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="15bb0-106">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="15bb0-106">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="15bb0-107">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="15bb0-107">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="15bb0-108">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="15bb0-108">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-the-form-containing-a-listview-and-treeview-control"></a><span data-ttu-id="15bb0-109">Pour créer le formulaire contenant un contrôle ListView et TreeView</span><span class="sxs-lookup"><span data-stu-id="15bb0-109">To create the form containing a ListView and TreeView control</span></span>  
  
1. <span data-ttu-id="15bb0-110">Dans le menu **Fichier** , pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="15bb0-110">On the **File** menu, point to **New**, and then click **Project**.</span></span>  
  
2. <span data-ttu-id="15bb0-111">Dans le **nouveau projet** boîte de dialogue zone, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="15bb0-111">In the **New Project** dialog box, do the following:</span></span>  
  
    1. <span data-ttu-id="15bb0-112">Dans les catégories, choisissez **Visual Basic** ou **Visual C#**.</span><span class="sxs-lookup"><span data-stu-id="15bb0-112">In the categories, choose either **Visual Basic** or **Visual C#**.</span></span>  
  
    2. <span data-ttu-id="15bb0-113">Dans la liste des modèles, choisissez **Windows Forms Application**.</span><span class="sxs-lookup"><span data-stu-id="15bb0-113">In the list of templates, choose **Windows Forms Application**.</span></span>  
  
3. <span data-ttu-id="15bb0-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="15bb0-114">Click **OK**.</span></span> <span data-ttu-id="15bb0-115">Un nouveau projet Windows Forms est créé.</span><span class="sxs-lookup"><span data-stu-id="15bb0-115">A new Windows Forms project is created.</span></span>  
  
4. <span data-ttu-id="15bb0-116">Ajouter un <xref:System.Windows.Forms.SplitContainer> au formulaire et définissez son <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="15bb0-116">Add a <xref:System.Windows.Forms.SplitContainer> control to the form and set its <xref:System.Windows.Forms.SplitContainer.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>  
  
5. <span data-ttu-id="15bb0-117">Ajouter un <xref:System.Windows.Forms.ImageList> nommé `imageList1` au formulaire et utilisez la fenêtre Propriétés pour ajouter deux images : une image de dossier et une image de document, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="15bb0-117">Add an <xref:System.Windows.Forms.ImageList> named `imageList1` to the form and use the Properties window to add two images: a folder image and a document image, in that order.</span></span>  
  
6. <span data-ttu-id="15bb0-118">Ajouter un <xref:System.Windows.Forms.TreeView> contrôle nommé `treeview1` au formulaire et placez-le sur le côté gauche de la <xref:System.Windows.Forms.SplitContainer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="15bb0-118">Add a <xref:System.Windows.Forms.TreeView> control named `treeview1` to the form, and position it on the left side of the <xref:System.Windows.Forms.SplitContainer> control.</span></span> <span data-ttu-id="15bb0-119">Dans la fenêtre Propriétés pour `treeView1` procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="15bb0-119">In the Properties window for `treeView1` do the following:</span></span>  
  
    1. <span data-ttu-id="15bb0-120">Affectez à la propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="15bb0-120">Set the <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>  
  
    2. <span data-ttu-id="15bb0-121">Affectez à la propriété <xref:System.Windows.Forms.TreeView.ImageList%2A> la valeur `imagelist1.`</span><span class="sxs-lookup"><span data-stu-id="15bb0-121">Set the <xref:System.Windows.Forms.TreeView.ImageList%2A> property to `imagelist1.`</span></span>  
  
7. <span data-ttu-id="15bb0-122">Ajouter un <xref:System.Windows.Forms.ListView> contrôle nommé `listView1` au formulaire et le positionner sur le côté droit de la <xref:System.Windows.Forms.SplitContainer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="15bb0-122">Add a <xref:System.Windows.Forms.ListView> control named `listView1` to the form, and position it on the right side of the <xref:System.Windows.Forms.SplitContainer> control.</span></span> <span data-ttu-id="15bb0-123">Dans la fenêtre Propriétés pour `listview1` procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="15bb0-123">In the Properties window for `listview1` do the following:</span></span>  
  
    1. <span data-ttu-id="15bb0-124">Affectez à la propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="15bb0-124">Set the <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>  
  
    2. <span data-ttu-id="15bb0-125">Affectez à la propriété <xref:System.Windows.Forms.ListView.View%2A> la valeur <xref:System.Windows.Forms.View.Details>.</span><span class="sxs-lookup"><span data-stu-id="15bb0-125">Set the <xref:System.Windows.Forms.ListView.View%2A> property to <xref:System.Windows.Forms.View.Details>.</span></span>  
  
    3. <span data-ttu-id="15bb0-126">Ouvrez l’éditeur de collections ColumnHeader en cliquant sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) dans le <xref:System.Windows.Forms.ListView.Columns%2A> propriété **.**</span><span class="sxs-lookup"><span data-stu-id="15bb0-126">Open the ColumnHeader Collection Editor by clicking the ellipses (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) in the <xref:System.Windows.Forms.ListView.Columns%2A> property **.**</span></span> <span data-ttu-id="15bb0-127">Ajoutez trois colonnes et définissez leurs <xref:System.Windows.Forms.ColumnHeader.Text%2A> propriété `Name`, `Type`, et `Last Modified`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="15bb0-127">Add three columns and set their <xref:System.Windows.Forms.ColumnHeader.Text%2A> property to `Name`, `Type`, and `Last Modified`, respectively.</span></span> <span data-ttu-id="15bb0-128">Cliquez sur **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="15bb0-128">Click **OK** to close the dialog box.</span></span>  
  
    4. <span data-ttu-id="15bb0-129">Affectez à la propriété <xref:System.Windows.Forms.ListView.SmallImageList%2A> la valeur `imageList1.`</span><span class="sxs-lookup"><span data-stu-id="15bb0-129">Set the <xref:System.Windows.Forms.ListView.SmallImageList%2A> property to `imageList1.`</span></span>  
  
8. <span data-ttu-id="15bb0-130">Implémentez le code pour remplir la <xref:System.Windows.Forms.TreeView> avec les nœuds et les sous-nœuds.</span><span class="sxs-lookup"><span data-stu-id="15bb0-130">Implement the code to populate the <xref:System.Windows.Forms.TreeView> with nodes and subnodes.</span></span> <span data-ttu-id="15bb0-131">Ajoutez ce code à la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="15bb0-131">Add this code to the `Form1` class.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#1)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#1)]  
  
9. <span data-ttu-id="15bb0-132">Étant donné que le code précédent utilise l’espace de noms System.IO, ajoutez l’utilisation appropriée ou importer l’instruction en haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="15bb0-132">Since the previous code uses the System.IO namespace, add the appropriate using or import statement at the top of the form.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#4)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#4)]  
  
10. <span data-ttu-id="15bb0-133">Appelez la méthode de configuration de l’étape précédente dans le constructeur du formulaire ou <xref:System.Windows.Forms.Form.Load> méthode de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="15bb0-133">Call the set-up method from the previous step in the form's constructor or <xref:System.Windows.Forms.Form.Load> event-handling method.</span></span> <span data-ttu-id="15bb0-134">Ajoutez ce code au constructeur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="15bb0-134">Add this code to the form constructor.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#2)]  
  
11. <span data-ttu-id="15bb0-135">Gérer le <xref:System.Windows.Forms.TreeView.NodeMouseClick> événement pour `treeview1` **,** et implémentez le code pour remplir `listview1` avec le contenu d’un nœud lorsque l’utilisateur clique sur un nœud.</span><span class="sxs-lookup"><span data-stu-id="15bb0-135">Handle the <xref:System.Windows.Forms.TreeView.NodeMouseClick> event for `treeview1`**,** and implement the code to populate `listview1` with a node's contents when a node is clicked.</span></span> <span data-ttu-id="15bb0-136">Ajoutez ce code à la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="15bb0-136">Add this code to the `Form1` class.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ExplorerStyleInterface#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/VB/Form1.vb#3)]  
  
     <span data-ttu-id="15bb0-137">Si vous utilisez c#, assurez-vous d’avoir le <xref:System.Windows.Forms.TreeView.NodeMouseClick> événement associé à sa méthode de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="15bb0-137">If you are using C#, make sure you have the <xref:System.Windows.Forms.TreeView.NodeMouseClick> event associated with its event-handling method.</span></span> <span data-ttu-id="15bb0-138">Ajoutez ce code au constructeur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="15bb0-138">Add this code to the form constructor.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ExplorerStyleInterface#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ExplorerStyleInterface/CS/Form1.cs#5)]  
  
## <a name="testing-the-application"></a><span data-ttu-id="15bb0-139">Test de l'application</span><span class="sxs-lookup"><span data-stu-id="15bb0-139">Testing the Application</span></span>  
 <span data-ttu-id="15bb0-140">Vous pouvez maintenant tester le formulaire pour vous assurer qu’il se comporte comme prévu.</span><span class="sxs-lookup"><span data-stu-id="15bb0-140">You can now test the form to make sure it behaves as expected.</span></span>  
  
#### <a name="to-test-the-form"></a><span data-ttu-id="15bb0-141">Pour tester le formulaire</span><span class="sxs-lookup"><span data-stu-id="15bb0-141">To test the form</span></span>  
  
- <span data-ttu-id="15bb0-142">Appuyez sur F5 pour exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="15bb0-142">Press F5 to run the application.</span></span>  
  
     <span data-ttu-id="15bb0-143">Vous verrez un formulaire de fractionnement contenant un <xref:System.Windows.Forms.TreeView> contrôle qui affiche votre répertoire de projet sur le côté gauche, et un <xref:System.Windows.Forms.ListView> contrôle sur le côté droit avec trois colonnes.</span><span class="sxs-lookup"><span data-stu-id="15bb0-143">You will see a split form containing a <xref:System.Windows.Forms.TreeView> control that displays your project directory on the left side, and a <xref:System.Windows.Forms.ListView> control on the right side with three columns.</span></span> <span data-ttu-id="15bb0-144">Vous pouvez parcourir le <xref:System.Windows.Forms.TreeView> en sélectionnant des nœuds de répertoire et le <xref:System.Windows.Forms.ListView> est rempli avec le contenu du répertoire sélectionné.</span><span class="sxs-lookup"><span data-stu-id="15bb0-144">You can traverse the <xref:System.Windows.Forms.TreeView> by selecting directory nodes, and the <xref:System.Windows.Forms.ListView> is populated with the contents of the selected directory.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="15bb0-145">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="15bb0-145">Next Steps</span></span>  
 <span data-ttu-id="15bb0-146">Cette application vous donne un exemple de la façon dont vous pouvez utiliser <xref:System.Windows.Forms.TreeView> et <xref:System.Windows.Forms.ListView> ensemble les contrôles.</span><span class="sxs-lookup"><span data-stu-id="15bb0-146">This application gives you an example of a way you can use <xref:System.Windows.Forms.TreeView> and <xref:System.Windows.Forms.ListView> controls together.</span></span> <span data-ttu-id="15bb0-147">Pour plus d’informations sur ces contrôles, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="15bb0-147">For more information on these controls, see the following topics:</span></span>  
  
- [<span data-ttu-id="15bb0-148">Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="15bb0-148">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)  
  
- [<span data-ttu-id="15bb0-149">Guide pratique pour Ajouter des fonctionnalités de recherche à un contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="15bb0-149">How to: Add Search Capabilities to a ListView Control</span></span>](how-to-add-search-capabilities-to-a-listview-control.md)  
  
- [<span data-ttu-id="15bb0-150">Guide pratique pour Attacher un Menu contextuel à un nœud TreeView</span><span class="sxs-lookup"><span data-stu-id="15bb0-150">How to: Attach a ShortCut Menu to a TreeView Node</span></span>](how-to-attach-a-shortcut-menu-to-a-treeview-node.md)  
  
## <a name="see-also"></a><span data-ttu-id="15bb0-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15bb0-151">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.TreeView>
- [<span data-ttu-id="15bb0-152">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="15bb0-152">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="15bb0-153">Guide pratique pour Ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="15bb0-153">How to: Add and Remove Nodes with the Windows Forms TreeView Control</span></span>](how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control.md)
- [<span data-ttu-id="15bb0-154">Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="15bb0-154">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [<span data-ttu-id="15bb0-155">Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="15bb0-155">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)
