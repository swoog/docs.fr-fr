---
title: Commande dotnet add package
description: La commande « dotnet add package » est une option pratique pour ajouter une référence de package NuGet à un projet.
ms.date: 12/04/2018
ms.openlocfilehash: 159b208feafb82e267629ea47dcef02d6b575055
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170000"
---
# <a name="dotnet-add-package"></a><span data-ttu-id="a3f43-103">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="a3f43-103">dotnet add package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="a3f43-104">Name</span><span class="sxs-lookup"><span data-stu-id="a3f43-104">Name</span></span>

<span data-ttu-id="a3f43-105">`dotnet add package` : Ajoute une référence de package à un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="a3f43-105">`dotnet add package` - Adds a package reference to a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="a3f43-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a3f43-106">Synopsis</span></span>

`dotnet add [<PROJECT>] package <PACKAGE_NAME> [-h|--help] [-f|--framework] [--interactive] [-n|--no-restore] [--package-directory] [-s|--source] [-v|--version]`

## <a name="description"></a><span data-ttu-id="a3f43-107">Description</span><span class="sxs-lookup"><span data-stu-id="a3f43-107">Description</span></span>

<span data-ttu-id="a3f43-108">La commande `dotnet add package` est une option pratique pour ajouter une référence de package à un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="a3f43-108">The `dotnet add package` command provides a convenient option to add a package reference to a project file.</span></span> <span data-ttu-id="a3f43-109">Une fois que vous avez exécuté la commande, il existe un contrôle de compatibilité qui vérifie que le package est compatible avec les frameworks du projet.</span><span class="sxs-lookup"><span data-stu-id="a3f43-109">After running the command, there's a compatibility check to ensure the package is compatible with the frameworks in the project.</span></span> <span data-ttu-id="a3f43-110">Si le résultat du contrôle est positif, un élément `<PackageReference>` est ajouté au fichier projet et la commande [dotnet restore](dotnet-restore.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="a3f43-110">If the check passes, a `<PackageReference>` element is added to the project file and [dotnet restore](dotnet-restore.md) is run.</span></span>

[!INCLUDE[DotNet Restore Note](../../../includes/dotnet-restore-note.md)]

<span data-ttu-id="a3f43-111">Par exemple, l’ajout de `Newtonsoft.Json` à *ToDo.csproj* produit une sortie similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="a3f43-111">For example, adding `Newtonsoft.Json` to *ToDo.csproj* produces output similar to the following example:</span></span>

```console
  Writing C:\Users\mairaw\AppData\Local\Temp\tmp95A8.tmp
info : Adding PackageReference for package 'Newtonsoft.Json' into project 'C:\projects\ToDo\ToDo.csproj'.
log  : Restoring packages for C:\Temp\projects\consoleproj\consoleproj.csproj...
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json 79ms
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/12.0.1/newtonsoft.json.12.0.1.nupkg 232ms
log  : Installing Newtonsoft.Json 12.0.1.
info : Package 'Newtonsoft.Json' is compatible with all the specified frameworks in project 'C:\projects\ToDo\ToDo.csproj'.
info : PackageReference for package 'Newtonsoft.Json' version '12.0.1' added to file 'C:\projects\ToDo\ToDo.csproj'.
```

<span data-ttu-id="a3f43-112">Le fichier *ToDo.csproj* contient à présent un élément [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) pour le package référencé.</span><span class="sxs-lookup"><span data-stu-id="a3f43-112">The *ToDo.csproj* file now contains a [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) element for the referenced package.</span></span>

```xml
<PackageReference Include="Newtonsoft.Json" Version="12.0.1" />
```

## <a name="arguments"></a><span data-ttu-id="a3f43-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="a3f43-113">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="a3f43-114">Spécifie le nom du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="a3f43-114">Specifies the project file.</span></span> <span data-ttu-id="a3f43-115">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="a3f43-115">If not specified, the command searches the current directory for one.</span></span>

* **`PACKAGE_NAME`**

  <span data-ttu-id="a3f43-116">Référence de package à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a3f43-116">The package reference to add.</span></span>

## <a name="options"></a><span data-ttu-id="a3f43-117">Options</span><span class="sxs-lookup"><span data-stu-id="a3f43-117">Options</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="a3f43-118">Ajoute une référence de package uniquement quand vous ciblez un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="a3f43-118">Adds a package reference only when targeting a specific [framework](../../standard/frameworks.md).</span></span>

* **`-h|--help`**

  <span data-ttu-id="a3f43-119">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a3f43-119">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="a3f43-120">Permet à la commande de s’arrêter et d’attendre une saisie ou une action de l’utilisateur (par exemple, s’authentifier).</span><span class="sxs-lookup"><span data-stu-id="a3f43-120">Allows the command to stop and wait for user input or action (for example to complete authentication).</span></span> <span data-ttu-id="a3f43-121">Disponible à partir du kit SDK .NET Core 2.1, version 2.1.400 (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="a3f43-121">Available since .NET Core 2.1 SDK, version 2.1.400 or later.</span></span>

* **`-n|--no-restore`**

  <span data-ttu-id="a3f43-122">Ajoute une référence de package sans effectuer d’aperçu de restauration ni de contrôle de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="a3f43-122">Adds a package reference without performing a restore preview and compatibility check.</span></span>

* **`--package-directory <PACKAGE_DIRECTORY>`**

  <span data-ttu-id="a3f43-123">Restaure le package dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3f43-123">Restores the package to the specified directory.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="a3f43-124">Utilise une source de package NuGet spécifique pendant l’opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="a3f43-124">Uses a specific NuGet package source during the restore operation.</span></span>

* **`-v|--version <VERSION>`**

  <span data-ttu-id="a3f43-125">Version du package.</span><span class="sxs-lookup"><span data-stu-id="a3f43-125">Version of the package.</span></span>

## <a name="examples"></a><span data-ttu-id="a3f43-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3f43-126">Examples</span></span>

* <span data-ttu-id="a3f43-127">Ajouter un package NuGet `Newtonsoft.Json` à un projet :</span><span class="sxs-lookup"><span data-stu-id="a3f43-127">Add `Newtonsoft.Json` NuGet package to a project:</span></span>

  ```console
  dotnet add package Newtonsoft.Json
  ```

* <span data-ttu-id="a3f43-128">Ajouter une version spécifique d’un package à un projet :</span><span class="sxs-lookup"><span data-stu-id="a3f43-128">Add a specific version of a package to a project:</span></span>

  ```console
  dotnet add ToDo.csproj package Microsoft.Azure.DocumentDB.Core -v 1.0.0
  ```

* <span data-ttu-id="a3f43-129">Ajouter un package à l’aide d’une source NuGet spécifique :</span><span class="sxs-lookup"><span data-stu-id="a3f43-129">Add a package using a specific NuGet source:</span></span>

  ```console
  dotnet add package Microsoft.AspNetCore.StaticFiles -s https://dotnet.myget.org/F/dotnet-core/api/v3/index.json
  ```