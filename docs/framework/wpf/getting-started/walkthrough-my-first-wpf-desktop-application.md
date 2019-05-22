---
title: Créer une application WPF dans Visual Studio
ms.date: 03/20/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting started [WPF], WPF
- WPF [WPF], getting started
ms.assetid: b96bed40-8946-4285-8fe4-88045ab854ed
author: mairaw
ms.author: mairaw
ms.custom: vs-dotnet
ms.openlocfilehash: c3440ddf6cdae6b24bcf1059ab2c76d8fb957263
ms.sourcegitcommit: 11deacc8ec9f229ab8ee3cd537515d4c2826515f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2019
ms.locfileid: "66003862"
---
# <a name="walkthrough-my-first-wpf-desktop-application"></a><span data-ttu-id="7a601-102">Procédure pas à pas : Ma première application de bureau WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-102">Walkthrough: My first WPF desktop application</span></span>

<span data-ttu-id="7a601-103">Cet article vous explique comment développer une application de bureau Windows Presentation Foundation (WPF) qui inclut les éléments qui sont communes à la plupart des applications WPF : Extensible Application Markup Language (XAML) balisage, code-behind, définitions d’application, contrôles, disposition, liaison de données et styles.</span><span class="sxs-lookup"><span data-stu-id="7a601-103">This article shows you how to develop a Windows Presentation Foundation (WPF) desktop application that includes the elements that are common to most WPF applications: Extensible Application Markup Language (XAML) markup, code-behind, application definitions, controls, layout, data binding, and styles.</span></span> <span data-ttu-id="7a601-104">Pour développer l’application, vous allez utiliser Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7a601-104">To develop the application, you'll use Visual Studio.</span></span> 

<span data-ttu-id="7a601-105">Cette procédure pas à pas comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a601-105">This walkthrough includes the following steps:</span></span>

- <span data-ttu-id="7a601-106">XAML permet de concevoir l’apparence de l’interface utilisateur de l’application (IU).</span><span class="sxs-lookup"><span data-stu-id="7a601-106">Use XAML to design the appearance of the application's user interface (UI).</span></span>

- <span data-ttu-id="7a601-107">Écrire du code pour générer le comportement de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-107">Write code to build the application's behavior.</span></span>

- <span data-ttu-id="7a601-108">Créer une définition d’application pour gérer l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-108">Create an application definition to manage the application.</span></span>

- <span data-ttu-id="7a601-109">Ajouter des contrôles et créer la disposition pour composer l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-109">Add controls and create the layout to compose the application UI.</span></span>

- <span data-ttu-id="7a601-110">Créer des styles pour une apparence cohérente tout au long de l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-110">Create styles for a consistent appearance throughout the application's UI.</span></span>

- <span data-ttu-id="7a601-111">Lier l’interface utilisateur à des données, pour remplir l’interface utilisateur à partir des données et de conserver les données et l’interface utilisateur synchronisé.</span><span class="sxs-lookup"><span data-stu-id="7a601-111">Bind the UI to data, both to populate the UI from data and to keep the data and UI synchronized.</span></span>

<span data-ttu-id="7a601-112">À la fin de la procédure pas à pas, vous aurez créé une application Windows qui permet aux utilisateurs d’afficher les notes de frais pour certaines personnes autonome.</span><span class="sxs-lookup"><span data-stu-id="7a601-112">By the end of the walkthrough, you'll have built a standalone Windows application that allows users to view expense reports for selected people.</span></span> <span data-ttu-id="7a601-113">L’application est composée de plusieurs pages WPF sont hébergées dans une fenêtre de style navigateur.</span><span class="sxs-lookup"><span data-stu-id="7a601-113">The application is composed of several WPF pages that are hosted in a browser-style window.</span></span>

> [!TIP]
> <span data-ttu-id="7a601-114">L’exemple de code qui est utilisé pour générer cette procédure pas à pas est disponible pour les deux Visual Basic et C# à [Code d’exemple de procédure pas à pas WPF application](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).</span><span class="sxs-lookup"><span data-stu-id="7a601-114">The sample code that is used to build this walkthrough is available for both Visual Basic and C# at [Walkthrough WPF App Sample Code](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).</span></span>
>
> <span data-ttu-id="7a601-115">Vous pouvez activer/désactiver le langage de code de l’exemple de code entre C# et Visual Basic à l’aide de la **\< />** déroulante sur le coin supérieur droit de cet article.</span><span class="sxs-lookup"><span data-stu-id="7a601-115">You can toggle the code language of the sample code between C# and Visual Basic by using the **\</>** drop-down on the upper right side of this article.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a601-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="7a601-116">Prerequisites</span></span>

