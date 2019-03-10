---
title: 'Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés'
ms.date: 03/30/2017
helpviewer_keywords:
- IToolboxService interface
- Toolbox [Windows Forms], populating
- custom components [Windows Forms], adding to Toolbox
ms.assetid: 2fa1e3e8-6b9f-42b2-97c0-2be57444dba4
ms.openlocfilehash: 8ddb248d2e011714ddc7fb68474f0e92e9ad8b5e
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57723970"
---
# <a name="walkthrough-automatically-populating-the-toolbox-with-custom-components"></a><span data-ttu-id="60a86-102">Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="60a86-102">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>
<span data-ttu-id="60a86-103">Si vos composants sont définis par un projet dans la solution actuellement ouverte, ils apparaissent automatiquement dans le **boîte à outils**, sans qu’aucune action requise par vous.</span><span class="sxs-lookup"><span data-stu-id="60a86-103">If your components are defined by a project in the currently open solution, they will automatically appear in the **Toolbox**, with no action required by you.</span></span> <span data-ttu-id="60a86-104">Vous pouvez également remplir manuellement la **boîte à outils** avec vos composants personnalisés à l’aide de la [boîte à outils éléments de boîte de dialogue Choisir (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100)), mais la **boîte à outils** tient compte d’éléments dans de votre solution générer les sorties avec toutes les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="60a86-104">You can also manually populate the **Toolbox** with your custom components by using the [Choose Toolbox Items Dialog Box (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100)), but the **Toolbox** takes account of items in your solution's build outputs with all the following characteristics:</span></span>  
  
-   <span data-ttu-id="60a86-105">Implémente <xref:System.ComponentModel.IComponent>;</span><span class="sxs-lookup"><span data-stu-id="60a86-105">Implements <xref:System.ComponentModel.IComponent>;</span></span>  
  
-   <span data-ttu-id="60a86-106">N’a pas <xref:System.ComponentModel.ToolboxItemAttribute> définie sur `false`;</span><span class="sxs-lookup"><span data-stu-id="60a86-106">Does not have <xref:System.ComponentModel.ToolboxItemAttribute> set to `false`;</span></span>  
  
-   <span data-ttu-id="60a86-107">N’a pas <xref:System.ComponentModel.DesignTimeVisibleAttribute> défini sur `false`.</span><span class="sxs-lookup"><span data-stu-id="60a86-107">Does not have <xref:System.ComponentModel.DesignTimeVisibleAttribute> set to `false`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="60a86-108">Le **boîte à outils** ne suit pas les chaînes de référence, il n’affichera pas les éléments qui ne sont pas générés par un projet dans votre solution.</span><span class="sxs-lookup"><span data-stu-id="60a86-108">The **Toolbox** does not follow reference chains, so it will not display items that are not built by a project in your solution.</span></span>  
  
 <span data-ttu-id="60a86-109">Cette procédure pas à pas montre comment un composant personnalisé apparaît automatiquement dans le **boîte à outils** une fois que le composant est généré.</span><span class="sxs-lookup"><span data-stu-id="60a86-109">This walkthrough demonstrates how a custom component automatically appears in the **Toolbox** once the component is built.</span></span> <span data-ttu-id="60a86-110">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="60a86-110">Tasks illustrated in this walkthrough include:</span></span>  
  
-   <span data-ttu-id="60a86-111">Création d’un projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="60a86-111">Creating a Windows Forms project.</span></span>  
  
-   <span data-ttu-id="60a86-112">Création d’un composant personnalisé.</span><span class="sxs-lookup"><span data-stu-id="60a86-112">Creating a custom component.</span></span>  
  
-   <span data-ttu-id="60a86-113">Création d’une instance d’un composant personnalisé.</span><span class="sxs-lookup"><span data-stu-id="60a86-113">Creating an instance of a custom component.</span></span>  
  
-   <span data-ttu-id="60a86-114">Déchargement et rechargement d’un composant personnalisé.</span><span class="sxs-lookup"><span data-stu-id="60a86-114">Unloading and reloading a custom component.</span></span>  
  
 <span data-ttu-id="60a86-115">Lorsque vous avez terminé, vous verrez que le **boîte à outils** est remplie avec un composant que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="60a86-115">When you are finished, you will see that the **Toolbox** is populated with a component that you have created.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="60a86-116">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="60a86-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="60a86-117">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="60a86-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="60a86-118">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="60a86-118">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="60a86-119">Création du projet</span><span class="sxs-lookup"><span data-stu-id="60a86-119">Creating the Project</span></span>  
 <span data-ttu-id="60a86-120">La première étape consiste à créer le projet et à configurer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="60a86-120">The first step is to create the project and to set up the form.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="60a86-121">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="60a86-121">To create the project</span></span>  
  
