---
title: Commande dotnet tool uninstall - CLI .NET Core
description: La commande dotnet tool uninstall permet de désinstaller l’outil global .NET Core spécifié de votre machine.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 93a43e19df4c7f220ac1e2d2db397cba4d791e83
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43738169"
---
# <a name="dotnet-tool-uninstall"></a>dotnet tool uninstall

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>Name

`dotnet tool uninstall` - Désinstalle l’[outil global .NET Core](global-tools.md) spécifié de votre machine.

## <a name="synopsis"></a>Résumé

```console
dotnet tool uninstall <PACKAGE_NAME> <-g|--global>
dotnet tool uninstall <PACKAGE_NAME> <--tool-path>
dotnet tool uninstall <-h|--help>
```

## <a name="description"></a>Description

La commande `dotnet tool uninstall` vous offre un moyen de désinstaller des outils globaux .NET Core de votre machine. Pour utiliser la commande, vous devez soit spécifier que vous voulez supprimer un outil à l’échelle de l’utilisateur en utilisant l’option `--global`, soit spécifier un chemin vers l’emplacement auquel l’outil est installé à l’aide de l’option `--tool-path`.

## <a name="arguments"></a>Arguments

`PACKAGE_NAME`

Nom/ID du package NuGet qui contient l’outil global .NET Core à désinstaller. Vous pouvez trouver le nom du package à l’aide de la commande [dotnet tool list](dotnet-tool-list.md).

## <a name="options"></a>Options

`-g|--global`

Spécifie que l’outil à supprimer se trouve dans une installation à l’échelle de l’utilisateur. Non combinable avec l’option `--tool-path`. Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--tool-path`.

`-h|--help`

Affiche une aide brève pour la commande.

`--tool-path <PATH>`

Spécifie l’emplacement de désinstallation de l’outil global. Le chemin peut être absolu ou relatif. Non combinable avec l’option `--global`. Si vous ne spécifiez pas cette option, vous devez spécifier l’option `--global`.

## <a name="examples"></a>Exemples

Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) :

`dotnet tool uninstall -g dotnetsay`

Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) d’un dossier Windows spécifique :

`dotnet tool uninstall dotnetsay --tool-path c:\global-tools`

Désinstalle l’outil global [dotnetsay](https://www.nuget.org/packages/dotnetsay/) d’un dossier Linux/macOS spécifique :

`dotnet tool uninstall dotnetsay --tool-path ~/bin`

## <a name="see-also"></a>Voir aussi

* [Outils globaux .NET Core](global-tools.md)