---
title: 'Procédure pas à pas : Hébergement d’un contrôle Composite 3-d WPF dans les Windows Forms'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosting WPF content in Windows Forms [WPF]
- composite controls [WPF], hosting WPF in
ms.assetid: 486369a9-606a-4a3b-b086-a06f2119c7b0
ms.openlocfilehash: d32b98fce3cf5e4fe82745c3d0ba8992ee75339e
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56746203"
---
# <a name="walkthrough-hosting-a-3-d-wpf-composite-control-in-windows-forms"></a><span data-ttu-id="01a2c-102">Procédure pas à pas : Hébergement d’un contrôle Composite 3-d WPF dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01a2c-102">Walkthrough: Hosting a 3-D WPF Composite Control in Windows Forms</span></span>

<span data-ttu-id="01a2c-103">Cette procédure pas à pas montre comment vous pouvez créer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] composite contrôler et l’héberger dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles et formulaires à l’aide de la <xref:System.Windows.Forms.Integration.ElementHost> contrôle.</span><span class="sxs-lookup"><span data-stu-id="01a2c-103">This walkthrough demonstrates how you can create a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] composite control and host it in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls and forms by using the <xref:System.Windows.Forms.Integration.ElementHost> control.</span></span>

<span data-ttu-id="01a2c-104">Dans cette procédure pas à pas, vous allez implémenter un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> qui contient deux contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="01a2c-104">In this walkthrough, you will implement a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> that contains two child controls.</span></span> <span data-ttu-id="01a2c-105">Le <xref:System.Windows.Controls.UserControl> affiche un cône tridimensionnel (3D).</span><span class="sxs-lookup"><span data-stu-id="01a2c-105">The <xref:System.Windows.Controls.UserControl> displays a three-dimensional (3-D) cone.</span></span> <span data-ttu-id="01a2c-106">Le rendu d’objets 3D est beaucoup plus facile avec le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] qu’avec [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span><span class="sxs-lookup"><span data-stu-id="01a2c-106">Rendering 3-D objects is much easier with the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] than with [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span> <span data-ttu-id="01a2c-107">Par conséquent, il est judicieux pour héberger un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> classe pour créer des graphiques 3D dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span><span class="sxs-lookup"><span data-stu-id="01a2c-107">Therefore, it makes sense to host a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> class to create 3-D graphics in [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].</span></span>

<span data-ttu-id="01a2c-108">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="01a2c-108">Tasks illustrated in this walkthrough include:</span></span>

-   <span data-ttu-id="01a2c-109">Création de la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span><span class="sxs-lookup"><span data-stu-id="01a2c-109">Creating the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span></span>

-   <span data-ttu-id="01a2c-110">Création du projet hôte Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="01a2c-110">Creating the Windows Forms host project.</span></span>

-   <span data-ttu-id="01a2c-111">Hébergement du [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span><span class="sxs-lookup"><span data-stu-id="01a2c-111">Hosting the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01a2c-112">Prérequis</span><span class="sxs-lookup"><span data-stu-id="01a2c-112">Prerequisites</span></span>

<span data-ttu-id="01a2c-113">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="01a2c-113">You need the following components to complete this walkthrough:</span></span>

-   <span data-ttu-id="01a2c-114">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="01a2c-114">Visual Studio 2017</span></span>

<a name="To_Create_the_UserControl"></a>
## <a name="create-the-usercontrol"></a><span data-ttu-id="01a2c-115">Créer le UserControl</span><span class="sxs-lookup"><span data-stu-id="01a2c-115">Create the UserControl</span></span>

1.  <span data-ttu-id="01a2c-116">Créer un **bibliothèque de contrôles utilisateur WPF** projet nommé `HostingWpfUserControlInWf`.</span><span class="sxs-lookup"><span data-stu-id="01a2c-116">Create a **WPF User Control Library** project named `HostingWpfUserControlInWf`.</span></span>

2.  <span data-ttu-id="01a2c-117">Ouvrez UserControl1.xaml dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="01a2c-117">Open UserControl1.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>

3.  <span data-ttu-id="01a2c-118">Remplacez le code généré par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="01a2c-118">Replace the generated code with the following code:</span></span>

     [!code-xaml[HostingWpfUserControlInWf#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/HostingWpfUserControlInWf/ConeControl.xaml#1)]

     <span data-ttu-id="01a2c-119">Ce code définit un <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> qui contient deux contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="01a2c-119">This code defines a <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> that contains two child controls.</span></span> <span data-ttu-id="01a2c-120">Le premier contrôle enfant est un <xref:System.Windows.Controls.Label?displayProperty=nameWithType> contrôle ; le second est un <xref:System.Windows.Controls.Viewport3D> contrôle qui affiche un cône 3D.</span><span class="sxs-lookup"><span data-stu-id="01a2c-120">The first child control is a <xref:System.Windows.Controls.Label?displayProperty=nameWithType> control; the second is a <xref:System.Windows.Controls.Viewport3D> control that displays a 3-D cone.</span></span>

<a name="To_Create_the_Windows_Forms_Host_Project"></a>
## <a name="create-the-host-project"></a><span data-ttu-id="01a2c-121">Créer le projet hôte</span><span class="sxs-lookup"><span data-stu-id="01a2c-121">Create the host project</span></span>

1.  <span data-ttu-id="01a2c-122">Ajouter un **application WPF (.NET Framework)** projet nommé `WpfUserControlHost` à la solution.</span><span class="sxs-lookup"><span data-stu-id="01a2c-122">Add a **WPF App (.NET Framework)** project named `WpfUserControlHost` to the solution.</span></span> <span data-ttu-id="01a2c-123">Pour plus d’informations, consultez [Procédure pas à pas : Ma première application de bureau WPF](../getting-started/walkthrough-my-first-wpf-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="01a2c-123">For more information, see [Walkthrough: My first WPF desktop application](../getting-started/walkthrough-my-first-wpf-desktop-application.md).</span></span>

2.  <span data-ttu-id="01a2c-124">Dans **l’Explorateur de solutions**, ajoutez une référence à l’assembly WindowsFormsIntegration, nommé WindowsFormsIntegration.dll.</span><span class="sxs-lookup"><span data-stu-id="01a2c-124">In **Solution Explorer**, add a reference to the WindowsFormsIntegration assembly, which is named WindowsFormsIntegration.dll.</span></span>

3.  <span data-ttu-id="01a2c-125">Ajouter des références à ce qui suit [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblys :</span><span class="sxs-lookup"><span data-stu-id="01a2c-125">Add references to the following [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblies:</span></span>

    -   <span data-ttu-id="01a2c-126">PresentationCore</span><span class="sxs-lookup"><span data-stu-id="01a2c-126">PresentationCore</span></span>

    -   <span data-ttu-id="01a2c-127">PresentationFramework</span><span class="sxs-lookup"><span data-stu-id="01a2c-127">PresentationFramework</span></span>

    -   <span data-ttu-id="01a2c-128">WindowsBase</span><span class="sxs-lookup"><span data-stu-id="01a2c-128">WindowsBase</span></span>

4.  <span data-ttu-id="01a2c-129">Ajoutez au projet une référence à `HostingWpfUserControlInWf`.</span><span class="sxs-lookup"><span data-stu-id="01a2c-129">Add a reference to the `HostingWpfUserControlInWf` project.</span></span>

5.  <span data-ttu-id="01a2c-130">Dans l’Explorateur de solutions, définissez le `WpfUserControlHost` projet comme projet de démarrage.</span><span class="sxs-lookup"><span data-stu-id="01a2c-130">In Solution Explorer, set the `WpfUserControlHost` project to be the startup project.</span></span>

<a name="To_Host_the_Windows_Presentation_Foundation"></a>
## <a name="host-the-usercontrol"></a><span data-ttu-id="01a2c-131">Héberger le contrôle utilisateur</span><span class="sxs-lookup"><span data-stu-id="01a2c-131">Host the UserControl</span></span>

1.  <span data-ttu-id="01a2c-132">Dans le Concepteur de formulaires Windows, ouvrez Form1.</span><span class="sxs-lookup"><span data-stu-id="01a2c-132">In the Windows Forms Designer, open Form1.</span></span>

2.  <span data-ttu-id="01a2c-133">Dans la fenêtre Propriétés, cliquez sur **événements**, puis double-cliquez sur le <xref:System.Windows.Forms.Form.Load> événement pour créer un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="01a2c-133">In the Properties window, click **Events**, and then double-click the <xref:System.Windows.Forms.Form.Load> event to create an event handler.</span></span>

     <span data-ttu-id="01a2c-134">Ouvre l’éditeur de Code nouvellement généré `Form1_Load` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="01a2c-134">The Code Editor opens to the newly generated `Form1_Load` event handler.</span></span>

3.  <span data-ttu-id="01a2c-135">Remplacez le code dans Form1.cs par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="01a2c-135">Replace the code in Form1.cs with the following code.</span></span>

     <span data-ttu-id="01a2c-136">Le `Form1_Load` Gestionnaire d’événements crée une instance de `UserControl1` et ajoute ses le <xref:System.Windows.Forms.Integration.ElementHost> collection de contrôles enfants du contrôle.</span><span class="sxs-lookup"><span data-stu-id="01a2c-136">The `Form1_Load` event handler creates an instance of `UserControl1` and adds itto the <xref:System.Windows.Forms.Integration.ElementHost> control's collection of child controls.</span></span> <span data-ttu-id="01a2c-137">Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle est ajouté à la collection du formulaire des contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="01a2c-137">The <xref:System.Windows.Forms.Integration.ElementHost> control is added to the form's collection of child controls.</span></span>

     [!code-csharp[HostingWpfUserControlInWf#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/WpfUserControlHost/Form1.cs#10)]
     [!code-vb[HostingWpfUserControlInWf#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWpfUserControlInWf/VisualBasic/WpfUserControlHost/Form1.vb#10)]

4.  <span data-ttu-id="01a2c-138">Appuyez sur **F5** pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="01a2c-138">Press **F5** to build and run the application.</span></span>

## <a name="see-also"></a><span data-ttu-id="01a2c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01a2c-139">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="01a2c-140">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01a2c-140">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
- [<span data-ttu-id="01a2c-141">Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="01a2c-141">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
- [<span data-ttu-id="01a2c-142">Procédure pas à pas : Hébergement d’un contrôle Composite de formulaires Windows dans WPF</span><span class="sxs-lookup"><span data-stu-id="01a2c-142">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [<span data-ttu-id="01a2c-143">Hébergement d’un contrôle Composite WPF dans Windows Forms, exemple</span><span class="sxs-lookup"><span data-stu-id="01a2c-143">Hosting a WPF Composite Control in Windows Forms Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=160001)