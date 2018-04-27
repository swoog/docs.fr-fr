---
title: Créer une application WPF dans Visual Studio
ms.custom: 04/12/2018
ms.prod: .net-framework
ms.technology: dotnet-wpf
ms.topic: conceptual
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting started [WPF], WPF
- WPF [WPF], getting started
ms.assetid: b96bed40-8946-4285-8fe4-88045ab854ed
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: edc7a22a7b108731e08c5d67ef8b8a52e9959ddc
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="walkthrough-my-first-wpf-desktop-application"></a><span data-ttu-id="d5495-102">Procédure pas à pas : ma première application de bureau WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-102">Walkthrough: My first WPF desktop application</span></span>

<span data-ttu-id="d5495-103">Cet article vous explique comment développer une application Windows Presentation Foundation (WPF) simple qui inclut les éléments qui sont communs à la plupart des applications WPF : balisage d’Application XAML Extensible Markup Language (), code-behind, définitions d’application, contrôles, disposition, liaison de données et styles.</span><span class="sxs-lookup"><span data-stu-id="d5495-103">This article shows you how to develop a simple Windows Presentation Foundation (WPF) application that includes the elements that are common to most WPF applications: Extensible Application Markup Language (XAML) markup, code-behind, application definitions, controls, layout, data binding, and styles.</span></span>

<span data-ttu-id="d5495-104">Cette procédure pas à pas inclut les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5495-104">This walkthrough includes the following steps:</span></span>

- <span data-ttu-id="d5495-105">Utiliser XAML pour concevoir l’apparence de l’interface utilisateur de l’application (IU).</span><span class="sxs-lookup"><span data-stu-id="d5495-105">Use XAML to design the appearance of the application's user interface (UI).</span></span>

- <span data-ttu-id="d5495-106">Écrire du code pour générer le comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-106">Write code to build the application's behavior.</span></span>

- <span data-ttu-id="d5495-107">Créer une définition d’application pour gérer l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-107">Create an application definition to manage the application.</span></span>

- <span data-ttu-id="d5495-108">Ajouter des contrôles et créer la disposition pour composer l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-108">Add controls and create the layout to compose the application UI.</span></span>

- <span data-ttu-id="d5495-109">Créer des styles pour une apparence cohérente dans toute l’interface utilisateur d’une application.</span><span class="sxs-lookup"><span data-stu-id="d5495-109">Create styles for a consistent appearance throughout an application's UI.</span></span>

- <span data-ttu-id="d5495-110">Lier l’interface utilisateur aux données pour remplir l’interface utilisateur à partir des données et de conserver les données et l’interface utilisateur synchronisé.</span><span class="sxs-lookup"><span data-stu-id="d5495-110">Bind the UI to data to both populate the UI from data and keep the data and UI synchronized.</span></span>

<span data-ttu-id="d5495-111">À la fin de la procédure pas à pas, vous devez avoir créé une application Windows qui permet aux utilisateurs d’afficher les notes de frais pour certaines personnes autonome.</span><span class="sxs-lookup"><span data-stu-id="d5495-111">By the end of the walkthrough, you'll have built a standalone Windows application that allows users to view expense reports for selected people.</span></span> <span data-ttu-id="d5495-112">L’application est composée de plusieurs pages WPF sont hébergées dans une fenêtre de style navigateur.</span><span class="sxs-lookup"><span data-stu-id="d5495-112">The application is composed of several WPF pages that are hosted in a browser-style window.</span></span>

> [!TIP]
> <span data-ttu-id="d5495-113">L’exemple de code qui est utilisé pour générer cette procédure pas à pas est disponible pour Visual Basic et c# à [Introduction à la génération d’Applications](http://go.microsoft.com/fwlink/?LinkID=160008).</span><span class="sxs-lookup"><span data-stu-id="d5495-113">The sample code that is used to build this walkthrough is available for both Visual Basic and C# at [Introduction to Building WPF Applications](http://go.microsoft.com/fwlink/?LinkID=160008).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d5495-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d5495-114">Prerequisites</span></span>

- <span data-ttu-id="d5495-115">Visual Studio 2012 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d5495-115">Visual Studio 2012 or later</span></span>

