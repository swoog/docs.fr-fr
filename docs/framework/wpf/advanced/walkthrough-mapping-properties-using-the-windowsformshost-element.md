---
title: 'Procédure pas à pas : Propriétés de mappage à l’aide de l’élément WindowsFormsHost'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mapping properties [WPF]
- WindowsFormsHost element property mapping [WPF]
ms.assetid: 74809167-bf8e-48b7-a2e7-b4ea08bc7d8c
ms.openlocfilehash: 943137017dcc1f8b347441669add13c3ab056f7d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493649"
---
# <a name="walkthrough-mapping-properties-using-the-windowsformshost-element"></a><span data-ttu-id="d439d-102">Procédure pas à pas : Propriétés de mappage à l’aide de l’élément WindowsFormsHost</span><span class="sxs-lookup"><span data-stu-id="d439d-102">Walkthrough: Mapping Properties Using the WindowsFormsHost Element</span></span>

<span data-ttu-id="d439d-103">Cette procédure pas à pas vous montre comment utiliser le <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A> propriété à mapper [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] propriétés aux propriétés correspondantes dans un hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.</span><span class="sxs-lookup"><span data-stu-id="d439d-103">This walkthrough shows you how to use the <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A> property to map [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] properties to corresponding properties on a hosted [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control.</span></span>

<span data-ttu-id="d439d-104">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d439d-104">Tasks illustrated in this walkthrough include:</span></span>

-   <span data-ttu-id="d439d-105">Création du projet.</span><span class="sxs-lookup"><span data-stu-id="d439d-105">Creating the project.</span></span>

-   <span data-ttu-id="d439d-106">Définition de la disposition de l’application.</span><span class="sxs-lookup"><span data-stu-id="d439d-106">Defining the application layout.</span></span>

-   <span data-ttu-id="d439d-107">Définition d’un nouveau mappage de propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-107">Defining a new property mapping.</span></span>

-   <span data-ttu-id="d439d-108">Suppression d’un mappage de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d439d-108">Removing a default property mapping.</span></span>

-   <span data-ttu-id="d439d-109">Remplacement d’un mappage de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d439d-109">Replacing a default property mapping.</span></span>

-   <span data-ttu-id="d439d-110">Extension d’un mappage de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d439d-110">Extending a default property mapping.</span></span>

<span data-ttu-id="d439d-111">Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [propriétés de mappage à l’aide de l’exemple d’élément WindowsFormsHost](https://go.microsoft.com/fwlink/?LinkID=160019).</span><span class="sxs-lookup"><span data-stu-id="d439d-111">For a complete code listing of the tasks illustrated in this walkthrough, see [Mapping Properties Using the WindowsFormsHost Element Sample](https://go.microsoft.com/fwlink/?LinkID=160019).</span></span>

<span data-ttu-id="d439d-112">Lorsque vous avez terminé, vous serez en mesure de mapper [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] propriétés aux propriétés correspondantes dans un hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.</span><span class="sxs-lookup"><span data-stu-id="d439d-112">When you are finished, you will be able to map [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] properties to corresponding properties on a hosted [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d439d-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d439d-113">Prerequisites</span></span>

<span data-ttu-id="d439d-114">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="d439d-114">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="d439d-115">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="d439d-115">Visual Studio 2017</span></span>

## <a name="create-and-set-up-the-project"></a><span data-ttu-id="d439d-116">Créer et configurer le projet</span><span class="sxs-lookup"><span data-stu-id="d439d-116">Create and set up the project</span></span>

1.  <span data-ttu-id="d439d-117">Créer un **application WPF** projet nommé `PropertyMappingWithWfhSample`.</span><span class="sxs-lookup"><span data-stu-id="d439d-117">Create a **WPF App** project named `PropertyMappingWithWfhSample`.</span></span>

2.  <span data-ttu-id="d439d-118">Dans **l’Explorateur de solutions**, ajoutez une référence à l’assembly WindowsFormsIntegration, nommé WindowsFormsIntegration.dll.</span><span class="sxs-lookup"><span data-stu-id="d439d-118">In **Solution Explorer**, add a reference to the WindowsFormsIntegration assembly, which is named WindowsFormsIntegration.dll.</span></span>

3.  <span data-ttu-id="d439d-119">Dans **l’Explorateur de solutions**, ajoutez des références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="d439d-119">In **Solution Explorer**, add references to the System.Drawing and System.Windows.Forms assemblies.</span></span>

## <a name="defining-the-application-layout"></a><span data-ttu-id="d439d-120">Définition de la disposition de l’application</span><span class="sxs-lookup"><span data-stu-id="d439d-120">Defining the Application Layout</span></span>

<span data-ttu-id="d439d-121">Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-application utilise le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément pour héberger un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.</span><span class="sxs-lookup"><span data-stu-id="d439d-121">The [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-based application uses the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element to host a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control.</span></span>

### <a name="to-define-the-application-layout"></a><span data-ttu-id="d439d-122">Pour définir la disposition de l’application</span><span class="sxs-lookup"><span data-stu-id="d439d-122">To define the application layout</span></span>

1.  <span data-ttu-id="d439d-123">Ouvrez Window1.xaml dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d439d-123">Open Window1.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>

2.  <span data-ttu-id="d439d-124">Remplacez le code existant par le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d439d-124">Replace the existing code with the following code.</span></span>

     [!code-xaml[PropertyMappingWithWfhSample#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml#1)]

3.  <span data-ttu-id="d439d-125">Ouvrez Window1.xaml.cs dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="d439d-125">Open Window1.xaml.cs in the Code Editor.</span></span>

4.  <span data-ttu-id="d439d-126">En haut du fichier, importez les espaces de noms suivants.</span><span class="sxs-lookup"><span data-stu-id="d439d-126">At the top of the file, import the following namespaces.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#20](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#20)]
     [!code-vb[PropertyMappingWithWfhSample#20](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#20)]

## <a name="defining-a-new-property-mapping"></a><span data-ttu-id="d439d-127">Définition d’un nouveau mappage de propriété</span><span class="sxs-lookup"><span data-stu-id="d439d-127">Defining a New Property Mapping</span></span>

<span data-ttu-id="d439d-128">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément fournit par défaut plusieurs mappages de propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-128">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element provides several default property mappings.</span></span> <span data-ttu-id="d439d-129">Vous ajoutez un nouveau mappage de propriété en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> méthode sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> l’élément <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span><span class="sxs-lookup"><span data-stu-id="d439d-129">You add a new property mapping by calling the <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> method on the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element's <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span></span>

### <a name="to-define-a-new-property-mapping"></a><span data-ttu-id="d439d-130">Pour définir un nouveau mappage de propriété</span><span class="sxs-lookup"><span data-stu-id="d439d-130">To define a new property mapping</span></span>

-   <span data-ttu-id="d439d-131">Copiez le code suivant dans la définition de la `Window1` classe.</span><span class="sxs-lookup"><span data-stu-id="d439d-131">Copy the following code into the definition for the `Window1` class.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#14](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#14)]
     [!code-vb[PropertyMappingWithWfhSample#14](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#14)]

     <span data-ttu-id="d439d-132">Le `AddClipMapping` méthode ajoute un nouveau mappage pour le <xref:System.Windows.UIElement.Clip%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-132">The `AddClipMapping` method adds a new mapping for the <xref:System.Windows.UIElement.Clip%2A> property.</span></span>

     <span data-ttu-id="d439d-133">Le `OnClipChange` méthode se traduit par la <xref:System.Windows.UIElement.Clip%2A> propriété le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.Control.Region%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-133">The `OnClipChange` method translates the <xref:System.Windows.UIElement.Clip%2A> property to the [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.Control.Region%2A> property.</span></span>

     <span data-ttu-id="d439d-134">Le `Window1_SizeChanged` méthode gère la fenêtre <xref:System.Windows.FrameworkElement.SizeChanged> événements et de la taille de la zone de découpage pour s’ajuster à la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="d439d-134">The `Window1_SizeChanged` method handles the window's <xref:System.Windows.FrameworkElement.SizeChanged> event and sizes the clipping region to fit the application window.</span></span>

## <a name="removing-a-default-property-mapping"></a><span data-ttu-id="d439d-135">Suppression d’un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-135">Removing a Default Property Mapping</span></span>

<span data-ttu-id="d439d-136">Supprimer un mappage de propriété par défaut en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Remove%2A> méthode sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> l’élément <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span><span class="sxs-lookup"><span data-stu-id="d439d-136">Remove a default property mapping by calling the <xref:System.Windows.Forms.Integration.PropertyMap.Remove%2A> method on the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element's <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span></span>

### <a name="to-remove-a-default-property-mapping"></a><span data-ttu-id="d439d-137">Pour supprimer un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-137">To remove a default property mapping</span></span>

-   <span data-ttu-id="d439d-138">Copiez le code suivant dans la définition de la `Window1` classe.</span><span class="sxs-lookup"><span data-stu-id="d439d-138">Copy the following code into the definition for the `Window1` class.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#13](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#13)]
     [!code-vb[PropertyMappingWithWfhSample#13](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#13)]

     <span data-ttu-id="d439d-139">Le `RemoveCursorMapping` méthode supprime le mappage par défaut pour le <xref:System.Windows.FrameworkElement.Cursor%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-139">The `RemoveCursorMapping` method deletes the default mapping for the <xref:System.Windows.FrameworkElement.Cursor%2A> property.</span></span>

## <a name="replacing-a-default-property-mapping"></a><span data-ttu-id="d439d-140">Remplacement d’un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-140">Replacing a Default Property Mapping</span></span>

<span data-ttu-id="d439d-141">Remplacez un mappage de propriété par défaut en supprimant le mappage par défaut et en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> méthode sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> l’élément <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span><span class="sxs-lookup"><span data-stu-id="d439d-141">Replace a default property mapping by removing the default mapping and calling the <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> method on the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element's <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A>.</span></span>

### <a name="to-replace-a-default-property-mapping"></a><span data-ttu-id="d439d-142">Pour remplacer un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-142">To replace a default property mapping</span></span>

-   <span data-ttu-id="d439d-143">Copiez le code suivant dans la définition de la `Window1` classe.</span><span class="sxs-lookup"><span data-stu-id="d439d-143">Copy the following code into the definition for the `Window1` class.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#12)]
     [!code-vb[PropertyMappingWithWfhSample#12](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#12)]

     <span data-ttu-id="d439d-144">Le `ReplaceFlowDirectionMapping` méthode remplace le mappage par défaut pour le <xref:System.Windows.FrameworkElement.FlowDirection%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-144">The `ReplaceFlowDirectionMapping` method replaces the default mapping for the <xref:System.Windows.FrameworkElement.FlowDirection%2A> property.</span></span>

     <span data-ttu-id="d439d-145">Le `OnFlowDirectionChange` méthode se traduit par la <xref:System.Windows.FrameworkElement.FlowDirection%2A> propriété le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.Control.RightToLeft%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-145">The `OnFlowDirectionChange` method translates the <xref:System.Windows.FrameworkElement.FlowDirection%2A> property to the [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.Control.RightToLeft%2A> property.</span></span>

     <span data-ttu-id="d439d-146">Le `cb_CheckedChanged` méthode gère le <xref:System.Windows.Forms.CheckBox.CheckedChanged> événement sur le <xref:System.Windows.Forms.CheckBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d439d-146">The `cb_CheckedChanged` method handles the <xref:System.Windows.Forms.CheckBox.CheckedChanged> event on the <xref:System.Windows.Forms.CheckBox> control.</span></span> <span data-ttu-id="d439d-147">Il assigne le <xref:System.Windows.FrameworkElement.FlowDirection%2A> propriété basée sur la valeur de la <xref:System.Windows.Forms.CheckBox.CheckState%2A> propriété</span><span class="sxs-lookup"><span data-stu-id="d439d-147">It assigns the <xref:System.Windows.FrameworkElement.FlowDirection%2A> property based on the value of the <xref:System.Windows.Forms.CheckBox.CheckState%2A> property</span></span>

## <a name="extending-a-default-property-mapping"></a><span data-ttu-id="d439d-148">Extension d’un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-148">Extending a Default Property Mapping</span></span>

<span data-ttu-id="d439d-149">Vous pouvez utiliser un mappage de propriété par défaut et l’étendre avec votre propre mappage.</span><span class="sxs-lookup"><span data-stu-id="d439d-149">You can use a default property mapping and also extend it with your own mapping.</span></span>

### <a name="to-extend-a-default-property-mapping"></a><span data-ttu-id="d439d-150">Pour étendre un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="d439d-150">To extend a default property mapping</span></span>

-   <span data-ttu-id="d439d-151">Copiez le code suivant dans la définition de la `Window1` classe.</span><span class="sxs-lookup"><span data-stu-id="d439d-151">Copy the following code into the definition for the `Window1` class.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#15)]
     [!code-vb[PropertyMappingWithWfhSample#15](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#15)]

     <span data-ttu-id="d439d-152">Le `ExtendBackgroundMapping` méthode ajoute un traducteur de propriété personnalisée à l’objet existant <xref:System.Windows.Controls.Control.Background%2A> mappage de propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-152">The `ExtendBackgroundMapping` method adds a custom property translator to the existing <xref:System.Windows.Controls.Control.Background%2A> property mapping.</span></span>

     <span data-ttu-id="d439d-153">Le `OnBackgroundChange` méthode assigne une image spécifique du contrôle hébergé <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="d439d-153">The `OnBackgroundChange` method assigns a specific image to the hosted control's <xref:System.Windows.Forms.Control.BackgroundImage%2A> property.</span></span> <span data-ttu-id="d439d-154">Le `OnBackgroundChange` méthode est appelée une fois que le mappage de propriété par défaut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="d439d-154">The `OnBackgroundChange` method is called after the default property mapping is applied.</span></span>

## <a name="initializing-your-property-mappings"></a><span data-ttu-id="d439d-155">Initialisation de vos mappages de propriétés</span><span class="sxs-lookup"><span data-stu-id="d439d-155">Initializing Your Property Mappings</span></span>

<span data-ttu-id="d439d-156">Définissez vos mappages de propriété en appelant les méthodes décrites précédemment le <xref:System.Windows.FrameworkElement.Loaded> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="d439d-156">Set up your property mappings by calling the previously described methods in the <xref:System.Windows.FrameworkElement.Loaded> event handler.</span></span>

### <a name="to-initialize-your-property-mappings"></a><span data-ttu-id="d439d-157">Pour initialiser vos mappages de propriétés</span><span class="sxs-lookup"><span data-stu-id="d439d-157">To initialize your property mappings</span></span>

1.  <span data-ttu-id="d439d-158">Copiez le code suivant dans la définition de la `Window1` classe.</span><span class="sxs-lookup"><span data-stu-id="d439d-158">Copy the following code into the definition for the `Window1` class.</span></span>

     [!code-csharp[PropertyMappingWithWfhSample#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithWfhSample/CSharp/PropertyMappingWithWfh/Window1.xaml.cs#11)]
     [!code-vb[PropertyMappingWithWfhSample#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithWfhSample/VisualBasic/PropertyMappingWithWfh/Window1.xaml.vb#11)]

     <span data-ttu-id="d439d-159">Le `WindowLoaded` méthode gère le <xref:System.Windows.FrameworkElement.Loaded> événement et effectue l’initialisation suivante.</span><span class="sxs-lookup"><span data-stu-id="d439d-159">The `WindowLoaded` method handles the <xref:System.Windows.FrameworkElement.Loaded> event and performs the following initialization.</span></span>

    -   <span data-ttu-id="d439d-160">Crée un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <xref:System.Windows.Forms.CheckBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d439d-160">Creates a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.CheckBox> control.</span></span>

    -   <span data-ttu-id="d439d-161">Appelle les méthodes que vous avez définies précédemment dans la procédure pas à pas pour configurer les mappages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d439d-161">Calls the methods you defined earlier in the walkthrough to set up the property mappings.</span></span>

    -   <span data-ttu-id="d439d-162">Assigne les valeurs initiales aux propriétés mappées.</span><span class="sxs-lookup"><span data-stu-id="d439d-162">Assigns initial values to the mapped properties.</span></span>

2.  <span data-ttu-id="d439d-163">Appuyez sur **F5** pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="d439d-163">Press **F5** to build and run the application.</span></span> <span data-ttu-id="d439d-164">Cliquez sur la case à cocher pour voir l’effet de la <xref:System.Windows.FrameworkElement.FlowDirection%2A> mappage.</span><span class="sxs-lookup"><span data-stu-id="d439d-164">Click the check box to see the effect of the <xref:System.Windows.FrameworkElement.FlowDirection%2A> mapping.</span></span> <span data-ttu-id="d439d-165">Quand vous cliquez sur la case à cocher, la disposition inverse son orientation de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="d439d-165">When you click the check box, the layout reverses its left-right orientation.</span></span>

## <a name="see-also"></a><span data-ttu-id="d439d-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d439d-166">See also</span></span>

- <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="d439d-167">Mappage de propriétés Windows Forms et WPF</span><span class="sxs-lookup"><span data-stu-id="d439d-167">Windows Forms and WPF Property Mapping</span></span>](../../../../docs/framework/wpf/advanced/windows-forms-and-wpf-property-mapping.md)
- [<span data-ttu-id="d439d-168">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d439d-168">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
- [<span data-ttu-id="d439d-169">Procédure pas à pas : Hébergement d’un contrôle de formulaires Windows dans WPF</span><span class="sxs-lookup"><span data-stu-id="d439d-169">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)