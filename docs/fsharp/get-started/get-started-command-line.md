---
title: Bien démarrer avec F# avec les outils de ligne de commande
description: Découvrez comment créer une solution à projets multiples simple sur F# à l’aide de l’interface CLI .NET Core sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux).
ms.date: 03/26/2018
ms.openlocfilehash: 8a82970f33c8bbe1b8cdd8fb6499b59b16d3cbf3
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "45673907"
---
# <a name="get-started-with-f-with-the-net-core-cli"></a><span data-ttu-id="dea3e-103">Bien démarrer avec F# avec l’interface CLI .NET Core</span><span class="sxs-lookup"><span data-stu-id="dea3e-103">Get started with F# with the .NET Core CLI</span></span>

<span data-ttu-id="dea3e-104">Cet article explique comment vous pouvez commencer avec F# sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux) avec l’interface CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="dea3e-104">This article covers how you can get started with F# on any operating system (Windows, macOS, or Linux) with the .NET Core CLI.</span></span> <span data-ttu-id="dea3e-105">Il passe par la création d’une solution à projets multiples avec une bibliothèque de classes est appelée par une application console.</span><span class="sxs-lookup"><span data-stu-id="dea3e-105">It goes through building a multi-project solution with a class library that is called by a console application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dea3e-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="dea3e-106">Prerequisites</span></span>

