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
# <a name="dotnet-sln"></a>dotnet sln

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet sln` : Modifie un fichier solution .NET Core.

## <a name="synopsis"></a>Résumé

```
dotnet sln [<SOLUTION_NAME>] add <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] add <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] remove <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] remove <GLOBBING_PATTERN>
dotnet sln [<SOLUTION_NAME>] list
dotnet sln [-h|--help]
```

## <a name="description"></a>Description

La commande `dotnet sln` offre un moyen pratique d’ajouter, de supprimer et de lister des projets dans un fichier solution.

Pour que la commande `dotnet sln` puisse être utilisée, le fichier solution doit déjà exister. Si vous devez en créer un, utilisez la commande [dotnet new](dotnet-new.md), comme dans l’exemple suivant :

```
dotnet new sln
```

## <a name="commands"></a>Commandes

`add <PROJECT> ...`

`add <GLOBBING_PATTERN>`

Ajoute un ou plusieurs projets au fichier solution. Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.

`remove <PROJECT> ...`

`remove <GLOBBING_PATTERN>`

Supprime un ou plusieurs projets du fichier solution. Les [modèles Globbing](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.

`list`

Liste tous les projets dans un fichier solution.

## <a name="arguments"></a>Arguments

`SOLUTION_NAME`

Fichier solution à utiliser. Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel. S’il existe plusieurs fichiers solution dans le répertoire, l’un d’eux doit être spécifié.

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.

## <a name="examples"></a>Exemples

Ajouter un projet C# à une solution :

`dotnet sln todo.sln add todo-app/todo-app.csproj`

Supprimer un projet C# d’une solution :

`dotnet sln todo.sln remove todo-app/todo-app.csproj`

Ajouter plusieurs projets C# à une solution :

`dotnet sln todo.sln add todo-app/todo-app.csproj back-end/back-end.csproj`

Supprimer plusieurs projets C# d’une solution :

`dotnet sln todo.sln remove todo-app/todo-app.csproj back-end/back-end.csproj`

Ajouter plusieurs projets C# à une solution avec un modèle d’utilisation des caractères génériques :

`dotnet sln todo.sln add **/*.csproj`

Supprimer plusieurs projets C# d’une solution avec un modèle d’utilisation des caractères génériques :

`dotnet sln todo.sln remove **/*.csproj`
