---
title: 'Démarrer avec les outils de ligne de commande avec F #'
description: 'Découvrez comment créer une solution à projets multiples simple sur F # à l’aide de l’interface de ligne de base de .NET sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux).'
author: cartermp
ms.author: phcart
ms.date: 03/26/2018
ms.topic: conceptual
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: 767385be605d863644db563a2e86a41ca80527c4
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="get-started-with-f-with-the-net-core-cli"></a><span data-ttu-id="b0138-103">Prise en main) (F # avec l’interface de ligne de base .NET</span><span class="sxs-lookup"><span data-stu-id="b0138-103">Get started with F# with the .NET Core CLI</span></span>

<span data-ttu-id="b0138-104">Cet article décrit comment vous pouvez commencer à utiliser F # sur tout système d’exploitation (Windows, Mac OS ou Linux) avec l’interface de ligne de base de .NET.</span><span class="sxs-lookup"><span data-stu-id="b0138-104">This article covers how you can get started with F# on any operating system (Windows, macOS, or Linux) with the .NET Core CLI.</span></span> <span data-ttu-id="b0138-105">Il passe par la création d’une solution à projets multiples avec une bibliothèque de classes est appelée par une application console.</span><span class="sxs-lookup"><span data-stu-id="b0138-105">It goes through building a multi-project solution with a class library that is called by a console application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b0138-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b0138-106">Prerequisites</span></span>

<span data-ttu-id="b0138-107">Pour commencer, vous devez installer le [.NET Core SDK 1.0 ou version ultérieure](https://www.microsoft.com/net/download/).</span><span class="sxs-lookup"><span data-stu-id="b0138-107">To begin, you must install the [.NET Core SDK 1.0 or later](https://www.microsoft.com/net/download/).</span></span> <span data-ttu-id="b0138-108">Il est inutile pour désinstaller une version précédente du SDK .NET Core, elle prend en charge les installations côte à côte.</span><span class="sxs-lookup"><span data-stu-id="b0138-108">There is no need to uninstall a previous version of the .NET Core SDK, as it supports side-by-side installations.</span></span>

<span data-ttu-id="b0138-109">Cet article suppose que vous savez comment utiliser une ligne de commande et un texte par défaut éditeur.</span><span class="sxs-lookup"><span data-stu-id="b0138-109">This article assumes that you know how to use a command line and have a preferred text editor.</span></span> <span data-ttu-id="b0138-110">Si vous ne l’utilisez déjà, [Visual Studio Code](https://code.visualstudio.com) est une option intéressante comme un éditeur de texte pour F #.</span><span class="sxs-lookup"><span data-stu-id="b0138-110">If you don't already use it, [Visual Studio Code](https://code.visualstudio.com) is a great option as a text editor for F#.</span></span> <span data-ttu-id="b0138-111">Pour obtenir des fonctionnalités comme IntelliSense, une meilleure mise en surbrillance de syntaxe et bien plus encore, vous pouvez télécharger le [Ionide Extension](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span><span class="sxs-lookup"><span data-stu-id="b0138-111">To get awesome features like IntelliSense, better syntax highlighting, and more, you can download the [Ionide Extension](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span></span>

## <a name="build-a-simple-multi-project-solution"></a><span data-ttu-id="b0138-112">Créer une simple solution à projets multiples</span><span class="sxs-lookup"><span data-stu-id="b0138-112">Build a simple multi-project solution</span></span>

<span data-ttu-id="b0138-113">Ouvrez une invite de commandes/terminal et utiliser le [dotnet nouvelle](../../core/tools/dotnet-new.md) commande pour créer le nouveau fichier de solution appelé `FSNetCore`:</span><span class="sxs-lookup"><span data-stu-id="b0138-113">Open a command prompt/terminal and use the [dotnet new](../../core/tools/dotnet-new.md) command to create new solution file called `FSNetCore`:</span></span>

```
dotnet new sln -o FSNetCore
```

<span data-ttu-id="b0138-114">La structure de répertoire suivante est générée après l’exécution de la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="b0138-114">The following directory structure is produced after running the previous command:</span></span>

```
FSNetCore
    ├── FSNetCore.sln
```

### <a name="write-a-class-library"></a><span data-ttu-id="b0138-115">Écriture d’une bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="b0138-115">Write a class library</span></span>

<span data-ttu-id="b0138-116">Remplacez les répertoires par *FSNetCore*.</span><span class="sxs-lookup"><span data-stu-id="b0138-116">Change directories to *FSNetCore*.</span></span>

<span data-ttu-id="b0138-117">Utilisez le `dotnet new` de commande, créez un projet de bibliothèque de classes dans le **src** dossier nommé bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b0138-117">Use the `dotnet new` command, create a class library project in the **src** folder named Library.</span></span>

```
dotnet new lib -lang F# -o src/Library
```

<span data-ttu-id="b0138-118">La structure de répertoire suivante est générée après l’exécution de la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="b0138-118">The following directory structure is produced after running the previous command:</span></span>

```
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

<span data-ttu-id="b0138-119">Remplacez le contenu de `Library.fs` par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b0138-119">Replace the contents of `Library.fs` with the following code:</span></span>

```fsharp
module Library

open Newtonsoft.Json

let getJsonNetJson value =
    sprintf "I used to be %s but now I'm %s thanks to JSON.NET!" value (JsonConvert.SerializeObject(value))
```

<span data-ttu-id="b0138-120">Ajoutez le package Newtonsoft.Json NuGet pour le projet de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b0138-120">Add the Newtonsoft.Json NuGet package to the Library project.</span></span>

```
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

<span data-ttu-id="b0138-121">Ajouter le `Library` de projet pour le `FSNetCore` à l’aide de la solution le [dotnet sln ajouter](../../core/tools/dotnet-sln.md) commande :</span><span class="sxs-lookup"><span data-stu-id="b0138-121">Add the `Library` project to the `FSNetCore` solution using the [dotnet sln add](../../core/tools/dotnet-sln.md) command:</span></span>

```
dotnet sln add src/Library/Library.fsproj
```

<span data-ttu-id="b0138-122">Restaurer les dépendances de NuGet à l’aide de la `dotnet restore` commande ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="b0138-122">Restore the NuGet dependencies using the `dotnet restore` command ([see note](#dotnet-restore-note)) and run `dotnet build` to build the project.</span></span>

### <a name="write-a-console-application-that-consumes-the-class-library"></a><span data-ttu-id="b0138-123">Écrire une application console qui utilise la bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="b0138-123">Write a console application that consumes the class library</span></span>

<span data-ttu-id="b0138-124">Utilisez le `dotnet new` de commande, créez une application console dans le **src** dossier nommé l’application.</span><span class="sxs-lookup"><span data-stu-id="b0138-124">Use the `dotnet new` command, create a console application in the **src** folder named App.</span></span>

```
dotnet new console -lang F# -o src/App
```

<span data-ttu-id="b0138-125">La structure de répertoire suivante est générée après l’exécution de la commande précédente :</span><span class="sxs-lookup"><span data-stu-id="b0138-125">The following directory structure is produced after running the previous command:</span></span>

```
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

<span data-ttu-id="b0138-126">Remplacez le contenu du fichier `Program.fs` avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b0138-126">Replace the contents of the `Program.fs` file with the following code:</span></span>

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

<span data-ttu-id="b0138-127">Ajoutez une référence à la `Library` à l’aide du projet [dotnet ajouter une référence](../../core/tools/dotnet-add-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b0138-127">Add a reference to the `Library` project using [dotnet add reference](../../core/tools/dotnet-add-reference.md).</span></span>

```
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

<span data-ttu-id="b0138-128">Ajouter le `App` de projet pour le `FSNetCore` à l’aide de la solution la `dotnet sln add` commande :</span><span class="sxs-lookup"><span data-stu-id="b0138-128">Add the `App` project to the `FSNetCore` solution using the `dotnet sln add` command:</span></span>

```
dotnet sln add src/App/App.fsproj
```

<span data-ttu-id="b0138-129">Restaurer les dépendances de NuGet, `dotnet restore` ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.</span><span class="sxs-lookup"><span data-stu-id="b0138-129">Restore the NuGet dependencies, `dotnet restore` ([see note](#dotnet-restore-note)) and run `dotnet build` to build the project.</span></span>

<span data-ttu-id="b0138-130">Remplacez le répertoire pour la `src/App` projet de console et exécuter le projet en passant `Hello World` en tant qu’arguments :</span><span class="sxs-lookup"><span data-stu-id="b0138-130">Change directory to the `src/App` console project and run the project passing `Hello World` as arguments:</span></span>

```
cd src/App
dotnet run Hello World
```

<span data-ttu-id="b0138-131">Vous devez voir les résultats suivants :</span><span class="sxs-lookup"><span data-stu-id="b0138-131">You should see the following results:</span></span>

```
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```

<a name="dotnet-restore-note"></a>
[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]