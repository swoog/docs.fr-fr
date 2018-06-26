---
title: Commande dotnet tool uninstall - CLI .NET Core
description: La commande dotnet tool uninstall permet de désinstaller l’outil global .NET Core spécifié de votre machine.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 5cf80d1756dbf4e88bb52a8028d186d44978f440
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696936"
---
# <a name="dotnet-tool-uninstall"></a><span data-ttu-id="d80ed-103">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="d80ed-103">dotnet tool uninstall</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="d80ed-104">Name</span><span class="sxs-lookup"><span data-stu-id="d80ed-104">Name</span></span>

<span data-ttu-id="d80ed-105">`dotnet tool uninstall` - Désinstalle l’[outil global .NET Core](global-tools.md) spécifié de votre machine.</span><span class="sxs-lookup"><span data-stu-id="d80ed-105">`dotnet tool uninstall` - Uninstalls the specified [.NET Core Global Tool](global-tools.md) from your machine.</span></span>

## <a name="synopsis"></a><span data-ttu-id="d80ed-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d80ed-106">Synopsis</span></span>

```
dotnet tool uninstall <PACKAGE_NAME> <-g|--global>
dotnet tool uninstall <PACKAGE_NAME> <--tool-path>
dotnet tool uninstall <-h|--help>
```

## <a name="description"></a><span data-ttu-id="d80ed-107">Description</span><span class="sxs-lookup"><span data-stu-id="d80ed-107">Description</span></span>

<span data-ttu-id="d80ed-108">La commande `dotnet tool uninstall` vous offre un moyen de désinstaller des outils globaux .NET Core de votre machine.</span><span class="sxs-lookup"><span data-stu-id="d80ed-108">The `dotnet tool uninstall` command provides a way for you to uninstall .NET Core Global Tools from your machine.</span></span> <span data-ttu-id="d80ed-109">Pour utiliser la commande, vous devez soit spécifier que vous voulez supprimer un outil à l’échelle de l’utilisateur en utilisant l’option `--global`, soit spécifier un chemin vers l’emplacement auquel l’outil est installé à l’aide de l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="d80ed-109">To use the command, you either have to specify that you want to remove a user-wide tool using the `--global` option or specify a path to where the tool is installed using the `--tool-path` option.</span></span>

## <a name="arguments"></a><span data-ttu-id="d80ed-110">Arguments</span><span class="sxs-lookup"><span data-stu-id="d80ed-110">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="d80ed-111">Nom/ID du package NuGet qui contient l’outil global .NET Core à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="d80ed-111">Name/ID of the NuGet package that contains the .NET Core Global Tool to uninstall.</span></span> <span data-ttu-id="d80ed-112">Vous pouvez trouver le nom du package à l’aide de la commande [dotnet tool list](dotnet-tool-list.md).</span><span class="sxs-lookup"><span data-stu-id="d80ed-112">You can find the package name using the [dotnet tool list](dotnet-tool-list.md) command.</span></span>

## <a name="options"></a><span data-ttu-id="d80ed-113">Options</span><span class="sxs-lookup"><span data-stu-id="d80ed-113">Options</span></span>

`-g|--global`

<span data-ttu-id="d80ed-114">Spécifie que l’outil à supprimer se trouve dans une installation à l’échelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d80ed-114">Specifies that the tool to be removed is from a user-wide installation.</span></span> <span data-ttu-id="d80ed-115">Non combinable avec l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="d80ed-115">Can't be combined with the `--tool-path` option.</span></span> <span data-ttu-id="d80ed-116">Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--tool-path`.</span><span class="sxs-lookup"><span data-stu-id="d80ed-116">If you don't specify this option, you must specify the `--tool-path` option.</span></span>

`-h|--help`

<span data-ttu-id="d80ed-117">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="d80ed-117">Prints out a short help for the command.</span></span>

`--tool-path <PATH>`

<span data-ttu-id="d80ed-118">Spécifie l’emplacement de désinstallation de l’outil global.</span><span class="sxs-lookup"><span data-stu-id="d80ed-118">Specifies the location where to uninstall the Global Tool.</span></span> <span data-ttu-id="d80ed-119">Le chemin peut être absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="d80ed-119">PATH can be absolute or relative.</span></span> <span data-ttu-id="d80ed-120">Non combinable avec l’option `--global`.</span><span class="sxs-lookup"><span data-stu-id="d80ed-120">Can't be combined with the `--global` option.</span></span> <span data-ttu-id="d80ed-121">Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--global`.</span><span class="sxs-lookup"><span data-stu-id="d80ed-121">If you don't specify this option, you must specify the `--global` option.</span></span>

## <a name="examples"></a><span data-ttu-id="d80ed-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="d80ed-122">Examples</span></span>

<span data-ttu-id="d80ed-123">Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) :</span><span class="sxs-lookup"><span data-stu-id="d80ed-123">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool:</span></span>

`dotnet tool uninstall -g dotnetsay`

<span data-ttu-id="d80ed-124">Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) d’un dossier Windows spécifique :</span><span class="sxs-lookup"><span data-stu-id="d80ed-124">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool from a specific Windows folder:</span></span>

`dotnet tool uninstall dotnetsay --tool-path c:\global-tools`

<span data-ttu-id="d80ed-125">Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) d’un dossier Linux/macOS spécifique :</span><span class="sxs-lookup"><span data-stu-id="d80ed-125">Uninstalls the [dotnetsay](https://www.nuget.org/packages/dotnetsay/) Global Tool from a specific Linux/macOS folder:</span></span>

`dotnet tool uninstall dotnetsay --tool-path ~/bin`

## <a name="see-also"></a><span data-ttu-id="d80ed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d80ed-126">See also</span></span>

[<span data-ttu-id="d80ed-127">Outils globaux .NET Core</span><span class="sxs-lookup"><span data-stu-id="d80ed-127">.NET Core Global Tools</span></span>](global-tools.md)