1.  <span data-ttu-id="60a86-122">Créer un projet d’application Windows appelé `ToolboxExample` (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="60a86-122">Create a Windows-based application project called `ToolboxExample` (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2.  <span data-ttu-id="60a86-123">Ajouter un nouveau composant au projet.</span><span class="sxs-lookup"><span data-stu-id="60a86-123">Add a new component to the project.</span></span> <span data-ttu-id="60a86-124">Appelez-le `DemoComponent`.</span><span class="sxs-lookup"><span data-stu-id="60a86-124">Call it `DemoComponent`.</span></span>  
  
     <span data-ttu-id="60a86-125">Pour plus d'informations, voir [Procédure : Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="60a86-125">For more information, see [How to: Add New Project Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span></span>  
  
3.  <span data-ttu-id="60a86-126">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="60a86-126">Build the project.</span></span>  
  
4.  <span data-ttu-id="60a86-127">À partir de la **outils** menu, cliquez sur le **Options** élément.</span><span class="sxs-lookup"><span data-stu-id="60a86-127">From the **Tools** menu, click the **Options** item.</span></span> <span data-ttu-id="60a86-128">Cliquez sur **général** sous le **Windows Forms Designer** d’élément et vérifiez que le **AutoToolboxPopulate a** option est définie sur **True**.</span><span class="sxs-lookup"><span data-stu-id="60a86-128">Click **General** under the **Windows Forms Designer** item and ensure that the **AutoToolboxPopulate** option is set to **True**.</span></span>  
  
## <a name="creating-an-instance-of-a-custom-component"></a><span data-ttu-id="60a86-129">Création d’une Instance d’un composant personnalisé</span><span class="sxs-lookup"><span data-stu-id="60a86-129">Creating an Instance of a Custom Component</span></span>  
 <span data-ttu-id="60a86-130">L’étape suivante consiste à créer une instance du composant personnalisé sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="60a86-130">The next step is to create an instance of the custom component on the form.</span></span> <span data-ttu-id="60a86-131">Étant donné que le **boîte à outils** automatiquement des comptes pour le nouveau composant, il s’agit aussi simple que la création de tout autre composant ou contrôle.</span><span class="sxs-lookup"><span data-stu-id="60a86-131">Because the **Toolbox** automatically accounts for the new component, this is as easy as creating any other component or control.</span></span>  
  
#### <a name="to-create-an-instance-of-a-custom-component"></a><span data-ttu-id="60a86-132">Pour créer une instance d’un composant personnalisé</span><span class="sxs-lookup"><span data-stu-id="60a86-132">To create an instance of a custom component</span></span>  
  
1.  <span data-ttu-id="60a86-133">Ouvrez le formulaire du projet dans le **Concepteur Forms**.</span><span class="sxs-lookup"><span data-stu-id="60a86-133">Open the project's form in the **Forms Designer**.</span></span>  
  
2.  <span data-ttu-id="60a86-134">Dans le **boîte à outils**, cliquez sur le nouvel onglet appelé **Composants ToolboxExample**.</span><span class="sxs-lookup"><span data-stu-id="60a86-134">In the **Toolbox**, click the new tab called **ToolboxExample Components**.</span></span>  
  
     <span data-ttu-id="60a86-135">Une fois que vous cliquez sur l’onglet, vous verrez **DemoComponent**.</span><span class="sxs-lookup"><span data-stu-id="60a86-135">Once you click the tab, you will see **DemoComponent**.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="60a86-136">Pour des raisons de performances, les composants dans la zone rempli automatiquement de la **boîte à outils** n’affichent pas de bitmaps personnalisées et le <xref:System.Drawing.ToolboxBitmapAttribute> n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="60a86-136">For performance reasons, components in the auto-populated area of the **Toolbox** do not display custom bitmaps, and the <xref:System.Drawing.ToolboxBitmapAttribute> is not supported.</span></span> <span data-ttu-id="60a86-137">Pour afficher une icône pour un composant personnalisé dans le **boîte à outils**, utilisez le **Choose Toolbox Items** boîte de dialogue charger votre composant.</span><span class="sxs-lookup"><span data-stu-id="60a86-137">To display an icon for a custom component in the **Toolbox**, use the **Choose Toolbox Items** dialog box to load your component.</span></span>  
  
3.  <span data-ttu-id="60a86-138">Faites glisser votre composant sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="60a86-138">Drag your component onto your form.</span></span>  
  
     <span data-ttu-id="60a86-139">Une instance du composant est créée et ajoutée à la **barre d’état du composant**.</span><span class="sxs-lookup"><span data-stu-id="60a86-139">An instance of the component is created and added to the **Component Tray**.</span></span>  
  
## <a name="unloading-and-reloading-a-custom-component"></a><span data-ttu-id="60a86-140">Déchargement et rechargement d’un composant personnalisé</span><span class="sxs-lookup"><span data-stu-id="60a86-140">Unloading and Reloading a Custom Component</span></span>  
 <span data-ttu-id="60a86-141">Le **boîte à outils** compte des composants dans chaque chargé de projet, et lorsqu’un projet est déchargé, elle supprime les références aux composants du projet.</span><span class="sxs-lookup"><span data-stu-id="60a86-141">The **Toolbox** takes account of the components in each loaded project, and when a project is unloaded, it removes references to the project's components.</span></span>  
  
#### <a name="to-experiment-with-the-effect-on-the-toolbox-of-unloading-and-reloading-components"></a><span data-ttu-id="60a86-142">Pour tester l’effet sur la boîte à outils de déchargement et rechargement des composants</span><span class="sxs-lookup"><span data-stu-id="60a86-142">To experiment with the effect on the Toolbox of unloading and reloading components</span></span>  
  
1.  <span data-ttu-id="60a86-143">Décharger le projet à partir de la solution.</span><span class="sxs-lookup"><span data-stu-id="60a86-143">Unload the project from the solution.</span></span>  
  
     <span data-ttu-id="60a86-144">Pour plus d’informations sur le déchargement de projets, consultez [Comment : Décharger et recharger des projets](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="60a86-144">For more information about unloading projects, see [How to: Unload and Reload Projects](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100)).</span></span> <span data-ttu-id="60a86-145">Si vous êtes invité à enregistrer, choisissez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="60a86-145">If you are prompted to save, choose **Yes**.</span></span>  
  
2.  <span data-ttu-id="60a86-146">Ajouter un nouveau **Windows Application** projet à la solution.</span><span class="sxs-lookup"><span data-stu-id="60a86-146">Add a new **Windows Application** project to the solution.</span></span> <span data-ttu-id="60a86-147">Ouvrez le formulaire dans le **concepteur**.</span><span class="sxs-lookup"><span data-stu-id="60a86-147">Open the form in the **Designer**.</span></span>  
  
     <span data-ttu-id="60a86-148">Le **Composants ToolboxExample** onglet à partir du projet précédent est désormais disparu.</span><span class="sxs-lookup"><span data-stu-id="60a86-148">The **ToolboxExample Components** tab from the previous project is now gone.</span></span>  
  
3.  <span data-ttu-id="60a86-149">Recharger la `ToolboxExample` projet.</span><span class="sxs-lookup"><span data-stu-id="60a86-149">Reload the `ToolboxExample` project.</span></span>  
  
     <span data-ttu-id="60a86-150">Le **Composants ToolboxExample** onglet maintenant s’affiche de nouveau.</span><span class="sxs-lookup"><span data-stu-id="60a86-150">The **ToolboxExample Components** tab now reappears.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="60a86-151">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="60a86-151">Next Steps</span></span>  
 <span data-ttu-id="60a86-152">Cette procédure pas à pas montre que la **boîte à outils** tient compte des composants d’un projet, mais la **boîte à outils** tient également compte des contrôles.</span><span class="sxs-lookup"><span data-stu-id="60a86-152">This walkthrough demonstrates that the **Toolbox** takes account of a project's components, but the **Toolbox** is also takes account of controls.</span></span> <span data-ttu-id="60a86-153">Faites des essais avec vos propres contrôles personnalisés en ajoutant et supprimant des projets de contrôle à partir de votre solution.</span><span class="sxs-lookup"><span data-stu-id="60a86-153">Experiment with your own custom controls by adding and removing control projects from your solution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60a86-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60a86-154">See also</span></span>
- <span data-ttu-id="60a86-155">[Général, le Concepteur Windows Forms, boîte de dialogue Options](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="60a86-155">[General, Windows Forms Designer, Options Dialog Box](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))</span></span>
- <span data-ttu-id="60a86-156">[Guide pratique pour Manipuler des onglets de boîte à outils](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="60a86-156">[How to: Manipulate Toolbox Tabs](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))</span></span>
- <span data-ttu-id="60a86-157">[Choisir des éléments de boîte à outils, boîte de dialogue (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="60a86-157">[Choose Toolbox Items Dialog Box (Visual Studio)](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span></span>
- [<span data-ttu-id="60a86-158">Placement de contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="60a86-158">Putting Controls on Windows Forms</span></span>](putting-controls-on-windows-forms.md)
