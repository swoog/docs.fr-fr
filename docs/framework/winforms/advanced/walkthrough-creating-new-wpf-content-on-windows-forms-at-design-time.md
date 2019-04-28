---
title: 'Procédure pas à pas : création de contenu WPF dans Windows Forms au moment du design'
ms.date: 08/18/2018
helpviewer_keywords:
- interoperability [Windows Forms], WPF and Windows Forms
- WPF content [Windows Forms], hosting in Windows Forms
- hosting WPF content in Windows Forms
- ElementHost control
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: 2e92d8e8-f0e4-4df7-9f07-2acf35cd798c
ms.openlocfilehash: ed48db399ba47f0e6be96f7bca33d3892b19e433
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61747679"
---
# <a name="walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time"></a><span data-ttu-id="3ede4-102">Procédure pas à pas : création de contenu WPF dans Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="3ede4-102">Walkthrough: Creating New WPF Content on Windows Forms at Design Time</span></span>

<span data-ttu-id="3ede4-103">Cette rubrique montre comment créer un contrôle Windows Presentation Foundation (WPF) pour une utilisation dans vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="3ede4-103">This topic shows you how to create a Windows Presentation Foundation (WPF) control for use in your Windows Forms-based applications.</span></span>

<span data-ttu-id="3ede4-104">Au cours de cette procédure pas à pas, vous allez exécuter les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ede4-104">In this walkthrough, you perform the following tasks:</span></span>

- <span data-ttu-id="3ede4-105">créer le projet ;</span><span class="sxs-lookup"><span data-stu-id="3ede4-105">Create the project.</span></span>

- <span data-ttu-id="3ede4-106">créer un projet WPF ;</span><span class="sxs-lookup"><span data-stu-id="3ede4-106">Create a new WPF control.</span></span>

- <span data-ttu-id="3ede4-107">ajouter le nouveau contrôle WPF à un Windows Form.</span><span class="sxs-lookup"><span data-stu-id="3ede4-107">Add the new WPF control to a Windows Form.</span></span> <span data-ttu-id="3ede4-108">Le contrôle WPF est hébergé dans un contrôle <xref:System.Windows.Forms.Integration.ElementHost>.</span><span class="sxs-lookup"><span data-stu-id="3ede4-108">The WPF control is hosted in an <xref:System.Windows.Forms.Integration.ElementHost> control.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ede4-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3ede4-109">Prerequisites</span></span>

<span data-ttu-id="3ede4-110">Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="3ede4-110">You need the following components to complete this walkthrough:</span></span>

- <span data-ttu-id="3ede4-111">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="3ede4-111">Visual Studio 2017</span></span>

## <a name="creating-the-project"></a><span data-ttu-id="3ede4-112">Création du projet</span><span class="sxs-lookup"><span data-stu-id="3ede4-112">Creating the Project</span></span>

<span data-ttu-id="3ede4-113">La première étape consiste à créer le projet Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="3ede4-113">The first step is to create the Windows Forms project.</span></span> <span data-ttu-id="3ede4-114">Ouvrez Visual Studio et créez un nouveau **Windows Forms App (.NET Framework)** projet dans Visual Basic ou Visual c# nommé `HostingWpf`.</span><span class="sxs-lookup"><span data-stu-id="3ede4-114">Open Visual Studio and create a new **Windows Forms App (.NET Framework)** project in Visual Basic or Visual C# named `HostingWpf`.</span></span>

> [!NOTE]
> <span data-ttu-id="3ede4-115">Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3ede4-115">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>

## <a name="creating-a-new-wpf-control"></a><span data-ttu-id="3ede4-116">Création d'un contrôle WPF</span><span class="sxs-lookup"><span data-stu-id="3ede4-116">Creating a New WPF Control</span></span>

<span data-ttu-id="3ede4-117">La création d'un contrôle WPF et son ajout à votre projet sont des tâches aussi simples que l'ajout de tout autre élément à votre projet.</span><span class="sxs-lookup"><span data-stu-id="3ede4-117">Creating a new WPF control and adding it to your project is as easy as adding any other item to your project.</span></span> <span data-ttu-id="3ede4-118">Le Concepteur de formulaires Windows fonctionne avec un type particulier de contrôle nommé *contrôle composite*, ou *contrôle utilisateur*.</span><span class="sxs-lookup"><span data-stu-id="3ede4-118">The Windows Forms Designer works with a particular kind of control named *composite control*, or *user control*.</span></span> <span data-ttu-id="3ede4-119">Pour plus d'informations sur les contrôles utilisateur WPF, consultez <xref:System.Windows.Controls.UserControl>.</span><span class="sxs-lookup"><span data-stu-id="3ede4-119">For more information about WPF user controls, see <xref:System.Windows.Controls.UserControl>.</span></span>

> [!NOTE]
> <span data-ttu-id="3ede4-120">Le type <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> pour WPF est distinct du type de contrôle utilisateur fourni par Windows Forms, également nommé <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="3ede4-120">The <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> type for WPF is distinct from the user control type provided by Windows Forms, which is also named <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>.</span></span>

