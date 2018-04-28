---
title: Commande dotnet remove reference - Interface CLI .NET Core
description: La commande dotnet remove reference est une option pratique pour supprimer des références entre projets.
author: mairaw
ms.author: mairaw
ms.date: 08/14/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 0b7fb2788ccc04b54bf02f0387141d501612c16d
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-remove-reference"></a><span data-ttu-id="1a4a9-103">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="1a4a9-103">dotnet remove reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="1a4a9-104">Name</span><span class="sxs-lookup"><span data-stu-id="1a4a9-104">Name</span></span>

<span data-ttu-id="1a4a9-105">`dotnet remove reference` - Supprime des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-105">`dotnet remove reference` - Removes project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="1a4a9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="1a4a9-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] reference [-f|--framework] <PROJECT_REFERENCES> [-h|--help]`

## <a name="description"></a><span data-ttu-id="1a4a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="1a4a9-107">Description</span></span>

<span data-ttu-id="1a4a9-108">La commande `dotnet remove reference` est une option pratique pour supprimer des références de projet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-108">The `dotnet remove reference` command provides a convenient option to remove project references from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="1a4a9-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="1a4a9-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="1a4a9-110">Fichier projet cible.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-110">Target project file.</span></span> <span data-ttu-id="1a4a9-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-111">If not specified, the command searches the current directory for one.</span></span>

`PROJECT_REFERENCES`

<span data-ttu-id="1a4a9-112">Références entre projets (P2P) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-112">Project to project (P2P references to remove.</span></span> <span data-ttu-id="1a4a9-113">Vous pouvez spécifier un ou plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-113">You can specify one or multiple projects.</span></span> <span data-ttu-id="1a4a9-114">Les [modèles Glob](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-114">[Glob patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

## <a name="options"></a><span data-ttu-id="1a4a9-115">Options</span><span class="sxs-lookup"><span data-stu-id="1a4a9-115">Options</span></span>

`-h|--help`

<span data-ttu-id="1a4a9-116">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-116">Prints out a short help for the command.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="1a4a9-117">Ne supprime une référence que quand [framework](../../standard/frameworks.md) spécifique est ciblé.</span><span class="sxs-lookup"><span data-stu-id="1a4a9-117">Removes the reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1a4a9-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a4a9-118">Examples</span></span>

<span data-ttu-id="1a4a9-119">Supprimer une référence de projet du projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="1a4a9-119">Remove a project reference from the specified project:</span></span>

`dotnet remove app/app.csproj reference lib/lib.csproj`

<span data-ttu-id="1a4a9-120">Supprimer plusieurs références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="1a4a9-120">Remove multiple project references from the project in the current directory:</span></span>

`dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj`

<span data-ttu-id="1a4a9-121">Supprimer plusieurs références de projet à l’aide du modèle Glob sous Unix/Linux :</span><span class="sxs-lookup"><span data-stu-id="1a4a9-121">Remove multiple project references using a glob pattern on Unix/Linux:</span></span>

`dotnet remove app/app.csproj reference **/*.csproj`
