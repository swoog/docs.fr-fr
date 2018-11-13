---
title: Bien démarrer avec .NET Core sur macOS à l’aide de Visual Studio pour Mac
description: Cette rubrique vous guide lors de la création d’une application console simple à l’aide de Visual Studio pour Mac et de .NET Core.
author: guardrex
ms.author: mairaw
ms.date: 06/12/2017
ms.openlocfilehash: f751e7532e9627de3d3733476f7214654089e468
ms.sourcegitcommit: 5fd80619c760fa8c25d33a6f5661247cb65da465
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50744112"
---
# <a name="getting-started-with-net-core-on-macos-using-visual-studio-for-mac"></a><span data-ttu-id="76735-103">Bien démarrer avec .NET Core sur macOS à l’aide de Visual Studio pour Mac</span><span class="sxs-lookup"><span data-stu-id="76735-103">Getting started with .NET Core on macOS using Visual Studio for Mac</span></span>

<span data-ttu-id="76735-104">Visual Studio pour Mac fournit un environnement de développement intégré (IDE) complet pour le développement d’applications .NET Core.</span><span class="sxs-lookup"><span data-stu-id="76735-104">Visual Studio for Mac provides a full-featured Integrated Development Environment (IDE) for developing .NET Core applications.</span></span> <span data-ttu-id="76735-105">Cette rubrique vous guide lors de la création d’une application console simple à l’aide de Visual Studio pour Mac et de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="76735-105">This topic walks you through building a simple console application using Visual Studio for Mac and .NET Core.</span></span>