<span data-ttu-id="d5495-116">Pour plus d’informations sur l’installation de la dernière version de Visual Studio, consultez [installer Visual Studio](/visualstudio/install/install-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="d5495-116">For more information about installing the latest version of Visual Studio, see [Install Visual Studio](/visualstudio/install/install-visual-studio).</span></span>

## <a name="create-the-application-project"></a><span data-ttu-id="d5495-117">Créer le projet d’application</span><span class="sxs-lookup"><span data-stu-id="d5495-117">Create the application project</span></span>

<span data-ttu-id="d5495-118">La première étape consiste à créer l’infrastructure d’application, qui inclut une définition d’application, deux pages et une image.</span><span class="sxs-lookup"><span data-stu-id="d5495-118">The first step is to create the application infrastructure, which includes an application definition, two pages, and an image.</span></span>

1. <span data-ttu-id="d5495-119">Créer un nouveau projet d’Application WPF dans Visual Basic ou Visual c# nommé **ExpenseIt**:</span><span class="sxs-lookup"><span data-stu-id="d5495-119">Create a new WPF Application project in Visual Basic or Visual C# named **ExpenseIt**:</span></span>

   1. <span data-ttu-id="d5495-120">Ouvrez Visual Studio et sélectionnez **fichier** > **nouveau** > **projet**.</span><span class="sxs-lookup"><span data-stu-id="d5495-120">Open Visual Studio and select **File** > **New** > **Project**.</span></span>

      <span data-ttu-id="d5495-121">Le **nouveau projet** boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="d5495-121">The **New Project** dialog opens.</span></span>

   2. <span data-ttu-id="d5495-122">Sous le **installé** catégorie, développez le **Visual C#** ou **Visual Basic** nœud, puis sélectionnez **bureau classique de Windows**.</span><span class="sxs-lookup"><span data-stu-id="d5495-122">Under the **Installed** category, expand either the **Visual C#** or **Visual Basic** node, and then select **Windows Classic Desktop**.</span></span>

   3. <span data-ttu-id="d5495-123">Sélectionnez le **l’application WPF (.NET Framework)** modèle.</span><span class="sxs-lookup"><span data-stu-id="d5495-123">Select the **WPF App (.NET Framework)** template.</span></span> <span data-ttu-id="d5495-124">Entrez le nom **ExpenseIt** , puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5495-124">Enter the name **ExpenseIt** and then select **OK**.</span></span>

      ![Boîte de dialogue Nouveau projet avec une application WPF sélectionnée](media/new-project-dialog.png)

      <span data-ttu-id="d5495-126">Visual Studio crée le projet et ouvre le concepteur pour la fenêtre d’application par défaut nommé **MainWindow.xaml**.</span><span class="sxs-lookup"><span data-stu-id="d5495-126">Visual Studio creates the project and opens the designer for the default application window named **MainWindow.xaml**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d5495-127">Cette procédure pas à pas utilise le <xref:System.Windows.Controls.DataGrid> contrôle qui est disponible dans le .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d5495-127">This walkthrough uses the <xref:System.Windows.Controls.DataGrid> control that is available in the .NET Framework 4 and later.</span></span> <span data-ttu-id="d5495-128">Être sûr que votre projet cible le .NET Framework 4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d5495-128">Be sure that your project targets the .NET Framework 4 or later.</span></span> <span data-ttu-id="d5495-129">Pour plus d’informations, consultez [Guide pratique pour cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span><span class="sxs-lookup"><span data-stu-id="d5495-129">For more information, see [How to: Target a Version of the .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span></span>

2. <span data-ttu-id="d5495-130">Ouvrez *Application.xaml* (Visual Basic) ou *App.xaml* (c#).</span><span class="sxs-lookup"><span data-stu-id="d5495-130">Open *Application.xaml* (Visual Basic) or *App.xaml* (C#).</span></span>

    <span data-ttu-id="d5495-131">Ce fichier XAML définit une application WPF et toutes les ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-131">This XAML file defines a WPF application and any application resources.</span></span> <span data-ttu-id="d5495-132">Vous utilisez également ce fichier pour spécifier l’interface utilisateur qui s’affiche automatiquement quand l’application démarre ; Dans ce cas, *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-132">You also use this file to specify the UI that automatically shows when the application starts; in this case, *MainWindow.xaml*.</span></span>

    <span data-ttu-id="d5495-133">En Visual Basic, votre code XAML doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-133">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#1_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/Application.xaml#1_a)]

    <span data-ttu-id="d5495-134">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="d5495-134">Or like this in C#:</span></span>

    [!code-xaml[ExpenseIt#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/App.xaml#1)]

3. <span data-ttu-id="d5495-135">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-135">Open *MainWindow.xaml*.</span></span>

    <span data-ttu-id="d5495-136">Ce fichier XAML est la fenêtre principale de votre application et affiche le contenu créé dans les pages.</span><span class="sxs-lookup"><span data-stu-id="d5495-136">This XAML file is the main window of your application and displays content created in pages.</span></span> <span data-ttu-id="d5495-137">La <xref:System.Windows.Window> classe définit les propriétés d’une fenêtre, telles que son titre, la taille ou icône et gère les événements, tels que la fermeture ou le masquage.</span><span class="sxs-lookup"><span data-stu-id="d5495-137">The <xref:System.Windows.Window> class defines the properties of a window, such as its title, size, or icon, and handles events, such as closing or hiding.</span></span>

4. <span data-ttu-id="d5495-138">Modifier la <xref:System.Windows.Window> élément à un <xref:System.Windows.Navigation.NavigationWindow>, comme illustré dans le code XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="d5495-138">Change the <xref:System.Windows.Window> element to a <xref:System.Windows.Navigation.NavigationWindow>, as shown in the following XAML:</span></span>

   ```xaml
   <NavigationWindow x:Class="ExpenseIt.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        ...
   </NavigationWindow>
   ```

   <span data-ttu-id="d5495-139">Cette application accède à un contenu différent en fonction de l’entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5495-139">This app navigates to different content depending on the user input.</span></span> <span data-ttu-id="d5495-140">C’est pourquoi le principal <xref:System.Windows.Window> doit être remplacé par un <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="d5495-140">This is why the main <xref:System.Windows.Window> needs to be changed to a <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="d5495-141"><xref:System.Windows.Navigation.NavigationWindow> hérite de toutes les propriétés de <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="d5495-141"><xref:System.Windows.Navigation.NavigationWindow> inherits all the properties of <xref:System.Windows.Window>.</span></span> <span data-ttu-id="d5495-142">Le <xref:System.Windows.Navigation.NavigationWindow> élément dans le fichier XAML crée une instance de la <xref:System.Windows.Navigation.NavigationWindow> classe.</span><span class="sxs-lookup"><span data-stu-id="d5495-142">The <xref:System.Windows.Navigation.NavigationWindow> element in the XAML file creates an instance of the <xref:System.Windows.Navigation.NavigationWindow> class.</span></span> <span data-ttu-id="d5495-143">Pour plus d’informations, consultez [vue d’ensemble de la Navigation](../../../../docs/framework/wpf/app-development/navigation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-143">For more information, see [Navigation overview](../../../../docs/framework/wpf/app-development/navigation-overview.md).</span></span>

5. <span data-ttu-id="d5495-144">Modifiez les propriétés suivantes sur le <xref:System.Windows.Navigation.NavigationWindow> élément :</span><span class="sxs-lookup"><span data-stu-id="d5495-144">Change the following properties on the <xref:System.Windows.Navigation.NavigationWindow> element:</span></span>

    - <span data-ttu-id="d5495-145">Définir le <xref:System.Windows.Window.Title%2A> propriété « ExpenseIt ».</span><span class="sxs-lookup"><span data-stu-id="d5495-145">Set the <xref:System.Windows.Window.Title%2A> property to "ExpenseIt".</span></span>

    - <span data-ttu-id="d5495-146">Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété 500 pixels.</span><span class="sxs-lookup"><span data-stu-id="d5495-146">Set the <xref:System.Windows.FrameworkElement.Width%2A> property to 500 pixels.</span></span>

    - <span data-ttu-id="d5495-147">Définir le <xref:System.Windows.FrameworkElement.Height%2A> propriété à 350 pixels.</span><span class="sxs-lookup"><span data-stu-id="d5495-147">Set the <xref:System.Windows.FrameworkElement.Height%2A> property to 350 pixels.</span></span>

    - <span data-ttu-id="d5495-148">Supprimer le <xref:System.Windows.Controls.Grid> éléments entre les <xref:System.Windows.Navigation.NavigationWindow> balises.</span><span class="sxs-lookup"><span data-stu-id="d5495-148">Remove the <xref:System.Windows.Controls.Grid> elements between the <xref:System.Windows.Navigation.NavigationWindow> tags.</span></span>

    <span data-ttu-id="d5495-149">En Visual Basic, votre code XAML doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-149">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#2_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt/MainWindow.xaml#2_a)]

    <span data-ttu-id="d5495-150">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="d5495-150">Or like this in C#:</span></span>

    [!code-xaml[ExpenseIt#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml#2)]

6. <span data-ttu-id="d5495-151">Ouvrez *MainWindow.xaml.vb* ou *MainWindow.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="d5495-151">Open *MainWindow.xaml.vb* or *MainWindow.xaml.cs*.</span></span>

    <span data-ttu-id="d5495-152">Ce fichier est un fichier code-behind qui contient le code pour gérer les événements déclarés dans *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-152">This file is a code-behind file that contains code to handle the events declared in *MainWindow.xaml*.</span></span> <span data-ttu-id="d5495-153">Ce fichier contient une classe partielle pour la fenêtre définie en XAML.</span><span class="sxs-lookup"><span data-stu-id="d5495-153">This file contains a partial class for the window defined in XAML.</span></span>

7. <span data-ttu-id="d5495-154">Si vous utilisez c#, modifiez le `MainWindow` classe à dériver de <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="d5495-154">If you are using C#, change the `MainWindow` class to derive from <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="d5495-155">(En Visual Basic, cela se produit automatiquement lorsque vous modifiez la fenêtre en XAML.)</span><span class="sxs-lookup"><span data-stu-id="d5495-155">(In Visual Basic, this happens automatically when you change the window in XAML.)</span></span>

   <span data-ttu-id="d5495-156">Votre code doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-156">Your code should look like this:</span></span>

   [!code-csharp[ExpenseIt#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml.cs#3)]
   [!code-vb[ExpenseIt#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml.vb#3)]

   > [!TIP]
   > <span data-ttu-id="d5495-157">Vous pouvez activer ou désactiver le langage de code de l’exemple de code entre c# et Visual Basic dans la **langage** liste déroulante dans le coin supérieur droit de cet article.</span><span class="sxs-lookup"><span data-stu-id="d5495-157">You can toggle the code language of the sample code between C# and Visual Basic in the **Language** drop-down on the upper right side of this article.</span></span>

## <a name="add-files-to-the-application"></a><span data-ttu-id="d5495-158">Ajouter des fichiers à l’application</span><span class="sxs-lookup"><span data-stu-id="d5495-158">Add files to the application</span></span>

<span data-ttu-id="d5495-159">Dans cette section, vous allez ajouter deux pages et une image à l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-159">In this section, you'll add two pages and an image to the application.</span></span>

1. <span data-ttu-id="d5495-160">Ajouter une nouvelle page WPF au projet et nommez-le *ExpenseItHome.xaml*:</span><span class="sxs-lookup"><span data-stu-id="d5495-160">Add a new WPF page to the project, and name it *ExpenseItHome.xaml*:</span></span>

   1. <span data-ttu-id="d5495-161">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **ExpenseIt** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="d5495-161">In **Solution Explorer**, right-click on the **ExpenseIt** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="d5495-162">Dans le **ajouter un nouvel élément** boîte de dialogue, la **Page (WPF)** modèle est déjà sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d5495-162">In the **Add New Item** dialog, the **Page (WPF)** template is already selected.</span></span> <span data-ttu-id="d5495-163">Entrez le nom **ExpenseItHome**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d5495-163">Enter the name **ExpenseItHome**, and then select **Add**.</span></span>

    <span data-ttu-id="d5495-164">Cette page est la première page qui s’affiche lorsque l’application est lancée.</span><span class="sxs-lookup"><span data-stu-id="d5495-164">This page is the first page that's displayed when the application is launched.</span></span> <span data-ttu-id="d5495-165">Il affiche une liste de personnes, pour afficher une note de frais.</span><span class="sxs-lookup"><span data-stu-id="d5495-165">It will show a list of people to select from, to show an expense report for.</span></span>

2. <span data-ttu-id="d5495-166">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-166">Open *ExpenseItHome.xaml*.</span></span>

3. <span data-ttu-id="d5495-167">Définir le <xref:System.Windows.Controls.Page.Title%2A> à « ExpenseIt - Home ».</span><span class="sxs-lookup"><span data-stu-id="d5495-167">Set the <xref:System.Windows.Controls.Page.Title%2A> to "ExpenseIt - Home".</span></span>

    <span data-ttu-id="d5495-168">En Visual Basic, votre code XAML doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-168">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#6_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml#6_a)]

    <span data-ttu-id="d5495-169">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="d5495-169">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml#6)]

4. <span data-ttu-id="d5495-170">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-170">Open *MainWindow.xaml*.</span></span>

5. <span data-ttu-id="d5495-171">Définir le <xref:System.Windows.Navigation.NavigationWindow.Source%2A> propriété sur le <xref:System.Windows.Navigation.NavigationWindow> à « ExpenseItHome.xaml ».</span><span class="sxs-lookup"><span data-stu-id="d5495-171">Set the <xref:System.Windows.Navigation.NavigationWindow.Source%2A> property on the <xref:System.Windows.Navigation.NavigationWindow> to "ExpenseItHome.xaml".</span></span>

    <span data-ttu-id="d5495-172">*ExpenseItHome.xaml* est alors la première page ouverte au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-172">This sets *ExpenseItHome.xaml* to be the first page opened when the application starts.</span></span> <span data-ttu-id="d5495-173">En Visual Basic, votre code XAML doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-173">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#7_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml#7_a)]

    <span data-ttu-id="d5495-174">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="d5495-174">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/MainWindow.xaml#7)]

   > [!TIP]
   > <span data-ttu-id="d5495-175">Vous pouvez également définir le **Source** propriété dans le **divers** catégorie de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d5495-175">You can also set the **Source** property in the **Miscellaneous** category of the **Properties** window.</span></span>
   >
   > ![Propriété source dans la fenêtre Propriétés](media/properties-source.png)

6. <span data-ttu-id="d5495-177">Ajouter une autre nouvelle page WPF au projet et nommez-le *ExpenseReportPage.xaml*::</span><span class="sxs-lookup"><span data-stu-id="d5495-177">Add another new WPF page to the project, and name it *ExpenseReportPage.xaml*::</span></span>

   1. <span data-ttu-id="d5495-178">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **ExpenseIt** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="d5495-178">In **Solution Explorer**, right-click on the **ExpenseIt** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="d5495-179">Dans le **ajouter un nouvel élément** boîte de dialogue, la **Page (WPF)** modèle est déjà sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d5495-179">In the **Add New Item** dialog, the **Page (WPF)** template is already selected.</span></span> <span data-ttu-id="d5495-180">Entrez le nom **ExpenseReportPage**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d5495-180">Enter the name **ExpenseReportPage**, and then select **Add**.</span></span>

    <span data-ttu-id="d5495-181">Cette page affiche la note de frais pour la personne qui est sélectionnée dans le **ExpenseItHome** page.</span><span class="sxs-lookup"><span data-stu-id="d5495-181">This page will show the expense report for the person that is selected on the **ExpenseItHome** page.</span></span>

7. <span data-ttu-id="d5495-182">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-182">Open *ExpenseReportPage.xaml*.</span></span>

8. <span data-ttu-id="d5495-183">Définir le <xref:System.Windows.Controls.Page.Title%2A> à « ExpenseIt - View Expense ».</span><span class="sxs-lookup"><span data-stu-id="d5495-183">Set the <xref:System.Windows.Controls.Page.Title%2A> to "ExpenseIt - View Expense".</span></span>

    <span data-ttu-id="d5495-184">En Visual Basic, votre code XAML doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-184">Your XAML should look like this in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#4_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml#4_a)]

    <span data-ttu-id="d5495-185">Ou à cela en C# :</span><span class="sxs-lookup"><span data-stu-id="d5495-185">Or this in C#:</span></span>

    [!code-xaml[ExpenseIt#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml#4)]

9. <span data-ttu-id="d5495-186">Ouvrez *ExpenseItHome.xaml.vb* et *ExpenseReportPage.xaml.vb*, ou *ExpenseItHome.xaml.cs* et *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="d5495-186">Open *ExpenseItHome.xaml.vb* and *ExpenseReportPage.xaml.vb*, or *ExpenseItHome.xaml.cs* and *ExpenseReportPage.xaml.cs*.</span></span>

    <span data-ttu-id="d5495-187">Lorsque vous créez un nouveau fichier de Page, Visual Studio crée automatiquement un *code-behind* fichier.</span><span class="sxs-lookup"><span data-stu-id="d5495-187">When you create a new Page file, Visual Studio automatically creates a *code-behind* file.</span></span> <span data-ttu-id="d5495-188">Ces fichiers code-behind gèrent la logique pour répondre à une saisie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5495-188">These code-behind files handle the logic for responding to user input.</span></span>

    <span data-ttu-id="d5495-189">Votre code doit ressembler à ceci pour **ExpenseItHome**:</span><span class="sxs-lookup"><span data-stu-id="d5495-189">Your code should look like this for **ExpenseItHome**:</span></span>

    [!code-csharp[ExpenseIt#2_5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml.cs#2_5)]
    [!code-vb[ExpenseIt#2_5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml.vb#2_5)]

    <span data-ttu-id="d5495-190">Et comme suit pour **ExpenseReport**:</span><span class="sxs-lookup"><span data-stu-id="d5495-190">And like this for **ExpenseReport**:</span></span>

    [!code-csharp[ExpenseIt#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml.cs#5)]
    [!code-vb[ExpenseIt#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml.vb#5)]

10. <span data-ttu-id="d5495-191">Ajouter une image nommée *watermark.png* au projet.</span><span class="sxs-lookup"><span data-stu-id="d5495-191">Add an image named *watermark.png* to the project.</span></span> <span data-ttu-id="d5495-192">Vous pouvez créer votre propre image, copiez le fichier à partir de l’exemple de code ou l’obtenir [ici](https://github.com/dotnet/docs/blob/master/docs/framework/wpf/getting-started/media/watermark.png).</span><span class="sxs-lookup"><span data-stu-id="d5495-192">You can create your own image, copy the file from the sample code, or get it [here](https://github.com/dotnet/docs/blob/master/docs/framework/wpf/getting-started/media/watermark.png).</span></span>

   1. <span data-ttu-id="d5495-193">Avec le bouton droit sur le nœud du projet et sélectionnez **ajouter** > **élément existant**, ou appuyez sur **MAJ**+**Alt** + **A**.</span><span class="sxs-lookup"><span data-stu-id="d5495-193">Right-click on the project node and select **Add** > **Existing Item**, or press **Shift**+**Alt**+**A**.</span></span>

   2. <span data-ttu-id="d5495-194">Dans le **ajouter un élément existant** boîte de dialogue, cliquez sur Parcourir pour le fichier image que vous souhaitez utiliser, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d5495-194">In the **Add Existing Item** dialog, browse to the image file you want to use, and then select **Add**.</span></span>

## <a name="build-and-run-the-application"></a><span data-ttu-id="d5495-195">Générez et exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="d5495-195">Build and run the application</span></span>

1. <span data-ttu-id="d5495-196">Pour générer et exécuter l’application, appuyez sur **F5** ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu.</span><span class="sxs-lookup"><span data-stu-id="d5495-196">To build and run the application, press **F5** or select **Start Debugging** from the **Debug** menu.</span></span>

    <span data-ttu-id="d5495-197">L’illustration suivante montre l’application avec le <xref:System.Windows.Navigation.NavigationWindow> boutons :</span><span class="sxs-lookup"><span data-stu-id="d5495-197">The following illustration shows the application with the <xref:System.Windows.Navigation.NavigationWindow> buttons:</span></span>

    ![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure1.png)

2. <span data-ttu-id="d5495-199">Fermez l’application pour revenir à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d5495-199">Close the application to return to Visual Studio.</span></span>

## <a name="create-the-layout"></a><span data-ttu-id="d5495-200">Créer la disposition</span><span class="sxs-lookup"><span data-stu-id="d5495-200">Create the layout</span></span>

<span data-ttu-id="d5495-201">Mise en page fournit de placer les éléments d’interface utilisateur de manière ordonnée et gère également la taille et la position de ces éléments à une interface utilisateur est redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="d5495-201">Layout provides an ordered way to place UI elements, and also manages the size and position of those elements when a UI is resized.</span></span> <span data-ttu-id="d5495-202">En règle générale, vous allez créer une disposition avec l’un des contrôles de disposition suivants :</span><span class="sxs-lookup"><span data-stu-id="d5495-202">You typically create a layout with one of the following layout controls:</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.VirtualizingStackPanel>
- <xref:System.Windows.Controls.WrapPanel>

<span data-ttu-id="d5495-203">Chacun de ces contrôles de disposition prend en charge un type spécial de disposition pour ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d5495-203">Each of these layout controls supports a special type of layout for its child elements.</span></span> <span data-ttu-id="d5495-204">Les pages ExpenseIt peuvent être redimensionnées et chaque page comporte des éléments organisés horizontalement et verticalement en même temps que d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="d5495-204">ExpenseIt pages can be resized, and each page has elements that are arranged horizontally and vertically alongside other elements.</span></span> <span data-ttu-id="d5495-205">Par conséquent, le <xref:System.Windows.Controls.Grid> est l’élément de disposition idéal pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-205">Consequently, the <xref:System.Windows.Controls.Grid> is the ideal layout element for the application.</span></span>

> [!TIP]
> <span data-ttu-id="d5495-206">Pour plus d’informations sur <xref:System.Windows.Controls.Panel> éléments, consultez [vue d’ensemble des panneaux](../../../../docs/framework/wpf/controls/panels-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-206">For more information about <xref:System.Windows.Controls.Panel> elements, see [Panels overview](../../../../docs/framework/wpf/controls/panels-overview.md).</span></span> <span data-ttu-id="d5495-207">Pour plus d’informations sur la mise en page, consultez [disposition](../../../../docs/framework/wpf/advanced/layout.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-207">For more information about layout, see [Layout](../../../../docs/framework/wpf/advanced/layout.md).</span></span>

<span data-ttu-id="d5495-208">Dans la section, vous créez une seule colonne de table avec trois lignes et une marge de 10 pixels en ajoutant des définitions de colonne et de ligne à la <xref:System.Windows.Controls.Grid> dans *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-208">In the section, you create a single-column table with three rows and a 10-pixel margin by adding column and row definitions to the <xref:System.Windows.Controls.Grid> in *ExpenseItHome.xaml*.</span></span>

1. <span data-ttu-id="d5495-209">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-209">Open *ExpenseItHome.xaml*.</span></span>

2. <span data-ttu-id="d5495-210">Définir le <xref:System.Windows.FrameworkElement.Margin%2A> propriété sur le <xref:System.Windows.Controls.Grid> élément à la valeur « 10,0,10,10 » qui correspond aux marges gauche, haut, droite et bas :</span><span class="sxs-lookup"><span data-stu-id="d5495-210">Set the <xref:System.Windows.FrameworkElement.Margin%2A> property on the <xref:System.Windows.Controls.Grid> element to "10,0,10,10", which corresponds to left, top, right and bottom margins:</span></span>

   ```xaml
   <Grid Margin="10,0,10,10">
   ```

   > [!TIP]
   > <span data-ttu-id="d5495-211">Vous pouvez également définir le **marge** des valeurs dans le **propriétés** fenêtre, sous le **disposition** catégorie :</span><span class="sxs-lookup"><span data-stu-id="d5495-211">You can also set the **Margin** values in the **Properties** window, under the **Layout** category:</span></span>
   >
   > ![Valeurs des marges dans la fenêtre Propriétés](media/properties-margin.png)

3. <span data-ttu-id="d5495-213">Ajoutez le code XAML suivant entre les <xref:System.Windows.Controls.Grid> balises pour créer les définitions de ligne et de colonne :</span><span class="sxs-lookup"><span data-stu-id="d5495-213">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags to create the row and column definitions:</span></span>

    [!code-xaml[ExpenseIt#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#8)]

    <span data-ttu-id="d5495-214">Le <xref:System.Windows.Controls.RowDefinition.Height%2A> de deux lignes est définie sur <xref:System.Windows.GridLength.Auto%2A>, ce qui signifie que les lignes sont d’une taille de base sur le contenu dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="d5495-214">The <xref:System.Windows.Controls.RowDefinition.Height%2A> of two rows is set to <xref:System.Windows.GridLength.Auto%2A>, which means that the rows are sized base on the content in the rows.</span></span> <span data-ttu-id="d5495-215">La valeur par défaut <xref:System.Windows.Controls.RowDefinition.Height%2A> est <xref:System.Windows.GridUnitType.Star> dimensionnement, ce qui signifie que la hauteur de ligne est une proportion pondérée de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="d5495-215">The default <xref:System.Windows.Controls.RowDefinition.Height%2A> is <xref:System.Windows.GridUnitType.Star> sizing, which means that the row height is a weighted proportion of the available space.</span></span> <span data-ttu-id="d5495-216">Par exemple, si deux lignes ont une <xref:System.Windows.Controls.RowDefinition.Height%2A> de « \* », ils ont chacun une hauteur qui représente la moitié de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="d5495-216">For example if two rows each have a <xref:System.Windows.Controls.RowDefinition.Height%2A> of "\*", they each have a height that is half of the available space.</span></span>

    <span data-ttu-id="d5495-217">Votre <xref:System.Windows.Controls.Grid> doit maintenant ressembler au code XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="d5495-217">Your <xref:System.Windows.Controls.Grid> should now look like the following XAML:</span></span>

    [!code-xaml[ExpenseIt#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#9)]

## <a name="add-controls"></a><span data-ttu-id="d5495-218">Ajouter des contrôles</span><span class="sxs-lookup"><span data-stu-id="d5495-218">Add controls</span></span>

<span data-ttu-id="d5495-219">Dans cette section, vous allez mettre à jour l’interface utilisateur pour afficher une liste des personnes un utilisateur peut sélectionner pour afficher la note de frais pour la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="d5495-219">In this section, you'll update the home page UI to show a list of people that a user can select from to show the expense report for.</span></span> <span data-ttu-id="d5495-220">Les contrôles sont des objets d’interface utilisateur qui permettent aux utilisateurs d’interagir avec votre application.</span><span class="sxs-lookup"><span data-stu-id="d5495-220">Controls are UI objects that allow users to interact with your application.</span></span> <span data-ttu-id="d5495-221">Pour plus d’informations, consultez [Contrôles](../../../../docs/framework/wpf/controls/index.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-221">For more information, see [Controls](../../../../docs/framework/wpf/controls/index.md).</span></span>

<span data-ttu-id="d5495-222">Pour créer cette interface utilisateur, vous allez ajouter les éléments suivants pour *ExpenseItHome.xaml*:</span><span class="sxs-lookup"><span data-stu-id="d5495-222">To create this UI, you'll add the following elements to *ExpenseItHome.xaml*:</span></span>

- <span data-ttu-id="d5495-223"><xref:System.Windows.Controls.ListBox> (pour la liste des personnes).</span><span class="sxs-lookup"><span data-stu-id="d5495-223"><xref:System.Windows.Controls.ListBox> (for the list of people).</span></span>
- <span data-ttu-id="d5495-224"><xref:System.Windows.Controls.Label> (pour l’en-tête de liste).</span><span class="sxs-lookup"><span data-stu-id="d5495-224"><xref:System.Windows.Controls.Label> (for the list header).</span></span>
- <span data-ttu-id="d5495-225"><xref:System.Windows.Controls.Button> (pour cliquez pour afficher la note de frais pour la personne qui est sélectionnée dans la liste).</span><span class="sxs-lookup"><span data-stu-id="d5495-225"><xref:System.Windows.Controls.Button> (to click to view the expense report for the person that is selected in the list).</span></span>

<span data-ttu-id="d5495-226">Chaque contrôle est placé dans une ligne de la <xref:System.Windows.Controls.Grid> en définissant le <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> propriété jointe.</span><span class="sxs-lookup"><span data-stu-id="d5495-226">Each control is placed in a row of the <xref:System.Windows.Controls.Grid> by setting the <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> attached property.</span></span> <span data-ttu-id="d5495-227">Pour plus d’informations sur les propriétés jointes, consultez [joint la vue d’ensemble des propriétés](../../../../docs/framework/wpf/advanced/attached-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-227">For more information about attached properties, see [Attached Properties Overview](../../../../docs/framework/wpf/advanced/attached-properties-overview.md).</span></span>

1. <span data-ttu-id="d5495-228">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-228">Open *ExpenseItHome.xaml*.</span></span>

2. <span data-ttu-id="d5495-229">Ajoutez le code XAML suivant quelque part entre le <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="d5495-229">Add the following XAML somewhere between the <xref:System.Windows.Controls.Grid> tags:</span></span>

   [!code-xaml[ExpenseIt#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt4/ExpenseItHome.xaml#10)]

   > [!TIP]
   > <span data-ttu-id="d5495-230">Vous pouvez également créer les contrôles en les faisant glisser à partir de la **boîte à outils** fenêtre sur la fenêtre de conception, puis en définissant leurs propriétés le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d5495-230">You can also create the controls by dragging them from the **Toolbox** window onto the design window, and then setting their properties in the **Properties** window.</span></span>

3. <span data-ttu-id="d5495-231">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-231">Build and run the application.</span></span>

<span data-ttu-id="d5495-232">L’illustration suivante montre les contrôles que vous venez de créer :</span><span class="sxs-lookup"><span data-stu-id="d5495-232">The following illustration shows the controls you just created:</span></span>

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure2.png)

## <a name="add-an-image-and-a-title"></a><span data-ttu-id="d5495-234">Ajouter une image et un titre</span><span class="sxs-lookup"><span data-stu-id="d5495-234">Add an image and a title</span></span>

<span data-ttu-id="d5495-235">Dans cette section, vous allez mettre à jour l’interface utilisateur de la page d’accueil avec une image et un titre de page.</span><span class="sxs-lookup"><span data-stu-id="d5495-235">In this section, you'll update the home page UI with an image and a page title.</span></span>

1. <span data-ttu-id="d5495-236">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-236">Open *ExpenseItHome.xaml*.</span></span>

2. <span data-ttu-id="d5495-237">Ajouter une colonne à la <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> fixe <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de 230 pixels :</span><span class="sxs-lookup"><span data-stu-id="d5495-237">Add another column to the <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> with a fixed <xref:System.Windows.Controls.ColumnDefinition.Width%2A> of 230 pixels:</span></span>

    [!code-xaml[ExpenseIt#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11)]

3. <span data-ttu-id="d5495-238">Ajouter une autre ligne pour le <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, pour un total de quatre lignes :</span><span class="sxs-lookup"><span data-stu-id="d5495-238">Add another row to the <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, for a total of four rows:</span></span>

    [!code-xaml[ExpenseIt#11b](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11b)]

4. <span data-ttu-id="d5495-239">Déplacer les contrôles vers la deuxième colonne en définissant le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété 1 dans chacun des trois contrôles (bordure, zone de liste et bouton).</span><span class="sxs-lookup"><span data-stu-id="d5495-239">Move the controls to the second column by setting the <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> property to 1 in each of the three controls (Border, ListBox, and Button).</span></span>

5. <span data-ttu-id="d5495-240">Déplacez chaque contrôle d’une ligne, vers le bas en incrémentant son <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> valeur par 1.</span><span class="sxs-lookup"><span data-stu-id="d5495-240">Move each control down a row, by incrementing its <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> value by 1.</span></span>

   <span data-ttu-id="d5495-241">Le code XAML pour les trois contrôles ressemble maintenant à ceci :</span><span class="sxs-lookup"><span data-stu-id="d5495-241">The XAML for the three controls now looks like this:</span></span>

    [!code-xaml[ExpenseIt#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#12)]

6. <span data-ttu-id="d5495-242">Définir le <xref:System.Windows.Controls.Panel.Background%2A> de la <xref:System.Windows.Controls.Grid> pour être le *watermark.png* fichier image, en ajoutant le code XAML suivant quelque part entre le `<Grid>` et `<\/Grid>` balises :</span><span class="sxs-lookup"><span data-stu-id="d5495-242">Set the <xref:System.Windows.Controls.Panel.Background%2A> of the <xref:System.Windows.Controls.Grid> to be the *watermark.png* image file, by adding the following XAML somewhere between the `<Grid>` and `<\/Grid>` tags:</span></span>

    [!code-xaml[ExpenseIt#14](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#14)]

7. <span data-ttu-id="d5495-243">Avant du <xref:System.Windows.Controls.Border> élément, ajouter un <xref:System.Windows.Controls.Label> avec le contenu « View Expense Report ».</span><span class="sxs-lookup"><span data-stu-id="d5495-243">Before the <xref:System.Windows.Controls.Border> element, add a <xref:System.Windows.Controls.Label> with the content "View Expense Report".</span></span> <span data-ttu-id="d5495-244">Il s’agit du titre de la page.</span><span class="sxs-lookup"><span data-stu-id="d5495-244">This is the title of the page.</span></span>

    [!code-xaml[ExpenseIt#13](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#13)]

8. <span data-ttu-id="d5495-245">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-245">Build and run the application.</span></span>

<span data-ttu-id="d5495-246">L’illustration suivante montre les résultats de ce que vous venez d’ajouter :</span><span class="sxs-lookup"><span data-stu-id="d5495-246">The following illustration shows the results of what you just added:</span></span>

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure3.png)

## <a name="add-code-to-handle-events"></a><span data-ttu-id="d5495-248">Ajoutez du code pour gérer les événements</span><span class="sxs-lookup"><span data-stu-id="d5495-248">Add code to handle events</span></span>

1. <span data-ttu-id="d5495-249">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-249">Open *ExpenseItHome.xaml*.</span></span>

2. <span data-ttu-id="d5495-250">Ajouter un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements à la <xref:System.Windows.Controls.Button> élément.</span><span class="sxs-lookup"><span data-stu-id="d5495-250">Add a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to the <xref:System.Windows.Controls.Button> element.</span></span> <span data-ttu-id="d5495-251">Pour plus d’informations, consultez [Comment : créer un gestionnaire d’événements simple](http://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).</span><span class="sxs-lookup"><span data-stu-id="d5495-251">For more information, see [How to: Create a simple event handler](http://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).</span></span>

    [!code-xaml[ExpenseIt#15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml#15)]

3. <span data-ttu-id="d5495-252">Ouvrez *ExpenseItHome.xaml.vb* ou *ExpenseItHome.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="d5495-252">Open *ExpenseItHome.xaml.vb* or *ExpenseItHome.xaml.cs*.</span></span>

4. <span data-ttu-id="d5495-253">Ajoutez le code suivant à la `ExpenseItHome` classe pour ajouter un bouton Gestionnaire d’événements click.</span><span class="sxs-lookup"><span data-stu-id="d5495-253">Add the following code to the `ExpenseItHome` class to add a button click event handler.</span></span> <span data-ttu-id="d5495-254">Le Gestionnaire d’événements ouvre le **ExpenseReportPage** page.</span><span class="sxs-lookup"><span data-stu-id="d5495-254">The event handler opens the **ExpenseReportPage** page.</span></span>

    [!code-csharp[ExpenseIt#16](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml.cs#16)]
    [!code-vb[ExpenseIt#16](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt6/ExpenseItHome.xaml.vb#16)]

## <a name="create-the-ui-for-expensereportpage"></a><span data-ttu-id="d5495-255">Créer l’interface utilisateur pour ExpenseReportPage</span><span class="sxs-lookup"><span data-stu-id="d5495-255">Create the UI for ExpenseReportPage</span></span>

<span data-ttu-id="d5495-256">*ExpenseReportPage.xaml* affiche la note de frais de la personne qui est sélectionnée dans le **ExpenseItHome** page.</span><span class="sxs-lookup"><span data-stu-id="d5495-256">*ExpenseReportPage.xaml* displays the expense report for the person that's selected on the **ExpenseItHome** page.</span></span> <span data-ttu-id="d5495-257">Dans cette section, vous allez les contrôles et créer l’interface utilisateur pour **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="d5495-257">In this section, you'll controls and create the UI for **ExpenseReportPage**.</span></span> <span data-ttu-id="d5495-258">Vous allez également ajouter en arrière-plan et couleurs aux divers éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5495-258">You'll also add background and fill colors to the various UI elements.</span></span>

1. <span data-ttu-id="d5495-259">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-259">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="d5495-260">Ajoutez le code XAML suivant entre les <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="d5495-260">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags:</span></span>

    [!code-xaml[ExpenseIt#17](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseReportPage.xaml#17)]

    <span data-ttu-id="d5495-261">Cette interface utilisateur est similaire à *ExpenseItHome.xaml*, sauf les données du rapport s’affiche dans un <xref:System.Windows.Controls.DataGrid>.</span><span class="sxs-lookup"><span data-stu-id="d5495-261">This UI is similar to *ExpenseItHome.xaml*, except the report data is displayed in a <xref:System.Windows.Controls.DataGrid>.</span></span>

3. <span data-ttu-id="d5495-262">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-262">Build and run the application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5495-263">Si vous obtenez une erreur qui le <xref:System.Windows.Controls.DataGrid> est introuvable ou n’existe pas, assurez-vous que votre projet cible le .NET Framework 4 ou version ultérieur.</span><span class="sxs-lookup"><span data-stu-id="d5495-263">If you get an error that the <xref:System.Windows.Controls.DataGrid> was not found or does not exist, make sure that your project targets the .NET Framework 4 or later.</span></span> <span data-ttu-id="d5495-264">Pour plus d’informations, consultez [Guide pratique pour cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span><span class="sxs-lookup"><span data-stu-id="d5495-264">For more information, see [How to: Target a Version of the .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).</span></span>

4. <span data-ttu-id="d5495-265">Sélectionnez le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="d5495-265">Select the **View** button.</span></span>

    <span data-ttu-id="d5495-266">La page de note de frais s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d5495-266">The expense report page appears.</span></span> <span data-ttu-id="d5495-267">Notez également que le bouton de navigation précédent est activé.</span><span class="sxs-lookup"><span data-stu-id="d5495-267">Also notice that the back navigation button is enabled.</span></span>

<span data-ttu-id="d5495-268">L’illustration suivante montre les éléments d’interface utilisateur ajoutés à *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-268">The following illustration shows the UI elements added to *ExpenseReportPage.xaml*.</span></span>

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure4.png)

## <a name="style-controls"></a><span data-ttu-id="d5495-270">Contrôles de style</span><span class="sxs-lookup"><span data-stu-id="d5495-270">Style controls</span></span>

<span data-ttu-id="d5495-271">L’apparence des différents éléments est souvent le même pour tous les éléments du même type dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5495-271">The appearance of various elements is often the same for all elements of the same type in a UI.</span></span> <span data-ttu-id="d5495-272">Interface utilisateur utilise [styles](../../../../docs/framework/wpf/controls/styling-and-templating.md) pour permettre la réutilisation des apparences dans plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="d5495-272">UI uses [styles](../../../../docs/framework/wpf/controls/styling-and-templating.md) to make appearances reusable across multiple elements.</span></span> <span data-ttu-id="d5495-273">La réutilisation des styles permet de simplifier la gestion et création de XAML.</span><span class="sxs-lookup"><span data-stu-id="d5495-273">The reusability of styles helps to simplify XAML creation and management.</span></span> <span data-ttu-id="d5495-274">Cette section remplace par des styles les attributs d’élément qui ont été définis lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="d5495-274">This section replaces the per-element attributes that were defined in previous steps with styles.</span></span>

1. <span data-ttu-id="d5495-275">Ouvrez *Application.xaml* ou *App.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-275">Open *Application.xaml* or *App.xaml*.</span></span>

2. <span data-ttu-id="d5495-276">Ajoutez le code XAML suivant entre les <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> balises :</span><span class="sxs-lookup"><span data-stu-id="d5495-276">Add the following XAML between the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> tags:</span></span>

    [!code-xaml[ExpenseIt#18](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/App.xaml#18)]

    <span data-ttu-id="d5495-277">Ce code XAML ajoute les styles suivants :</span><span class="sxs-lookup"><span data-stu-id="d5495-277">This XAML adds the following styles:</span></span>

    - <span data-ttu-id="d5495-278">`headerTextStyle`: pour mettre en forme le titre de la page <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="d5495-278">`headerTextStyle`: To format the page title <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="d5495-279">`labelStyle`: pour mettre en forme les contrôles <xref:System.Windows.Controls.Label> .</span><span class="sxs-lookup"><span data-stu-id="d5495-279">`labelStyle`: To format the <xref:System.Windows.Controls.Label> controls.</span></span>

    - <span data-ttu-id="d5495-280">`columnHeaderStyle`: pour mettre en forme <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span><span class="sxs-lookup"><span data-stu-id="d5495-280">`columnHeaderStyle`: To format the <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span></span>

    - <span data-ttu-id="d5495-281">`listHeaderStyle`: pour mettre en forme les contrôles <xref:System.Windows.Controls.Border> de l’en-tête de liste.</span><span class="sxs-lookup"><span data-stu-id="d5495-281">`listHeaderStyle`: To format the list header <xref:System.Windows.Controls.Border> controls.</span></span>

    - <span data-ttu-id="d5495-282">`listHeaderTextStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="d5495-282">`listHeaderTextStyle`: To format the list header <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="d5495-283">`buttonStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Button> sur ExpenseItHome.xaml.</span><span class="sxs-lookup"><span data-stu-id="d5495-283">`buttonStyle`: To format the <xref:System.Windows.Controls.Button> on ExpenseItHome.xaml.</span></span>

    <span data-ttu-id="d5495-284">Notez que les styles sont des ressources et des enfants de le <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> élément de propriété.</span><span class="sxs-lookup"><span data-stu-id="d5495-284">Notice that the styles are resources and children of the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> property element.</span></span> <span data-ttu-id="d5495-285">À cet emplacement, les styles sont appliqués à tous les éléments d’une application.</span><span class="sxs-lookup"><span data-stu-id="d5495-285">In this location, the styles are applied to all the elements in an application.</span></span> <span data-ttu-id="d5495-286">Pour obtenir un exemple d’utilisation des ressources dans une application .NET Framework, consultez [utiliser les ressources](../../../../docs/framework/wpf/advanced/how-to-use-application-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-286">For an example of using resources in a .NET Framework application, see [Use Application Resources](../../../../docs/framework/wpf/advanced/how-to-use-application-resources.md).</span></span>

3. <span data-ttu-id="d5495-287">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-287">Open *ExpenseItHome.xaml*.</span></span>

4. <span data-ttu-id="d5495-288">Remplacez tout le contenu entre les <xref:System.Windows.Controls.Grid> éléments avec le code XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="d5495-288">Replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#19](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseItHome.xaml#19)]

    <span data-ttu-id="d5495-289">Les propriétés qui définissent l’apparence de chaque contrôle, comme <xref:System.Windows.VerticalAlignment> et <xref:System.Windows.Media.FontFamily> , sont supprimées et remplacées lors de l’application de styles.</span><span class="sxs-lookup"><span data-stu-id="d5495-289">The properties such as <xref:System.Windows.VerticalAlignment> and <xref:System.Windows.Media.FontFamily> that define the look of each control are removed and replaced by applying the styles.</span></span> <span data-ttu-id="d5495-290">Par exemple, le `headerTextStyle` est appliqué à la « View Expense Report » <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="d5495-290">For example, the `headerTextStyle` is applied to the "View Expense Report" <xref:System.Windows.Controls.Label>.</span></span>

5. <span data-ttu-id="d5495-291">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-291">Open *ExpenseReportPage.xaml*.</span></span>

6. <span data-ttu-id="d5495-292">Remplacez tout le contenu entre les <xref:System.Windows.Controls.Grid> éléments avec le code XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="d5495-292">Replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#20](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseReportPage.xaml#20)]

    <span data-ttu-id="d5495-293">Des styles sont ajoutés aux éléments <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Border> .</span><span class="sxs-lookup"><span data-stu-id="d5495-293">This adds styles to the <xref:System.Windows.Controls.Label> and <xref:System.Windows.Controls.Border> elements.</span></span>

## <a name="bind-data-to-a-control"></a><span data-ttu-id="d5495-294">Lier des données à un contrôle</span><span class="sxs-lookup"><span data-stu-id="d5495-294">Bind data to a control</span></span>

<span data-ttu-id="d5495-295">Dans cette section, vous allez créer les données XML qui sont liées aux différents contrôles.</span><span class="sxs-lookup"><span data-stu-id="d5495-295">In this section, you'll create the XML data that is bound to various controls.</span></span>

1. <span data-ttu-id="d5495-296">Ouvrez *ExpenseItHome.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-296">Open *ExpenseItHome.xaml*.</span></span>

2. <span data-ttu-id="d5495-297">Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez le code XAML suivant pour créer un <xref:System.Windows.Data.XmlDataProvider> qui contient les données pour chaque personne :</span><span class="sxs-lookup"><span data-stu-id="d5495-297">After the opening <xref:System.Windows.Controls.Grid> element, add the following XAML to create an <xref:System.Windows.Data.XmlDataProvider> that contains the data for each person:</span></span>

    [!code-xaml[ExpenseIt#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#23](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#23)]
    [!code-xaml[ExpenseIt#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    <span data-ttu-id="d5495-298">Les données sont créées en tant qu’un <xref:System.Windows.Controls.Grid> ressource.</span><span class="sxs-lookup"><span data-stu-id="d5495-298">The data is created as a <xref:System.Windows.Controls.Grid> resource.</span></span> <span data-ttu-id="d5495-299">Les données sont normalement chargées en tant que fichier, mais pour des raisons pratiques, elles sont ajoutées inline.</span><span class="sxs-lookup"><span data-stu-id="d5495-299">Normally this would be loaded as a file, but for simplicity the data is added inline.</span></span>

3. <span data-ttu-id="d5495-300">Dans le `<Grid.Resources>` élément, ajoutez le code suivant <xref:System.Windows.DataTemplate>, qui définit comment afficher les données dans le <xref:System.Windows.Controls.ListBox>:</span><span class="sxs-lookup"><span data-stu-id="d5495-300">Within the `<Grid.Resources>` element, add the following <xref:System.Windows.DataTemplate>, which defines how to display the data in the <xref:System.Windows.Controls.ListBox>:</span></span>

    [!code-xaml[ExpenseIt#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#24](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#24)]
    [!code-xaml[ExpenseIt#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    <span data-ttu-id="d5495-301">Pour plus d’informations sur les modèles de données, consultez [vue d’ensemble des modèles de données](../../../../docs/framework/wpf/data/data-templating-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-301">For more information about data templates, see [Data templating overview](../../../../docs/framework/wpf/data/data-templating-overview.md).</span></span>

4. <span data-ttu-id="d5495-302">Remplacer la <xref:System.Windows.Controls.ListBox> avec le code XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="d5495-302">Replace the existing <xref:System.Windows.Controls.ListBox> with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#25](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#25)]

    <span data-ttu-id="d5495-303">Ce code XAML lie le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la source de données et applique le modèle de données en tant que le <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span><span class="sxs-lookup"><span data-stu-id="d5495-303">This XAML binds the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.ListBox> to the data source and applies the data template as the <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span></span>

## <a name="connect-data-to-controls"></a><span data-ttu-id="d5495-304">Connecter des données aux contrôles</span><span class="sxs-lookup"><span data-stu-id="d5495-304">Connect data to controls</span></span>

<span data-ttu-id="d5495-305">Ensuite, vous ajouterez du code pour récupérer le nom qui est sélectionné dans le **ExpenseItHome** page et le passer au constructeur de **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="d5495-305">Next, you'll add code to retrieve the name that's selected on the **ExpenseItHome** page and pass it to the constructor of **ExpenseReportPage**.</span></span> <span data-ttu-id="d5495-306">**ExpenseReportPage** définit son contexte de données avec l’élément passé, qui est définie par les contrôles dans *ExpenseReportPage.xaml* lier.</span><span class="sxs-lookup"><span data-stu-id="d5495-306">**ExpenseReportPage** sets its data context with the passed item, which is what the controls defined in *ExpenseReportPage.xaml* bind to.</span></span>

1. <span data-ttu-id="d5495-307">Ouvrez *ExpenseReportPage.xaml.vb* ou *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="d5495-307">Open *ExpenseReportPage.xaml.vb* or *ExpenseReportPage.xaml.cs*.</span></span>

2. <span data-ttu-id="d5495-308">Ajoutez un constructeur qui prend un objet de façon à pouvoir transmettre les données de note de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d5495-308">Add a constructor that takes an object so you can pass the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#26](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseReportPage.xaml.cs#26)]
    [!code-vb[ExpenseIt#26](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseReportPage.xaml.vb#26)]

3. <span data-ttu-id="d5495-309">Ouvrez *ExpenseItHome.xaml.vb* ou *ExpenseItHome.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="d5495-309">Open *ExpenseItHome.xaml.vb* or *ExpenseItHome.xaml.cs*.</span></span>

4. <span data-ttu-id="d5495-310">Modifier la <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements pour appeler le constructeur de nouveau en passant les données de rapport de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d5495-310">Change the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to call the new constructor passing the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#27](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml.cs#27)]
    [!code-vb[ExpenseIt#27](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseItHome.xaml.vb#27)]

## <a name="style-data-with-data-templates"></a><span data-ttu-id="d5495-311">Données de style avec les modèles de données</span><span class="sxs-lookup"><span data-stu-id="d5495-311">Style data with data templates</span></span>

<span data-ttu-id="d5495-312">Dans cette section, vous allez mettre à jour l’interface utilisateur pour chaque élément dans les listes liées aux données à l’aide de modèles de données.</span><span class="sxs-lookup"><span data-stu-id="d5495-312">In this section, you'll update the UI for each item in the data-bound lists by using data templates.</span></span>

1. <span data-ttu-id="d5495-313">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="d5495-313">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="d5495-314">Lier le contenu de la « Nom » et « Département » <xref:System.Windows.Controls.Label> éléments pour les données appropriées de propriété source.</span><span class="sxs-lookup"><span data-stu-id="d5495-314">Bind the content of the "Name" and "Department" <xref:System.Windows.Controls.Label> elements to the appropriate data source property.</span></span> <span data-ttu-id="d5495-315">Pour plus d’informations sur la liaison de données, consultez [vue d’ensemble de liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5495-315">For more information about data binding, see [Data binding overview](../../../../docs/framework/wpf/data/data-binding-overview.md).</span></span>

    [!code-xaml[ExpenseIt#31](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#31)]

3. <span data-ttu-id="d5495-316">Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajouter les modèles de données suivants, qui définissent comment afficher les données de rapport de frais :</span><span class="sxs-lookup"><span data-stu-id="d5495-316">After the opening <xref:System.Windows.Controls.Grid> element, add the following data templates, which define how to display the expense report data:</span></span>

    [!code-xaml[ExpenseIt#30](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#30)]

4. <span data-ttu-id="d5495-317">Appliquer les modèles à la <xref:System.Windows.Controls.DataGrid> rapporter des données de colonnes qui affichent la dépense.</span><span class="sxs-lookup"><span data-stu-id="d5495-317">Apply the templates to the <xref:System.Windows.Controls.DataGrid> columns that display the expense report data.</span></span>

    [!code-xaml[ExpenseIt#32](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#32)]

5. <span data-ttu-id="d5495-318">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="d5495-318">Build and run the application.</span></span>

6. <span data-ttu-id="d5495-319">Sélectionnez une personne, puis sélectionnez le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="d5495-319">Select a person and then select the **View** button.</span></span>

<span data-ttu-id="d5495-320">L’illustration suivante montre les deux pages de l’application ExpenseIt avec les contrôles, disposition, les styles, la liaison de données et modèles de données appliqués :</span><span class="sxs-lookup"><span data-stu-id="d5495-320">The following illustration shows both pages of the ExpenseIt application with controls, layout, styles, data binding, and data templates applied:</span></span>

![Captures d’écran, exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure5.png)

> [!NOTE]
> <span data-ttu-id="d5495-322">Cet exemple présente une fonctionnalité spécifique de WPF et ne suit pas toutes les meilleures pratiques pour les éléments tels que la sécurité, localisation et l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="d5495-322">This sample demonstrates a specific feature of WPF and doesn't follow all best practices for things like security, localization, and accessibility.</span></span> <span data-ttu-id="d5495-323">Pour une couverture complète de WPF et les .NET Framework application meilleures pratiques de développement, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5495-323">For comprehensive coverage of WPF and the .NET Framework application development best practices, see the following topics:</span></span>
>
> - [<span data-ttu-id="d5495-324">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="d5495-324">Accessibility</span></span>](../../../../docs/framework/ui-automation/accessibility-best-practices.md)
>
> - [<span data-ttu-id="d5495-325">Sécurité</span><span class="sxs-lookup"><span data-stu-id="d5495-325">Security</span></span>](../../../../docs/framework/wpf/security-wpf.md)
>
> - [<span data-ttu-id="d5495-326">Localisation et globalisation de WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-326">WPF globalization and localization</span></span>](../../../../docs/framework/wpf/advanced/wpf-globalization-and-localization-overview.md)
>
> - [<span data-ttu-id="d5495-327">Performances de WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-327">WPF performance</span></span>](../../../../docs/framework/wpf/advanced/optimizing-wpf-application-performance.md)

## <a name="next-steps"></a><span data-ttu-id="d5495-328">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d5495-328">Next steps</span></span>

<span data-ttu-id="d5495-329">Dans cette procédure pas à pas, vous avez appris un certain nombre de techniques pour la création d’une interface utilisateur à l’aide de Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="d5495-329">In this walkthrough you learned a number of techniques for creating a UI using Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="d5495-330">Vous devez maintenant avoir une compréhension de base des blocs de construction d’une application .NET Framework de liaison de données.</span><span class="sxs-lookup"><span data-stu-id="d5495-330">You should now have a basic understanding of the building blocks of a data-bound, .NET Framework application.</span></span> <span data-ttu-id="d5495-331">Pour plus d’informations sur les modèles d’architecture et de programmation WPF, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5495-331">For more information about the WPF architecture and programming models, see the following topics:</span></span>

- [<span data-ttu-id="d5495-332">Architecture de WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-332">WPF architecture</span></span>](../../../../docs/framework/wpf/advanced/wpf-architecture.md)
- [<span data-ttu-id="d5495-333">Vue d’ensemble XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="d5495-333">XAML overview (WPF)</span></span>](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
- [<span data-ttu-id="d5495-334">Vue d’ensemble des propriétés de dépendance</span><span class="sxs-lookup"><span data-stu-id="d5495-334">Dependency properties overview</span></span>](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md)
- [<span data-ttu-id="d5495-335">Disposition</span><span class="sxs-lookup"><span data-stu-id="d5495-335">Layout</span></span>](../../../../docs/framework/wpf/advanced/layout.md)

<span data-ttu-id="d5495-336">Pour plus d’informations sur la création d’applications, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5495-336">For more information about creating applications, see the following topics:</span></span>

- [<span data-ttu-id="d5495-337">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="d5495-337">Application development</span></span>](../../../../docs/framework/wpf/app-development/index.md)
- [<span data-ttu-id="d5495-338">Contrôles</span><span class="sxs-lookup"><span data-stu-id="d5495-338">Controls</span></span>](../../../../docs/framework/wpf/controls/index.md)
- [<span data-ttu-id="d5495-339">Vue d’ensemble de liaison de données</span><span class="sxs-lookup"><span data-stu-id="d5495-339">Data binding overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="d5495-340">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="d5495-340">Graphics and multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [<span data-ttu-id="d5495-341">Documents dans WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-341">Documents in WPF</span></span>](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)

## <a name="see-also"></a><span data-ttu-id="d5495-342">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5495-342">See also</span></span>

- [<span data-ttu-id="d5495-343">Vue d’ensemble des panneaux</span><span class="sxs-lookup"><span data-stu-id="d5495-343">Panels overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
- [<span data-ttu-id="d5495-344">Vue d’ensemble des modèles de données</span><span class="sxs-lookup"><span data-stu-id="d5495-344">Data templating overview</span></span>](../../../../docs/framework/wpf/data/data-templating-overview.md)
- [<span data-ttu-id="d5495-345">Générer une application WPF</span><span class="sxs-lookup"><span data-stu-id="d5495-345">Build a WPF application</span></span>](../../../../docs/framework/wpf/app-development/building-a-wpf-application-wpf.md)
- [<span data-ttu-id="d5495-346">Styles et modèles</span><span class="sxs-lookup"><span data-stu-id="d5495-346">Styles and templates</span></span>](../../../../docs/framework/wpf/controls/styles-and-templates.md)
