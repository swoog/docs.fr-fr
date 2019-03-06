---
title: 'Procédure pas à pas : Mappage de propriétés à l’aide du contrôle ElementHost'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mapping properties [WPF]
- ElementHost control [WPF], mapping properties
ms.assetid: bccd6e0d-2272-4924-9107-ff8ed58b88aa
ms.openlocfilehash: 3fe3f00950fdfdf92c3f95dc42b27cc9110e0c95
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371682"
---
# <a name="walkthrough-mapping-properties-using-the-elementhost-control"></a><span data-ttu-id="c76d7-102">Procédure pas à pas : Mappage de propriétés à l’aide du contrôle ElementHost</span><span class="sxs-lookup"><span data-stu-id="c76d7-102">Walkthrough: Mapping Properties Using the ElementHost Control</span></span>

<span data-ttu-id="c76d7-103">Cette procédure pas à pas vous montre comment utiliser le <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A> propriété à mapper [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] propriétés aux propriétés correspondantes dans un hébergé [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] élément.</span><span class="sxs-lookup"><span data-stu-id="c76d7-103">This walkthrough shows you how to use the <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A> property to map [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] properties to corresponding properties on a hosted [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] element.</span></span>

<span data-ttu-id="c76d7-104">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c76d7-104">Tasks illustrated in this walkthrough include:</span></span>

-   <span data-ttu-id="c76d7-105">Création du projet</span><span class="sxs-lookup"><span data-stu-id="c76d7-105">Creating the project.</span></span>

-   <span data-ttu-id="c76d7-106">Définition d’un nouveau mappage de propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-106">Defining a new property mapping.</span></span>

-   <span data-ttu-id="c76d7-107">Suppression d’un mappage de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="c76d7-107">Removing a default property mapping.</span></span>

-   <span data-ttu-id="c76d7-108">Extension d’un mappage de propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="c76d7-108">Extending a default property mapping.</span></span>

