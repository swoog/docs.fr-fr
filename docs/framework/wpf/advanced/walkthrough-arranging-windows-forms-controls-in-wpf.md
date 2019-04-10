---
title: 'Procédure pas à pas : organisation des contrôles Windows Forms dans WPF'
ms.date: 04/03/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hybrid applications [WPF interoperability]
- arranging controls [WPF]
ms.assetid: a1db8049-15c7-45d6-ae3d-36a6735cb848
ms.openlocfilehash: d2bd3a7d4b8e84542f1c5fa3dbb15f1a9753a180
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59168582"
---
# <a name="walkthrough-arranging-windows-forms-controls-in-wpf"></a><span data-ttu-id="b79f4-102">Procédure pas à pas : organisation des contrôles Windows Forms dans WPF</span><span class="sxs-lookup"><span data-stu-id="b79f4-102">Walkthrough: Arranging Windows Forms Controls in WPF</span></span>
<span data-ttu-id="b79f4-103">Cette procédure pas à pas vous montre comment utiliser [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] des fonctionnalités de disposition pour réorganiser [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles dans une application hybride.</span><span class="sxs-lookup"><span data-stu-id="b79f4-103">This walkthrough shows you how to use [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] layout features to arrange [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls in a hybrid application.</span></span>  
  
 <span data-ttu-id="b79f4-104">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b79f4-104">Tasks illustrated in this walkthrough include:</span></span>  
  
-   <span data-ttu-id="b79f4-105">Création du projet</span><span class="sxs-lookup"><span data-stu-id="b79f4-105">Creating the project.</span></span>  
  
-   <span data-ttu-id="b79f4-106">Utilisation des paramètres de disposition par défaut</span><span class="sxs-lookup"><span data-stu-id="b79f4-106">Using default layout settings.</span></span>  
  
-   <span data-ttu-id="b79f4-107">Dimensionnement en fonction du contenu</span><span class="sxs-lookup"><span data-stu-id="b79f4-107">Sizing to content.</span></span>  
  
-   <span data-ttu-id="b79f4-108">Utilisation du positionnement absolu</span><span class="sxs-lookup"><span data-stu-id="b79f4-108">Using absolute positioning.</span></span>  
  
-   <span data-ttu-id="b79f4-109">Spécification explicite de la taille</span><span class="sxs-lookup"><span data-stu-id="b79f4-109">Specifying size explicitly.</span></span>  
  
-   <span data-ttu-id="b79f4-110">Définition des propriétés de disposition</span><span class="sxs-lookup"><span data-stu-id="b79f4-110">Setting layout properties.</span></span>  
  
-   <span data-ttu-id="b79f4-111">Présentation des limitations dans l’ordre de plan</span><span class="sxs-lookup"><span data-stu-id="b79f4-111">Understanding z-order limitations.</span></span>  
  
-   <span data-ttu-id="b79f4-112">Ancrage</span><span class="sxs-lookup"><span data-stu-id="b79f4-112">Docking.</span></span>  
  
-   <span data-ttu-id="b79f4-113">Définition de la visibilité</span><span class="sxs-lookup"><span data-stu-id="b79f4-113">Setting visibility.</span></span>  
  
-   <span data-ttu-id="b79f4-114">Hébergement d’un contrôle qui ne s’étire pas</span><span class="sxs-lookup"><span data-stu-id="b79f4-114">Hosting a control that does not stretch.</span></span>  
  
-   <span data-ttu-id="b79f4-115">Mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="b79f4-115">Scaling.</span></span>  
  
-   <span data-ttu-id="b79f4-116">Rotation</span><span class="sxs-lookup"><span data-stu-id="b79f4-116">Rotating.</span></span>  
  
-   <span data-ttu-id="b79f4-117">Définition d’une marge intérieure et de marges</span><span class="sxs-lookup"><span data-stu-id="b79f4-117">Setting padding and margins.</span></span>  
  
-   <span data-ttu-id="b79f4-118">Utilisation de conteneurs de présentation dynamiques</span><span class="sxs-lookup"><span data-stu-id="b79f4-118">Using dynamic layout containers.</span></span>  
  
 <span data-ttu-id="b79f4-119">Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [disposition de contrôles Windows Forms dans WPF, exemple](https://go.microsoft.com/fwlink/?LinkID=159971).</span><span class="sxs-lookup"><span data-stu-id="b79f4-119">For a complete code listing of the tasks illustrated in this walkthrough, see [Arranging Windows Forms Controls in WPF Sample](https://go.microsoft.com/fwlink/?LinkID=159971).</span></span>  
  
 <span data-ttu-id="b79f4-120">Lorsque vous avez terminé, vous aurez une compréhension de [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] des fonctionnalités de disposition dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-en fonction des applications.</span><span class="sxs-lookup"><span data-stu-id="b79f4-120">When you are finished, you will have an understanding of [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] layout features in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-based applications.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="b79f4-121">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b79f4-121">Prerequisites</span></span>  

<span data-ttu-id="b79f4-122">Cette procédure pas à pas nécessite Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b79f4-122">You need Visual Studio to complete this walkthrough.</span></span>
  
## <a name="creating-the-project"></a><span data-ttu-id="b79f4-123">Création du projet</span><span class="sxs-lookup"><span data-stu-id="b79f4-123">Creating the Project</span></span>  
  
#### <a name="to-create-and-set-up-the-project"></a><span data-ttu-id="b79f4-124">Pour créer et configurer le projet</span><span class="sxs-lookup"><span data-stu-id="b79f4-124">To create and set up the project</span></span>  
  
1.  <span data-ttu-id="b79f4-125">Créez un projet d’Application WPF nommé `WpfLayoutHostingWf`.</span><span class="sxs-lookup"><span data-stu-id="b79f4-125">Create a WPF Application project named `WpfLayoutHostingWf`.</span></span>  
  
2.  <span data-ttu-id="b79f4-126">Dans l’Explorateur de solutions, ajoutez des références aux assemblys suivants.</span><span class="sxs-lookup"><span data-stu-id="b79f4-126">In Solution Explorer, add references to the following assemblies.</span></span>  
  
    -   <span data-ttu-id="b79f4-127">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="b79f4-127">WindowsFormsIntegration</span></span>  
  
    -   <span data-ttu-id="b79f4-128">System.Windows.Forms</span><span class="sxs-lookup"><span data-stu-id="b79f4-128">System.Windows.Forms</span></span>  
  
    -   <span data-ttu-id="b79f4-129">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="b79f4-129">System.Drawing</span></span>  
  
3.  <span data-ttu-id="b79f4-130">Double-cliquez sur MainWindow.xaml pour l’ouvrir dans la vue XAML.</span><span class="sxs-lookup"><span data-stu-id="b79f4-130">Double-click MainWindow.xaml to open it in XAML view.</span></span>  
  
4.  <span data-ttu-id="b79f4-131">Dans le <xref:System.Windows.Window> élément, ajoutez le code suivant [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] mappage d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b79f4-131">In the <xref:System.Windows.Window> element, add the following [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] namespace mapping.</span></span>  
  
    ```xaml  
    xmlns:wf="clr-namespace:System.Windows.Forms;assembly=System.Windows.Forms"  
    ```  
  
5.  <span data-ttu-id="b79f4-132">Dans le <xref:System.Windows.Controls.Grid> élément défini le <xref:System.Windows.Controls.Grid.ShowGridLines%2A> propriété `true` et définissez cinq lignes et trois colonnes.</span><span class="sxs-lookup"><span data-stu-id="b79f4-132">In the <xref:System.Windows.Controls.Grid> element set the <xref:System.Windows.Controls.Grid.ShowGridLines%2A> property to `true` and define five rows and three columns.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#2](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#2)]  
  
## <a name="using-default-layout-settings"></a><span data-ttu-id="b79f4-133">Utilisation des paramètres de disposition par défaut</span><span class="sxs-lookup"><span data-stu-id="b79f4-133">Using Default Layout Settings</span></span>  
 <span data-ttu-id="b79f4-134">Par défaut, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément gère la disposition pour hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.</span><span class="sxs-lookup"><span data-stu-id="b79f4-134">By default, the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element handles the layout for the hosted [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control.</span></span>  
  
#### <a name="to-use-default-layout-settings"></a><span data-ttu-id="b79f4-135">Pour utiliser les paramètres de disposition par défaut</span><span class="sxs-lookup"><span data-stu-id="b79f4-135">To use default layout settings</span></span>  
  
1.  <span data-ttu-id="b79f4-136">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-136">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#3](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#3)]  
  
2.  <span data-ttu-id="b79f4-137">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-137">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-138">Le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.Button?displayProperty=nameWithType> contrôle s’affiche dans le <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="b79f4-138">The [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]<xref:System.Windows.Forms.Button?displayProperty=nameWithType> control appears in the <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="b79f4-139">Le contrôle hébergé est dimensionné selon son contenu et le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est dimensionné selon le contrôle hébergé.</span><span class="sxs-lookup"><span data-stu-id="b79f4-139">The hosted control is sized based on its content, and the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is sized to accommodate the hosted control.</span></span>  
  
## <a name="sizing-to-content"></a><span data-ttu-id="b79f4-140">Dimensionnement en fonction du contenu</span><span class="sxs-lookup"><span data-stu-id="b79f4-140">Sizing to Content</span></span>  
 <span data-ttu-id="b79f4-141">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément garantit que le contrôle hébergé est dimensionné pour afficher correctement son contenu.</span><span class="sxs-lookup"><span data-stu-id="b79f4-141">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element ensures that the hosted control is sized to display its content properly.</span></span>  
  
#### <a name="to-size-to-content"></a><span data-ttu-id="b79f4-142">Pour dimensionner en fonction du contenu</span><span class="sxs-lookup"><span data-stu-id="b79f4-142">To size to content</span></span>  
  
1.  <span data-ttu-id="b79f4-143">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-143">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#4](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#4)]  
  
2.  <span data-ttu-id="b79f4-144">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-144">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-145">Les deux nouveaux contrôles bouton sont dimensionnés pour s’afficher correctement, la plus longue chaîne de texte et la taille de police et la <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments sont redimensionnés pour contenir les contrôles hébergés.</span><span class="sxs-lookup"><span data-stu-id="b79f4-145">The two new button controls are sized to display the longer text string and larger font size properly, and the <xref:System.Windows.Forms.Integration.WindowsFormsHost> elements are resized to accommodate the hosted controls.</span></span>  
  
## <a name="using-absolute-positioning"></a><span data-ttu-id="b79f4-146">Utilisation du positionnement absolu</span><span class="sxs-lookup"><span data-stu-id="b79f4-146">Using Absolute Positioning</span></span>  
 <span data-ttu-id="b79f4-147">Vous pouvez utiliser le positionnement absolu pour placer le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément n’importe où dans l’interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="b79f4-147">You can use absolute positioning to place the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element anywhere in the user interface (UI).</span></span>  
  
#### <a name="to-use-absolute-positioning"></a><span data-ttu-id="b79f4-148">Pour utiliser le positionnement absolu</span><span class="sxs-lookup"><span data-stu-id="b79f4-148">To use absolute positioning</span></span>  
  
1.  <span data-ttu-id="b79f4-149">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-149">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#5](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#5)]  
  
2.  <span data-ttu-id="b79f4-150">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-150">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-151">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est placé à 20 pixels du haut de la cellule de grille et 20 pixels à partir de la gauche.</span><span class="sxs-lookup"><span data-stu-id="b79f4-151">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is placed 20 pixels from the top side of the grid cell and 20 pixels from the left.</span></span>  
  
## <a name="specifying-size-explicitly"></a><span data-ttu-id="b79f4-152">Spécification explicite de la taille</span><span class="sxs-lookup"><span data-stu-id="b79f4-152">Specifying Size Explicitly</span></span>  
 <span data-ttu-id="b79f4-153">Vous pouvez spécifier la taille de la <xref:System.Windows.Forms.Integration.WindowsFormsHost> à l’aide de l’élément le <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="b79f4-153">You can specify the size of the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element using the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties.</span></span>  
  
#### <a name="to-specify-size-explicitly"></a><span data-ttu-id="b79f4-154">Pour spécifier explicitement la taille</span><span class="sxs-lookup"><span data-stu-id="b79f4-154">To specify size explicitly</span></span>  
  
1.  <span data-ttu-id="b79f4-155">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-155">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#6](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#6)]  
  
2.  <span data-ttu-id="b79f4-156">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-156">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-157">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément a une taille de 50 pixels de large sur 70 pixels en hauteur, qui est plus petit que les paramètres de disposition par défaut.</span><span class="sxs-lookup"><span data-stu-id="b79f4-157">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is set to a size of 50 pixels wide by 70 pixels high, which is smaller than the default layout settings.</span></span> <span data-ttu-id="b79f4-158">Le contenu de la [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est réorganisé en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b79f4-158">The content of the [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control is rearranged accordingly.</span></span>  
  
## <a name="setting-layout-properties"></a><span data-ttu-id="b79f4-159">Définition des propriétés de disposition</span><span class="sxs-lookup"><span data-stu-id="b79f4-159">Setting Layout Properties</span></span>  
 <span data-ttu-id="b79f4-160">Toujours défini les propriétés relatives à la disposition sur le contrôle hébergé en utilisant les propriétés de la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-160">Always set layout-related properties on the hosted control by using the properties of the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element.</span></span> <span data-ttu-id="b79f4-161">Si vous définissez les propriétés de disposition directement sur le contrôle hébergé, vous obtiendrez des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="b79f4-161">Setting layout properties directly on the hosted control will yield unintended results.</span></span>  
  
 <span data-ttu-id="b79f4-162">Définition des propriétés relatives à la disposition sur le contrôle hébergé dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="b79f4-162">Setting layout-related properties on the hosted control in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] has no effect.</span></span>  
  
#### <a name="to-see-the-effects-of-setting-properties-on-the-hosted-control"></a><span data-ttu-id="b79f4-163">Pour afficher les effets de la définition des propriétés sur le contrôle hébergé</span><span class="sxs-lookup"><span data-stu-id="b79f4-163">To see the effects of setting properties on the hosted control</span></span>  
  
1.  <span data-ttu-id="b79f4-164">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-164">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>  
  
     [!code-xaml[WpfLayoutHostingWfWithXaml#7](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#7)]  
  
2.  <span data-ttu-id="b79f4-165">Dans l’Explorateur de solutions, double-cliquez sur MainWindow.xaml.</span><span class="sxs-lookup"><span data-stu-id="b79f4-165">In Solution Explorer, double-click MainWindow.xaml.</span></span> <span data-ttu-id="b79f4-166">vb ou MainWindow.xaml.cs pour l’ouvrir dans l’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="b79f4-166">vb or MainWindow.xaml.cs to open it in the Code Editor.</span></span>  
  
3.  <span data-ttu-id="b79f4-167">Copiez le code suivant dans le `MainWindow` définition de classe.</span><span class="sxs-lookup"><span data-stu-id="b79f4-167">Copy the following code into the `MainWindow` class definition.</span></span>  
  
     [!code-csharp[WpfLayoutHostingWfWithXaml#101](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#101)]
     [!code-vb[WpfLayoutHostingWfWithXaml#101](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#101)]

4.  <span data-ttu-id="b79f4-168">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-168">Press F5 to build and run the application.</span></span>

5.  <span data-ttu-id="b79f4-169">Cliquez sur le **Click me** bouton.</span><span class="sxs-lookup"><span data-stu-id="b79f4-169">Click the **Click me** button.</span></span> <span data-ttu-id="b79f4-170">Le `button1_Click` Gestionnaire d’événements définit la <xref:System.Windows.Forms.Control.Top%2A> et <xref:System.Windows.Forms.Control.Left%2A> propriétés sur le contrôle hébergé.</span><span class="sxs-lookup"><span data-stu-id="b79f4-170">The `button1_Click` event handler sets the <xref:System.Windows.Forms.Control.Top%2A> and <xref:System.Windows.Forms.Control.Left%2A> properties on the hosted control.</span></span> <span data-ttu-id="b79f4-171">Le contrôle hébergé est ainsi repositionné dans le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-171">This causes the hosted control to be repositioned within the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element.</span></span> <span data-ttu-id="b79f4-172">L’hôte conserve la même zone d’écran, mais le contrôle hébergé est découpé.</span><span class="sxs-lookup"><span data-stu-id="b79f4-172">The host maintains the same screen area, but the hosted control is clipped.</span></span> <span data-ttu-id="b79f4-173">Au lieu de cela, le contrôle hébergé doit toujours remplir le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-173">Instead, the hosted control should always fill the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element.</span></span>

## <a name="understanding-z-order-limitations"></a><span data-ttu-id="b79f4-174">Présentation des limitations dans l’ordre de plan</span><span class="sxs-lookup"><span data-stu-id="b79f4-174">Understanding Z-Order Limitations</span></span>
 <span data-ttu-id="b79f4-175">Visible <xref:System.Windows.Forms.Integration.WindowsFormsHost> éléments sont toujours dessinés sur d’autres éléments WPF, et ils ne sont pas affectés par l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="b79f4-175">Visible <xref:System.Windows.Forms.Integration.WindowsFormsHost> elements are always drawn on top of other WPF elements, and they are unaffected by z-order.</span></span> <span data-ttu-id="b79f4-176">Pour voir ce comportement de l’ordre de plan, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b79f4-176">To see this z-order behavior, do the following:</span></span>

1.  <span data-ttu-id="b79f4-177">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-177">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#8](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#8)]

2.  <span data-ttu-id="b79f4-178">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-178">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-179">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est peint sur l’élément label.</span><span class="sxs-lookup"><span data-stu-id="b79f4-179">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is painted over the label element.</span></span>

## <a name="docking"></a><span data-ttu-id="b79f4-180">Ancrage</span><span class="sxs-lookup"><span data-stu-id="b79f4-180">Docking</span></span>
 <xref:System.Windows.Forms.Integration.WindowsFormsHost> <span data-ttu-id="b79f4-181">prend en charge de l’élément [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="b79f4-181">element supports [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] docking.</span></span> <span data-ttu-id="b79f4-182">Définir le <xref:System.Windows.Controls.DockPanel.Dock%2A> propriété jointe pour ancrer le contrôle hébergé dans un <xref:System.Windows.Controls.DockPanel> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-182">Set the <xref:System.Windows.Controls.DockPanel.Dock%2A> attached property to dock the hosted control in a <xref:System.Windows.Controls.DockPanel> element.</span></span>

#### <a name="to-dock-a-hosted-control"></a><span data-ttu-id="b79f4-183">Pour ancrer un contrôle hébergé</span><span class="sxs-lookup"><span data-stu-id="b79f4-183">To dock a hosted control</span></span>

1.  <span data-ttu-id="b79f4-184">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-184">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#9](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#9)]

2.  <span data-ttu-id="b79f4-185">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-185">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-186">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est ancré à droite de la <xref:System.Windows.Controls.DockPanel> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-186">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is docked to the right side of the <xref:System.Windows.Controls.DockPanel> element.</span></span>

## <a name="setting-visibility"></a><span data-ttu-id="b79f4-187">Définition de la visibilité</span><span class="sxs-lookup"><span data-stu-id="b79f4-187">Setting Visibility</span></span>
 <span data-ttu-id="b79f4-188">Vous pouvez rendre votre [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle invisible ou réduit en définissant le <xref:System.Windows.UIElement.Visibility%2A> propriété sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-188">You can make your [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control invisible or collapse it by setting the <xref:System.Windows.UIElement.Visibility%2A> property on the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element.</span></span> <span data-ttu-id="b79f4-189">Quand un contrôle est invisible, il n’est pas affiché, mais il occupe l’espace de disposition.</span><span class="sxs-lookup"><span data-stu-id="b79f4-189">When a control is invisible, it is not displayed, but it occupies layout space.</span></span> <span data-ttu-id="b79f4-190">Quand un contrôle est réduit, il n’est pas affiché et n’occupe pas l’espace de disposition.</span><span class="sxs-lookup"><span data-stu-id="b79f4-190">When a control is collapsed, it is not displayed, nor does it occupy layout space.</span></span>

#### <a name="to-set-the-visibility-of-a-hosted-control"></a><span data-ttu-id="b79f4-191">Pour définir la visibilité d’un contrôle hébergé</span><span class="sxs-lookup"><span data-stu-id="b79f4-191">To set the visibility of a hosted control</span></span>

1.  <span data-ttu-id="b79f4-192">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-192">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#10](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#10)]

2.  <span data-ttu-id="b79f4-193">Dans MainWindow.xaml.vb ou MainWindow.xaml.cs, copiez le code suivant dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="b79f4-193">In MainWindow.xaml.vb or MainWindow.xaml.cs, copy the following code into the class definition.</span></span>

     [!code-csharp[WpfLayoutHostingWfWithXaml#102](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#102)]
     [!code-vb[WpfLayoutHostingWfWithXaml#102](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#102)]

3.  <span data-ttu-id="b79f4-194">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-194">Press F5 to build and run the application.</span></span>

4.  <span data-ttu-id="b79f4-195">Cliquez sur le **cliquer pour rendre invisible** bouton pour rendre le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément invisible.</span><span class="sxs-lookup"><span data-stu-id="b79f4-195">Click the **Click to make invisible** button to make the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element invisible.</span></span>

5.  <span data-ttu-id="b79f4-196">Cliquez sur le **cliquer pour réduire** bouton pour masquer la <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément à partir de la mise en page entièrement.</span><span class="sxs-lookup"><span data-stu-id="b79f4-196">Click the **Click to collapse** button to hide the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element from the layout entirely.</span></span> <span data-ttu-id="b79f4-197">Lorsque le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle est réduit, les éléments voisins sont réorganisés pour occuper son espace.</span><span class="sxs-lookup"><span data-stu-id="b79f4-197">When the [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control is collapsed, the surrounding elements are rearranged to occupy its space.</span></span>

## <a name="hosting-a-control-that-does-not-stretch"></a><span data-ttu-id="b79f4-198">Hébergement d’un contrôle qui ne s’étire pas</span><span class="sxs-lookup"><span data-stu-id="b79f4-198">Hosting a Control That Does Not Stretch</span></span>
 <span data-ttu-id="b79f4-199">Certains [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles ont une taille fixe et ne s’étirent pas pour remplir l’espace disponible dans la disposition.</span><span class="sxs-lookup"><span data-stu-id="b79f4-199">Some [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls have a fixed size and do not stretch to fill available space in the layout.</span></span> <span data-ttu-id="b79f4-200">Par exemple, le <xref:System.Windows.Forms.MonthCalendar> contrôle affiche un mois dans un espace fixe.</span><span class="sxs-lookup"><span data-stu-id="b79f4-200">For example, the <xref:System.Windows.Forms.MonthCalendar> control displays a month in a fixed space.</span></span>

#### <a name="to-host-a-control-that-does-not-stretch"></a><span data-ttu-id="b79f4-201">Pour héberger un contrôle qui ne s’étire pas</span><span class="sxs-lookup"><span data-stu-id="b79f4-201">To host a control that does not stretch</span></span>

1.  <span data-ttu-id="b79f4-202">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-202">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#11](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#11)]

2.  <span data-ttu-id="b79f4-203">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-203">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-204">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément est centré dans la ligne de grille, mais il n’est pas étiré pour remplir l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="b79f4-204">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element is centered in the grid row, but it is not stretched to fill the available space.</span></span> <span data-ttu-id="b79f4-205">Si la fenêtre est suffisamment grande, vous pouvez voir deux mois ou plus affichées par hébergé <xref:System.Windows.Forms.MonthCalendar> contrôle, mais ils sont centrés dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="b79f4-205">If the window is large enough, you may see two or more months displayed by the hosted <xref:System.Windows.Forms.MonthCalendar> control, but these are centered in the row.</span></span> <span data-ttu-id="b79f4-206">Le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] moteur de disposition centre les éléments qui ne peut pas être redimensionnés pour remplir l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="b79f4-206">The [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] layout engine centers elements that cannot be sized to fill the available space.</span></span>

## <a name="scaling"></a><span data-ttu-id="b79f4-207">Mise à l'échelle</span><span class="sxs-lookup"><span data-stu-id="b79f4-207">Scaling</span></span>
 <span data-ttu-id="b79f4-208">Contrairement aux éléments WPF, la plupart des contrôles Windows Forms ne sont pas évolutives en continu.</span><span class="sxs-lookup"><span data-stu-id="b79f4-208">Unlike WPF elements, most Windows Forms controls are not continuously scalable.</span></span> <span data-ttu-id="b79f4-209">Pour fournir la mise à l’échelle personnalisée, vous substituez le <xref:System.Windows.Forms.Integration.WindowsFormsHost.ScaleChild%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="b79f4-209">To provide custom scaling, you override the <xref:System.Windows.Forms.Integration.WindowsFormsHost.ScaleChild%2A?displayProperty=nameWithType> method.</span></span>

#### <a name="to-scale-a-hosted-control-by-using-the-default-behavior"></a><span data-ttu-id="b79f4-210">Pour mettre à l’échelle un contrôle hébergé selon le comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="b79f4-210">To scale a hosted control by using the default behavior</span></span>

1.  <span data-ttu-id="b79f4-211">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-211">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#12](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#12)]

2.  <span data-ttu-id="b79f4-212">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-212">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-213">Le contrôle hébergé et ses éléments voisins sont mis à l’échelle par un facteur de 0,5.</span><span class="sxs-lookup"><span data-stu-id="b79f4-213">The hosted control and its surrounding elements are scaled by a factor of 0.5.</span></span> <span data-ttu-id="b79f4-214">Toutefois, la police du contrôle hébergé n’est pas mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="b79f4-214">However, the hosted control's font is not scaled.</span></span>

<!-- This could use an example of custom scaling. -->

## <a name="rotating"></a><span data-ttu-id="b79f4-215">Rotation</span><span class="sxs-lookup"><span data-stu-id="b79f4-215">Rotating</span></span>
 <span data-ttu-id="b79f4-216">Contrairement aux éléments WPF, les contrôles Windows Forms ne gèrent pas de rotation.</span><span class="sxs-lookup"><span data-stu-id="b79f4-216">Unlike WPF elements, Windows Forms controls do not support rotation.</span></span> <span data-ttu-id="b79f4-217">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément ne pivote pas avec d’autres éléments WPF lorsqu’une transformation de rotation est appliquée.</span><span class="sxs-lookup"><span data-stu-id="b79f4-217">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element does not rotate with other WPF elements when a rotation transformation is applied.</span></span> <span data-ttu-id="b79f4-218">Toute valeur de rotation autre que 180 degrés déclenche le <xref:System.Windows.Forms.Integration.WindowsFormsHost.LayoutError> événement.</span><span class="sxs-lookup"><span data-stu-id="b79f4-218">Any rotation value other than 180 degrees raises the <xref:System.Windows.Forms.Integration.WindowsFormsHost.LayoutError> event.</span></span>

#### <a name="to-see-the-effect-of-rotation-in-a-hybrid-application"></a><span data-ttu-id="b79f4-219">Pour voir l’effet de la rotation dans une application hybride</span><span class="sxs-lookup"><span data-stu-id="b79f4-219">To see the effect of rotation in a hybrid application</span></span>

1.  <span data-ttu-id="b79f4-220">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-220">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#13](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#13)]

2.  <span data-ttu-id="b79f4-221">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-221">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-222">Le contrôle hébergé ne pivote pas, mais ses éléments voisins subissent une rotation de 180 degrés.</span><span class="sxs-lookup"><span data-stu-id="b79f4-222">The hosted control is not rotated, but its surrounding elements are rotated by an angle of 180 degrees.</span></span> <span data-ttu-id="b79f4-223">Vous devrez peut-être redimensionner la fenêtre pour apercevoir les éléments.</span><span class="sxs-lookup"><span data-stu-id="b79f4-223">You may have to resize the window to see the elements.</span></span>

## <a name="setting-padding-and-margins"></a><span data-ttu-id="b79f4-224">Définition d’une marge intérieure et de marges</span><span class="sxs-lookup"><span data-stu-id="b79f4-224">Setting Padding and Margins</span></span>
 <span data-ttu-id="b79f4-225">Marge intérieure et marges dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont semblables aux marge intérieure et marges dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b79f4-225">Padding and margins in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] layout are similar to padding and margins in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span> <span data-ttu-id="b79f4-226">Il suffit de définir la <xref:System.Windows.Controls.Control.Padding%2A> et <xref:System.Windows.FrameworkElement.Margin%2A> propriétés sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-226">Simply set the <xref:System.Windows.Controls.Control.Padding%2A> and <xref:System.Windows.FrameworkElement.Margin%2A> properties on the <xref:System.Windows.Forms.Integration.WindowsFormsHost> element.</span></span>

#### <a name="to-set-padding-and-margins-for-a-hosted-control"></a><span data-ttu-id="b79f4-227">Pour définir la marge intérieure et les marges d’un contrôle hébergé</span><span class="sxs-lookup"><span data-stu-id="b79f4-227">To set padding and margins for a hosted control</span></span>

1.  <span data-ttu-id="b79f4-228">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-228">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#14](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#14)]
    [!code-xaml[WpfLayoutHostingWfWithXaml#15](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#15)]

2.  <span data-ttu-id="b79f4-229">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-229">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-230">Les paramètres de marge intérieure et marges sont appliqués à hébergé [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles de la même façon qu’ils seraient appliqués dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b79f4-230">The padding and margin settings are applied to the hosted [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls in the same way they would be applied in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span>

## <a name="using-dynamic-layout-containers"></a><span data-ttu-id="b79f4-231">Utilisation de conteneurs de disposition dynamiques</span><span class="sxs-lookup"><span data-stu-id="b79f4-231">Using Dynamic Layout Containers</span></span>
 [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] <span data-ttu-id="b79f4-232">fournit deux conteneurs de disposition dynamique, <xref:System.Windows.Forms.FlowLayoutPanel> et <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="b79f4-232">provides two dynamic layout containers, <xref:System.Windows.Forms.FlowLayoutPanel> and <xref:System.Windows.Forms.TableLayoutPanel>.</span></span> <span data-ttu-id="b79f4-233">Vous pouvez également utiliser ces conteneurs dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] dispositions.</span><span class="sxs-lookup"><span data-stu-id="b79f4-233">You can also use these containers in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] layouts.</span></span>

#### <a name="to-use-a-dynamic-layout-container"></a><span data-ttu-id="b79f4-234">Pour utiliser un conteneur de disposition dynamique</span><span class="sxs-lookup"><span data-stu-id="b79f4-234">To use a dynamic layout container</span></span>

1.  <span data-ttu-id="b79f4-235">Copiez le XAML suivant dans le <xref:System.Windows.Controls.Grid> élément.</span><span class="sxs-lookup"><span data-stu-id="b79f4-235">Copy the following XAML into the <xref:System.Windows.Controls.Grid> element.</span></span>

     [!code-xaml[WpfLayoutHostingWfWithXaml#16](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml#16)]

2.  <span data-ttu-id="b79f4-236">Dans MainWindow.xaml.vb ou MainWindow.xaml.cs, copiez le code suivant dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="b79f4-236">In MainWindow.xaml.vb or MainWindow.xaml.cs copy the following code into the class definition.</span></span>

     [!code-csharp[WpfLayoutHostingWfWithXaml#103](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#103)]
     [!code-vb[WpfLayoutHostingWfWithXaml#103](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#103)]

3.  <span data-ttu-id="b79f4-237">Ajoutez un appel à la méthode `InitializeFlowLayoutPanel` dans le constructeur.</span><span class="sxs-lookup"><span data-stu-id="b79f4-237">Add a call to the `InitializeFlowLayoutPanel` method in the constructor.</span></span>

     [!code-csharp[WpfLayoutHostingWfWithXaml#104](~/samples/snippets/csharp/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/CSharp/Window1.xaml.cs#104)]
     [!code-vb[WpfLayoutHostingWfWithXaml#104](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WpfLayoutHostingWfWithXaml/VisualBasic/Window1.xaml.vb#104)]  
  
4.  <span data-ttu-id="b79f4-238">Appuyez sur F5 pour générer et exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="b79f4-238">Press F5 to build and run the application.</span></span> <span data-ttu-id="b79f4-239">Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément remplit la <xref:System.Windows.Controls.DockPanel>, et <xref:System.Windows.Forms.FlowLayoutPanel> réorganise ses contrôles enfants dans la valeur par défaut <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>.</span><span class="sxs-lookup"><span data-stu-id="b79f4-239">The <xref:System.Windows.Forms.Integration.WindowsFormsHost> element fills the <xref:System.Windows.Controls.DockPanel>, and <xref:System.Windows.Forms.FlowLayoutPanel> arranges its child controls in the default <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b79f4-240">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b79f4-240">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="b79f4-241">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b79f4-241">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
- [<span data-ttu-id="b79f4-242">Considérations sur la disposition de l'élément WindowsFormsHost</span><span class="sxs-lookup"><span data-stu-id="b79f4-242">Layout Considerations for the WindowsFormsHost Element</span></span>](layout-considerations-for-the-windowsformshost-element.md)
- [<span data-ttu-id="b79f4-243">Organisation des Windows Forms contrôles dans WPF, exemple</span><span class="sxs-lookup"><span data-stu-id="b79f4-243">Arranging Windows Forms Controls in WPF Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159971)
- [<span data-ttu-id="b79f4-244">Procédure pas à pas : hébergement d’un contrôle composite Windows Forms dans WPF</span><span class="sxs-lookup"><span data-stu-id="b79f4-244">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [<span data-ttu-id="b79f4-245">Procédure pas à pas : hébergement d’un contrôle composite WPF dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b79f4-245">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
