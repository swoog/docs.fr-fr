---
title: Commande dotnet remove reference
description: La commande dotnet remove reference est une option pratique pour supprimer des références entre projets.
ms.date: 05/29/2018
ms.openlocfilehash: bfac4721743babcf48fd8e86a50c8df136e1bfce
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170611"
---
# <a name="dotnet-remove-reference"></a><span data-ttu-id="313d6-103">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="313d6-103">dotnet remove reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="313d6-104">Name</span><span class="sxs-lookup"><span data-stu-id="313d6-104">Name</span></span>

<span data-ttu-id="313d6-105">`dotnet remove reference` - Supprime des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="313d6-105">`dotnet remove reference` - Removes project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="313d6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="313d6-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] reference [-f|--framework] <PROJECT_REFERENCES> [-h|--help]`

## <a name="description"></a><span data-ttu-id="313d6-107">Description</span><span class="sxs-lookup"><span data-stu-id="313d6-107">Description</span></span>

<span data-ttu-id="313d6-108">La commande `dotnet remove reference` est une option pratique pour supprimer des références de projet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="313d6-108">The `dotnet remove reference` command provides a convenient option to remove project references from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="313d6-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="313d6-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="313d6-110">Fichier projet cible.</span><span class="sxs-lookup"><span data-stu-id="313d6-110">Target project file.</span></span> <span data-ttu-id="313d6-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="313d6-111">If not specified, the command searches the current directory for one.</span></span>

`PROJECT_REFERENCES`

<span data-ttu-id="313d6-112">Références entre projets (P2P) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="313d6-112">Project-to-project (P2P) references to remove.</span></span> <span data-ttu-id="313d6-113">Vous pouvez spécifier un ou plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="313d6-113">You can specify one or multiple projects.</span></span> <span data-ttu-id="313d6-114">Les [modèles Glob](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="313d6-114">[Glob patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

## <a name="options"></a><span data-ttu-id="313d6-115">Options</span><span class="sxs-lookup"><span data-stu-id="313d6-115">Options</span></span>

`-h|--help`

<span data-ttu-id="313d6-116">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="313d6-116">Prints out a short help for the command.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="313d6-117">Ne supprime une référence que quand [framework](../../standard/frameworks.md) spécifique est ciblé.</span><span class="sxs-lookup"><span data-stu-id="313d6-117">Removes the reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

## <a name="examples"></a><span data-ttu-id="313d6-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="313d6-118">Examples</span></span>

<span data-ttu-id="313d6-119">Supprimer une référence de projet du projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="313d6-119">Remove a project reference from the specified project:</span></span>

`dotnet remove app/app.csproj reference lib/lib.csproj`

<span data-ttu-id="313d6-120">Supprimer plusieurs références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="313d6-120">Remove multiple project references from the project in the current directory:</span></span>

`dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj`

<span data-ttu-id="313d6-121">Supprimer plusieurs références de projet à l’aide du modèle Glob sous Unix/Linux :</span><span class="sxs-lookup"><span data-stu-id="313d6-121">Remove multiple project references using a glob pattern on Unix/Linux:</span></span>

`dotnet remove app/app.csproj reference **/*.csproj`
