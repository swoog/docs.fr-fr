---
title: Bien démarrer avec C# et Visual Studio Code - Guide C#
description: Découvrez comment créer et déboguer votre première application .NET Core en C# à l’aide de Visual Studio Code.
author: kendrahavens
ms.author: mairaw
ms.date: 09/27/2017
ms.topic: conceptual
ms.prod: .net
ms.technology: devlang-csharp
ms.workload:
- dotnetcore
ms.openlocfilehash: d4ee1c9ef66ef61156453786f65d16470d7a5ea2
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="get-started-with-c-and-visual-studio-code"></a><span data-ttu-id="fab4d-103">Bien démarrer avec C# et Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fab4d-103">Get Started with C# and Visual Studio Code</span></span>

<span data-ttu-id="fab4d-104">.NET Core vous offre une plateforme rapide et évolutive pour la création d’applications qui s’exécutent sur Windows, Linux et Mac OS.</span><span class="sxs-lookup"><span data-stu-id="fab4d-104">.NET Core gives you a fast and modular platform for creating applications that run on Windows, Linux, and macOS.</span></span> <span data-ttu-id="fab4d-105">Utilisez Visual Studio Code avec l’extension de langage C# pour une expérience d’édition puissante avec prise en charge complète de C# IntelliSense (saisie semi-automatique intelligente de code).</span><span class="sxs-lookup"><span data-stu-id="fab4d-105">Use Visual Studio Code with the C# extension to get a powerful editing experience with full support for C# IntelliSense (smart code completion) and debugging.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fab4d-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fab4d-106">Prerequisites</span></span>

