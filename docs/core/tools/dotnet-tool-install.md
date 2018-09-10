---
title: Commande dotnet tool install - CLI .NET Core
description: La commande dotnet tool install permet d’installer l’outil global .NET Core spécifié sur votre machine.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: aad5a3e815936749d90f40975a8b13d34e89386c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512193"
---
# <a name="dotnet-tool-install"></a><span data-ttu-id="b9c3d-103">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="b9c3d-103">dotnet tool install</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="b9c3d-104">Name</span><span class="sxs-lookup"><span data-stu-id="b9c3d-104">Name</span></span>

<span data-ttu-id="b9c3d-105">`dotnet tool install` - Installe l’[outil global .NET Core](global-tools.md) spécifié sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-105">`dotnet tool install` - Installs the specified [.NET Core Global Tool](global-tools.md) on your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b9c3d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b9c3d-106">Synopsis</span></span>

```console
dotnet tool install <PACKAGE_NAME> <-g|--global> [--add-source] [--configfile] [--framework] [-v|--verbosity] [--version]
dotnet tool install <PACKAGE_NAME> <--tool-path> [--add-source] [--configfile] [--framework] [-v|--verbosity] [--version]
dotnet tool install <-h|--help>
```

## <a name="description"></a><span data-ttu-id="b9c3d-107">Description</span><span class="sxs-lookup"><span data-stu-id="b9c3d-107">Description</span></span>

<span data-ttu-id="b9c3d-108">La commande `dotnet tool install` vous offre un moyen d’installer des outils globaux .NET Core sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-108">The `dotnet tool install` command provides a way for you to install .NET Core Global Tools on your machine.</span></span> <span data-ttu-id="b9c3d-109">Pour utiliser la commande, vous devez spécifier que vous voulez une installation à l’échelle de l’utilisateur à l’aide de l’option `--global` ou vous spécifiez un chemin d’installation à l’aide de l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-109">To use the command, you either have to specify that you want a user-wide installation using the `--global` option or you specify a path to install it using the `--tool-path` option.</span></span>

<span data-ttu-id="b9c3d-110">Les outils globaux sont installés par défaut dans les répertoires suivants quand vous spécifiez l’option `-g` (ou `--global`) :</span><span class="sxs-lookup"><span data-stu-id="b9c3d-110">Global Tools are installed in the following directories by default when you specify the `-g` (or `--global`) option:</span></span>

| <span data-ttu-id="b9c3d-111">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9c3d-111">OS</span></span>          | <span data-ttu-id="b9c3d-112">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="b9c3d-112">Path</span></span>                          |
|-------------|-------------------------------|
| <span data-ttu-id="b9c3d-113">Linux/macOS</span><span class="sxs-lookup"><span data-stu-id="b9c3d-113">Linux/macOS</span></span> | `$HOME/.dotnet/tools`         |
| <span data-ttu-id="b9c3d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b9c3d-114">Windows</span></span>     | `%USERPROFILE%\.dotnet\tools` |

## <a name="arguments"></a><span data-ttu-id="b9c3d-115">Arguments</span><span class="sxs-lookup"><span data-stu-id="b9c3d-115">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="b9c3d-116">Nom/ID du package NuGet qui contient l’outil global .NET Core à installer.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-116">Name/ID of the NuGet package that contains the .NET Core Global Tool to install.</span></span>

## <a name="options"></a><span data-ttu-id="b9c3d-117">Options</span><span class="sxs-lookup"><span data-stu-id="b9c3d-117">Options</span></span>

`--add-source <SOURCE>`

<span data-ttu-id="b9c3d-118">Ajoute une source de package NuGet supplémentaire à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-118">Adds an additional NuGet package source to use during installation.</span></span>

`--configfile <FILE>`

<span data-ttu-id="b9c3d-119">Fichier de configuration NuGet (*nuget.config*) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-119">The NuGet configuration (*nuget.config*) file to use.</span></span>

`--framework <FRAMEWORK>`

<span data-ttu-id="b9c3d-120">Spécifie le [framework cible](../../standard/frameworks.md) pour lequel installer l’outil.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-120">Specifies the [target framework](../../standard/frameworks.md) to install the tool for.</span></span> <span data-ttu-id="b9c3d-121">Par défaut, le SDK .NET Core essaie de choisir le framework cible le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-121">By default, the .NET Core SDK tries to choose the most appropriate target framework.</span></span>

`-g|--global`

<span data-ttu-id="b9c3d-122">Spécifie que l’installation est à l’échelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-122">Specifies that the installation is user wide.</span></span> <span data-ttu-id="b9c3d-123">Non combinable avec l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-123">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="b9c3d-124">Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-124">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="b9c3d-125">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-125">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="b9c3d-126">Spécifie l’emplacement d’installation de l’outil global.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-126">Specifies the location where to install the Global Tool.</span></span> <span data-ttu-id="b9c3d-127">Le chemin peut être absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-127">PATH can be absolute or relative.</span></span> <span data-ttu-id="b9c3d-128">Si le chemin n’existe pas, la commande essaie de le créer.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-128">If PATH doesn't exist, the command tries to create it.</span></span> <span data-ttu-id="b9c3d-129">Non combinable avec l’option `--global`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-129">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="b9c3d-130">Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--global`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-130">If you don't specify this option, you must specify the `--global` option.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="b9c3d-131">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-131">Sets the verbosity level of the command.</span></span> <span data-ttu-id="b9c3d-132">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-132">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version <VERSION_NUMBER>`

<span data-ttu-id="b9c3d-133">Version de l’outil à installer.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-133">The version of the tool to install.</span></span> <span data-ttu-id="b9c3d-134">Par défaut, la dernière version stable du package est installée.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-134">By default, the latest stable package version is installed.</span></span> <span data-ttu-id="b9c3d-135">Utilisez cette option pour installer la préversion ou des versions antérieures de l’outil.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-135">Use this option to install preview or older versions of the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="b9c3d-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="b9c3d-136">Examples</span></span>

<span data-ttu-id="b9c3d-137">Installe l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) à l’emplacement par défaut :</span><span class="sxs-lookup"><span data-stu-id="b9c3d-137">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool in the default location:</span></span>

`dotnet tool install -g dotnetsay`

<span data-ttu-id="b9c3d-138">Installe l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) dans un dossier Windows spécifique :</span><span class="sxs-lookup"><span data-stu-id="b9c3d-138">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool on a specific Windows folder:</span></span>

`dotnet tool install dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="b9c3d-139">Installe l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) dans un dossier Linux/macOS spécifique :</span><span class="sxs-lookup"><span data-stu-id="b9c3d-139">Installs the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool on a specific Linux/macOS folder:</span></span>

`dotnet tool install dotnetsay --tool-path ~/bin`

<span data-ttu-id="b9c3d-140">Installe la version 2.0.0 de l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) :</span><span class="sxs-lookup"><span data-stu-id="b9c3d-140">Installs version 2.0.0 of the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool install -g dotnetsay --version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="b9c3d-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9c3d-141">See also</span></span>

* [<span data-ttu-id="b9c3d-142">Outils globaux .NET Core</span><span class="sxs-lookup"><span data-stu-id="b9c3d-142">.NET Core Global Tools</span></span>](global-tools.md)