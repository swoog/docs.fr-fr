---
title: Commande dotnet remove reference - Interface CLI .NET Core
description: La commande dotnet remove reference est une option pratique pour supprimer des références entre projets.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: b281b255be7f49a99a6b4928c340cd4fb085f085
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696229"
---
# <a name="dotnet-remove-reference"></a><span data-ttu-id="c5091-103">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="c5091-103">dotnet remove reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="c5091-104">Name</span><span class="sxs-lookup"><span data-stu-id="c5091-104">Name</span></span>

<span data-ttu-id="c5091-105">`dotnet remove reference` - Supprime des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="c5091-105">`dotnet remove reference` - Removes project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="c5091-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c5091-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] reference [-f|--framework] <PROJECT_REFERENCES> [-h|--help]`

## <a name="description"></a><span data-ttu-id="c5091-107">Description</span><span class="sxs-lookup"><span data-stu-id="c5091-107">Description</span></span>

<span data-ttu-id="c5091-108">La commande `dotnet remove reference` est une option pratique pour supprimer des références de projet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="c5091-108">The `dotnet remove reference` command provides a convenient option to remove project references from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="c5091-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="c5091-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="c5091-110">Fichier projet cible.</span><span class="sxs-lookup"><span data-stu-id="c5091-110">Target project file.</span></span> <span data-ttu-id="c5091-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="c5091-111">If not specified, the command searches the current directory for one.</span></span>

`PROJECT_REFERENCES`

<span data-ttu-id="c5091-112">Références entre projets (P2P) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c5091-112">Project-to-project (P2P) references to remove.</span></span> <span data-ttu-id="c5091-113">Vous pouvez spécifier un ou plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="c5091-113">You can specify one or multiple projects.</span></span> <span data-ttu-id="c5091-114">Les [modèles Glob](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="c5091-114">[Glob patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

## <a name="options"></a><span data-ttu-id="c5091-115">Options</span><span class="sxs-lookup"><span data-stu-id="c5091-115">Options</span></span>

`-h|--help`

<span data-ttu-id="c5091-116">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="c5091-116">Prints out a short help for the command.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="c5091-117">Ne supprime une référence que quand [framework](../../standard/frameworks.md) spécifique est ciblé.</span><span class="sxs-lookup"><span data-stu-id="c5091-117">Removes the reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c5091-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="c5091-118">Examples</span></span>

<span data-ttu-id="c5091-119">Supprimer une référence de projet du projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="c5091-119">Remove a project reference from the specified project:</span></span>

`dotnet remove app/app.csproj reference lib/lib.csproj`

<span data-ttu-id="c5091-120">Supprimer plusieurs références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="c5091-120">Remove multiple project references from the project in the current directory:</span></span>

`dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj`

<span data-ttu-id="c5091-121">Supprimer plusieurs références de projet à l’aide du modèle Glob sous Unix/Linux :</span><span class="sxs-lookup"><span data-stu-id="c5091-121">Remove multiple project references using a glob pattern on Unix/Linux:</span></span>

`dotnet remove app/app.csproj reference **/*.csproj`