1. <span data-ttu-id="fab4d-107">Installez [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="fab4d-107">Install [Visual Studio Code](https://code.visualstudio.com/).</span></span>
2. <span data-ttu-id="fab4d-108">Installez le [SDK .NET Core](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="fab4d-108">Install the [.NET Core SDK](https://www.microsoft.com/net/download/core).</span></span>
3. <span data-ttu-id="fab4d-109">Installez l’[extension C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp) pour Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="fab4d-109">Install the [C# extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp) for Visual Studio Code.</span></span> <span data-ttu-id="fab4d-110">Pour plus d’informations sur l’installation d’extensions pour Visual Studio Code, consultez [Place de marché des extensions VS Code](https://code.visualstudio.com/docs/editor/extension-gallery).</span><span class="sxs-lookup"><span data-stu-id="fab4d-110">For more information about how to install extensions on Visual Studio Code, see [VS Code Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-gallery).</span></span>

## <a name="hello-world"></a><span data-ttu-id="fab4d-111">Hello World</span><span class="sxs-lookup"><span data-stu-id="fab4d-111">Hello World</span></span>

<span data-ttu-id="fab4d-112">Commençons par un programme « Hello World » simple sur .NET Core :</span><span class="sxs-lookup"><span data-stu-id="fab4d-112">Let's get started with a simple "Hello World" program on .NET Core:</span></span>

1. <span data-ttu-id="fab4d-113">Ouvrez un projet :</span><span class="sxs-lookup"><span data-stu-id="fab4d-113">Open a project:</span></span>

    * <span data-ttu-id="fab4d-114">Ouvrez Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="fab4d-114">Open Visual Studio Code.</span></span>
    * <span data-ttu-id="fab4d-115">Cliquez sur l’icône Explorer dans le menu de gauche, puis sur **Ouvrir le dossier**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-115">Click on the Explorer icon on the left menu and then click **Open Folder**.</span></span>
    * <span data-ttu-id="fab4d-116">Sélectionnez **Fichier** > **Ouvrir le dossier** dans le menu principal pour ouvrir le dossier dans lequel vous souhaitez que votre projet C# se trouve et cliquez sur **Sélectionner le dossier**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-116">Select **File** > **Open Folder** from the main menu to open the folder you want your C# project to be in and click **Select Folder**.</span></span> <span data-ttu-id="fab4d-117">Dans notre exemple, nous créons un dossier pour notre projet nommé *HelloWorld*.</span><span class="sxs-lookup"><span data-stu-id="fab4d-117">For our example, we're creating a folder for our project named *HelloWorld*.</span></span>

      ![VSCodeOpenFolder](media/with-visual-studio-code/vscodeopenfolder.png)

2. <span data-ttu-id="fab4d-119">Initialiser un projet C# :</span><span class="sxs-lookup"><span data-stu-id="fab4d-119">Initialize a C# project:</span></span>
    * <span data-ttu-id="fab4d-120">Ouvrez le terminal intégré à partir de Visual Studio Code en sélectionnant **Vue** > **Terminal intégré** dans le menu principal.</span><span class="sxs-lookup"><span data-stu-id="fab4d-120">Open the Integrated Terminal from Visual Studio Code by selecting **View** > **Integrated Terminal** from the main menu.</span></span>
    * <span data-ttu-id="fab4d-121">Dans la fenêtre de Terminal, tapez `dotnet new console`.</span><span class="sxs-lookup"><span data-stu-id="fab4d-121">In the terminal window, type `dotnet new console`.</span></span>
    * <span data-ttu-id="fab4d-122">Cette commande crée un fichier `Program.cs` dans votre dossier avec un simple programme « Hello World » déjà écrit, ainsi qu’un fichier projet C# nommé `HelloWorld.csproj`.</span><span class="sxs-lookup"><span data-stu-id="fab4d-122">This command creates a `Program.cs` file in your folder with a simple "Hello World" program already written, along with a C# project file named `HelloWorld.csproj`.</span></span>

      ![La nouvelle commande dotnet](media/with-visual-studio-code/dotnetnew.png)

3. <span data-ttu-id="fab4d-124">Résolution des ressources de génération :</span><span class="sxs-lookup"><span data-stu-id="fab4d-124">Resolve the build assets:</span></span>

    * <span data-ttu-id="fab4d-125">Pour **.NET Core 1.x**, tapez `dotnet restore`.</span><span class="sxs-lookup"><span data-stu-id="fab4d-125">For **.NET Core 1.x**, type `dotnet restore`.</span></span> <span data-ttu-id="fab4d-126">Exécuter `dotnet restore` vous donne accès aux packages .NET Core qui sont nécessaires pour générer votre projet.</span><span class="sxs-lookup"><span data-stu-id="fab4d-126">Running `dotnet restore` gives you access to the  required .NET Core packages that are needed to build your project.</span></span>

      ![La commande dotnet restore](media/with-visual-studio-code/dotnetrestore.png)

      [!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

4. <span data-ttu-id="fab4d-128">Exécutez le programme Hello World :</span><span class="sxs-lookup"><span data-stu-id="fab4d-128">Run the "Hello World" program:</span></span>

    * <span data-ttu-id="fab4d-129">Tapez `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="fab4d-129">Type `dotnet run`.</span></span> 

      ![La commande dotnet run](media/with-visual-studio-code/dotnetrun.png)

<span data-ttu-id="fab4d-131">Vous pouvez également regarder un court didacticiel vidéo pour plus d’informations sur la configuration sur [Windows](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core), [macOS](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core-on-MacOS) ou [Linux](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-Csharp-dotnet-Core-Ubuntu).</span><span class="sxs-lookup"><span data-stu-id="fab4d-131">You can also watch a short video tutorial for further setup help on [Windows](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core), [macOS](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core-on-MacOS), or [Linux](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-Csharp-dotnet-Core-Ubuntu).</span></span>

## <a name="debug"></a><span data-ttu-id="fab4d-132">Débogage</span><span class="sxs-lookup"><span data-stu-id="fab4d-132">Debug</span></span>

1. <span data-ttu-id="fab4d-133">Ouvrez *Program.cs* en cliquant dessus.</span><span class="sxs-lookup"><span data-stu-id="fab4d-133">Open *Program.cs* by clicking on it.</span></span> <span data-ttu-id="fab4d-134">La première fois que vous ouvrez un fichier C# dans Visual Studio Code, [OmniSharp](http://www.omnisharp.net/) se charge dans l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="fab4d-134">The first time you open a C# file in Visual Studio Code, [OmniSharp](http://www.omnisharp.net/) loads in the editor.</span></span>

    ![Ouvrez le fichier Program.cs](media/with-visual-studio-code/opencs.png)

2. <span data-ttu-id="fab4d-136">Visual Studio Code doit vous inviter à ajouter les ressources manquantes pour générer et déboguer votre application.</span><span class="sxs-lookup"><span data-stu-id="fab4d-136">Visual Studio Code should prompt you to add the missing assets to build and debug your app.</span></span> <span data-ttu-id="fab4d-137">Sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-137">Select **Yes**.</span></span> 

    ![Invite pour les fichiers manquants](media/with-visual-studio-code/missing-assets.png)

3. <span data-ttu-id="fab4d-139">Pour ouvrir la vue de débogage, cliquez sur l’icône de débogage dans le menu de gauche.</span><span class="sxs-lookup"><span data-stu-id="fab4d-139">To open the Debug view, click on the Debugging icon on the left side menu.</span></span>

    ![Ouvrez l'onglet Déboguer](media/with-visual-studio-code/opendebug.png)

4. <span data-ttu-id="fab4d-141">Cherchez la flèche verte en haut du volet.</span><span class="sxs-lookup"><span data-stu-id="fab4d-141">Locate the green arrow at the top of the pane.</span></span> <span data-ttu-id="fab4d-142">Assurez-vous que `.NET Core Launch (console)` est sélectionné dans la liste déroulante à côté du volet.</span><span class="sxs-lookup"><span data-stu-id="fab4d-142">Make sure the drop-down next to it has `.NET Core Launch (console)` selected.</span></span>

    ![Sélection de .NET Core](media/with-visual-studio-code/selectcore.png)

5. <span data-ttu-id="fab4d-144">Ajoutez un point d’arrêt à votre projet en cliquant sur la **marge de l’éditeur**, qui est l’espace à gauche des numéros de ligne dans l’éditeur, à côté de la ligne 9.</span><span class="sxs-lookup"><span data-stu-id="fab4d-144">Add a breakpoint to your project by clicking on the **editor margin**, which is the space on the left of the line numbers in the editor, next to line 9.</span></span>

    ![Définition d'un point d'arrêt](media/with-visual-studio-code/setbreakpoint.png)

6. <span data-ttu-id="fab4d-146">Pour démarrer le débogage, sélectionnez <kbd>F5</kbd> ou la flèche verte.</span><span class="sxs-lookup"><span data-stu-id="fab4d-146">To start debugging, select <kbd>F5</kbd> or the green arrow.</span></span> <span data-ttu-id="fab4d-147">Le débogueur arrête l’exécution de votre programme lorsqu’il atteint le point d’arrêt que vous avez défini à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="fab4d-147">The debugger stops execution of your program when it reaches the breakpoint you set in the previous step.</span></span>
    * <span data-ttu-id="fab4d-148">Pendant le débogage, vous pouvez afficher vos variables locales dans le volet supérieur gauche ou utiliser la console de débogage.</span><span class="sxs-lookup"><span data-stu-id="fab4d-148">While debugging, you can view your local variables in the top left pane or use the debug console.</span></span>

    ![Exécuter et déboguer](media/with-visual-studio-code/rundebug.png)

7. <span data-ttu-id="fab4d-150">Cliquez sur la flèche verte en haut pour continuer le débogage, ou sélectionnez le carré rouge en haut pour arrêter.</span><span class="sxs-lookup"><span data-stu-id="fab4d-150">Select the green arrow at the top to continue debugging, or select the red square at the top to stop.</span></span>

> [!TIP] 
> <span data-ttu-id="fab4d-151">Pour obtenir plus d’informations et de conseils de dépannage sur le débogage de .NET Core avec OmniSharp dans Visual Studio Code, consultez [Instructions de configuration du débogueur .NET Core](https://github.com/OmniSharp/omnisharp-vscode/blob/master/debugger.md).</span><span class="sxs-lookup"><span data-stu-id="fab4d-151">For more information and troubleshooting tips on .NET Core debugging with OmniSharp in Visual Studio Code, see [Instructions for setting up the .NET Core debugger](https://github.com/OmniSharp/omnisharp-vscode/blob/master/debugger.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fab4d-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fab4d-152">See also</span></span>
<span data-ttu-id="fab4d-153">[Configuration de Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview) </span><span class="sxs-lookup"><span data-stu-id="fab4d-153">[Setting up Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview) </span></span>  
[<span data-ttu-id="fab4d-154">Débogage dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fab4d-154">Debugging in Visual Studio Code</span></span>](https://code.visualstudio.com/Docs/editor/debugging)
