---
title: Commande dotnet-add reference
description: La commande dotnet add reference est une option pratique pour ajouter des références entre projets.
ms.date: 04/24/2019
ms.openlocfilehash: f33a379534dca88133babbb5ca78bca614e441c8
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64755193"
---
# <a name="dotnet-add-reference"></a><span data-ttu-id="6f2be-103">dotnet-add reference</span><span class="sxs-lookup"><span data-stu-id="6f2be-103">dotnet-add reference</span></span>

<span data-ttu-id="6f2be-104">**Cet article s’applique à : ✓** SDK .NET Core 1.x et ultérieur</span><span class="sxs-lookup"><span data-stu-id="6f2be-104">**This article applies to: ✓** .NET Core 1.x SDK and later versions</span></span>

<!-- todo: uncomment when all CLI commands are reviewed
[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]
-->

## <a name="name"></a><span data-ttu-id="6f2be-105">Name</span><span class="sxs-lookup"><span data-stu-id="6f2be-105">Name</span></span>

<span data-ttu-id="6f2be-106">`dotnet add reference` : ajoute des références entre projets (P2P).</span><span class="sxs-lookup"><span data-stu-id="6f2be-106">`dotnet add reference` - Adds project-to-project (P2P) references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="6f2be-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="6f2be-107">Synopsis</span></span>

`dotnet add [<PROJECT>] reference [-f|--framework] <PROJECT_REFERENCES> [-h|--help]`

## <a name="description"></a><span data-ttu-id="6f2be-108">Description</span><span class="sxs-lookup"><span data-stu-id="6f2be-108">Description</span></span>

<span data-ttu-id="6f2be-109">La commande `dotnet add reference` est une option pratique pour ajouter des références de projet à un projet.</span><span class="sxs-lookup"><span data-stu-id="6f2be-109">The `dotnet add reference` command provides a convenient option to add project references to a project.</span></span> <span data-ttu-id="6f2be-110">Une fois que vous avez exécuté la commande, les éléments [`<ProjectReference>`](/visualstudio/msbuild/common-msbuild-project-items) sont ajoutés au fichier projet.</span><span class="sxs-lookup"><span data-stu-id="6f2be-110">After running the command, the [`<ProjectReference>`](/visualstudio/msbuild/common-msbuild-project-items) elements are added to the project file.</span></span>

```xml
<ItemGroup>
  <ProjectReference Include="app.csproj" />
  <ProjectReference Include="..\lib2\lib2.csproj" />
  <ProjectReference Include="..\lib1\lib1.csproj" />
</ItemGroup>
```

## <a name="arguments"></a><span data-ttu-id="6f2be-111">Arguments</span><span class="sxs-lookup"><span data-stu-id="6f2be-111">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="6f2be-112">Spécifie le nom du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="6f2be-112">Specifies the project file.</span></span> <span data-ttu-id="6f2be-113">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="6f2be-113">If not specified, the command searches the current directory for one.</span></span>

* **`PROJECT_REFERENCES`**

  <span data-ttu-id="6f2be-114">Références entre projets (P2P) à ajouter.</span><span class="sxs-lookup"><span data-stu-id="6f2be-114">Project-to-project (P2P) references to add.</span></span> <span data-ttu-id="6f2be-115">Spécifiez un ou plusieurs projets.</span><span class="sxs-lookup"><span data-stu-id="6f2be-115">Specify one or more projects.</span></span> <span data-ttu-id="6f2be-116">Les [modèles Glob](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les systèmes Unix/Linux.</span><span class="sxs-lookup"><span data-stu-id="6f2be-116">[Glob patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux-based systems.</span></span>

## <a name="options"></a><span data-ttu-id="6f2be-117">Options</span><span class="sxs-lookup"><span data-stu-id="6f2be-117">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="6f2be-118">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="6f2be-118">Prints out a short help for the command.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="6f2be-119">Ajoute des références de projet uniquement quand vous ciblez un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="6f2be-119">Adds project references only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6f2be-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f2be-120">Examples</span></span>

* <span data-ttu-id="6f2be-121">Ajouter une référence de projet :</span><span class="sxs-lookup"><span data-stu-id="6f2be-121">Add a project reference:</span></span>

  ```console
  dotnet add app/app.csproj reference lib/lib.csproj
  ```

* <span data-ttu-id="6f2be-122">Ajouter plusieurs références de projet au projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="6f2be-122">Add multiple project references to the project in the current directory:</span></span>

  ```console
  dotnet add reference lib1/lib1.csproj lib2/lib2.csproj
  ```

* <span data-ttu-id="6f2be-123">Ajouter plusieurs références de projet à l’aide du modèle d’utilisation des caractères génériques (globbing) sur Linux/Unix :</span><span class="sxs-lookup"><span data-stu-id="6f2be-123">Add multiple project references using a globbing pattern on Linux/Unix:</span></span>

  ```console
  dotnet add app/app.csproj reference **/*.csproj
  ```