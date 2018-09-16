---
title: 'Bien démarrer avec F # avec les outils de ligne de commande'
description: 'Découvrez comment créer une solution à projets multiples simple sur F # à l’aide de l’interface CLI .NET Core sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux).'
ms.date: 03/26/2018
ms.openlocfilehash: 8a82970f33c8bbe1b8cdd8fb6499b59b16d3cbf3
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45673907"
---
# <a name="get-started-with-f-with-the-net-core-cli"></a>Bien démarrer avec F # avec l’interface CLI .NET Core

Cet article explique comment vous pouvez commencer avec F # sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux) avec l’interface CLI .NET Core. Il passe par la création d’une solution à projets multiples avec une bibliothèque de classes est appelée par une application console.

## <a name="prerequisites"></a>Prérequis

Pour commencer, vous devez installer la dernière version [du SDK .NET Core](https://www.microsoft.com/net/download/).

Cet article suppose que vous savez comment utiliser une ligne de commande et un texte par défaut est l’éditeur. Si vous ne l’utilisez déjà, [Visual Studio Code](get-started-vscode.md) est une excellente option comme un éditeur de texte pour F #.

## <a name="build-a-simple-multi-project-solution"></a>Créer une solution à projets multiples simple

Ouvrez un invite de commandes/terminal et utilisez le [dotnet nouvelle](../../core/tools/dotnet-new.md) commande pour créer le nouveau fichier de solution appelé `FSNetCore`:

```console
dotnet new sln -o FSNetCore
```

La structure de répertoire suivante est générée après avoir exécuté la commande précédente :

```console
FSNetCore
    ├── FSNetCore.sln
```

### <a name="write-a-class-library"></a>Écrire une bibliothèque de classes

Remplacez les répertoires par *FSNetCore*.

Utilisez le `dotnet new` de commande, créez un projet de bibliothèque de classes dans le **src** dossier nommé bibliothèque.

```console
dotnet new classlib -lang F# -o src/Library
```

La structure de répertoire suivante est générée après avoir exécuté la commande précédente :

```console
└── FSNetCore
    ├── FSNetCore.sln
    └── src
        └── Library
            ├── Library.fs
            └── Library.fsproj
```

Remplacez le contenu de `Library.fs` par le code suivant :

```fsharp
module Library

open Newtonsoft.Json

let getJsonNetJson value =
    sprintf "I used to be %s but now I'm %s thanks to JSON.NET!" value (JsonConvert.SerializeObject(value))
```

Ajoutez le package Newtonsoft.Json NuGet au projet de bibliothèque.

```console
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

Ajouter le `Library` de projet pour le `FSNetCore` à l’aide de la solution le [dotnet sln ajouter](../../core/tools/dotnet-sln.md) commande :

```console
dotnet sln add src/Library/Library.fsproj
```

Exécutez `dotnet build` pour générer le projet. Dépendances non résolues seront restaurées lors de la génération.

### <a name="write-a-console-application-that-consumes-the-class-library"></a>Écrire une application console qui utilise la bibliothèque de classes

Utilisez le `dotnet new` de commande, créez une application console dans le **src** dossier nommé application.

```console
dotnet new console -lang F# -o src/App
```

La structure de répertoire suivante est générée après avoir exécuté la commande précédente :

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

Remplacez le contenu du fichier `Program.fs` avec le code suivant :

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

Ajoutez une référence à la `Library` à l’aide de projet [dotnet ajouter une référence](../../core/tools/dotnet-add-reference.md).

```console
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

Ajouter le `App` de projet pour le `FSNetCore` à l’aide de la solution le `dotnet sln add` commande :

```console
dotnet sln add src/App/App.fsproj
```

Restaurer les dépendances NuGet, `dotnet restore` ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.

Accédez au répertoire le `src/App` projet de console et exécuter le projet en passant `Hello World` en tant qu’arguments :

```console
cd src/App
dotnet run Hello World
```

Vous devez voir les résultats suivants :

```console
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```

## <a name="next-steps"></a>Étapes suivantes

Consultez ensuite le [visite guidée de F #](../tour.md) pour en savoir plus sur les différentes fonctionnalités de F #.