<span data-ttu-id="c76d7-109">Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [propriétés de mappage à l’aide de l’exemple de contrôle ElementHost](https://go.microsoft.com/fwlink/?LinkID=160018).</span><span class="sxs-lookup"><span data-stu-id="c76d7-109">For a complete code listing of the tasks illustrated in this walkthrough, see [Mapping Properties Using the ElementHost Control Sample](https://go.microsoft.com/fwlink/?LinkID=160018).</span></span>

<span data-ttu-id="c76d7-110">Lorsque vous avez terminé, vous serez en mesure de mapper [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] propriétés correspondant [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] propriétés sur un élément hébergé.</span><span class="sxs-lookup"><span data-stu-id="c76d7-110">When you are finished, you will be able to map [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] properties to corresponding [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] properties on a hosted element.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c76d7-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c76d7-111">Prerequisites</span></span>

<span data-ttu-id="c76d7-112">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="c76d7-112">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="c76d7-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="c76d7-113">Visual Studio 2017</span></span>

## <a name="creating-the-project"></a><span data-ttu-id="c76d7-114">Création du projet</span><span class="sxs-lookup"><span data-stu-id="c76d7-114">Creating the Project</span></span>

### <a name="to-create-the-project"></a><span data-ttu-id="c76d7-115">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="c76d7-115">To create the project</span></span>

1.  <span data-ttu-id="c76d7-116">Créer un **Windows Forms application** projet nommé `PropertyMappingWithElementHost`.</span><span class="sxs-lookup"><span data-stu-id="c76d7-116">Create a **Windows Forms App** project named `PropertyMappingWithElementHost`.</span></span>

2.  <span data-ttu-id="c76d7-117">Dans **l’Explorateur de solutions**, ajoutez des références à ce qui suit [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblys.</span><span class="sxs-lookup"><span data-stu-id="c76d7-117">In **Solution Explorer**, add references to the following [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblies.</span></span>

    -   <span data-ttu-id="c76d7-118">PresentationCore</span><span class="sxs-lookup"><span data-stu-id="c76d7-118">PresentationCore</span></span>

    -   <span data-ttu-id="c76d7-119">PresentationFramework</span><span class="sxs-lookup"><span data-stu-id="c76d7-119">PresentationFramework</span></span>

    -   <span data-ttu-id="c76d7-120">WindowsBase</span><span class="sxs-lookup"><span data-stu-id="c76d7-120">WindowsBase</span></span>

    -   <span data-ttu-id="c76d7-121">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="c76d7-121">WindowsFormsIntegration</span></span>

3.  <span data-ttu-id="c76d7-122">Copiez le code suivant en haut de la `Form1` fichier de code.</span><span class="sxs-lookup"><span data-stu-id="c76d7-122">Copy the following code into the top of the `Form1` code file.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#10](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#10)]
     [!code-vb[PropertyMappingWithElementHost#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#10)]

4.  <span data-ttu-id="c76d7-123">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="c76d7-123">Open `Form1` in the Windows Forms Designer.</span></span> <span data-ttu-id="c76d7-124">Double-cliquez sur le formulaire pour ajouter un gestionnaire d’événements pour le <xref:System.Windows.Forms.Form.Load> événement.</span><span class="sxs-lookup"><span data-stu-id="c76d7-124">Double-click the form to add an event handler for the <xref:System.Windows.Forms.Form.Load> event.</span></span>

5.  <span data-ttu-id="c76d7-125">Revenez au Concepteur Windows Forms et ajouter un gestionnaire d’événements pour le formulaire <xref:System.Windows.Forms.Control.Resize> événement.</span><span class="sxs-lookup"><span data-stu-id="c76d7-125">Return to the Windows Forms Designer and add an event handler for the form's <xref:System.Windows.Forms.Control.Resize> event.</span></span> <span data-ttu-id="c76d7-126">Pour plus d'informations, voir [Procédure : Créer des gestionnaires d’événements à l’aide du concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="c76d7-126">For more information, see [How to: Create Event Handlers Using the Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)).</span></span>

6.  <span data-ttu-id="c76d7-127">Déclarez un <xref:System.Windows.Forms.Integration.ElementHost> champ dans le `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-127">Declare an <xref:System.Windows.Forms.Integration.ElementHost> field in the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#16](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#16)]
     [!code-vb[PropertyMappingWithElementHost#16](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#16)]

## <a name="defining-new-property-mappings"></a><span data-ttu-id="c76d7-128">Définition de nouveaux mappages de propriété</span><span class="sxs-lookup"><span data-stu-id="c76d7-128">Defining New Property Mappings</span></span>

<span data-ttu-id="c76d7-129">Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle fournit par défaut plusieurs mappages de propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-129">The <xref:System.Windows.Forms.Integration.ElementHost> control provides several default property mappings.</span></span> <span data-ttu-id="c76d7-130">Vous ajoutez un nouveau mappage de propriété en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> méthode sur le <xref:System.Windows.Forms.Integration.ElementHost> du contrôle <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.</span><span class="sxs-lookup"><span data-stu-id="c76d7-130">You add a new property mapping by calling the <xref:System.Windows.Forms.Integration.PropertyMap.Add%2A> method on the <xref:System.Windows.Forms.Integration.ElementHost> control's <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.</span></span>

### <a name="to-define-new-property-mappings"></a><span data-ttu-id="c76d7-131">Pour définir de nouveaux mappages de propriété</span><span class="sxs-lookup"><span data-stu-id="c76d7-131">To define new property mappings</span></span>

1.  <span data-ttu-id="c76d7-132">Copiez le code suivant dans la définition de la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-132">Copy the following code into the definition for the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#12](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#12)]
     [!code-vb[PropertyMappingWithElementHost#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#12)]

     <span data-ttu-id="c76d7-133">Le `AddMarginMapping` méthode ajoute un nouveau mappage pour le <xref:System.Windows.Forms.Control.Margin%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-133">The `AddMarginMapping` method adds a new mapping for the <xref:System.Windows.Forms.Control.Margin%2A> property.</span></span>

     <span data-ttu-id="c76d7-134">Le `OnMarginChange` méthode se traduit par la <xref:System.Windows.Forms.Control.Margin%2A> propriété le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.FrameworkElement.Margin%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-134">The `OnMarginChange` method translates the <xref:System.Windows.Forms.Control.Margin%2A> property to the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.FrameworkElement.Margin%2A> property.</span></span>

2.  <span data-ttu-id="c76d7-135">Copiez le code suivant dans la définition de la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-135">Copy the following code into the definition for the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#14](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#14)]
     [!code-vb[PropertyMappingWithElementHost#14](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#14)]

     <span data-ttu-id="c76d7-136">Le `AddRegionMapping` méthode ajoute un nouveau mappage pour le <xref:System.Windows.Forms.Control.Region%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-136">The `AddRegionMapping` method adds a new mapping for the <xref:System.Windows.Forms.Control.Region%2A> property.</span></span>

     <span data-ttu-id="c76d7-137">Le `OnRegionChange` méthode se traduit par la <xref:System.Windows.Forms.Control.Region%2A> propriété le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.UIElement.Clip%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-137">The `OnRegionChange` method translates the <xref:System.Windows.Forms.Control.Region%2A> property to the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.UIElement.Clip%2A> property.</span></span>

     <span data-ttu-id="c76d7-138">Le `Form1_Resize` méthode gère le formulaire <xref:System.Windows.Forms.Control.Resize> événements et de la taille de la zone de découpage pour s’ajuster à l’élément hébergé.</span><span class="sxs-lookup"><span data-stu-id="c76d7-138">The `Form1_Resize` method handles the form's <xref:System.Windows.Forms.Control.Resize> event and sizes the clipping region to fit the hosted element.</span></span>

## <a name="removing-a-default-property-mapping"></a><span data-ttu-id="c76d7-139">Suppression d’un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="c76d7-139">Removing a Default Property Mapping</span></span>

<span data-ttu-id="c76d7-140">Supprimer un mappage de propriété par défaut en appelant le <xref:System.Windows.Forms.Integration.PropertyMap.Remove%2A> méthode sur le <xref:System.Windows.Forms.Integration.ElementHost> du contrôle <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.</span><span class="sxs-lookup"><span data-stu-id="c76d7-140">Remove a default property mapping by calling the <xref:System.Windows.Forms.Integration.PropertyMap.Remove%2A> method on the <xref:System.Windows.Forms.Integration.ElementHost> control's <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A>.</span></span>

### <a name="to-remove-a-default-property-mapping"></a><span data-ttu-id="c76d7-141">Pour supprimer un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="c76d7-141">To remove a default property mapping</span></span>

-   <span data-ttu-id="c76d7-142">Copiez le code suivant dans la définition de la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-142">Copy the following code into the definition for the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#13](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#13)]
     [!code-vb[PropertyMappingWithElementHost#13](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#13)]

     <span data-ttu-id="c76d7-143">Le `RemoveCursorMapping` méthode supprime le mappage par défaut pour le <xref:System.Windows.Forms.Control.Cursor%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-143">The `RemoveCursorMapping` method deletes the default mapping for the <xref:System.Windows.Forms.Control.Cursor%2A> property.</span></span>

## <a name="extending-a-default-property-mapping"></a><span data-ttu-id="c76d7-144">Extension d’un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="c76d7-144">Extending a Default Property Mapping</span></span>

<span data-ttu-id="c76d7-145">Vous pouvez utiliser un mappage de propriété par défaut et l’étendre avec votre propre mappage.</span><span class="sxs-lookup"><span data-stu-id="c76d7-145">You can use a default property mapping and also extend it with your own mapping.</span></span>

### <a name="to-extend-a-default-property-mapping"></a><span data-ttu-id="c76d7-146">Pour étendre un mappage de propriété par défaut</span><span class="sxs-lookup"><span data-stu-id="c76d7-146">To extend a default property mapping</span></span>

-   <span data-ttu-id="c76d7-147">Copiez le code suivant dans la définition de la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-147">Copy the following code into the definition for the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#15](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#15)]
     [!code-vb[PropertyMappingWithElementHost#15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#15)]

     <span data-ttu-id="c76d7-148">Le `ExtendBackColorMapping` méthode ajoute un traducteur de propriété personnalisée à l’objet existant <xref:System.Windows.Forms.Control.BackColor%2A> mappage de propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-148">The `ExtendBackColorMapping` method adds a custom property translator to the existing <xref:System.Windows.Forms.Control.BackColor%2A> property mapping.</span></span>

     <span data-ttu-id="c76d7-149">Le `OnBackColorChange` méthode assigne une image spécifique du contrôle hébergé <xref:System.Windows.Controls.Control.Background%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c76d7-149">The `OnBackColorChange` method assigns a specific image to the hosted control's <xref:System.Windows.Controls.Control.Background%2A> property.</span></span> <span data-ttu-id="c76d7-150">Le `OnBackColorChange` méthode est appelée une fois que le mappage de propriété par défaut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="c76d7-150">The `OnBackColorChange` method is called after the default property mapping is applied.</span></span>

## <a name="initialize-your-property-mappings"></a><span data-ttu-id="c76d7-151">Initialiser vos mappages de propriétés</span><span class="sxs-lookup"><span data-stu-id="c76d7-151">Initialize your property mappings</span></span>

1.  <span data-ttu-id="c76d7-152">Copiez le code suivant dans la définition de la `Form1` classe.</span><span class="sxs-lookup"><span data-stu-id="c76d7-152">Copy the following code into the definition for the `Form1` class.</span></span>

     [!code-csharp[PropertyMappingWithElementHost#11](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertyMappingWithElementHost/CSharp/PropertyMappingWithElementHost/Form1.cs#11)]
     [!code-vb[PropertyMappingWithElementHost#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertyMappingWithElementHost/VisualBasic/PropertyMappingWithElementHost/Form1.vb#11)]

     <span data-ttu-id="c76d7-153">Le `Form1_Load` méthode gère le <xref:System.Windows.Forms.Form.Load> événement et effectue l’initialisation suivante.</span><span class="sxs-lookup"><span data-stu-id="c76d7-153">The `Form1_Load` method handles the <xref:System.Windows.Forms.Form.Load> event and performs the following initialization.</span></span>

    -   <span data-ttu-id="c76d7-154">Crée un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Button> élément.</span><span class="sxs-lookup"><span data-stu-id="c76d7-154">Creates a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.Button> element.</span></span>

    -   <span data-ttu-id="c76d7-155">Appelle les méthodes que vous avez définies précédemment dans la procédure pas à pas pour configurer les mappages de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c76d7-155">Calls the methods you defined earlier in the walkthrough to set up the property mappings.</span></span>

    -   <span data-ttu-id="c76d7-156">Assigne les valeurs initiales aux propriétés mappées.</span><span class="sxs-lookup"><span data-stu-id="c76d7-156">Assigns initial values to the mapped properties.</span></span>

2.  <span data-ttu-id="c76d7-157">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="c76d7-157">Press F5 to build and run the application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c76d7-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c76d7-158">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost.PropertyMap%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="c76d7-159">Mappage de propriétés Windows Forms et WPF</span><span class="sxs-lookup"><span data-stu-id="c76d7-159">Windows Forms and WPF Property Mapping</span></span>](windows-forms-and-wpf-property-mapping.md)
- [<span data-ttu-id="c76d7-160">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c76d7-160">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
- [<span data-ttu-id="c76d7-161">Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c76d7-161">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)