<span data-ttu-id="dea3e-107">Pour commencer, vous devez installer la dernière version [du SDK .NET Core](https://www.microsoft.com/net/download/).</span><span class="sxs-lookup"><span data-stu-id="dea3e-107">To begin, you must install the latest [.NET Core SDK](https://www.microsoft.com/net/download/).</span></span>

<span data-ttu-id="dea3e-108">Cet article suppose que vous savez comment utiliser une ligne de commande et un texte par défaut est l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="dea3e-108">This article assumes that you know how to use a command line and have a preferred text editor.</span></span> <span data-ttu-id="dea3e-109">Si vous ne l’utilisez déjà, [Visual Studio Code](get-started-vscode.md) est une excellente option comme un éditeur de texte pour F#.</span><span class="sxs-lookup"><span data-stu-id="dea3e-109">If you don't already use it, [Visual Studio Code](get-started-vscode.md) is a great option as a text editor for F#.</span></span>

## <a name="build-a-simple-multi-project-solution"></a><span data-ttu-id="dea3e-110">Créer une solution à projets multiples simple</span><span class="sxs-lookup"><span data-stu-id="dea3e-110">Build a simple multi-project solution</span></span>

<span data-ttu-id="dea3e-111">Ouvrez un invite de commandes/terminal et utilisez le [dotnet nouvelle](../../core/tools/dotnet-new.md) commande pour créer le nouveau fichier de solution appelé `FSNetCore`:</span><span class="sxs-lookup"><span data-stu-id="dea3e-111">Open a command prompt/terminal and use the [dotnet new](../../core/tools/dotnet-new.md) command to create new solution file called `FSNetCore`:</span></span>

```console
dotnet new sln -o FSNetCore
```

<span data-ttu-id="dea3e-112">La structure de répertoire suivante est générée après avoir exécuté la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="dea3e-112">The following directory structure is produced after running the previous command:</span></span>

```console
FSNetCore
    ├── FSNetCore.sln
```

### <a name="write-a-class-library"></a><span data-ttu-id="dea3e-113">Écrire une bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="dea3e-113">Write a class library</span></span>

<span data-ttu-id="dea3e-114">Remplacez les répertoires par *FSNetCore*.</span><span class="sxs-lookup"><span data-stu-id="dea3e-114">Change directories to *FSNetCore*.</span></span>

<span data-ttu-id="dea3e-115">Utilisez le `dotnet new` de commande, créez un projet de bibliothèque de classes dans le **src** dossier nommé bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dea3e-115">Use the `dotnet new` command, create a class library project in the **src** folder named Library.</span></span>

```console
dotnet new classlib -lang F# -o src/Library
```

<span data-ttu-id="dea3e-116">La structure de répertoire suivante est générée après avoir exécuté la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="dea3e-116">The following directory structure is produced after running the previous command:</span></span>

```console
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

<span data-ttu-id="dea3e-117">Remplacez le contenu de `Library.fs` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="dea3e-117">Replace the contents of `Library.fs` with the following code:</span></span>

```fsharp
module Library

open Newtonsoft.Json

let getJsonNetJson value =
    sprintf "I used to be %s but now I'm %s thanks to JSON.NET!" value (JsonConvert.SerializeObject(value))
```

<span data-ttu-id="dea3e-118">Ajoutez le package Newtonsoft.Json NuGet au projet de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dea3e-118">Add the Newtonsoft.Json NuGet package to the Library project.</span></span>

```console
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

<span data-ttu-id="dea3e-119">Ajouter le `Library` de projet pour le `FSNetCore` à l’aide de la solution le [dotnet sln ajouter](../../core/tools/dotnet-sln.md) commande :</span><span class="sxs-lookup"><span data-stu-id="dea3e-119">Add the `Library` project to the `FSNetCore` solution using the [dotnet sln add](../../core/tools/dotnet-sln.md) command:</span></span>

```console
dotnet sln add src/Library/Library.fsproj
```

<span data-ttu-id="dea3e-120">Exécutez `dotnet build` pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="dea3e-120">Run `dotnet build` to build the project.</span></span> <span data-ttu-id="dea3e-121">Dépendances non résolues seront restaurées lors de la génération.</span><span class="sxs-lookup"><span data-stu-id="dea3e-121">Unresolved dependencies will be restored when building.</span></span>

### <a name="write-a-console-application-that-consumes-the-class-library"></a><span data-ttu-id="dea3e-122">Écrire une application console qui utilise la bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="dea3e-122">Write a console application that consumes the class library</span></span>

<span data-ttu-id="dea3e-123">Utilisez le `dotnet new` de commande, créez une application console dans le **src** dossier nommé application.</span><span class="sxs-lookup"><span data-stu-id="dea3e-123">Use the `dotnet new` command, create a console application in the **src** folder named App.</span></span>

```console
dotnet new console -lang F# -o src/App
```

<span data-ttu-id="dea3e-124">La structure de répertoire suivante est générée après avoir exécuté la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="dea3e-124">The following directory structure is produced after running the previous command:</span></span>

```console
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        ├── App
        │   ├── App.fsproj
        │   ├── Program.fs
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

<span data-ttu-id="dea3e-125">Remplacez le contenu du fichier `Program.fs` avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="dea3e-125">Replace the contents of the `Program.fs` file with the following code:</span></span>

```fsharp
open System
open Library

[<EntryPoint>]
let main argv =
    printfn "Nice command-line arguments! Here's what JSON.NET has to say about them:"

    argv
    |> Array.map getJsonNetJson
    |> Array.iter (printfn "%s")

    0 // return an integer exit code
```

<span data-ttu-id="dea3e-126">Ajoutez une référence à la `Library` à l’aide de projet [dotnet ajouter une référence](../../core/tools/dotnet-add-reference.md).</span><span class="sxs-lookup"><span data-stu-id="dea3e-126">Add a reference to the `Library` project using [dotnet add reference](../../core/tools/dotnet-add-reference.md).</span></span>

```console
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

<span data-ttu-id="dea3e-127">Ajouter le `App` de projet pour le `FSNetCore` à l’aide de la solution le `dotnet sln add` commande :</span><span class="sxs-lookup"><span data-stu-id="dea3e-127">Add the `App` project to the `FSNetCore` solution using the `dotnet sln add` command:</span></span>

```console
dotnet sln add src/App/App.fsproj
```

<span data-ttu-id="dea3e-128">Restaurer les dépendances NuGet, `dotnet restore` ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="dea3e-128">Restore the NuGet dependencies, `dotnet restore` ([see note](#dotnet-restore-note)) and run `dotnet build` to build the project.</span></span>

<span data-ttu-id="dea3e-129">Accédez au répertoire le `src/App` projet de console et exécuter le projet en passant `Hello World` en tant qu’arguments :</span><span class="sxs-lookup"><span data-stu-id="dea3e-129">Change directory to the `src/App` console project and run the project passing `Hello World` as arguments:</span></span>

```console
cd src/App
dotnet run Hello World
```

<span data-ttu-id="dea3e-130">Vous devez voir les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="dea3e-130">You should see the following results:</span></span>

```console
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```

## <a name="next-steps"></a><span data-ttu-id="dea3e-131">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dea3e-131">Next steps</span></span>

<span data-ttu-id="dea3e-132">Consultez ensuite le [visite guidée de F#](../tour.md) pour en savoir plus sur les différentes fonctionnalités de F#.</span><span class="sxs-lookup"><span data-stu-id="dea3e-132">Next, check out the [Tour of F#](../tour.md) to learn more about different F# features.</span></span>
