---
title: Commande dotnet sln - Interface CLI .NET Core
description: La commande dotnet-sln offre une option pratique pour ajouter, supprimer et lister des projets dans un fichier solution.
author: mairaw
ms.author: mairaw
ms.date: 06/13/2018
ms.openlocfilehash: 65ae402ef5519863886c8cf833598f5314b4bdad
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36207771"
---
# <a name="dotnet-sln"></a><span data-ttu-id="0fbd5-103">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="0fbd5-103">dotnet sln</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="0fbd5-104">Name</span><span class="sxs-lookup"><span data-stu-id="0fbd5-104">Name</span></span>

<span data-ttu-id="0fbd5-105">`dotnet sln` : Modifie un fichier solution .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-105">`dotnet sln` - Modifies a .NET Core solution file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="0fbd5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0fbd5-106">Synopsis</span></span>

```
dotnet sln [<SOLUTION_NAME>] add <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] add <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] remove <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] remove <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] list
dotnet sln [-h|--help]
```

## <a name="description"></a><span data-ttu-id="0fbd5-107">Description</span><span class="sxs-lookup"><span data-stu-id="0fbd5-107">Description</span></span>

<span data-ttu-id="0fbd5-108">La commande `dotnet sln` offre un moyen pratique d’ajouter, de supprimer et de lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-108">The `dotnet sln` command provides a convenient way to add, remove, and list projects in a solution file.</span></span>

<span data-ttu-id="0fbd5-109">Pour que la commande `dotnet sln` puisse être utilisée, le fichier solution doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-109">To use the `dotnet sln` command, the solution file must already exist.</span></span> <span data-ttu-id="0fbd5-110">Si vous devez en créer un, utilisez la commande [dotnet new](dotnet-new.md), comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-110">If you need to create one, use the [dotnet new](dotnet-new.md) command, like in the following example:</span></span>

```
dotnet new sln
```

## <a name="commands"></a><span data-ttu-id="0fbd5-111">Commandes</span><span class="sxs-lookup"><span data-stu-id="0fbd5-111">Commands</span></span>

`add <PROJECT> ...`

`add <GLOBBING_PATTERN>`

<span data-ttu-id="0fbd5-112">Ajoute un ou plusieurs projets au fichier solution.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-112">Adds a project or multiple projects to the solution file.</span></span> <span data-ttu-id="0fbd5-113">Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-113">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`remove <PROJECT> ...`

`remove <GLOBBING_PATTERN>`

<span data-ttu-id="0fbd5-114">Supprime un ou plusieurs projets du fichier solution.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-114">Removes a project or multiple projects from the solution file.</span></span> <span data-ttu-id="0fbd5-115">Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-115">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`list`

<span data-ttu-id="0fbd5-116">Liste tous les projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-116">Lists all projects in a solution file.</span></span>

## <a name="arguments"></a><span data-ttu-id="0fbd5-117">Arguments</span><span class="sxs-lookup"><span data-stu-id="0fbd5-117">Arguments</span></span>

`SOLUTION_NAME`

<span data-ttu-id="0fbd5-118">Fichier solution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-118">Solution file to use.</span></span> <span data-ttu-id="0fbd5-119">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-119">If not specified, the command searches the current directory for one.</span></span> <span data-ttu-id="0fbd5-120">S’il existe plusieurs fichiers solution dans le répertoire, l’un d’eux doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-120">If there are multiple solution files in the directory, one must be specified.</span></span>

## <a name="options"></a><span data-ttu-id="0fbd5-121">Options</span><span class="sxs-lookup"><span data-stu-id="0fbd5-121">Options</span></span>

`-h|--help`

<span data-ttu-id="0fbd5-122">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-122">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="0fbd5-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="0fbd5-123">Examples</span></span>

<span data-ttu-id="0fbd5-124">Ajouter un projet C# à une solution :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-124">Add a C# project to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj`

<span data-ttu-id="0fbd5-125">Supprimer un projet C# d’une solution :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-125">Remove a C# project from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj`

<span data-ttu-id="0fbd5-126">Ajouter plusieurs projets C# à une solution :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-126">Add multiple C# projects to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="0fbd5-127">Supprimer plusieurs projets C# d’une solution :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-127">Remove multiple C# projects from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="0fbd5-128">Ajouter plusieurs projets C# à une solution avec un modèle d’utilisation des caractères génériques :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-128">Add multiple C# projects to a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln add **/*.csproj`

<span data-ttu-id="0fbd5-129">Supprimer plusieurs projets C# d’une solution avec un modèle d’utilisation des caractères génériques :</span><span class="sxs-lookup"><span data-stu-id="0fbd5-129">Remove multiple C# projects from a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln remove **/*.csproj`