- <span data-ttu-id="7a601-117">Visual Studio 2017 ou version ultérieure (cet article utilise Visual Studio 2019)</span><span class="sxs-lookup"><span data-stu-id="7a601-117">Visual Studio 2017 or later (this article uses Visual Studio 2019)</span></span>

   <span data-ttu-id="7a601-118">Pour plus d’informations sur l’installation de la dernière version de Visual Studio, consultez [installer Visual Studio](/visualstudio/install/install-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="7a601-118">For more information about installing the latest version of Visual Studio, see [Install Visual Studio](/visualstudio/install/install-visual-studio).</span></span>

## <a name="create-the-application-project"></a><span data-ttu-id="7a601-119">Créer le projet d’application</span><span class="sxs-lookup"><span data-stu-id="7a601-119">Create the application project</span></span>

<span data-ttu-id="7a601-120">La première étape consiste à créer l’infrastructure d’application, qui inclut une définition d’application, deux pages et une image.</span><span class="sxs-lookup"><span data-stu-id="7a601-120">The first step is to create the application infrastructure, which includes an application definition, two pages, and an image.</span></span>

1. <span data-ttu-id="7a601-121">Créer un nouveau projet d’Application WPF en Visual Basic ou Visual c# nommé **`ExpenseIt`**:</span><span class="sxs-lookup"><span data-stu-id="7a601-121">Create a new WPF Application project in Visual Basic or Visual C# named **`ExpenseIt`**:</span></span>

   1. <span data-ttu-id="7a601-122">Ouvrez Visual Studio et sélectionnez **créer un nouveau projet** sous le **prise en main** menu.</span><span class="sxs-lookup"><span data-stu-id="7a601-122">Open Visual Studio and select **Create a new project** under the **Get started** menu.</span></span>

      <span data-ttu-id="7a601-123">Le **créer un nouveau projet** boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7a601-123">The **Create a new project** dialog opens.</span></span>

   2. <span data-ttu-id="7a601-124">Dans le **langage** liste déroulante, sélectionnez **C#** ou **Visual Basic**.</span><span class="sxs-lookup"><span data-stu-id="7a601-124">In the **Language** dropdown, select either **C#** or **Visual Basic**.</span></span>
      
   3. <span data-ttu-id="7a601-125">Sélectionnez le **application WPF (.NET Framework)** modèle, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7a601-125">Select the **WPF App (.NET Framework)** template and then select **Next**.</span></span> 
     
      ![Créer une boîte de dialogue Nouveau projet](./media/walkthrough-my-first-wpf-desktop-application/create-new-project-dialog.png)
    
      <span data-ttu-id="7a601-127">Le **configurer votre nouveau projet** boîte de dialogue s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7a601-127">The **Configure your new project** dialog opens.</span></span>

   4. <span data-ttu-id="7a601-128">Entrez le nom du projet **`ExpenseIt`** , puis sélectionnez **créer**.</span><span class="sxs-lookup"><span data-stu-id="7a601-128">Enter the project name **`ExpenseIt`** and then select **Create**.</span></span>

      ![Configurer une boîte de dialogue Nouveau projet](./media/walkthrough-my-first-wpf-desktop-application/configure-new-project-dialog.png)

      <span data-ttu-id="7a601-130">Visual Studio crée le projet et ouvre le concepteur pour la fenêtre d’application par défaut nommé **MainWindow.xaml**.</span><span class="sxs-lookup"><span data-stu-id="7a601-130">Visual Studio creates the project and opens the designer for the default application window named **MainWindow.xaml**.</span></span>

2. <span data-ttu-id="7a601-131">Ouvrez *Application.xaml* (Visual Basic) ou *App.xaml* (c#).</span><span class="sxs-lookup"><span data-stu-id="7a601-131">Open *Application.xaml* (Visual Basic) or *App.xaml* (C#).</span></span>

    <span data-ttu-id="7a601-132">Ce fichier XAML définit une application WPF et les ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-132">This XAML file defines a WPF application and any application resources.</span></span> <span data-ttu-id="7a601-133">Vous utilisez également ce fichier pour spécifier l’interface utilisateur, dans ce cas *MainWindow.xaml*, qui s’affiche automatiquement lorsque l’application démarre.</span><span class="sxs-lookup"><span data-stu-id="7a601-133">You also use this file to specify the UI, in this case *MainWindow.xaml*, that automatically shows when the application starts.</span></span>

    <span data-ttu-id="7a601-134">Votre XAML doit ressembler à ce qui suit dans Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7a601-134">Your XAML should look like the following in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#1_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/Application.xaml#1_a)]

    <span data-ttu-id="7a601-135">Et comme le suivant dans C#:</span><span class="sxs-lookup"><span data-stu-id="7a601-135">And like the following in C#:</span></span>

    [!code-xaml[ExpenseIt#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/App.xaml#1)]

3. <span data-ttu-id="7a601-136">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-136">Open *MainWindow.xaml*.</span></span>

    <span data-ttu-id="7a601-137">Ce fichier XAML est la fenêtre principale de votre application et affiche le contenu créé dans les pages.</span><span class="sxs-lookup"><span data-stu-id="7a601-137">This XAML file is the main window of your application and displays content created in pages.</span></span> <span data-ttu-id="7a601-138">Le <xref:System.Windows.Window> classe définit les propriétés d’une fenêtre, telles que son titre, taille ou icône et gère les événements, tels que la fermeture ou le masquage.</span><span class="sxs-lookup"><span data-stu-id="7a601-138">The <xref:System.Windows.Window> class defines the properties of a window, such as its title, size, or icon, and handles events, such as closing or hiding.</span></span>

4. <span data-ttu-id="7a601-139">Modifier le <xref:System.Windows.Window> élément à un <xref:System.Windows.Navigation.NavigationWindow>, comme illustré dans le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="7a601-139">Change the <xref:System.Windows.Window> element to a <xref:System.Windows.Navigation.NavigationWindow>, as shown in the following XAML:</span></span>

   ```xaml
   <NavigationWindow x:Class="ExpenseIt.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        ...
   </NavigationWindow>
   ```

   <span data-ttu-id="7a601-140">Cette application accède à un contenu différent en fonction de l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a601-140">This app navigates to different content depending on the user input.</span></span> <span data-ttu-id="7a601-141">C’est pourquoi les principaux <xref:System.Windows.Window> doit être changé en un <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="7a601-141">This is why the main <xref:System.Windows.Window> needs to be changed to a <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="7a601-142"><xref:System.Windows.Navigation.NavigationWindow> hérite de toutes les propriétés de <xref:System.Windows.Window>.</span><span class="sxs-lookup"><span data-stu-id="7a601-142"><xref:System.Windows.Navigation.NavigationWindow> inherits all the properties of <xref:System.Windows.Window>.</span></span> <span data-ttu-id="7a601-143">Le <xref:System.Windows.Navigation.NavigationWindow> élément dans le fichier XAML crée une instance de la <xref:System.Windows.Navigation.NavigationWindow> classe.</span><span class="sxs-lookup"><span data-stu-id="7a601-143">The <xref:System.Windows.Navigation.NavigationWindow> element in the XAML file creates an instance of the <xref:System.Windows.Navigation.NavigationWindow> class.</span></span> <span data-ttu-id="7a601-144">Pour plus d’informations, consultez [vue d’ensemble de la Navigation](../app-development/navigation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-144">For more information, see [Navigation overview](../app-development/navigation-overview.md).</span></span>

5. <span data-ttu-id="7a601-145">Supprimer le <xref:System.Windows.Controls.Grid> éléments entre le <xref:System.Windows.Navigation.NavigationWindow> balises.</span><span class="sxs-lookup"><span data-stu-id="7a601-145">Remove the <xref:System.Windows.Controls.Grid> elements from between the <xref:System.Windows.Navigation.NavigationWindow> tags.</span></span>

6. <span data-ttu-id="7a601-146">Modifiez les propriétés suivantes dans le code XAML pour le <xref:System.Windows.Navigation.NavigationWindow> élément :</span><span class="sxs-lookup"><span data-stu-id="7a601-146">Change the following properties in the XAML code for the <xref:System.Windows.Navigation.NavigationWindow> element:</span></span>

    - <span data-ttu-id="7a601-147">Définir le <xref:System.Windows.Window.Title%2A> propriété à «`ExpenseIt`».</span><span class="sxs-lookup"><span data-stu-id="7a601-147">Set the <xref:System.Windows.Window.Title%2A> property to "`ExpenseIt`".</span></span>

    - <span data-ttu-id="7a601-148">Définir le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur 350 pixels.</span><span class="sxs-lookup"><span data-stu-id="7a601-148">Set the <xref:System.Windows.FrameworkElement.Height%2A> property to 350 pixels.</span></span>

    - <span data-ttu-id="7a601-149">Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété 500 pixels.</span><span class="sxs-lookup"><span data-stu-id="7a601-149">Set the <xref:System.Windows.FrameworkElement.Width%2A> property to 500 pixels.</span></span>

    <span data-ttu-id="7a601-150">Votre XAML doit ressembler à ce qui suit pour Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7a601-150">Your XAML should look like the following for Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#2_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt/MainWindow.xaml#2_a)]

    <span data-ttu-id="7a601-151">Et comme suit pour C#:</span><span class="sxs-lookup"><span data-stu-id="7a601-151">And like the following for C#:</span></span>

    [!code-xaml[ExpenseIt#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml#2)]

7. <span data-ttu-id="7a601-152">Ouvrez *MainWindow.xaml.vb* ou *MainWindow.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="7a601-152">Open *MainWindow.xaml.vb* or *MainWindow.xaml.cs*.</span></span>

    <span data-ttu-id="7a601-153">Ce fichier est un fichier code-behind qui contient le code pour gérer les événements déclarés dans *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-153">This file is a code-behind file that contains code to handle the events declared in *MainWindow.xaml*.</span></span> <span data-ttu-id="7a601-154">Ce fichier contient une classe partielle pour la fenêtre définie en XAML.</span><span class="sxs-lookup"><span data-stu-id="7a601-154">This file contains a partial class for the window defined in XAML.</span></span>

8. <span data-ttu-id="7a601-155">Si vous utilisez C#, modifiez le `MainWindow` classe à dériver de <xref:System.Windows.Navigation.NavigationWindow>.</span><span class="sxs-lookup"><span data-stu-id="7a601-155">If you're using C#, change the `MainWindow` class to derive from <xref:System.Windows.Navigation.NavigationWindow>.</span></span> <span data-ttu-id="7a601-156">(En Visual Basic, cela se produit automatiquement lorsque vous modifiez la fenêtre en XAML.) Votre C# code doit maintenant ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="7a601-156">(In Visual Basic, this happens automatically when you change the window in XAML.) Your C# code should now look like this:</span></span>

   [!code-csharp[ExpenseIt#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/MainWindow.xaml.cs?highlight=21)]

## <a name="add-files-to-the-application"></a><span data-ttu-id="7a601-157">Ajouter des fichiers à l’application</span><span class="sxs-lookup"><span data-stu-id="7a601-157">Add files to the application</span></span>

<span data-ttu-id="7a601-158">Dans cette section, vous allez ajouter deux pages et une image à l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-158">In this section, you'll add two pages and an image to the application.</span></span>

1. <span data-ttu-id="7a601-159">Ajoutez une nouvelle page au projet et nommez-le *`ExpenseItHome.xaml`*:</span><span class="sxs-lookup"><span data-stu-id="7a601-159">Add a new page to the project, and name it *`ExpenseItHome.xaml`*:</span></span>

   1. <span data-ttu-id="7a601-160">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="7a601-160">In **Solution Explorer**, right-click on the **`ExpenseIt`** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="7a601-161">Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7a601-161">In the **Add New Item** dialog, the **Page (WPF)** template is already selected.</span></span> <span data-ttu-id="7a601-162">Entrez le nom **`ExpenseItHome`**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7a601-162">Enter the name **`ExpenseItHome`**, and then select **Add**.</span></span>

    <span data-ttu-id="7a601-163">Cette page est la première page qui s’affiche lorsque l’application est lancée.</span><span class="sxs-lookup"><span data-stu-id="7a601-163">This page is the first page that's displayed when the application is launched.</span></span> <span data-ttu-id="7a601-164">Il affiche une liste de personnes, pour afficher une note de frais.</span><span class="sxs-lookup"><span data-stu-id="7a601-164">It will show a list of people to select from, to show an expense report for.</span></span>

1. <span data-ttu-id="7a601-165">Ouvrez *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="7a601-165">Open *`ExpenseItHome.xaml`*.</span></span>

1. <span data-ttu-id="7a601-166">Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - Home`».</span><span class="sxs-lookup"><span data-stu-id="7a601-166">Set the <xref:System.Windows.Controls.Page.Title%2A> to "`ExpenseIt - Home`".</span></span>

1. <span data-ttu-id="7a601-167">Définir le `DesignHeight` et `DesignWidth` valeurs d’élément de 300 pixels.</span><span class="sxs-lookup"><span data-stu-id="7a601-167">Set the `DesignHeight` and `DesignWidth` element values to 300 pixels.</span></span>

    <span data-ttu-id="7a601-168">Le XAML apparaît maintenant comme suit pour Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7a601-168">The XAML now appears as follows for Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#6_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml#6_a)]

    <span data-ttu-id="7a601-169">Et comme suit pour C#:</span><span class="sxs-lookup"><span data-stu-id="7a601-169">And like the following for C#:</span></span>

    [!code-xaml[ExpenseIt#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml#6)]

1. <span data-ttu-id="7a601-170">Ouvrez *MainWindow.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-170">Open *MainWindow.xaml*.</span></span>

1. <span data-ttu-id="7a601-171">Ajouter un <xref:System.Windows.Navigation.NavigationWindow.Source%2A> propriété le <xref:System.Windows.Navigation.NavigationWindow> élément et affectez-lui la valeur «`ExpenseItHome.xaml`».</span><span class="sxs-lookup"><span data-stu-id="7a601-171">Add a <xref:System.Windows.Navigation.NavigationWindow.Source%2A> property to the <xref:System.Windows.Navigation.NavigationWindow> element and set it to "`ExpenseItHome.xaml`".</span></span>

    <span data-ttu-id="7a601-172">Cela définit *`ExpenseItHome.xaml`* être la première page ouverte au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-172">This sets *`ExpenseItHome.xaml`* to be the first page opened when the application starts.</span></span> 

    <span data-ttu-id="7a601-173">Exemple XAML dans Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7a601-173">Example XAML in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#7_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml#7_a)]

    <span data-ttu-id="7a601-174">Et en C# :</span><span class="sxs-lookup"><span data-stu-id="7a601-174">And in C#:</span></span>

    [!code-xaml[ExpenseIt#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/MainWindow.xaml#7)]

   > [!TIP]
   > <span data-ttu-id="7a601-175">Vous pouvez également définir le **Source** propriété dans le **divers** catégorie de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a601-175">You can also set the **Source** property in the **Miscellaneous** category of the **Properties** window.</span></span>
   >
   > ![Propriété de source dans la fenêtre Propriétés](./media/properties-source.png)

1. <span data-ttu-id="7a601-177">Ajoutez une autre nouvelle page WPF au projet et nommez-le *ExpenseReportPage.xaml*::</span><span class="sxs-lookup"><span data-stu-id="7a601-177">Add another new WPF page to the project, and name it *ExpenseReportPage.xaml*::</span></span>

   1. <span data-ttu-id="7a601-178">Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.</span><span class="sxs-lookup"><span data-stu-id="7a601-178">In **Solution Explorer**, right-click on the **`ExpenseIt`** project node and choose **Add** > **Page**.</span></span>

   1. <span data-ttu-id="7a601-179">Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez le **Page (WPF)** modèle.</span><span class="sxs-lookup"><span data-stu-id="7a601-179">In the **Add New Item** dialog, select the **Page (WPF)** template.</span></span> <span data-ttu-id="7a601-180">Entrez le nom **ExpenseReportPage**, puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7a601-180">Enter the name **ExpenseReportPage**, and then select **Add**.</span></span>

    <span data-ttu-id="7a601-181">Cette page affiche la note de frais pour la personne sélectionnée sur le **`ExpenseItHome`** page.</span><span class="sxs-lookup"><span data-stu-id="7a601-181">This page will show the expense report for the person that is selected on the **`ExpenseItHome`** page.</span></span>

1. <span data-ttu-id="7a601-182">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-182">Open *ExpenseReportPage.xaml*.</span></span>

1. <span data-ttu-id="7a601-183">Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - View Expense`».</span><span class="sxs-lookup"><span data-stu-id="7a601-183">Set the <xref:System.Windows.Controls.Page.Title%2A> to "`ExpenseIt - View Expense`".</span></span>

1. <span data-ttu-id="7a601-184">Définir le `DesignHeight` et `DesignWidth` valeurs d’élément de 300 pixels.</span><span class="sxs-lookup"><span data-stu-id="7a601-184">Set the `DesignHeight` and `DesignWidth` element values to 300 pixels.</span></span>

    <span data-ttu-id="7a601-185">*ExpenseReportPage.xaml* se présente maintenant comme suit dans Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="7a601-185">*ExpenseReportPage.xaml* now looks like the following in Visual Basic:</span></span>

    [!code-xaml[ExpenseIt#4_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml#4_a)]

    <span data-ttu-id="7a601-186">Et comme le suivant dans C#:</span><span class="sxs-lookup"><span data-stu-id="7a601-186">And like the following in C#:</span></span>

    [!code-xaml[ExpenseIt#4](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml#4)]

1. <span data-ttu-id="7a601-187">Ouvrez *ExpenseItHome.xaml.vb* et *ExpenseReportPage.xaml.vb*, ou *ExpenseItHome.xaml.cs* et *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="7a601-187">Open *ExpenseItHome.xaml.vb* and *ExpenseReportPage.xaml.vb*, or *ExpenseItHome.xaml.cs* and *ExpenseReportPage.xaml.cs*.</span></span>

    <span data-ttu-id="7a601-188">Lorsque vous créez un nouveau fichier de Page, Visual Studio crée automatiquement ses *code-behind* fichier.</span><span class="sxs-lookup"><span data-stu-id="7a601-188">When you create a new Page file, Visual Studio automatically creates its *code-behind* file.</span></span> <span data-ttu-id="7a601-189">Ces fichiers code-behind gèrent la logique pour répondre à une saisie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a601-189">These code-behind files handle the logic for responding to user input.</span></span>

    <span data-ttu-id="7a601-190">Votre code doit ressembler à ce qui suit pour **`ExpenseItHome`**:</span><span class="sxs-lookup"><span data-stu-id="7a601-190">Your code should look like the following for **`ExpenseItHome`**:</span></span>

    [!code-csharp[ExpenseIt#2_5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml.cs#2_5)]

    [!code-vb[ExpenseIt#2_5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml.vb#2_5)]

    <span data-ttu-id="7a601-191">Et comme suit pour **ExpenseReportPage**:</span><span class="sxs-lookup"><span data-stu-id="7a601-191">And like the following for **ExpenseReportPage**:</span></span>

    [!code-csharp[ExpenseIt#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml.cs#5)]

    [!code-vb[ExpenseIt#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml.vb#5)]

1. <span data-ttu-id="7a601-192">Ajouter une image nommée *watermark.png* au projet.</span><span class="sxs-lookup"><span data-stu-id="7a601-192">Add an image named *watermark.png* to the project.</span></span> <span data-ttu-id="7a601-193">Vous pouvez créer votre propre image, copiez le fichier à partir de l’exemple de code ou obtenez-le [ici](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).</span><span class="sxs-lookup"><span data-stu-id="7a601-193">You can create your own image, copy the file from the sample code, or get it [here](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).</span></span>

    1. <span data-ttu-id="7a601-194">Avec le bouton droit sur le nœud du projet et sélectionnez **ajouter** > **élément existant**, ou appuyez sur **MAJ**+**Alt** + **A**.</span><span class="sxs-lookup"><span data-stu-id="7a601-194">Right-click on the project node and select **Add** > **Existing Item**, or press **Shift**+**Alt**+**A**.</span></span>

    2. <span data-ttu-id="7a601-195">Dans le **ajouter un élément existant** boîte de dialogue, définissez le filtre de fichier soit **tous les fichiers** ou **fichiers Image**, accédez au fichier image que vous souhaitez utiliser, puis sélectionnez **ajouter** .</span><span class="sxs-lookup"><span data-stu-id="7a601-195">In the **Add Existing Item** dialog, set the file filter to either **All Files** or **Image Files**, browse to the image file you want to use, and then select **Add**.</span></span>

## <a name="build-and-run-the-application"></a><span data-ttu-id="7a601-196">Générez et exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="7a601-196">Build and run the application</span></span>

1. <span data-ttu-id="7a601-197">Pour générer et exécuter l’application, appuyez sur **F5** ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu.</span><span class="sxs-lookup"><span data-stu-id="7a601-197">To build and run the application, press **F5** or select **Start Debugging** from the **Debug** menu.</span></span>

    <span data-ttu-id="7a601-198">L’illustration suivante montre l’application avec le <xref:System.Windows.Navigation.NavigationWindow> boutons :</span><span class="sxs-lookup"><span data-stu-id="7a601-198">The following illustration shows the application with the <xref:System.Windows.Navigation.NavigationWindow> buttons:</span></span>

    ![Une fois que vous générez et exécutez l’application.](./media/walkthrough-my-first-wpf-desktop-application/build-run-application.png)

2. <span data-ttu-id="7a601-200">Fermez l’application pour revenir à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7a601-200">Close the application to return to Visual Studio.</span></span>

## <a name="create-the-layout"></a><span data-ttu-id="7a601-201">Créer la disposition</span><span class="sxs-lookup"><span data-stu-id="7a601-201">Create the layout</span></span>

<span data-ttu-id="7a601-202">Mise en page offre un moyen ordonné de placer des éléments d’interface utilisateur et gère également la taille et la position de ces éléments lors du redimensionnée d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a601-202">Layout provides an ordered way to place UI elements, and also manages the size and position of those elements when a UI is resized.</span></span> <span data-ttu-id="7a601-203">En règle générale, vous allez créer une disposition avec l’un des contrôles de disposition suivants :</span><span class="sxs-lookup"><span data-stu-id="7a601-203">You typically create a layout with one of the following layout controls:</span></span>

- <span data-ttu-id="7a601-204"><xref:System.Windows.Controls.Canvas> -Définit une zone dans laquelle vous pouvez explicitement positionner des éléments enfants à l’aide des coordonnées relatives à la zone du canevas.</span><span class="sxs-lookup"><span data-stu-id="7a601-204"><xref:System.Windows.Controls.Canvas> - Defines an area within which you can explicitly position child elements by using coordinates that are relative to the Canvas area.</span></span>
- <span data-ttu-id="7a601-205"><xref:System.Windows.Controls.DockPanel> -Définit une zone où vous pouvez organiser les éléments enfants horizontalement ou verticalement, par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="7a601-205"><xref:System.Windows.Controls.DockPanel> - Defines an area where you can arrange child elements either horizontally or vertically, relative to each other.</span></span>
- <span data-ttu-id="7a601-206"><xref:System.Windows.Controls.Grid> -Définit une grille flexible composée de colonnes et de lignes.</span><span class="sxs-lookup"><span data-stu-id="7a601-206"><xref:System.Windows.Controls.Grid> - Defines a flexible grid area that consists of columns and rows.</span></span>
- <span data-ttu-id="7a601-207"><xref:System.Windows.Controls.StackPanel> -Organise les éléments enfants sur une seule ligne qui peut être orientée horizontalement ou verticalement.</span><span class="sxs-lookup"><span data-stu-id="7a601-207"><xref:System.Windows.Controls.StackPanel> - Arranges child elements into a single line that can be oriented horizontally or vertically.</span></span>
- <span data-ttu-id="7a601-208"><xref:System.Windows.Controls.VirtualizingStackPanel> -Organise et virtualise un contenu sur une seule ligne est orienté horizontalement ou verticalement.</span><span class="sxs-lookup"><span data-stu-id="7a601-208"><xref:System.Windows.Controls.VirtualizingStackPanel> - Arranges and virtualizes content on a single line that is oriented either horizontally or vertically.</span></span>
- <span data-ttu-id="7a601-209"><xref:System.Windows.Controls.WrapPanel> -Éléments enfants de positions dans un ordre séquentiel de gauche à droite, en faisant passer le contenu à la ligne suivante à la périphérie de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a601-209"><xref:System.Windows.Controls.WrapPanel> - Positions child elements in sequential position from left to right, breaking content to the next line at the edge of the containing box.</span></span> <span data-ttu-id="7a601-210">Classement continue ensuite séquentiellement de haut en bas ou de droite à gauche, selon la valeur de la propriété Orientation.</span><span class="sxs-lookup"><span data-stu-id="7a601-210">Subsequent ordering happens sequentially from top to bottom or from right to left, depending on the value of the Orientation property.</span></span>

<span data-ttu-id="7a601-211">Chacun de ces contrôles de disposition prend en charge un type particulier de disposition pour ses éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="7a601-211">Each of these layout controls supports a particular type of layout for its child elements.</span></span> <span data-ttu-id="7a601-212">`ExpenseIt` pages peuvent être redimensionnés, et chaque page comporte des éléments organisés horizontalement et verticalement en même temps que d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="7a601-212">`ExpenseIt` pages can be resized, and each page has elements that are arranged horizontally and vertically alongside other elements.</span></span> <span data-ttu-id="7a601-213">Dans cet exemple, le <xref:System.Windows.Controls.Grid> est utilisé comme élément de disposition de l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-213">In this example, the <xref:System.Windows.Controls.Grid> is used as  layout element for the application.</span></span>

> [!TIP]
> <span data-ttu-id="7a601-214">Pour plus d’informations sur <xref:System.Windows.Controls.Panel> éléments, consultez [vue d’ensemble de panneaux](../controls/panels-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-214">For more information about <xref:System.Windows.Controls.Panel> elements, see [Panels overview](../controls/panels-overview.md).</span></span> <span data-ttu-id="7a601-215">Pour plus d’informations sur la disposition, consultez [disposition](../advanced/layout.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-215">For more information about layout, see [Layout](../advanced/layout.md).</span></span>

<span data-ttu-id="7a601-216">Dans cette section, vous créez une seule colonne de table avec trois lignes et une marge de 10 pixels en ajoutant des définitions de colonne et de ligne à la <xref:System.Windows.Controls.Grid> dans *`ExpenseItHome.xaml`*.</span><span class="sxs-lookup"><span data-stu-id="7a601-216">In this section, you create a single-column table with three rows and a 10-pixel margin by adding column and row definitions to the <xref:System.Windows.Controls.Grid> in *`ExpenseItHome.xaml`*.</span></span>

1. <span data-ttu-id="7a601-217">Dans *`ExpenseItHome.xaml`*, définissez le <xref:System.Windows.FrameworkElement.Margin%2A> propriété sur le <xref:System.Windows.Controls.Grid> élément valeur « 10,0,10,10 » qui correspond aux marges gauche, haut, droite et bas :</span><span class="sxs-lookup"><span data-stu-id="7a601-217">In *`ExpenseItHome.xaml`*, set the <xref:System.Windows.FrameworkElement.Margin%2A> property on the <xref:System.Windows.Controls.Grid> element to "10,0,10,10", which corresponds to left, top, right and bottom margins:</span></span>

   ```xaml
   <Grid Margin="10,0,10,10">
   ```

   > [!TIP]
   > <span data-ttu-id="7a601-218">Vous pouvez également définir le **marge** des valeurs dans le **propriétés** fenêtre, sous le **disposition** catégorie :</span><span class="sxs-lookup"><span data-stu-id="7a601-218">You can also set the **Margin** values in the **Properties** window, under the **Layout** category:</span></span>
   >
   > ![Valeurs de marge dans la fenêtre Propriétés](./media/properties-margin.png)

2. <span data-ttu-id="7a601-220">Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises pour créer les définitions de ligne et de colonne :</span><span class="sxs-lookup"><span data-stu-id="7a601-220">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags to create the row and column definitions:</span></span>

    [!code-xaml[ExpenseIt#8](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#8)]

    <span data-ttu-id="7a601-221">Le <xref:System.Windows.Controls.RowDefinition.Height%2A> de deux lignes est définie sur <xref:System.Windows.GridLength.Auto%2A>, ce qui signifie que les lignes sont dimensionnés en fonction du contenu dans les lignes.</span><span class="sxs-lookup"><span data-stu-id="7a601-221">The <xref:System.Windows.Controls.RowDefinition.Height%2A> of two rows is set to <xref:System.Windows.GridLength.Auto%2A>, which means that the rows are sized based on the content in the rows.</span></span> <span data-ttu-id="7a601-222">La valeur par défaut <xref:System.Windows.Controls.RowDefinition.Height%2A> est <xref:System.Windows.GridUnitType.Star> dimensionnement, ce qui signifie que la hauteur de ligne est une proportion pondérée de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="7a601-222">The default <xref:System.Windows.Controls.RowDefinition.Height%2A> is <xref:System.Windows.GridUnitType.Star> sizing, which means that the row height is a weighted proportion of the available space.</span></span> <span data-ttu-id="7a601-223">Par exemple, si deux lignes ont une <xref:System.Windows.Controls.RowDefinition.Height%2A> de « \* », ils ont chacun une hauteur qui représente la moitié de l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="7a601-223">For example if two rows each have a <xref:System.Windows.Controls.RowDefinition.Height%2A> of "\*", they each have a height that is half of the available space.</span></span>

    <span data-ttu-id="7a601-224">Votre <xref:System.Windows.Controls.Grid> doit maintenant contenir le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="7a601-224">Your <xref:System.Windows.Controls.Grid> should now contain the following XAML:</span></span>

    [!code-xaml[ExpenseIt#9](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#9)]

## <a name="add-controls"></a><span data-ttu-id="7a601-225">Ajouter des contrôles</span><span class="sxs-lookup"><span data-stu-id="7a601-225">Add controls</span></span>

<span data-ttu-id="7a601-226">Dans cette section, vous allez mettre à jour l’interface utilisateur pour afficher une liste de personnes, où vous sélectionnez une personne pour afficher l’état de leurs dépenses de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="7a601-226">In this section, you'll update the home page UI to show a list of people, where you select one person to display their expense report.</span></span> <span data-ttu-id="7a601-227">Les contrôles sont des objets d’interface utilisateur qui permettent aux utilisateurs d’interagir avec votre application.</span><span class="sxs-lookup"><span data-stu-id="7a601-227">Controls are UI objects that allow users to interact with your application.</span></span> <span data-ttu-id="7a601-228">Pour plus d’informations, consultez [Contrôles](../controls/index.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-228">For more information, see [Controls](../controls/index.md).</span></span>

<span data-ttu-id="7a601-229">Pour créer cette interface utilisateur, vous allez ajouter les éléments suivants à *`ExpenseItHome.xaml`*:</span><span class="sxs-lookup"><span data-stu-id="7a601-229">To create this UI, you'll add the following elements to *`ExpenseItHome.xaml`*:</span></span>

- <span data-ttu-id="7a601-230">Un <xref:System.Windows.Controls.ListBox> (pour la liste de personnes).</span><span class="sxs-lookup"><span data-stu-id="7a601-230">A <xref:System.Windows.Controls.ListBox> (for the list of people).</span></span>
- <span data-ttu-id="7a601-231">Un <xref:System.Windows.Controls.Label> (pour l’en-tête de liste).</span><span class="sxs-lookup"><span data-stu-id="7a601-231">A <xref:System.Windows.Controls.Label> (for the list header).</span></span>
- <span data-ttu-id="7a601-232">Un <xref:System.Windows.Controls.Button> (sur lequel cliquer pour afficher la note de frais pour la personne qui est sélectionnée dans la liste).</span><span class="sxs-lookup"><span data-stu-id="7a601-232">A <xref:System.Windows.Controls.Button> (to click to view the expense report for the person that is selected in the list).</span></span>

<span data-ttu-id="7a601-233">Chaque contrôle est placé dans une ligne de la <xref:System.Windows.Controls.Grid> en définissant le <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> propriété jointe.</span><span class="sxs-lookup"><span data-stu-id="7a601-233">Each control is placed in a row of the <xref:System.Windows.Controls.Grid> by setting the <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> attached property.</span></span> <span data-ttu-id="7a601-234">Pour plus d’informations sur les propriétés jointes, consultez [vue d’ensemble des propriétés jointes](../advanced/attached-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-234">For more information about attached properties, see [Attached Properties Overview](../advanced/attached-properties-overview.md).</span></span>

1. <span data-ttu-id="7a601-235">Dans *`ExpenseItHome.xaml`*, ajoutez le XAML suivant quelque part entre le <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="7a601-235">In *`ExpenseItHome.xaml`*, add the following XAML somewhere between the <xref:System.Windows.Controls.Grid> tags:</span></span>

   [!code-xaml[ExpenseIt#10](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt4/ExpenseItHome.xaml#10)]

   > [!TIP]
   > <span data-ttu-id="7a601-236">Vous pouvez également créer les contrôles en les faisant glisser à partir de la **boîte à outils** fenêtre sur la fenêtre de conception, puis en définissant leurs propriétés le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a601-236">You can also create the controls by dragging them from the **Toolbox** window onto the design window, and then setting their properties in the **Properties** window.</span></span>

2. <span data-ttu-id="7a601-237">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-237">Build and run the application.</span></span>

    <span data-ttu-id="7a601-238">L’illustration suivante montre les contrôles que vous avez créé :</span><span class="sxs-lookup"><span data-stu-id="7a601-238">The following illustration shows the controls you created:</span></span>

![Capture d’écran de l’exemple ExpenseIt affichant une liste de noms](./media/walkthrough-my-first-wpf-desktop-application/add-application-controls.png)

## <a name="add-an-image-and-a-title"></a><span data-ttu-id="7a601-240">Ajouter une image et un titre</span><span class="sxs-lookup"><span data-stu-id="7a601-240">Add an image and a title</span></span>

<span data-ttu-id="7a601-241">Dans cette section, vous allez mettre à jour l’interface utilisateur de la page d’accueil avec une image et un titre de page.</span><span class="sxs-lookup"><span data-stu-id="7a601-241">In this section, you'll update the home page UI with an image and a page title.</span></span>

1. <span data-ttu-id="7a601-242">Dans *`ExpenseItHome.xaml`*, ajoutez une autre colonne à la <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> fixe <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de 230 pixels :</span><span class="sxs-lookup"><span data-stu-id="7a601-242">In *`ExpenseItHome.xaml`*, add another column to the <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> with a fixed <xref:System.Windows.Controls.ColumnDefinition.Width%2A> of 230 pixels:</span></span>

    [!code-xaml[ExpenseIt#11](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseItHome.xaml?highlight=52-55)]

2. <span data-ttu-id="7a601-243">Ajouter une autre ligne à la <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, pour un total de quatre lignes :</span><span class="sxs-lookup"><span data-stu-id="7a601-243">Add another row to the <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, for a total of four rows:</span></span>

    [!code-xaml[ExpenseIt#11b](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseItHome.xaml?highlight=57-62)]

3. <span data-ttu-id="7a601-244">Déplacer les contrôles vers la deuxième colonne en définissant le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété sur 1 dans chacun des trois contrôles (bordure, ListBox et bouton).</span><span class="sxs-lookup"><span data-stu-id="7a601-244">Move the controls to the second column by setting the <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> property to 1 in each of the three controls (Border, ListBox, and Button).</span></span>

4. <span data-ttu-id="7a601-245">Déplacez chaque contrôle d’une ligne vers le bas en incrémentant son <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> valeur de 1 pour chacun des trois contrôles (bordure, ListBox et bouton) et pour l’élément Border.</span><span class="sxs-lookup"><span data-stu-id="7a601-245">Move each control down a row by incrementing its <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> value by 1 for each of the three controls (Border, ListBox, and Button) and for the Border element.</span></span>

   <span data-ttu-id="7a601-246">Le XAML pour les trois contrôles se présente désormais comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a601-246">The XAML for the three controls now looks like the following:</span></span>

    [!code-xaml[ExpenseIt#12](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#12)]

5. <span data-ttu-id="7a601-247">Définir le <xref:System.Windows.Controls.Panel.Background%2A?displayProperty=nameWithType> propriété le *watermark.png* fichier image, en ajoutant le XAML suivant n’importe où entre le `<Grid>` et `</Grid>` balises :</span><span class="sxs-lookup"><span data-stu-id="7a601-247">Set the <xref:System.Windows.Controls.Panel.Background%2A?displayProperty=nameWithType> property to the *watermark.png* image file, by adding the following XAML anywhere between the `<Grid>` and `</Grid>` tags:</span></span>

    [!code-xaml[ExpenseIt#14](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#14)]

6. <span data-ttu-id="7a601-248">Avant du <xref:System.Windows.Controls.Border> élément, ajoutez un <xref:System.Windows.Controls.Label> avec le contenu « View Expense Report ».</span><span class="sxs-lookup"><span data-stu-id="7a601-248">Before the <xref:System.Windows.Controls.Border> element, add a <xref:System.Windows.Controls.Label> with the content "View Expense Report".</span></span> <span data-ttu-id="7a601-249">Cette étiquette est le titre de la page.</span><span class="sxs-lookup"><span data-stu-id="7a601-249">This label is the title of the page.</span></span>

    [!code-xaml[ExpenseIt#13](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#13)]

7. <span data-ttu-id="7a601-250">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-250">Build and run the application.</span></span>

<span data-ttu-id="7a601-251">L’illustration suivante montre les résultats de ce que vous venez d’ajouter :</span><span class="sxs-lookup"><span data-stu-id="7a601-251">The following illustration shows the results of what you just added:</span></span>

![Capture d’écran de l’exemple ExpenseIt montrant le nouveau titre image d’arrière-plan et de page](./media/walkthrough-my-first-wpf-desktop-application/add-application-image-title.png)

## <a name="add-code-to-handle-events"></a><span data-ttu-id="7a601-253">Ajoutez du code pour gérer les événements</span><span class="sxs-lookup"><span data-stu-id="7a601-253">Add code to handle events</span></span>

1. <span data-ttu-id="7a601-254">Dans *`ExpenseItHome.xaml`*, ajoutez un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements à la <xref:System.Windows.Controls.Button> élément.</span><span class="sxs-lookup"><span data-stu-id="7a601-254">In *`ExpenseItHome.xaml`*, add a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to the <xref:System.Windows.Controls.Button> element.</span></span> <span data-ttu-id="7a601-255">Pour plus d'informations, voir [Procédure : Créez un gestionnaire d’événements simple](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7a601-255">For more information, see [How to: Create a simple event handler](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).</span></span>

    [!code-xaml[ExpenseIt#15](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml#15)]

2. <span data-ttu-id="7a601-256">Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.</span><span class="sxs-lookup"><span data-stu-id="7a601-256">Open *`ExpenseItHome.xaml.vb`* or *`ExpenseItHome.xaml.cs`*.</span></span>

3. <span data-ttu-id="7a601-257">Ajoutez le code suivant à la `ExpenseItHome` classe pour ajouter un bouton Gestionnaire d’événements click.</span><span class="sxs-lookup"><span data-stu-id="7a601-257">Add the following code to the `ExpenseItHome` class to add a button click event handler.</span></span> <span data-ttu-id="7a601-258">Le Gestionnaire d’événements ouvre le **ExpenseReportPage** page.</span><span class="sxs-lookup"><span data-stu-id="7a601-258">The event handler opens the **ExpenseReportPage** page.</span></span>

    [!code-csharp[ExpenseIt#16](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml.cs#16)]
    [!code-vb[ExpenseIt#16](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt6/ExpenseItHome.xaml.vb#16)]

## <a name="create-the-ui-for-expensereportpage"></a><span data-ttu-id="7a601-259">Créer l’interface utilisateur pour ExpenseReportPage</span><span class="sxs-lookup"><span data-stu-id="7a601-259">Create the UI for ExpenseReportPage</span></span>

<span data-ttu-id="7a601-260">*ExpenseReportPage.xaml* affiche la note de frais de la personne qui est sélectionnée sur la **`ExpenseItHome`** page.</span><span class="sxs-lookup"><span data-stu-id="7a601-260">*ExpenseReportPage.xaml* displays the expense report for the person that's selected on the **`ExpenseItHome`** page.</span></span> <span data-ttu-id="7a601-261">Dans cette section, vous allez créer l’interface utilisateur pour **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="7a601-261">In this section, you'll create the UI for **ExpenseReportPage**.</span></span> <span data-ttu-id="7a601-262">Vous également ajouter d’arrière-plan et les couleurs aux divers éléments d’interface utilisateur de remplissage.</span><span class="sxs-lookup"><span data-stu-id="7a601-262">You'll also add background and fill colors to the various UI elements.</span></span>

1. <span data-ttu-id="7a601-263">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-263">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="7a601-264">Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises :</span><span class="sxs-lookup"><span data-stu-id="7a601-264">Add the following XAML between the <xref:System.Windows.Controls.Grid> tags:</span></span>

    [!code-xaml[ExpenseIt#17](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseReportPage.xaml#17)]

    <span data-ttu-id="7a601-265">Cette interface utilisateur est similaire à *`ExpenseItHome.xaml`*, sauf que les données du rapport s’affiche dans un <xref:System.Windows.Controls.DataGrid>.</span><span class="sxs-lookup"><span data-stu-id="7a601-265">This UI is similar to *`ExpenseItHome.xaml`*, except the report data is displayed in a <xref:System.Windows.Controls.DataGrid>.</span></span>

3. <span data-ttu-id="7a601-266">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-266">Build and run the application.</span></span>

4. <span data-ttu-id="7a601-267">Sélectionnez le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="7a601-267">Select the **View** button.</span></span>

    <span data-ttu-id="7a601-268">La page de note de frais s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7a601-268">The expense report page appears.</span></span> <span data-ttu-id="7a601-269">Notez également que le bouton de navigation arrière est activé.</span><span class="sxs-lookup"><span data-stu-id="7a601-269">Also notice that the back navigation button is enabled.</span></span>

<span data-ttu-id="7a601-270">L’illustration suivante montre les éléments d’interface utilisateur ajoutés à *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-270">The following illustration shows the UI elements added to *ExpenseReportPage.xaml*.</span></span>

![ExpenseIt exemple capture d’écran montrant l’interface utilisateur pour le ExpenseReportPage venez de créer.](./media/walkthrough-my-first-wpf-desktop-application/create-application-ui.png)

## <a name="style-controls"></a><span data-ttu-id="7a601-272">Style aux contrôles</span><span class="sxs-lookup"><span data-stu-id="7a601-272">Style controls</span></span>

<span data-ttu-id="7a601-273">L’apparence des différents éléments est souvent le même pour tous les éléments du même type dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a601-273">The appearance of various elements is often the same for all elements of the same type in a UI.</span></span> <span data-ttu-id="7a601-274">Utilise l’interface utilisateur [styles](../controls/styling-and-templating.md) pour pouvoir réutiliser l’apparence des différents éléments.</span><span class="sxs-lookup"><span data-stu-id="7a601-274">UI uses [styles](../controls/styling-and-templating.md) to make appearances reusable across multiple elements.</span></span> <span data-ttu-id="7a601-275">La réutilisation des styles permet de simplifier la gestion et la création de XAML.</span><span class="sxs-lookup"><span data-stu-id="7a601-275">The reusability of styles helps to simplify XAML creation and management.</span></span> <span data-ttu-id="7a601-276">Cette section remplace par des styles les attributs d’élément qui ont été définis lors des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="7a601-276">This section replaces the per-element attributes that were defined in previous steps with styles.</span></span>

1. <span data-ttu-id="7a601-277">Ouvrez *Application.xaml* ou *App.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-277">Open *Application.xaml* or *App.xaml*.</span></span>

2. <span data-ttu-id="7a601-278">Ajoutez le XAML suivant entre les <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> balises :</span><span class="sxs-lookup"><span data-stu-id="7a601-278">Add the following XAML between the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> tags:</span></span>

    [!code-xaml[ExpenseIt#18](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/App.xaml#18)]

    <span data-ttu-id="7a601-279">Ce code XAML ajoute les styles suivants :</span><span class="sxs-lookup"><span data-stu-id="7a601-279">This XAML adds the following styles:</span></span>

    - <span data-ttu-id="7a601-280">`headerTextStyle`: Pour mettre en forme le titre de la page <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="7a601-280">`headerTextStyle`: To format the page title <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="7a601-281">`labelStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Label> contrôles.</span><span class="sxs-lookup"><span data-stu-id="7a601-281">`labelStyle`: To format the <xref:System.Windows.Controls.Label> controls.</span></span>

    - <span data-ttu-id="7a601-282">`columnHeaderStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span><span class="sxs-lookup"><span data-stu-id="7a601-282">`columnHeaderStyle`: To format the <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.</span></span>

    - <span data-ttu-id="7a601-283">`listHeaderStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Border> contrôles.</span><span class="sxs-lookup"><span data-stu-id="7a601-283">`listHeaderStyle`: To format the list header <xref:System.Windows.Controls.Border> controls.</span></span>

    - <span data-ttu-id="7a601-284">`listHeaderTextStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="7a601-284">`listHeaderTextStyle`: To format the list header <xref:System.Windows.Controls.Label>.</span></span>

    - <span data-ttu-id="7a601-285">`buttonStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Button> sur `ExpenseItHome.xaml`.</span><span class="sxs-lookup"><span data-stu-id="7a601-285">`buttonStyle`: To format the <xref:System.Windows.Controls.Button> on `ExpenseItHome.xaml`.</span></span>

    <span data-ttu-id="7a601-286">Notez que les styles sont des ressources et des enfants de le <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> élément de propriété.</span><span class="sxs-lookup"><span data-stu-id="7a601-286">Notice that the styles are resources and children of the <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> property element.</span></span> <span data-ttu-id="7a601-287">À cet emplacement, les styles sont appliqués à tous les éléments d’une application.</span><span class="sxs-lookup"><span data-stu-id="7a601-287">In this location, the styles are applied to all the elements in an application.</span></span> <span data-ttu-id="7a601-288">Pour obtenir un exemple d’utilisation des ressources dans une application .NET, consultez [utiliser les ressources Application](../advanced/how-to-use-application-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-288">For an example of using resources in a .NET app, see [Use Application Resources](../advanced/how-to-use-application-resources.md).</span></span>

3. <span data-ttu-id="7a601-289">Dans *`ExpenseItHome.xaml`*, remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="7a601-289">In *`ExpenseItHome.xaml`*, replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#19](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseItHome.xaml#19)]

    <span data-ttu-id="7a601-290">Les propriétés qui définissent l’apparence de chaque contrôle, comme <xref:System.Windows.VerticalAlignment> et <xref:System.Windows.Media.FontFamily> , sont supprimées et remplacées lors de l’application de styles.</span><span class="sxs-lookup"><span data-stu-id="7a601-290">The properties such as <xref:System.Windows.VerticalAlignment> and <xref:System.Windows.Media.FontFamily> that define the look of each control are removed and replaced by applying the styles.</span></span> <span data-ttu-id="7a601-291">Par exemple, le `headerTextStyle` est appliqué à la « View Expense Report » <xref:System.Windows.Controls.Label>.</span><span class="sxs-lookup"><span data-stu-id="7a601-291">For example, the `headerTextStyle` is applied to the "View Expense Report" <xref:System.Windows.Controls.Label>.</span></span>

4. <span data-ttu-id="7a601-292">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-292">Open *ExpenseReportPage.xaml*.</span></span>

5. <span data-ttu-id="7a601-293">Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="7a601-293">Replace everything between the <xref:System.Windows.Controls.Grid> elements with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#20](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseReportPage.xaml#20)]

    <span data-ttu-id="7a601-294">Ce XAML ajoute les styles pour le <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Border> éléments.</span><span class="sxs-lookup"><span data-stu-id="7a601-294">This XAML adds styles to the <xref:System.Windows.Controls.Label> and <xref:System.Windows.Controls.Border> elements.</span></span>

6. <span data-ttu-id="7a601-295">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-295">Build and run the application.</span></span> <span data-ttu-id="7a601-296">L’apparence de la fenêtre est le même que précédemment.</span><span class="sxs-lookup"><span data-stu-id="7a601-296">The window appearance is the same as previously.</span></span>

    ![Capture d’écran ExpenseIt exemple avec la même apparence que dans la dernière section.](./media/walkthrough-my-first-wpf-desktop-application/create-application-ui.png)

7. <span data-ttu-id="7a601-298">Fermez l’application pour revenir à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7a601-298">Close the application to return to Visual Studio.</span></span>

## <a name="bind-data-to-a-control"></a><span data-ttu-id="7a601-299">Lier des données à un contrôle</span><span class="sxs-lookup"><span data-stu-id="7a601-299">Bind data to a control</span></span>

<span data-ttu-id="7a601-300">Dans cette section, vous allez créer les données XML qui sont liées à différents contrôles.</span><span class="sxs-lookup"><span data-stu-id="7a601-300">In this section, you'll create the XML data that is bound to various controls.</span></span>

1. <span data-ttu-id="7a601-301">Dans *`ExpenseItHome.xaml`*, après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez le XAML suivant pour créer un <xref:System.Windows.Data.XmlDataProvider> qui contient les données pour chaque personne :</span><span class="sxs-lookup"><span data-stu-id="7a601-301">In *`ExpenseItHome.xaml`*, after the opening <xref:System.Windows.Controls.Grid> element, add the following XAML to create an <xref:System.Windows.Data.XmlDataProvider> that contains the data for each person:</span></span>

    [!code-xaml[ExpenseIt#23](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml?range=13,16-40,49)]

    <span data-ttu-id="7a601-302">Les données sont créées en tant qu’un <xref:System.Windows.Controls.Grid> ressource.</span><span class="sxs-lookup"><span data-stu-id="7a601-302">The data is created as a <xref:System.Windows.Controls.Grid> resource.</span></span> <span data-ttu-id="7a601-303">Normalement, ces données seraient chargées en tant que fichier, mais par souci de simplicité, les données sont ajoutées inline.</span><span class="sxs-lookup"><span data-stu-id="7a601-303">Normally this data would be loaded as a file, but for simplicity the data is added inline.</span></span>

2. <span data-ttu-id="7a601-304">Dans le `<Grid.Resources>` élément, ajoutez le code suivant `<xref:System.Windows.DataTemplate>` élément, qui définit comment afficher les données dans le <xref:System.Windows.Controls.ListBox>, après le `<XmlDataProvider>` élément :</span><span class="sxs-lookup"><span data-stu-id="7a601-304">Within the `<Grid.Resources>` element, add the following `<xref:System.Windows.DataTemplate>` element, which defines how to display the data in the <xref:System.Windows.Controls.ListBox>, after the `<XmlDataProvider>` element:</span></span>

    [!code-xaml[ExpenseIt#24](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml?range=13,43-46,49)]

    <span data-ttu-id="7a601-305">Pour plus d’informations sur les modèles de données, consultez [vue d’ensemble de création de modèles de données](../data/data-templating-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-305">For more information about data templates, see [Data templating overview](../data/data-templating-overview.md).</span></span>

3. <span data-ttu-id="7a601-306">Remplacer la <xref:System.Windows.Controls.ListBox> avec le XAML suivant :</span><span class="sxs-lookup"><span data-stu-id="7a601-306">Replace the existing <xref:System.Windows.Controls.ListBox> with the following XAML:</span></span>

    [!code-xaml[ExpenseIt#25](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#25)]

    <span data-ttu-id="7a601-307">Ce XAML lie le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la source de données et applique le modèle de données en tant que le <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span><span class="sxs-lookup"><span data-stu-id="7a601-307">This XAML binds the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.ListBox> to the data source and applies the data template as the <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.</span></span>

## <a name="connect-data-to-controls"></a><span data-ttu-id="7a601-308">Connectez des données aux contrôles</span><span class="sxs-lookup"><span data-stu-id="7a601-308">Connect data to controls</span></span>

<span data-ttu-id="7a601-309">Ensuite, vous ajouterez du code pour récupérer le nom qui est sélectionné sur la **`ExpenseItHome`** page et le passer au constructeur de **ExpenseReportPage**.</span><span class="sxs-lookup"><span data-stu-id="7a601-309">Next, you'll add code to retrieve the name that's selected on the **`ExpenseItHome`** page and pass it to the constructor of **ExpenseReportPage**.</span></span> <span data-ttu-id="7a601-310">**ExpenseReportPage** définit son contexte de données avec l’élément passé, ce qui est définie par les contrôles dans *ExpenseReportPage.xaml* lier à.</span><span class="sxs-lookup"><span data-stu-id="7a601-310">**ExpenseReportPage** sets its data context with the passed item, which is what the controls defined in *ExpenseReportPage.xaml* bind to.</span></span>

1. <span data-ttu-id="7a601-311">Ouvrez *ExpenseReportPage.xaml.vb* ou *ExpenseReportPage.xaml.cs*.</span><span class="sxs-lookup"><span data-stu-id="7a601-311">Open *ExpenseReportPage.xaml.vb* or *ExpenseReportPage.xaml.cs*.</span></span>

2. <span data-ttu-id="7a601-312">Ajoutez un constructeur qui prend un objet de façon à pouvoir transmettre les données de note de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7a601-312">Add a constructor that takes an object so you can pass the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#26](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseReportPage.xaml.cs#26)]
    [!code-vb[ExpenseIt#26](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseReportPage.xaml.vb#26)]

3. <span data-ttu-id="7a601-313">Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.</span><span class="sxs-lookup"><span data-stu-id="7a601-313">Open *`ExpenseItHome.xaml.vb`* or *`ExpenseItHome.xaml.cs`*.</span></span>

4. <span data-ttu-id="7a601-314">Modifier le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements pour appeler le nouveau constructeur en passant les données de rapport de frais de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7a601-314">Change the <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler to call the new constructor passing the expense report data of the selected person.</span></span>

    [!code-csharp[ExpenseIt#27](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml.cs#27)]
    [!code-vb[ExpenseIt#27](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseItHome.xaml.vb#27)]

## <a name="style-data-with-data-templates"></a><span data-ttu-id="7a601-315">Données de style avec les modèles de données</span><span class="sxs-lookup"><span data-stu-id="7a601-315">Style data with data templates</span></span>

<span data-ttu-id="7a601-316">Dans cette section, vous allez mettre à jour l’interface utilisateur pour chaque élément dans les listes liées aux données à l’aide de modèles de données.</span><span class="sxs-lookup"><span data-stu-id="7a601-316">In this section, you'll update the UI for each item in the data-bound lists by using data templates.</span></span>

1. <span data-ttu-id="7a601-317">Ouvrez *ExpenseReportPage.xaml*.</span><span class="sxs-lookup"><span data-stu-id="7a601-317">Open *ExpenseReportPage.xaml*.</span></span>

2. <span data-ttu-id="7a601-318">Lier le contenu de la « Name » et « Department » <xref:System.Windows.Controls.Label> éléments pour les données appropriées de propriété source.</span><span class="sxs-lookup"><span data-stu-id="7a601-318">Bind the content of the "Name" and "Department" <xref:System.Windows.Controls.Label> elements to the appropriate data source property.</span></span> <span data-ttu-id="7a601-319">Pour plus d’informations sur la liaison de données, consultez [vue d’ensemble de liaison de données](../data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a601-319">For more information about data binding, see [Data binding overview](../data/data-binding-overview.md).</span></span>

    [!code-xaml[ExpenseIt#31](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#31)]

3. <span data-ttu-id="7a601-320">Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez les modèles de données suivants, qui définissent comment afficher les données de rapport de frais :</span><span class="sxs-lookup"><span data-stu-id="7a601-320">After the opening <xref:System.Windows.Controls.Grid> element, add the following data templates, which define how to display the expense report data:</span></span>

    [!code-xaml[ExpenseIt#30](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#30)]

4. <span data-ttu-id="7a601-321">Remplacez le <xref:System.Windows.Controls.DataGridTextColumn> éléments avec <xref:System.Windows.Controls.DataGridTemplateColumn> sous le <xref:System.Windows.Controls.DataGrid> élément et appliquer les modèles.</span><span class="sxs-lookup"><span data-stu-id="7a601-321">Replace the <xref:System.Windows.Controls.DataGridTextColumn> elements with <xref:System.Windows.Controls.DataGridTemplateColumn> under the <xref:System.Windows.Controls.DataGrid> element and apply the templates to them.</span></span>

    [!code-xaml[ExpenseIt#32](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#32)]

5. <span data-ttu-id="7a601-322">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="7a601-322">Build and run the application.</span></span>

6. <span data-ttu-id="7a601-323">Sélectionnez une personne, puis le **vue** bouton.</span><span class="sxs-lookup"><span data-stu-id="7a601-323">Select a person and then select the **View** button.</span></span>

<span data-ttu-id="7a601-324">L’illustration suivante montre les deux pages de le `ExpenseIt` application avec des contrôles, styles, la disposition, liaison de données et modèles de données appliqués :</span><span class="sxs-lookup"><span data-stu-id="7a601-324">The following illustration shows both pages of the `ExpenseIt` application with controls, layout, styles, data binding, and data templates applied:</span></span>

![Les deux pages de l’application qui affiche la liste de noms et une note de frais.](./media/walkthrough-my-first-wpf-desktop-application/application-data-templates.png)

> [!NOTE]
> <span data-ttu-id="7a601-326">Cet exemple montre une fonctionnalité spécifique de WPF et ne respecte pas toutes les meilleures pratiques pour les éléments tels que la sécurité, la localisation et d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="7a601-326">This sample demonstrates a specific feature of WPF and doesn't follow all best practices for things like security, localization, and accessibility.</span></span> <span data-ttu-id="7a601-327">Pour une couverture complète de WPF et les .NET application meilleures pratiques de développement, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a601-327">For comprehensive coverage of WPF and the .NET app development best practices, see the following topics:</span></span>
>
> - [<span data-ttu-id="7a601-328">Accessibilité</span><span class="sxs-lookup"><span data-stu-id="7a601-328">Accessibility</span></span>](../../ui-automation/accessibility-best-practices.md)
>
> - [<span data-ttu-id="7a601-329">Sécurité</span><span class="sxs-lookup"><span data-stu-id="7a601-329">Security</span></span>](../security-wpf.md)
>
> - [<span data-ttu-id="7a601-330">Globalisation et localisation pour WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-330">WPF globalization and localization</span></span>](../advanced/wpf-globalization-and-localization-overview.md)
>
> - [<span data-ttu-id="7a601-331">Performances WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-331">WPF performance</span></span>](../advanced/optimizing-wpf-application-performance.md)

## <a name="next-steps"></a><span data-ttu-id="7a601-332">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7a601-332">Next steps</span></span>

<span data-ttu-id="7a601-333">Dans cette procédure pas à pas, vous avez appris un certain nombre de techniques pour la création d’une interface utilisateur à l’aide de Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="7a601-333">In this walkthrough you learned a number of techniques for creating a UI using Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="7a601-334">Vous devez maintenant avoir une compréhension élémentaire des blocs de construction d’une application de .NET lié aux données.</span><span class="sxs-lookup"><span data-stu-id="7a601-334">You should now have a basic understanding of the building blocks of a data-bound .NET app.</span></span> <span data-ttu-id="7a601-335">Pour plus d’informations sur les modèles d’architecture et de programmation WPF, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a601-335">For more information about the WPF architecture and programming models, see the following topics:</span></span>

- [<span data-ttu-id="7a601-336">Architecture de WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-336">WPF architecture</span></span>](../advanced/wpf-architecture.md)
- [<span data-ttu-id="7a601-337">Vue d’ensemble du langage XAML (WPF)</span><span class="sxs-lookup"><span data-stu-id="7a601-337">XAML overview (WPF)</span></span>](../advanced/xaml-overview-wpf.md)
- [<span data-ttu-id="7a601-338">Vue d’ensemble des propriétés de dépendance</span><span class="sxs-lookup"><span data-stu-id="7a601-338">Dependency properties overview</span></span>](../advanced/dependency-properties-overview.md)
- [<span data-ttu-id="7a601-339">Disposition</span><span class="sxs-lookup"><span data-stu-id="7a601-339">Layout</span></span>](../advanced/layout.md)

<span data-ttu-id="7a601-340">Pour plus d’informations sur la création d’applications, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a601-340">For more information about creating applications, see the following topics:</span></span>

- [<span data-ttu-id="7a601-341">Développement d’applications</span><span class="sxs-lookup"><span data-stu-id="7a601-341">Application development</span></span>](../app-development/index.md)
- [<span data-ttu-id="7a601-342">Contrôles</span><span class="sxs-lookup"><span data-stu-id="7a601-342">Controls</span></span>](../controls/index.md)
- [<span data-ttu-id="7a601-343">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="7a601-343">Data binding overview</span></span>](../data/data-binding-overview.md)
- [<span data-ttu-id="7a601-344">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="7a601-344">Graphics and multimedia</span></span>](../graphics-multimedia/index.md)
- [<span data-ttu-id="7a601-345">Documents dans WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-345">Documents in WPF</span></span>](../advanced/documents-in-wpf.md)

## <a name="see-also"></a><span data-ttu-id="7a601-346">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a601-346">See also</span></span>

- [<span data-ttu-id="7a601-347">Vue d’ensemble des panneaux</span><span class="sxs-lookup"><span data-stu-id="7a601-347">Panels overview</span></span>](../controls/panels-overview.md)
- [<span data-ttu-id="7a601-348">Vue d’ensemble de création de modèles de données</span><span class="sxs-lookup"><span data-stu-id="7a601-348">Data templating overview</span></span>](../data/data-templating-overview.md)
- [<span data-ttu-id="7a601-349">Créer une application WPF</span><span class="sxs-lookup"><span data-stu-id="7a601-349">Build a WPF application</span></span>](../app-development/building-a-wpf-application-wpf.md)
- [<span data-ttu-id="7a601-350">Styles et modèles</span><span class="sxs-lookup"><span data-stu-id="7a601-350">Styles and templates</span></span>](../controls/styles-and-templates.md)
