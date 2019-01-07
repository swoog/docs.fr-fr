---
title: Commande dotnet tool update
description: La commande dotnet tool update met à jour l’outil global .NET Core spécifié sur votre machine.
ms.date: 05/29/2018
ms.openlocfilehash: 2716f7f88ffe364bebacf970d7152f5509edc888
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169734"
---
# <a name="dotnet-tool-update"></a>dotnet tool update

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>Name

`dotnet tool update` - Met à jour l’[outil global .NET Core](global-tools.md) spécifié sur votre machine.

## <a name="synopsis"></a>Résumé

```console
dotnet tool update <PACKAGE_NAME> <-g|--global> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <PACKAGE_NAME> <--tool-path> [--configfile] [--framework] [-v|--verbosity]
dotnet tool update <-h|--help>
```

## <a name="description"></a>Description

La commande `dotnet tool update` vous offre un moyen de mettre à jour des outils globaux .NET Core sur votre machine vers la dernière version stable du package. La commande désinstalle et réinstalle un outil en le mettant à jour. Pour utiliser la commande, vous devez soit spécifier que vous voulez mettre à jour un outil à partir d’une installation à l’échelle de l’utilisateur en utilisant l’option `--global`, soit spécifier un chemin vers l’emplacement auquel l’outil est installé à l’aide de l’option `--tool-path`.

## <a name="arguments"></a>Arguments

`PACKAGE_NAME`

Nom/ID du package NuGet qui contient l’outil global .NET Core à mettre à jour. Vous pouvez trouver le nom du package à l’aide de la commande [dotnet tool list](dotnet-tool-list.md).

## <a name="options"></a>Options

`--add-source <SOURCE>`

Ajoute une source de package NuGet supplémentaire à utiliser pendant l’installation.

`--configfile <FILE>`

Fichier de configuration NuGet (*nuget.config*) à utiliser.

`--framework <FRAMEWORK>`

Spécifie le [framework cible](../../standard/frameworks.md) pour lequel mettre à jour l’outil.

`-g|--global`

Spécifie que la mise à jour concerne un outil à l’échelle de l’utilisateur. Non combinable avec l’option `--tool-path`. Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--tool-path`.

`-h|--help`

Affiche une aide brève pour la commande.

`--tool-path <PATH>`

Spécifie l’emplacement d’installation de l’outil global. Le chemin peut être absolu ou relatif. Non combinable avec l’option `--global`. Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--global`.

`-v|--verbosity <LEVEL>`

Définit le niveau de détail de la commande. Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.

## <a name="examples"></a>Exemples

Met à jour l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) :

`dotnet tool update -g dotnetsay`

Met à jour l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) situé dans un dossier Windows spécifique :

`dotnet tool update dotnetsay --tool-path c:\global-tools`

Met à jour l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) situé dans un dossier Linux/macOS spécifique :

`dotnet tool update dotnetsay --tool-path ~/bin`

## <a name="see-also"></a>Voir aussi

* [Outils globaux .NET Core](global-tools.md)