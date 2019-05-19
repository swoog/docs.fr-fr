---
title: À l’aide de la gestion des packages avec F# pour Azure
description: Permet de gérer Paket ou Nuget F# dépendances Azure
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: b180024e2276a2fd7786f35cb922b1aa1d91f0ad
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880017"
---
# <a name="package-management-for-f-azure-dependencies"></a><span data-ttu-id="848b7-103">Gestion des packages pour les dépendances F# Azure</span><span class="sxs-lookup"><span data-stu-id="848b7-103">Package Management for F# Azure Dependencies</span></span>

<span data-ttu-id="848b7-104">Il est facile d’obtenir des packages pour le développement Azure lorsque vous utilisez un gestionnaire de package.</span><span class="sxs-lookup"><span data-stu-id="848b7-104">Obtaining packages for Azure development is easy when you use a package manager.</span></span> <span data-ttu-id="848b7-105">Les deux options sont [Paket](https://fsprojects.github.io/Paket/) et [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="848b7-105">The two options are [Paket](https://fsprojects.github.io/Paket/) and [NuGet](https://www.nuget.org/).</span></span>

## <a name="using-paket"></a><span data-ttu-id="848b7-106">À l’aide de Paket</span><span class="sxs-lookup"><span data-stu-id="848b7-106">Using Paket</span></span>

<span data-ttu-id="848b7-107">Si vous utilisez [Paket](https://fsprojects.github.io/Paket/) en tant que votre gestionnaire de dépendances, vous pouvez utiliser le `paket.exe` outil pour ajouter des dépendances Azure.</span><span class="sxs-lookup"><span data-stu-id="848b7-107">If you're using [Paket](https://fsprojects.github.io/Paket/) as your dependency manager, you can use the `paket.exe` tool to add Azure dependencies.</span></span> <span data-ttu-id="848b7-108">Exemple :</span><span class="sxs-lookup"><span data-stu-id="848b7-108">For example:</span></span>

```
> paket add nuget WindowsAzure.Storage
```

<span data-ttu-id="848b7-109">Ou, si vous utilisez [Mono](https://www.mono-project.com/) pour le développement multiplateforme .NET :</span><span class="sxs-lookup"><span data-stu-id="848b7-109">Or, if you're using [Mono](https://www.mono-project.com/) for cross-platform .NET development:</span></span>

```
> mono paket.exe add nuget WindowsAzure.Storage
```

<span data-ttu-id="848b7-110">Cela ajoutera `WindowsAzure.Storage` dans votre jeu de dépendances de package pour le projet dans le répertoire actif, vous devez modifier le `paket.dependencies` de fichier et téléchargez le package.</span><span class="sxs-lookup"><span data-stu-id="848b7-110">This will add `WindowsAzure.Storage` to your set of package dependencies for the project in the current directory, modify the `paket.dependencies` file, and download the package.</span></span> <span data-ttu-id="848b7-111">Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :</span><span class="sxs-lookup"><span data-stu-id="848b7-111">If you have previously set up dependencies, or are working with a project where dependencies have been set up by another developer, you can resolve and install dependencies locally like this:</span></span>

```
> paket install
```

<span data-ttu-id="848b7-112">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="848b7-112">Or, for Mono development:</span></span>

```
> mono paket.exe install
```

<span data-ttu-id="848b7-113">Vous pouvez mettre à jour toutes vos dépendances de package vers la dernière version comme suit :</span><span class="sxs-lookup"><span data-stu-id="848b7-113">You can update all your package dependencies to the latest version like this:</span></span>

```
> paket update
```

<span data-ttu-id="848b7-114">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="848b7-114">Or, for Mono development:</span></span>

```
> mono paket.exe update
```

## <a name="using-nuget"></a><span data-ttu-id="848b7-115">À l’aide de Nuget</span><span class="sxs-lookup"><span data-stu-id="848b7-115">Using Nuget</span></span>

<span data-ttu-id="848b7-116">Si vous utilisez [NuGet](https://www.nuget.org/) en tant que votre gestionnaire de dépendances, vous pouvez utiliser le `nuget.exe` outil pour ajouter des dépendances Azure.</span><span class="sxs-lookup"><span data-stu-id="848b7-116">If you're using [NuGet](https://www.nuget.org/) as your dependency manager, you can use the `nuget.exe` tool to add Azure dependencies.</span></span> <span data-ttu-id="848b7-117">Exemple :</span><span class="sxs-lookup"><span data-stu-id="848b7-117">For example:</span></span>

```
> nuget install WindowsAzure.Storage -ExcludeVersion
```

<span data-ttu-id="848b7-118">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="848b7-118">Or, for Mono development:</span></span>

```
> mono nuget.exe install WindowsAzure.Storage -ExcludeVersion
```

<span data-ttu-id="848b7-119">Cela ajoutera `WindowsAzure.Storage` dans votre jeu de dépendances de package pour le projet dans le répertoire actif et le téléchargement du package.</span><span class="sxs-lookup"><span data-stu-id="848b7-119">This will add `WindowsAzure.Storage` to your set of package dependencies for the project in the current directory, and download the package.</span></span> <span data-ttu-id="848b7-120">Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :</span><span class="sxs-lookup"><span data-stu-id="848b7-120">If you have previously set up dependencies, or are working with a project where dependencies have been set up by another developer, you can resolve and install dependencies locally like this:</span></span>

```
> nuget restore
```

<span data-ttu-id="848b7-121">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="848b7-121">Or, for Mono development:</span></span>

```
> mono nuget.exe restore
```

<span data-ttu-id="848b7-122">Vous pouvez mettre à jour toutes vos dépendances de package vers la dernière version comme suit :</span><span class="sxs-lookup"><span data-stu-id="848b7-122">You can update all your package dependencies to the latest version like this:</span></span>

```
> nuget update
```

<span data-ttu-id="848b7-123">Ou, pour le développement Mono :</span><span class="sxs-lookup"><span data-stu-id="848b7-123">Or, for Mono development:</span></span>

```
> mono nuget.exe update
```

## <a name="referencing-assemblies"></a><span data-ttu-id="848b7-124">Référencement d'assemblys</span><span class="sxs-lookup"><span data-stu-id="848b7-124">Referencing Assemblies</span></span>

<span data-ttu-id="848b7-125">Pour pouvoir utiliser vos packages dans votre F# script, vous devez référencer les assemblys inclus dans les packages en utilisant un `#r` directive.</span><span class="sxs-lookup"><span data-stu-id="848b7-125">In order to use your packages in your F# script, you need to reference the assemblies included in the packages using a `#r` directive.</span></span> <span data-ttu-id="848b7-126">Exemple :</span><span class="sxs-lookup"><span data-stu-id="848b7-126">For example:</span></span>

```
> #r "packages/WindowsAzure.Storage/lib/net40/Microsoft.WindowsAzure.Storage.dll"
```

<span data-ttu-id="848b7-127">Comme vous pouvez le voir, vous devez spécifier le chemin d’accès relatif à la DLL et le nom complet de la DLL, qui ne peut être exactement le même que le nom du package.</span><span class="sxs-lookup"><span data-stu-id="848b7-127">As you can see, you'll need to specify the relative path to the DLL and the full DLL name, which may not be exactly the same as the package name.</span></span> <span data-ttu-id="848b7-128">Le chemin d’accès inclut une version de framework et éventuellement un numéro de version du package.</span><span class="sxs-lookup"><span data-stu-id="848b7-128">The path will include a framework version and possibly a package version number.</span></span> <span data-ttu-id="848b7-129">Pour rechercher tous les assemblys installés, vous pouvez utiliser quelque chose comme ceci sur une ligne de commande de Windows :</span><span class="sxs-lookup"><span data-stu-id="848b7-129">To find all the installed assemblies, you can use something like this on a Windows command line:</span></span>

```
> cd packages/WindowsAzure.Storage
> dir /s/b *.dll
```

<span data-ttu-id="848b7-130">Ou dans un interpréteur de commandes Unix, quelque chose comme ceci :</span><span class="sxs-lookup"><span data-stu-id="848b7-130">Or in a Unix shell, something like this:</span></span>

```
> find packages/WindowsAzure.Storage -name "*.dll"
```

<span data-ttu-id="848b7-131">Cela vous donnera les chemins d’accès aux assemblys installés.</span><span class="sxs-lookup"><span data-stu-id="848b7-131">This will give you the paths to the installed assemblies.</span></span> <span data-ttu-id="848b7-132">À partir de là, vous pouvez sélectionner le chemin d’accès correct pour votre version de framework.</span><span class="sxs-lookup"><span data-stu-id="848b7-132">From there, you can select the correct path for your framework version.</span></span>
