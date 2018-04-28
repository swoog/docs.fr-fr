---
title: 'À l’aide de la gestion des packages avec F # pour Azure'
description: 'Permet de gérer les dépendances de F # Azure Paket ou Nuget'
author: sylvanc
ms.author: phcart
ms.date: 09/20/2016
ms.topic: conceptual
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: da6938c6ee29292571f4269c68a9148c13738422
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="package-management-for-f-azure-dependencies"></a><span data-ttu-id="b561a-103">Gestion des packages pour les dépendances F# Azure</span><span class="sxs-lookup"><span data-stu-id="b561a-103">Package Management for F# Azure Dependencies</span></span>

<span data-ttu-id="b561a-104">Il est facile d’obtention de packages pour le développement Azure lorsque vous utilisez un gestionnaire de package.</span><span class="sxs-lookup"><span data-stu-id="b561a-104">Obtaining packages for Azure development is easy when you use a package manager.</span></span> <span data-ttu-id="b561a-105">Les deux options sont [Paket](https://fsprojects.github.io/Paket/) et [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="b561a-105">The two options are [Paket](https://fsprojects.github.io/Paket/) and [NuGet](https://www.nuget.org/).</span></span>

## <a name="using-paket"></a><span data-ttu-id="b561a-106">À l’aide de Paket</span><span class="sxs-lookup"><span data-stu-id="b561a-106">Using Paket</span></span>

<span data-ttu-id="b561a-107">Si vous utilisez [Paket](https://fsprojects.github.io/Paket/) comme gestionnaire de dépendance, vous pouvez utiliser la `paket.exe` outil pour ajouter des dépendances Azure.</span><span class="sxs-lookup"><span data-stu-id="b561a-107">If you're using [Paket](https://fsprojects.github.io/Paket/) as your dependency manager, you can use the `paket.exe` tool to add Azure dependencies.</span></span> <span data-ttu-id="b561a-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b561a-108">For example:</span></span>

    > paket add nuget WindowsAzure.Storage

<span data-ttu-id="b561a-109">Ou, si vous utilisez [Mono](https://www.mono-project.com/) pour le développement d’inter-plateformes .NET :</span><span class="sxs-lookup"><span data-stu-id="b561a-109">Or, if you're using [Mono](https://www.mono-project.com/) for cross-platform .NET development:</span></span>

    > mono paket.exe add nuget WindowsAzure.Storage

<span data-ttu-id="b561a-110">Cela ajoutera `WindowsAzure.Storage` à votre jeu de dépendances de package pour le projet dans le répertoire actif, vous devez modifier le `paket.dependencies` de fichiers et de télécharger le package.</span><span class="sxs-lookup"><span data-stu-id="b561a-110">This will add `WindowsAzure.Storage` to your set of package dependencies for the project in the current directory, modify the `paket.dependencies` file, and download the package.</span></span> <span data-ttu-id="b561a-111">Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :</span><span class="sxs-lookup"><span data-stu-id="b561a-111">If you have previously set up dependencies, or are working with a project where dependencies have been set up by another developer, you can resolve and install dependencies locally like this:</span></span>

    > paket install

<span data-ttu-id="b561a-112">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="b561a-112">Or, for Mono development:</span></span>

    > mono paket.exe install

<span data-ttu-id="b561a-113">Vous pouvez mettre à jour toutes les dépendances de votre package vers la dernière version à ceci :</span><span class="sxs-lookup"><span data-stu-id="b561a-113">You can update all your package dependencies to the latest version like this:</span></span>

    > paket update

<span data-ttu-id="b561a-114">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="b561a-114">Or, for Mono development:</span></span>

    > mono paket.exe update

## <a name="using-nuget"></a><span data-ttu-id="b561a-115">À l’aide de Nuget</span><span class="sxs-lookup"><span data-stu-id="b561a-115">Using Nuget</span></span>

<span data-ttu-id="b561a-116">Si vous utilisez [NuGet](https://www.nuget.org/) comme gestionnaire de dépendance, vous pouvez utiliser la `nuget.exe` outil pour ajouter des dépendances Azure.</span><span class="sxs-lookup"><span data-stu-id="b561a-116">If you're using [NuGet](https://www.nuget.org/) as your dependency manager, you can use the `nuget.exe` tool to add Azure dependencies.</span></span> <span data-ttu-id="b561a-117">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b561a-117">For example:</span></span>

    > nuget install WindowsAzure.Storage -ExcludeVersion

<span data-ttu-id="b561a-118">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="b561a-118">Or, for Mono development:</span></span>

    > mono nuget.exe install WindowsAzure.Storage -ExcludeVersion

<span data-ttu-id="b561a-119">Cela ajoutera `WindowsAzure.Storage` à votre jeu de dépendances de package pour le projet dans le répertoire actif et téléchargez le package.</span><span class="sxs-lookup"><span data-stu-id="b561a-119">This will add `WindowsAzure.Storage` to your set of package dependencies for the project in the current directory, and download the package.</span></span> <span data-ttu-id="b561a-120">Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :</span><span class="sxs-lookup"><span data-stu-id="b561a-120">If you have previously set up dependencies, or are working with a project where dependencies have been set up by another developer, you can resolve and install dependencies locally like this:</span></span>

    > nuget restore 

<span data-ttu-id="b561a-121">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="b561a-121">Or, for Mono development:</span></span>

    > mono nuget.exe restore

<span data-ttu-id="b561a-122">Vous pouvez mettre à jour toutes les dépendances de votre package vers la dernière version à ceci :</span><span class="sxs-lookup"><span data-stu-id="b561a-122">You can update all your package dependencies to the latest version like this:</span></span>

    > nuget update

<span data-ttu-id="b561a-123">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="b561a-123">Or, for Mono development:</span></span>

    > mono nuget.exe update

## <a name="referencing-assemblies"></a><span data-ttu-id="b561a-124">Référencement d'assemblys</span><span class="sxs-lookup"><span data-stu-id="b561a-124">Referencing Assemblies</span></span>

<span data-ttu-id="b561a-125">Pour utiliser vos packages dans votre script F #, vous devez référencer les assemblys inclus dans les packages à l’aide un `#r` la directive.</span><span class="sxs-lookup"><span data-stu-id="b561a-125">In order to use your packages in your F# script, you need to reference the assemblies included in the packages using a `#r` directive.</span></span> <span data-ttu-id="b561a-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b561a-126">For example:</span></span>

    > #r "packages/WindowsAzure.Storage/lib/net40/Microsoft.WindowsAzure.Storage.dll"

<span data-ttu-id="b561a-127">Comme vous pouvez le voir, vous devez spécifier le chemin d’accès relatif à la DLL et le nom complet de la DLL, qui peut ne pas être exactement le même que le nom du package.</span><span class="sxs-lookup"><span data-stu-id="b561a-127">As you can see, you'll need to specify the relative path to the DLL and the full DLL name, which may not be exactly the same as the package name.</span></span> <span data-ttu-id="b561a-128">Le chemin d’accès inclut une version du framework et éventuellement un numéro de version du package.</span><span class="sxs-lookup"><span data-stu-id="b561a-128">The path will include a framework version and possibly a package version number.</span></span> <span data-ttu-id="b561a-129">Pour rechercher tous les assemblys installés, vous pouvez utiliser quelque chose comme ceci sur une ligne de commande de Windows :</span><span class="sxs-lookup"><span data-stu-id="b561a-129">To find all the installed assemblies, you can use something like this on a Windows command line:</span></span>

    > cd packages/WindowsAzure.Storage
    > dir /s/b *.dll

<span data-ttu-id="b561a-130">Ou dans un interpréteur de commandes Unix, quelque chose comme ceci :</span><span class="sxs-lookup"><span data-stu-id="b561a-130">Or in a Unix shell, something like this:</span></span>

    > find packages/WindowsAzure.Storage -name "*.dll"

<span data-ttu-id="b561a-131">Cela vous donne les chemins d’accès vers les assemblys installés.</span><span class="sxs-lookup"><span data-stu-id="b561a-131">This will give you the paths to the installed assemblies.</span></span> <span data-ttu-id="b561a-132">À partir de là, vous pouvez sélectionner le chemin d’accès approprié pour votre version de framework.</span><span class="sxs-lookup"><span data-stu-id="b561a-132">From there, you can select the correct path for your framework version.</span></span>
