---
title: Commande dotnet add package - Interface CLI .NET Core
description: La commande « dotnet add package » est une option pratique pour ajouter une référence de package NuGet à un projet.
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 31dda9dbb101238b3a33d8b0d9a17765744480e0
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39244391"
---
# <a name="dotnet-add-package"></a>dotnet add package

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet add package` : Ajoute une référence de package à un fichier projet.

## <a name="synopsis"></a>Résumé

`dotnet add [<PROJECT>] package <PACKAGE_NAME> [-h|--help] [-f|--framework] [-n|--no-restore] [--package-directory] [-s|--source] [-v|--version]`

## <a name="description"></a>Description

La commande `dotnet add package` est une option pratique pour ajouter une référence de package à un fichier projet. Une fois que vous avez exécuté la commande, il existe un contrôle de compatibilité qui vérifie que le package est compatible avec les frameworks du projet. Si le résultat du contrôle est positif, un élément `<PackageReference>` est ajouté au fichier projet et la commande [dotnet restore](dotnet-restore.md) est exécutée.

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

Par exemple, l’ajout de `Newtonsoft.Json` à *ToDo.csproj* produit une sortie similaire à l’exemple suivant :

```console
  Writing C:\Users\mairaw\AppData\Local\Temp\tmp95A8.tmp
info : Adding PackageReference for package 'Newtonsoft.Json' into project 'C:\projects\ToDo\ToDo.csproj'.
log  : Restoring packages for C:\projects\ToDo\ToDo.csproj...
info :   GET https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json
info :   OK https://api.nuget.org/v3-flatcontainer/newtonsoft.json/index.json 235ms
info : Package 'Newtonsoft.Json' is compatible with all the specified frameworks in project 'C:\projects\ToDo\ToDo.csproj'.
info : PackageReference for package 'Newtonsoft.Json' version '10.0.3' added to file 'C:\projects\ToDo\ToDo.csproj'.
```

Le fichier *ToDo.csproj* contient à présent un élément [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) pour le package référencé.

```xml
<PackageReference Include="Newtonsoft.Json" Version="9.0.1" />
```

## <a name="arguments"></a>Arguments

`PROJECT`

Spécifie le nom du fichier projet. Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.

`PACKAGE_NAME`

Référence de package à ajouter.

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.

`-f|--framework <FRAMEWORK>`

Ajoute une référence de package uniquement quand vous ciblez un [framework](../../standard/frameworks.md) spécifique.

`-n|--no-restore`

Ajoute une référence de package sans effectuer d’aperçu de restauration ni de contrôle de compatibilité.

`--package-directory <PACKAGE_DIRECTORY>`

Restaure le package dans le répertoire spécifié.

`-s|--source <SOURCE>`

Utilise une source de package NuGet spécifique pendant l’opération de restauration.

`-v|--version <VERSION>`

Version du package.

## <a name="examples"></a>Exemples

Ajouter un package NuGet `Newtonsoft.Json` à un projet :

`dotnet add package Newtonsoft.Json`

Ajouter une version spécifique d’un package à un projet :

`dotnet add ToDo.csproj package Microsoft.Azure.DocumentDB.Core -v 1.0.0`

Ajouter un package à l’aide d’une source NuGet spécifique :

`dotnet add package Microsoft.AspNetCore.StaticFiles -s https://dotnet.myget.org/F/dotnet-core/api/v3/index.json`
