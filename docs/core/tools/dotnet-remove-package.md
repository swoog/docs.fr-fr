---
title: Commande dotnet remove package
description: La commande dotnet remove package est une option pratique pour supprimer une référence de package NuGet d’un projet.
ms.date: 05/29/2018
ms.openlocfilehash: 4cc8ac927b761547dc5e53be9abeba827bf1e1d9
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53168726"
---
# <a name="dotnet-remove-package"></a><span data-ttu-id="8ed3a-103">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="8ed3a-103">dotnet remove package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="8ed3a-104">Name</span><span class="sxs-lookup"><span data-stu-id="8ed3a-104">Name</span></span>

<span data-ttu-id="8ed3a-105">`dotnet remove package` : Supprime une référence de package d’un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-105">`dotnet remove package` - Removes package reference from a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="8ed3a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8ed3a-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="8ed3a-107">Description</span><span class="sxs-lookup"><span data-stu-id="8ed3a-107">Description</span></span>

<span data-ttu-id="8ed3a-108">La commande `dotnet remove package` est une option pratique pour supprimer une référence de package NuGet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-108">The `dotnet remove package` command provides a convenient option to remove a NuGet package reference from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="8ed3a-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="8ed3a-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="8ed3a-110">Spécifie le nom du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-110">Specifies the project file.</span></span> <span data-ttu-id="8ed3a-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-111">If not specified, the command searches the current directory for one.</span></span>

`PACKAGE_NAME`

<span data-ttu-id="8ed3a-112">Référence de package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-112">The package reference to remove.</span></span>

## <a name="options"></a><span data-ttu-id="8ed3a-113">Options</span><span class="sxs-lookup"><span data-stu-id="8ed3a-113">Options</span></span>

`-h|--help`

<span data-ttu-id="8ed3a-114">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="8ed3a-114">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="8ed3a-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="8ed3a-115">Examples</span></span>

<span data-ttu-id="8ed3a-116">Supprime le package NuGet `Newtonsoft.Json` d’un projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="8ed3a-116">Removes `Newtonsoft.Json` NuGet package from a project in the current directory:</span></span>

`dotnet remove package Newtonsoft.Json`