### <a name="to-create-a-new-wpf-control"></a><span data-ttu-id="3ede4-121">Pour créer un contrôle WPF</span><span class="sxs-lookup"><span data-stu-id="3ede4-121">To create a new WPF control</span></span>

1. <span data-ttu-id="3ede4-122">Dans **l’Explorateur de solutions**, ajoutez un nouveau **bibliothèque de contrôles utilisateur WPF (.NET Framework)** projet à la solution.</span><span class="sxs-lookup"><span data-stu-id="3ede4-122">In **Solution Explorer**, add a new **WPF User Control Library (.NET Framework)** project to the solution.</span></span> <span data-ttu-id="3ede4-123">Utilisez le nom par défaut pour la bibliothèque de contrôles, `WpfControlLibrary1`.</span><span class="sxs-lookup"><span data-stu-id="3ede4-123">Use the default name for the control library, `WpfControlLibrary1`.</span></span> <span data-ttu-id="3ede4-124">Le nom du contrôle par défaut est `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="3ede4-124">The default control name is `UserControl1.xaml`.</span></span>

     <span data-ttu-id="3ede4-125">Ajout du nouveau contrôle a les effets suivants :</span><span class="sxs-lookup"><span data-stu-id="3ede4-125">Adding the new control has the following effects:</span></span>

    - <span data-ttu-id="3ede4-126">Le fichier UserControl1.xaml est ajouté.</span><span class="sxs-lookup"><span data-stu-id="3ede4-126">File UserControl1.xaml is added.</span></span>

    - <span data-ttu-id="3ede4-127">Le fichier UserControl1.xaml.cs ou UserControl1.xaml.vb est ajouté.</span><span class="sxs-lookup"><span data-stu-id="3ede4-127">Either file UserControl1.xaml.cs or UserControl1.xaml.vb is added.</span></span> <span data-ttu-id="3ede4-128">Ce fichier contient le code-behind pour les gestionnaires d'événements et autre implémentation.</span><span class="sxs-lookup"><span data-stu-id="3ede4-128">This file contains the code-behind for event handlers and other implementation.</span></span>

    - <span data-ttu-id="3ede4-129">Les références aux assemblys WPF sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="3ede4-129">References to WPF assemblies are added.</span></span>

    - <span data-ttu-id="3ede4-130">Le fichier UserControl1.xaml s'ouvre dans le [!INCLUDE[wpfdesigner_current_long](../../../../includes/wpfdesigner-current-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3ede4-130">File UserControl1.xaml opens in the [!INCLUDE[wpfdesigner_current_long](../../../../includes/wpfdesigner-current-long-md.md)].</span></span>

2. <span data-ttu-id="3ede4-131">En mode Design, assurez-vous que `UserControl1` est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3ede4-131">In Design view, make sure that `UserControl1` is selected.</span></span> <span data-ttu-id="3ede4-132">Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="3ede4-132">For more information, see [How to: Select and Move Elements on the Design Surface](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span></span>

3. <span data-ttu-id="3ede4-133">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à **200**.</span><span class="sxs-lookup"><span data-stu-id="3ede4-133">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to **200**.</span></span>

4. <span data-ttu-id="3ede4-134">À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> contrôle sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="3ede4-134">From the **Toolbox**, drag a <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control onto the design surface.</span></span>

5. <span data-ttu-id="3ede4-135">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **le contenu hébergé**.</span><span class="sxs-lookup"><span data-stu-id="3ede4-135">In the **Properties** window, set the value of the <xref:System.Windows.Controls.TextBox.Text%2A> property to **Hosted Content**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ede4-136">En général, vous devez héberger du contenu WPF plus sophistiqué.</span><span class="sxs-lookup"><span data-stu-id="3ede4-136">In general, you should host more sophisticated WPF content.</span></span> <span data-ttu-id="3ede4-137">Le contrôle <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> est utilisé ici uniquement à titre d'illustration.</span><span class="sxs-lookup"><span data-stu-id="3ede4-137">The <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control is used here for illustrative purposes only.</span></span>

6. <span data-ttu-id="3ede4-138">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="3ede4-138">Build the project.</span></span>

## <a name="adding-a-wpf-control-to-a-windows-form"></a><span data-ttu-id="3ede4-139">Ajout d'un contrôle WPF à un Windows Form</span><span class="sxs-lookup"><span data-stu-id="3ede4-139">Adding a WPF Control to a Windows Form</span></span>

<span data-ttu-id="3ede4-140">Votre nouveau contrôle WPF est prêt à être utilisé sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3ede4-140">Your new WPF control is ready for use on the form.</span></span> <span data-ttu-id="3ede4-141">Windows Forms utilise le <xref:System.Windows.Forms.Integration.ElementHost> contrôle pour héberger le contenu WPF.</span><span class="sxs-lookup"><span data-stu-id="3ede4-141">Windows Forms uses the <xref:System.Windows.Forms.Integration.ElementHost> control to host WPF content.</span></span>

### <a name="to-add-a-wpf-control-to-a-windows-form"></a><span data-ttu-id="3ede4-142">Pour ajouter un contrôle WPF à un Windows Form</span><span class="sxs-lookup"><span data-stu-id="3ede4-142">To add a WPF control to a Windows Form</span></span>

1. <span data-ttu-id="3ede4-143">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="3ede4-143">Open `Form1` in the Windows Forms Designer.</span></span>

2. <span data-ttu-id="3ede4-144">Dans le **boîte à outils**, recherchez l’onglet **contrôles utilisateur WPF WPFUserControlLibrary**.</span><span class="sxs-lookup"><span data-stu-id="3ede4-144">In the **Toolbox**, find the tab labeled **WPFUserControlLibrary WPF User Controls**.</span></span>

3. <span data-ttu-id="3ede4-145">Faites glisser une instance de `UserControl1` sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3ede4-145">Drag an instance of `UserControl1` onto the form.</span></span>

    - <span data-ttu-id="3ede4-146">Un contrôle <xref:System.Windows.Forms.Integration.ElementHost> est créé automatiquement sur le formulaire pour héberger le contrôle WPF.</span><span class="sxs-lookup"><span data-stu-id="3ede4-146">An <xref:System.Windows.Forms.Integration.ElementHost> control is created automatically on the form to host the WPF control.</span></span>

    - <span data-ttu-id="3ede4-147">Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle est nommé `elementHost1` et dans le **propriétés** fenêtre, vous pouvez voir son <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> propriété est définie sur **UserControl1**.</span><span class="sxs-lookup"><span data-stu-id="3ede4-147">The <xref:System.Windows.Forms.Integration.ElementHost> control is named `elementHost1` and in the **Properties** window, you can see its <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> property is set to **UserControl1**.</span></span>

    - <span data-ttu-id="3ede4-148">des références aux assemblys WPF sont ajoutées au projet.</span><span class="sxs-lookup"><span data-stu-id="3ede4-148">References to WPF assemblies are added to the project.</span></span>

    - <span data-ttu-id="3ede4-149">Le contrôle `elementHost1` a un panneau de Smart Tags qui affiche les options d’hébergement disponibles.</span><span class="sxs-lookup"><span data-stu-id="3ede4-149">The `elementHost1` control has a smart tag panel that shows the available hosting options.</span></span>

4. <span data-ttu-id="3ede4-150">Dans le **tâches ElementHost** panneau des balises actives, sélectionnez **ancrer dans le conteneur parent**.</span><span class="sxs-lookup"><span data-stu-id="3ede4-150">In the **ElementHost Tasks** smart tag panel, select **Dock in parent container**.</span></span>

5. <span data-ttu-id="3ede4-151">Appuyez sur **F5** pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="3ede4-151">Press **F5** to build and run the application.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3ede4-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3ede4-152">Next Steps</span></span>

<span data-ttu-id="3ede4-153">Windows Forms et WPF sont des technologies différentes, mais elles sont conçues pour interagir étroitement.</span><span class="sxs-lookup"><span data-stu-id="3ede4-153">Windows Forms and WPF are different technologies, but they are designed to interoperate closely.</span></span> <span data-ttu-id="3ede4-154">Pour fournir l’apparence et le comportement dans vos applications plus riches, essayez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="3ede4-154">To provide richer appearance and behavior in your applications, try the following:</span></span>

- <span data-ttu-id="3ede4-155">Hébergez un contrôle Windows Forms dans une page WPF.</span><span class="sxs-lookup"><span data-stu-id="3ede4-155">Host a Windows Forms control in a WPF page.</span></span> <span data-ttu-id="3ede4-156">Pour plus d’informations, consultez [Procédure pas à pas : Hébergement d’un Windows contrôle Forms dans WPF](../../wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="3ede4-156">For more information, see [Walkthrough: Hosting a Windows Forms Control in WPF](../../wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md).</span></span>

- <span data-ttu-id="3ede4-157">Appliquez des styles visuels Windows Forms à votre contenu WPF.</span><span class="sxs-lookup"><span data-stu-id="3ede4-157">Apply Windows Forms visual styles to your WPF content.</span></span> <span data-ttu-id="3ede4-158">Pour plus d'informations, voir [Procédure : Activer des Styles visuels dans une Application hybride](../../wpf/advanced/how-to-enable-visual-styles-in-a-hybrid-application.md).</span><span class="sxs-lookup"><span data-stu-id="3ede4-158">For more information, see [How to: Enable Visual Styles in a Hybrid Application](../../wpf/advanced/how-to-enable-visual-styles-in-a-hybrid-application.md).</span></span>

- <span data-ttu-id="3ede4-159">Modifiez le style de votre contenu WPF.</span><span class="sxs-lookup"><span data-stu-id="3ede4-159">Change the style of your WPF content.</span></span> <span data-ttu-id="3ede4-160">Pour plus d’informations, consultez [Procédure pas à pas : Contenu WPF de style](walkthrough-styling-wpf-content.md).</span><span class="sxs-lookup"><span data-stu-id="3ede4-160">For more information, see [Walkthrough: Styling WPF Content](walkthrough-styling-wpf-content.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ede4-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ede4-161">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="3ede4-162">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="3ede4-162">Migration and Interoperability</span></span>](../../wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="3ede4-163">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="3ede4-163">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="3ede4-164">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ede4-164">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
