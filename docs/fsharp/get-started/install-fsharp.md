---
title: 'Installer F #'
description: 'Découvrez comment installer F # en fonction de votre environnement.'
ms.date: 08/28/2018
ms.openlocfilehash: 909e1c07ff7f6d52db77a987639d1c749146fdca
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49120932"
---
# <a name="install-f"></a><span data-ttu-id="e1467-103">Installer F #</span><span class="sxs-lookup"><span data-stu-id="e1467-103">Install F#</span></span> #

<span data-ttu-id="e1467-104">Vous pouvez installer F # de plusieurs façons, selon votre environnement.</span><span class="sxs-lookup"><span data-stu-id="e1467-104">You can install F# in multiple ways, depending on your environment.</span></span>

## <a name="install-f-with-visual-studio"></a><span data-ttu-id="e1467-105">Installer F # avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e1467-105">Install F# with Visual Studio</span></span>

<span data-ttu-id="e1467-106">Si vous effectuez un téléchargement [Visual Studio](https://visualstudio.microsoft.com/) pour la première fois, il installera d’abord le programme d’installation de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e1467-106">If you're downloading [Visual Studio](https://visualstudio.microsoft.com/) for the first time, it will first install the Visual Studio installer.</span></span> <span data-ttu-id="e1467-107">Installez la référence SKU appropriée de Visual Studio à partir du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="e1467-107">Install the appropriate SKU of Visual Studio from the installer.</span></span> <span data-ttu-id="e1467-108">Si vous avez déjà installé, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="e1467-108">If you already have it installed, click **Modify**.</span></span>

<span data-ttu-id="e1467-109">Vous verrez ensuite une liste de charges de travail.</span><span class="sxs-lookup"><span data-stu-id="e1467-109">You'll next see a list of Workloads.</span></span> <span data-ttu-id="e1467-110">Sélectionnez **ASP.NET et développement web** qui installera la prise en charge F # et .NET Core pour les projets ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e1467-110">Select **ASP.NET and web development** which will install F# support and .NET Core support for ASP.NET Core projects.</span></span>

<span data-ttu-id="e1467-111">Ensuite, cliquez sur **modifier** dans l’angle inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="e1467-111">Next, click **Modify** in the lower right-hand side.</span></span>  <span data-ttu-id="e1467-112">Cela installera tout ce dont vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e1467-112">This will install everything you have selected.</span></span> <span data-ttu-id="e1467-113">Vous pouvez ensuite ouvrir Visual Studio 2017 avec prise en charge de langage F # en cliquant sur **lancer**.</span><span class="sxs-lookup"><span data-stu-id="e1467-113">You can then open Visual Studio 2017 with F# language support by clicking **Launch**.</span></span>

## <a name="install-f-with-visual-studio-for-mac"></a><span data-ttu-id="e1467-114">Installer F # avec Visual Studio pour Mac</span><span class="sxs-lookup"><span data-stu-id="e1467-114">Install F# with Visual Studio for Mac</span></span>

<span data-ttu-id="e1467-115">F # est installé par défaut dans [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/), quelle que soit la configuration que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="e1467-115">F# is installed by default in [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/), no matter which configuration you choose.</span></span>

<span data-ttu-id="e1467-116">Une fois l’installation terminée, cliquez sur « Démarrer Visual Studio ».</span><span class="sxs-lookup"><span data-stu-id="e1467-116">After the install completes, choose "Start Visual Studio".</span></span> <span data-ttu-id="e1467-117">Vous pouvez également la lancer via Finder sur macOS.</span><span class="sxs-lookup"><span data-stu-id="e1467-117">You can also launch it through Finder on macOS.</span></span>

## <a name="install-f-with-visual-studio-code"></a><span data-ttu-id="e1467-118">Installer F # avec Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e1467-118">Install F# with Visual Studio Code</span></span>

<span data-ttu-id="e1467-119">Vous devez avoir [git installé](https://git-scm.com/download) et disponible sur votre chemin d’accès s’utiliser des modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="e1467-119">You must have [git installed](https://git-scm.com/download) and available on your PATH to make use of project templates.</span></span> <span data-ttu-id="e1467-120">Vous pouvez vérifier qu’il est correctement installé en tapant `git --version` à l’invite de commandes et en appuyant sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="e1467-120">You can verify that it is installed correctly by typing `git --version` at a command prompt and pressing **Enter**.</span></span>

### <a name="macostabmacos"></a>[<span data-ttu-id="e1467-121">macOS</span><span class="sxs-lookup"><span data-stu-id="e1467-121">macOS</span></span>](#tab/macos)

<span data-ttu-id="e1467-122">[Mono](http://www.mono-project.com) est utilisé pour [F # Interactive](../tutorials/fsharp-interactive/index.md) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="e1467-122">[Mono](http://www.mono-project.com) is used for [F# Interactive](../tutorials/fsharp-interactive/index.md) support.</span></span> <span data-ttu-id="e1467-123">Le moyen le plus simple pour installer Mono sur macOS est via Homebrew.</span><span class="sxs-lookup"><span data-stu-id="e1467-123">The easiest way to install Mono on macOS is via Homebrew.</span></span> <span data-ttu-id="e1467-124">Tapez simplement la commande suivante dans votre terminal :</span><span class="sxs-lookup"><span data-stu-id="e1467-124">Simply type the following into your terminal:</span></span>

```console
brew install mono
```

<span data-ttu-id="e1467-125">Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="e1467-125">Also install the [.NET Core SDK](https://www.microsoft.com/net/download).</span></span>

### <a name="linuxtablinux"></a>[<span data-ttu-id="e1467-126">Linux</span><span class="sxs-lookup"><span data-stu-id="e1467-126">Linux</span></span>](#tab/linux)

<span data-ttu-id="e1467-127">[Mono](https://www.mono-project.com) est utilisé pour [F # Interactive](../tutorials/fsharp-interactive/index.md) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="e1467-127">[Mono](https://www.mono-project.com) is used for [F# Interactive](../tutorials/fsharp-interactive/index.md) support.</span></span> <span data-ttu-id="e1467-128">Si vous êtes sur Debian ou Ubuntu, vous pouvez utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e1467-128">If you're on Debian or Ubuntu, you can use the following:</span></span>

```console
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

<span data-ttu-id="e1467-129">Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="e1467-129">Also install the [.NET Core SDK](https://www.microsoft.com/net/download).</span></span>

### <a name="windowstabwindows"></a>[<span data-ttu-id="e1467-130">Windows</span><span class="sxs-lookup"><span data-stu-id="e1467-130">Windows</span></span>](#tab/windows)

<span data-ttu-id="e1467-131">Installer [Visual Studio avec prise en charge F #](#install-f-with-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="e1467-131">Install [Visual Studio with F# support](#install-f-with-visual-studio).</span></span> <span data-ttu-id="e1467-132">Cette opération installe tous les composants nécessaires pour écrire, compiler et exécuter du code F #.</span><span class="sxs-lookup"><span data-stu-id="e1467-132">This installs all the necessary components to write, compile, and execute F# code.</span></span>

<span data-ttu-id="e1467-133">Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download/).</span><span class="sxs-lookup"><span data-stu-id="e1467-133">Also install the [.NET Core SDK](https://www.microsoft.com/net/download/).</span></span>

---

<span data-ttu-id="e1467-134">Vous devez ensuite [Visual Studio Code](https://code.visualstudio.com) installé.</span><span class="sxs-lookup"><span data-stu-id="e1467-134">You will then need [Visual Studio Code](https://code.visualstudio.com) installed.</span></span>

<span data-ttu-id="e1467-135">Ensuite, cliquez sur l’icône des Extensions et recherchez « Ionide » :</span><span class="sxs-lookup"><span data-stu-id="e1467-135">Next, click the Extensions icon and search for "Ionide":</span></span>

<span data-ttu-id="e1467-136">Le plug-in uniquement requis pour la prise en charge F # dans Visual Studio Code est [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span><span class="sxs-lookup"><span data-stu-id="e1467-136">The only plugin required for F# support in Visual Studio Code is [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span></span> <span data-ttu-id="e1467-137">Toutefois, vous pouvez également installer [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) pour obtenir [fictif](https://fsharp.github.io/FAKE/) prennent en charge et [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) pour obtenir [Paket](https://fsprojects.github.io/Paket/) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="e1467-137">However, you can also install [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) to get [FAKE](https://fsharp.github.io/FAKE/) support and [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) to get [Paket](https://fsprojects.github.io/Paket/) support.</span></span> <span data-ttu-id="e1467-138">FALSIFIER et Paket sont F # Communauté des outils supplémentaires pour la création de projets et de gestion des dépendances, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e1467-138">FAKE and Paket are additional F# community tools for building projects and managing dependencies, respectively.</span></span>
