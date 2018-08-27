---
title: Créer un InkCanvas dans une application WPF dans Visual Studio
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- procedural code in lieu of XAML [WPF]
- XAML [WPF], procedural code in lieu of
- InkCanvas (WPF)
ms.assetid: 760332dd-594a-475d-865b-01659db8cab7
ms.openlocfilehash: 600d8528125606c6e1af5b031e2fc31aabb79206
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925042"
---
# <a name="get-started-with-ink-in-wpf"></a><span data-ttu-id="8bda0-102">Bien démarrer avec l’encre dans WPF</span><span class="sxs-lookup"><span data-stu-id="8bda0-102">Get Started with Ink in WPF</span></span>

<span data-ttu-id="8bda0-103">Windows Presentation Foundation (WPF) possède une fonctionnalité de l’encre qui permet de facilement incorporer l’encre numérique dans votre application.</span><span class="sxs-lookup"><span data-stu-id="8bda0-103">Windows Presentation Foundation (WPF) has an ink feature that makes it easy to incorporate digital ink into your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8bda0-104">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8bda0-104">Prerequisites</span></span>

<span data-ttu-id="8bda0-105">Pour utiliser les exemples suivants, tout d’abord [installer Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).</span><span class="sxs-lookup"><span data-stu-id="8bda0-105">To use the following examples, first [install Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).</span></span> <span data-ttu-id="8bda0-106">Cela permet également de savoir comment écrire des applications WPF de base.</span><span class="sxs-lookup"><span data-stu-id="8bda0-106">It also helps to know how to write basic WPF apps.</span></span> <span data-ttu-id="8bda0-107">Pour bien démarrer avec WPF, consultez [procédure pas à pas : Ma première application de bureau WPF](../../../../docs/framework/wpf/getting-started/walkthrough-my-first-wpf-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="8bda0-107">For help getting started with WPF, see [Walkthrough: My first WPF desktop application](../../../../docs/framework/wpf/getting-started/walkthrough-my-first-wpf-desktop-application.md).</span></span>

## <a name="quick-start"></a><span data-ttu-id="8bda0-108">Guide de démarrage rapide</span><span class="sxs-lookup"><span data-stu-id="8bda0-108">Quick Start</span></span>

<span data-ttu-id="8bda0-109">Cette section vous permet d’écrire une application WPF simple qui collecte d’encre.</span><span class="sxs-lookup"><span data-stu-id="8bda0-109">This section helps you write a simple WPF application that collects ink.</span></span>

### <a name="got-ink"></a><span data-ttu-id="8bda0-110">Vous avez l’encre ?</span><span class="sxs-lookup"><span data-stu-id="8bda0-110">Got Ink?</span></span>

<span data-ttu-id="8bda0-111">Pour créer une application WPF qui prend en charge de l’encre :</span><span class="sxs-lookup"><span data-stu-id="8bda0-111">To create a WPF app that supports ink:</span></span>

1. <span data-ttu-id="8bda0-112">Ouvrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8bda0-112">Open Visual Studio.</span></span>

2. <span data-ttu-id="8bda0-113">Créer un nouveau **application WPF**.</span><span class="sxs-lookup"><span data-stu-id="8bda0-113">Create a new **WPF App**.</span></span>

   <span data-ttu-id="8bda0-114">Dans le **nouveau projet** boîte de dialogue, développez le **installé** > **Visual C#** ou **Visual Basic**  >   **Windows Desktop** catégorie.</span><span class="sxs-lookup"><span data-stu-id="8bda0-114">In the **New Project** dialog, expand the **Installed** > **Visual C#** or **Visual Basic** > **Windows Desktop** category.</span></span> <span data-ttu-id="8bda0-115">Ensuite, sélectionnez le **application WPF (.NET Framework)** modèle d’application.</span><span class="sxs-lookup"><span data-stu-id="8bda0-115">Then, select the **WPF App (.NET Framework)** app template.</span></span> <span data-ttu-id="8bda0-116">Entrez un nom, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bda0-116">Enter a name, and then select **OK**.</span></span>

   <span data-ttu-id="8bda0-117">Visual Studio crée le projet, et *MainWindow.xaml* s’ouvre dans le concepteur.</span><span class="sxs-lookup"><span data-stu-id="8bda0-117">Visual Studio creates the project, and *MainWindow.xaml* opens in the designer.</span></span>

3. <span data-ttu-id="8bda0-118">Type `<InkCanvas/>` entre le `<Grid>` balises.</span><span class="sxs-lookup"><span data-stu-id="8bda0-118">Type `<InkCanvas/>` between the `<Grid>` tags.</span></span>

   ![Concepteur XAML avec la balise de InkCanvas](media/getting-started-with-ink/inkcanvas-xaml.png)

4. <span data-ttu-id="8bda0-120">Appuyez sur **F5** pour lancer votre application dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="8bda0-120">Press **F5** to launch your application in the debugger.</span></span>

5. <span data-ttu-id="8bda0-121">À l’aide d’un stylet ou une souris, écrire **Bonjour** dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8bda0-121">Using a stylus or mouse, write **hello world** in the window.</span></span>

<span data-ttu-id="8bda0-122">Vous avez écrit l’équivalent de l’encre d’une application « hello world » avec des séquences de touches que 12 !</span><span class="sxs-lookup"><span data-stu-id="8bda0-122">You've written the ink equivalent of a "hello world" application with only 12 keystrokes!</span></span>

### <a name="spice-up-your-app"></a><span data-ttu-id="8bda0-123">Pimenter votre application</span><span class="sxs-lookup"><span data-stu-id="8bda0-123">Spice Up Your App</span></span>

<span data-ttu-id="8bda0-124">Tirez parti de certaines fonctionnalités de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bda0-124">Let’s take advantage of some features of the WPF.</span></span> <span data-ttu-id="8bda0-125">Remplacez tous les éléments entre les balises \<fenêtre > balises par le balisage suivant :</span><span class="sxs-lookup"><span data-stu-id="8bda0-125">Replace everything between the opening and closing \<Window> tags with the following markup:</span></span>

```xaml
<Page>
  <InkCanvas Name="myInkCanvas" MouseRightButtonUp="RightMouseUpHandler">
    <InkCanvas.Background>
      <LinearGradientBrush>
        <GradientStop Color="Yellow" Offset="0.0" />
          <GradientStop Color="Blue" Offset="0.5" />
            <GradientStop Color="HotPink" Offset="1.0" />
              </LinearGradientBrush>
    </InkCanvas.Background>
  </InkCanvas>
</Page>
```

<span data-ttu-id="8bda0-126">Ce XAML crée un arrière-plan de pinceau de dégradé sur votre surface d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="8bda0-126">This XAML creates a gradient brush background on your inking surface.</span></span>

![Couleurs de dégradé sur l’écriture manuscrite surface dans une application WPF](media/getting-started-with-ink/gradient-colors.png)

### <a name="add-some-code-behind-the-xaml"></a><span data-ttu-id="8bda0-128">Ajouter du Code derrière le XAML</span><span class="sxs-lookup"><span data-stu-id="8bda0-128">Add Some Code Behind the XAML</span></span>

<span data-ttu-id="8bda0-129">Bien que XAML rend très facile de concevoir l’interface utilisateur, n’importe quelle application réelle doit ajouter du code pour gérer les événements.</span><span class="sxs-lookup"><span data-stu-id="8bda0-129">While XAML makes it very easy to design the user interface, any real-world application needs to add code to handle events.</span></span> <span data-ttu-id="8bda0-130">Voici un exemple simple qui se concentre sur l’encre en réponse à un clic droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="8bda0-130">Here is a simple example that zooms in on the ink in response to a right-click from a mouse.</span></span>

1. <span data-ttu-id="8bda0-131">Définir le `MouseRightButtonUp` gestionnaire dans votre XAML :</span><span class="sxs-lookup"><span data-stu-id="8bda0-131">Set the `MouseRightButtonUp` handler in your XAML:</span></span>

   [!code-xaml[DigitalInkTopics#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#3)]

1. <span data-ttu-id="8bda0-132">Dans **l’Explorateur de solutions**, développez MainWindow.xaml et ouvrez le fichier code-behind (MainWindow.xaml.cs ou MainWindow.xaml.vb).</span><span class="sxs-lookup"><span data-stu-id="8bda0-132">In **Solution Explorer**, expand MainWindow.xaml and open the code-behind file (MainWindow.xaml.cs or MainWindow.xaml.vb).</span></span> <span data-ttu-id="8bda0-133">Ajoutez le code de gestionnaire d’événements suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bda0-133">Add the following event handler code:</span></span>

   [!code-csharp[DigitalInkTopics#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml.cs#4)]
   [!code-vb[DigitalInkTopics#4](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window2.xaml.vb#4)]

1. <span data-ttu-id="8bda0-134">Exécutez l'application.</span><span class="sxs-lookup"><span data-stu-id="8bda0-134">Run the application.</span></span> <span data-ttu-id="8bda0-135">Ajouter du contenu de texte, puis le bouton droit de la souris ou effectuer un équivalent d’appuyer et maintenir un stylet.</span><span class="sxs-lookup"><span data-stu-id="8bda0-135">Add some ink, and then right-click with the mouse or perform a press-and-hold equivalent with a stylus.</span></span>

   <span data-ttu-id="8bda0-136">L’affichage effectue un zoom avant dans chaque fois que vous cliquez avec le bouton droit de la souris.</span><span class="sxs-lookup"><span data-stu-id="8bda0-136">The display zooms in each time you click with the right mouse button.</span></span>

### <a name="use-procedural-code-instead-of-xaml"></a><span data-ttu-id="8bda0-137">Utiliser du Code procédural au lieu de XAML</span><span class="sxs-lookup"><span data-stu-id="8bda0-137">Use Procedural Code Instead of XAML</span></span>

<span data-ttu-id="8bda0-138">Vous pouvez accéder à toutes les fonctionnalités WPF à partir de code procédural.</span><span class="sxs-lookup"><span data-stu-id="8bda0-138">You can access all WPF features from procedural code.</span></span> <span data-ttu-id="8bda0-139">Suivez ces étapes pour créer une application « Hello Ink World » pour WPF qui n’utilise pas n’importe quel XAML du tout.</span><span class="sxs-lookup"><span data-stu-id="8bda0-139">Follow these steps to create a "Hello Ink World" application for WPF that doesn’t use any XAML at all.</span></span>

1. <span data-ttu-id="8bda0-140">Créer un nouveau projet d’application console dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8bda0-140">Create a new console application project in Visual Studio.</span></span>

   <span data-ttu-id="8bda0-141">Dans le **nouveau projet** boîte de dialogue, développez le **installé** > **Visual C#** ou **Visual Basic**  >   **Windows Desktop** catégorie.</span><span class="sxs-lookup"><span data-stu-id="8bda0-141">In the **New Project** dialog, expand the **Installed** > **Visual C#** or **Visual Basic** > **Windows Desktop** category.</span></span> <span data-ttu-id="8bda0-142">Ensuite, sélectionnez le **application Console (.NET Framework)** modèle d’application.</span><span class="sxs-lookup"><span data-stu-id="8bda0-142">Then, select the **Console App (.NET Framework)** app template.</span></span> <span data-ttu-id="8bda0-143">Entrez un nom, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8bda0-143">Enter a name, and then select **OK**.</span></span>

1. <span data-ttu-id="8bda0-144">Collez le code suivant dans le fichier Program.cs ou Program.vb :</span><span class="sxs-lookup"><span data-stu-id="8bda0-144">Paste the following code into the Program.cs or Program.vb file:</span></span>

   [!code-csharp[InkCanvasConsoleApp#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasConsoleApp/CSharp/Program.cs#1)]
   [!code-vb[InkCanvasConsoleApp#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InkCanvasConsoleApp/VisualBasic/Module1.vb#1)]

1. <span data-ttu-id="8bda0-145">Ajouter des références aux assemblys PresentationCore, PresentationFramework et WindowsBase en cliquant sur **références** dans **l’Explorateur de solutions** et en choisissant **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="8bda0-145">Add references to the PresentationCore, PresentationFramework, and WindowsBase assemblies by right-clicking on **References** in **Solution Explorer** and choosing **Add Reference**.</span></span>

   ![Gestionnaire de références montrant PresentationCore et PresentationFramework](media/getting-started-with-ink/references.png)

1. <span data-ttu-id="8bda0-147">Générez l’application en appuyant sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="8bda0-147">Build the application by pressing **F5**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bda0-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bda0-148">See Also</span></span>

- [<span data-ttu-id="8bda0-149">Encre numérique</span><span class="sxs-lookup"><span data-stu-id="8bda0-149">Digital Ink</span></span>](../../../../docs/framework/wpf/advanced/digital-ink.md)
- [<span data-ttu-id="8bda0-150">Collecte d'encre</span><span class="sxs-lookup"><span data-stu-id="8bda0-150">Collecting Ink</span></span>](../../../../docs/framework/wpf/advanced/collecting-ink.md)
- [<span data-ttu-id="8bda0-151">Reconnaissance d'écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="8bda0-151">Handwriting Recognition</span></span>](../../../../docs/framework/wpf/advanced/handwriting-recognition.md)
- [<span data-ttu-id="8bda0-152">Stockage de l’encre</span><span class="sxs-lookup"><span data-stu-id="8bda0-152">Storing Ink</span></span>](../../../../docs/framework/wpf/advanced/storing-ink.md)