> [!NOTE]
> <span data-ttu-id="76735-106">Vos commentaires sont extrêmement précieux.</span><span class="sxs-lookup"><span data-stu-id="76735-106">Your feedback is highly valued.</span></span> <span data-ttu-id="76735-107">Il existe deux moyens de transmettre vos commentaires à l’équipe de développement sur Visual Studio pour Mac :</span><span class="sxs-lookup"><span data-stu-id="76735-107">There are two ways you can provide feedback to the development team on Visual Studio for Mac:</span></span>
> * <span data-ttu-id="76735-108">Dans Visual Studio pour Mac, sélectionnez **Aide** > **Signaler un problème** dans le menu ou **Signaler un problème** sur l’écran d’accueil, ce qui ouvre une fenêtre permettant de soumettre un rapport de bogue.</span><span class="sxs-lookup"><span data-stu-id="76735-108">In Visual Studio for Mac, select **Help** > **Report a Problem** from the menu or **Report a Problem** from the Welcome screen, which will open a window for filing a bug report.</span></span> <span data-ttu-id="76735-109">Vous pouvez effectuer le suivi de vos commentaires dans le portail de la [communauté des développeurs](https://developercommunity.visualstudio.com/spaces/8/index.html).</span><span class="sxs-lookup"><span data-stu-id="76735-109">You can track your feedback in the [Developer Community](https://developercommunity.visualstudio.com/spaces/8/index.html) portal.</span></span>
> * <span data-ttu-id="76735-110">Pour soumettre une suggestion, sélectionnez **Aide** > **Faire une suggestion** dans le menu ou **Faire une suggestion** sur l’écran d’accueil, ce qui vous amène à la [page web de la communauté des développeurs Visual Studio pour Mac](https://developercommunity.visualstudio.com/content/idea/post.html?space=41).</span><span class="sxs-lookup"><span data-stu-id="76735-110">To make a suggestion, select **Help** > **Provide a Suggestion** from the menu or **Provide a Suggestion** from the Welcome screen, which will take you to the [Visual Studio for Mac Developer Community webpage](https://developercommunity.visualstudio.com/content/idea/post.html?space=41).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="76735-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="76735-111">Prerequisites</span></span>

<span data-ttu-id="76735-112">Consultez la rubrique [Prérequis de .NET Core sur Mac](../../core/macos-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="76735-112">See the [Prerequisites for .NET Core on Mac](../../core/macos-prerequisites.md) topic.</span></span>

## <a name="getting-started"></a><span data-ttu-id="76735-113">Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="76735-113">Getting started</span></span>

<span data-ttu-id="76735-114">Si vous avez déjà installé les composants requis et Visual Studio pour Mac, ignorez cette section et passez à la [création d’un projet](#creating-a-project).</span><span class="sxs-lookup"><span data-stu-id="76735-114">If you've already installed the prerequisites and Visual Studio for Mac, skip this section and proceed to [Creating a project](#creating-a-project).</span></span> <span data-ttu-id="76735-115">Suivez ces étapes pour installer les composants requis et Visual Studio pour Mac :</span><span class="sxs-lookup"><span data-stu-id="76735-115">Follow these steps to install the prerequisites and Visual Studio for Mac:</span></span>

<span data-ttu-id="76735-116">Téléchargez le [programme d’installation de Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span><span class="sxs-lookup"><span data-stu-id="76735-116">Download the [Visual Studio for Mac installer](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span></span> <span data-ttu-id="76735-117">Exécutez le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="76735-117">Run the installer.</span></span> <span data-ttu-id="76735-118">Lisez et acceptez le contrat de licence.</span><span class="sxs-lookup"><span data-stu-id="76735-118">Read and accept the license agreement.</span></span> <span data-ttu-id="76735-119">Lors de l’installation, vous avez la possibilité d’installer Xamarin, une technologie de développement d’application mobile multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="76735-119">During the install, you're provided the opportunity to install Xamarin, a cross-platform mobile app development technology.</span></span> <span data-ttu-id="76735-120">L’installation de Xamarin et de ses composants associés est facultative pour le développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="76735-120">Installing Xamarin and its related components is optional for .NET Core development.</span></span> <span data-ttu-id="76735-121">Pour obtenir une vue d’ensemble du processus d’installation de Visual Studio pour Mac, consultez [Présentation de Visual Studio pour Mac](https://developer.xamarin.com/guides/cross-platform/visual-studio-mac/).</span><span class="sxs-lookup"><span data-stu-id="76735-121">For a walk-through of the Visual Studio for Mac install process, see [Introducing Visual Studio for Mac](https://developer.xamarin.com/guides/cross-platform/visual-studio-mac/).</span></span> <span data-ttu-id="76735-122">Une fois l’installation terminée, démarrez l’IDE Visual Studio pour Mac.</span><span class="sxs-lookup"><span data-stu-id="76735-122">When the install is complete, start the Visual Studio for Mac IDE.</span></span>

## <a name="creating-a-project"></a><span data-ttu-id="76735-123">Création d'un projet</span><span class="sxs-lookup"><span data-stu-id="76735-123">Creating a project</span></span>

1. <span data-ttu-id="76735-124">Sélectionnez **Nouveau projet** sur l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="76735-124">Select **New Project** on the Welcome screen.</span></span>

   ![Bouton Nouveau projet sur l’écran d’accueil Visual Studio pour Mac](./media/using-on-mac-vs/vsmac1.png)

1. <span data-ttu-id="76735-126">Dans la boîte de dialogue **Nouveau projet**, sélectionnez **App** dans le nœud **.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="76735-126">In the **New Project** dialog, select **App** under the **.NET Core** node.</span></span> <span data-ttu-id="76735-127">Sélectionnez le modèle **Application console** puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="76735-127">Select the **Console Application** template followed by **Next**.</span></span>

   ![Liste des modèles Nouveau projet](./media/using-on-mac-vs/vsmac2.png)

1. <span data-ttu-id="76735-129">Tapez « HelloWorld » comme **nom de projet**.</span><span class="sxs-lookup"><span data-stu-id="76735-129">Type "HelloWorld" for the **Project Name**.</span></span> <span data-ttu-id="76735-130">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="76735-130">Select **Create**.</span></span>

   ![Boîte de dialogue de configuration de votre nouvelle application console](./media/using-on-mac-vs/vsmac3.png)

1. <span data-ttu-id="76735-132">Attendez la restauration des dépendances du projet.</span><span class="sxs-lookup"><span data-stu-id="76735-132">Wait while the project's dependencies are restored.</span></span> <span data-ttu-id="76735-133">Le projet comporte un seul fichier C#, *Program.cs*, contenant une classe `Program` avec une méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="76735-133">The project has a single C# file, *Program.cs*, containing a `Program` class with a `Main` method.</span></span> <span data-ttu-id="76735-134">L’instruction `Console.WriteLine` affichera « Hello World! »</span><span class="sxs-lookup"><span data-stu-id="76735-134">The `Console.WriteLine` statement will output "Hello World!"</span></span> <span data-ttu-id="76735-135">dans la console lorsque l’application est exécutée.</span><span class="sxs-lookup"><span data-stu-id="76735-135">to the console when the app is run.</span></span>

   ![Fenêtre principale avec le fichier Program.cs ouvert](./media/using-on-mac-vs/vsmac4.png)

## <a name="run-the-application"></a><span data-ttu-id="76735-137">Exécuter l'application</span><span class="sxs-lookup"><span data-stu-id="76735-137">Run the application</span></span>

<span data-ttu-id="76735-138">Exécutez l’application en mode débogage à l’aide de <kbd>F5</kbd> ou en mode release avec <kbd>CTRL</kbd>+<kbd>F5</kbd>.</span><span class="sxs-lookup"><span data-stu-id="76735-138">Run the app in Debug mode using <kbd>F5</kbd> or in Release mode using <kbd>CTRL</kbd>+<kbd>F5</kbd>.</span></span>

![Le volet de sortie de l’application affiche Hello World!](./media/using-on-mac-vs/vsmac5.png)

## <a name="next-step"></a><span data-ttu-id="76735-140">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="76735-140">Next step</span></span>

<span data-ttu-id="76735-141">La rubrique [Génération d’une solution .NET Core complète sur macOS à l’aide de Visual Studio pour Mac](using-on-mac-vs-full-solution.md) vous montre comment créer une solution complète .NET Core qui inclut une bibliothèque réutilisable et un test unitaire.</span><span class="sxs-lookup"><span data-stu-id="76735-141">The [Building a complete .NET Core solution on macOS using Visual Studio for Mac](using-on-mac-vs-full-solution.md) topic shows you how to build a complete .NET Core solution that includes a reusable library and unit testing.</span></span>
