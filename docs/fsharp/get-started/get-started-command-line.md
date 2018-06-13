---
title: 'Démarrer avec les outils de ligne de commande avec F #'
description: 'Découvrez comment créer une solution à projets multiples simple sur F # à l’aide de l’interface de ligne de base de .NET sur n’importe quel système d’exploitation (Windows, Mac OS ou Linux).'
ms.date: 03/26/2018
ms.openlocfilehash: 35ec2313742a0b14c92f3de2662a16aff389b214
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33562035"
---
# <a name="get-started-with-f-with-the-net-core-cli"></a>Prise en main) (F # avec l’interface de ligne de base .NET

Cet article décrit comment vous pouvez commencer à utiliser F # sur tout système d’exploitation (Windows, Mac OS ou Linux) avec l’interface de ligne de base de .NET. Il passe par la création d’une solution à projets multiples avec une bibliothèque de classes est appelée par une application console.

## <a name="prerequisites"></a>Prérequis

Pour commencer, vous devez installer le [.NET Core SDK 1.0 ou version ultérieure](https://www.microsoft.com/net/download/). Il est inutile pour désinstaller une version précédente du SDK .NET Core, elle prend en charge les installations côte à côte.

Cet article suppose que vous savez comment utiliser une ligne de commande et un texte par défaut éditeur. Si vous ne l’utilisez déjà, [Visual Studio Code](https://code.visualstudio.com) est une option intéressante comme un éditeur de texte pour F #. Pour obtenir des fonctionnalités comme IntelliSense, une meilleure mise en surbrillance de syntaxe et bien plus encore, vous pouvez télécharger le [Ionide Extension](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).

## <a name="build-a-simple-multi-project-solution"></a>Créer une simple solution à projets multiples

Ouvrez une invite de commandes/terminal et utiliser le [dotnet nouvelle](../../core/tools/dotnet-new.md) commande pour créer le nouveau fichier de solution appelé `FSNetCore`:

```
dotnet new sln -o FSNetCore
```

La structure de répertoire suivante est générée après l’exécution de la commande précédente :

```
FSNetCore
    ├── FSNetCore.sln
```

### <a name="write-a-class-library"></a>Écriture d’une bibliothèque de classes

Remplacez les répertoires par *FSNetCore*.

Utilisez le `dotnet new` de commande, créez un projet de bibliothèque de classes dans le **src** dossier nommé bibliothèque.

```
dotnet new lib -lang F# -o src/Library
```

La structure de répertoire suivante est générée après l’exécution de la commande précédente :

```
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

Ajoutez le package Newtonsoft.Json NuGet pour le projet de bibliothèque.

```
dotnet add src/Library/Library.fsproj package Newtonsoft.Json
```

Ajouter le `Library` de projet pour le `FSNetCore` à l’aide de la solution le [dotnet sln ajouter](../../core/tools/dotnet-sln.md) commande :

```
dotnet sln add src/Library/Library.fsproj
```

Restaurer les dépendances de NuGet à l’aide de la `dotnet restore` commande ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.

### <a name="write-a-console-application-that-consumes-the-class-library"></a>Écrire une application console qui utilise la bibliothèque de classes

Utilisez le `dotnet new` de commande, créez une application console dans le **src** dossier nommé l’application.

```
dotnet new console -lang F# -o src/App
```

La structure de répertoire suivante est générée après l’exécution de la commande précédente :

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

Ajoutez une référence à la `Library` à l’aide du projet [dotnet ajouter une référence](../../core/tools/dotnet-add-reference.md).

```
dotnet add src/App/App.fsproj reference src/Library/Library.fsproj
```

Ajouter le `App` de projet pour le `FSNetCore` à l’aide de la solution la `dotnet sln add` commande :

```
dotnet sln add src/App/App.fsproj
```

Restaurer les dépendances de NuGet, `dotnet restore` ([voir la Remarque](#dotnet-restore-note)) et exécutez `dotnet build` pour générer le projet.

Remplacez le répertoire pour la `src/App` projet de console et exécuter le projet en passant `Hello World` en tant qu’arguments :

```
cd src/App
dotnet run Hello World
```

Vous devez voir les résultats suivants :

```
Nice command-line arguments! Here's what JSON.NET has to say about them:

I used to be Hello but now I'm ""Hello"" thanks to JSON.NET!
I used to be World but now I'm ""World"" thanks to JSON.NET!
```

<a name="dotnet-restore-note"></a>
[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]