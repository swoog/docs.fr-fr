---
title: Commande dotnet sln
description: La commande dotnet-sln offre une option pratique pour ajouter, supprimer et lister des projets dans un fichier solution.
ms.date: 06/13/2018
ms.openlocfilehash: a88e22c68f639f2a42e59f9a271e431f04e24a2b
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169142"
---
# <a name="dotnet-sln"></a><span data-ttu-id="77e22-103">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="77e22-103">dotnet sln</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="77e22-104">Name</span><span class="sxs-lookup"><span data-stu-id="77e22-104">Name</span></span>

<span data-ttu-id="77e22-105">`dotnet sln` : Modifie un fichier solution .NET Core.</span><span class="sxs-lookup"><span data-stu-id="77e22-105">`dotnet sln` - Modifies a .NET Core solution file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="77e22-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="77e22-106">Synopsis</span></span>

```
dotnet sln [<SOLUTION_NAME>] add <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] add <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] remove <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] remove <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] list
dotnet sln [-h|--help]
```

## <a name="description"></a><span data-ttu-id="77e22-107">Description</span><span class="sxs-lookup"><span data-stu-id="77e22-107">Description</span></span>

<span data-ttu-id="77e22-108">La commande `dotnet sln` offre un moyen pratique d’ajouter, de supprimer et de lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="77e22-108">The `dotnet sln` command provides a convenient way to add, remove, and list projects in a solution file.</span></span>

<span data-ttu-id="77e22-109">Pour que la commande `dotnet sln` puisse être utilisée, le fichier solution doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="77e22-109">To use the `dotnet sln` command, the solution file must already exist.</span></span> <span data-ttu-id="77e22-110">Si vous devez en créer un, utilisez la commande [dotnet new](dotnet-new.md), comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="77e22-110">If you need to create one, use the [dotnet new](dotnet-new.md) command, like in the following example:</span></span>

```
dotnet new sln
```

## <a name="commands"></a><span data-ttu-id="77e22-111">Commandes</span><span class="sxs-lookup"><span data-stu-id="77e22-111">Commands</span></span>

`add <PROJECT> ...`

`add <GLOBBING_PATTERN>`

<span data-ttu-id="77e22-112">Ajoute un ou plusieurs projets au fichier solution.</span><span class="sxs-lookup"><span data-stu-id="77e22-112">Adds a project or multiple projects to the solution file.</span></span> <span data-ttu-id="77e22-113">Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="77e22-113">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`remove <PROJECT> ...`

`remove <GLOBBING_PATTERN>`

<span data-ttu-id="77e22-114">Supprime un ou plusieurs projets du fichier solution.</span><span class="sxs-lookup"><span data-stu-id="77e22-114">Removes a project or multiple projects from the solution file.</span></span> <span data-ttu-id="77e22-115">Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="77e22-115">[Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.</span></span>

`list`

<span data-ttu-id="77e22-116">Liste tous les projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="77e22-116">Lists all projects in a solution file.</span></span>

## <a name="arguments"></a><span data-ttu-id="77e22-117">Arguments</span><span class="sxs-lookup"><span data-stu-id="77e22-117">Arguments</span></span>

`SOLUTION_NAME`

<span data-ttu-id="77e22-118">Fichier solution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="77e22-118">Solution file to use.</span></span> <span data-ttu-id="77e22-119">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="77e22-119">If not specified, the command searches the current directory for one.</span></span> <span data-ttu-id="77e22-120">S’il existe plusieurs fichiers solution dans le répertoire, l’un d’eux doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="77e22-120">If there are multiple solution files in the directory, one must be specified.</span></span>

## <a name="options"></a><span data-ttu-id="77e22-121">Options</span><span class="sxs-lookup"><span data-stu-id="77e22-121">Options</span></span>

`-h|--help`

<span data-ttu-id="77e22-122">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="77e22-122">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="77e22-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="77e22-123">Examples</span></span>

<span data-ttu-id="77e22-124">Ajouter un projet C# à une solution :</span><span class="sxs-lookup"><span data-stu-id="77e22-124">Add a C# project to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj`

<span data-ttu-id="77e22-125">Supprimer un projet C# d’une solution :</span><span class="sxs-lookup"><span data-stu-id="77e22-125">Remove a C# project from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj`

<span data-ttu-id="77e22-126">Ajouter plusieurs projets C# à une solution :</span><span class="sxs-lookup"><span data-stu-id="77e22-126">Add multiple C# projects to a solution:</span></span>

`dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="77e22-127">Supprimer plusieurs projets C# d’une solution :</span><span class="sxs-lookup"><span data-stu-id="77e22-127">Remove multiple C# projects from a solution:</span></span>

`dotnet sln todo.sln remove todo-app/todo-app.csproj back-end/back-end.csproj`

<span data-ttu-id="77e22-128">Ajouter plusieurs projets C# à une solution avec un modèle d’utilisation des caractères génériques :</span><span class="sxs-lookup"><span data-stu-id="77e22-128">Add multiple C# projects to a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln add **/*.csproj`

<span data-ttu-id="77e22-129">Supprimer plusieurs projets C# d’une solution avec un modèle d’utilisation des caractères génériques :</span><span class="sxs-lookup"><span data-stu-id="77e22-129">Remove multiple C# projects from a solution using a globbing pattern:</span></span>

`dotnet sln todo.sln remove **/*.csproj`

> [!NOTE]
> <span data-ttu-id="77e22-130">L’utilisation des caractères génériques n’est pas une fonctionnalité de l’interface CLI, mais une fonctionnalité de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="77e22-130">Globbing is not a CLI feature but rather a feature of the command shell.</span></span> <span data-ttu-id="77e22-131">Pour pouvoir développer les fichiers, vous devez utiliser un interpréteur de commandes qui prend en charge l’utilisation des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="77e22-131">To successfully expand the files, you must use a shell that supports globbing.</span></span> <span data-ttu-id="77e22-132">Pour plus d’informations sur l’utilisation des caractères génériques, voir [Wikipédia](https://en.wikipedia.org/wiki/Glob_(programming)).</span><span class="sxs-lookup"><span data-stu-id="77e22-132">For more information about globbing, see [Wikipedia](https://en.wikipedia.org/wiki/Glob_(programming)).</span></span>
