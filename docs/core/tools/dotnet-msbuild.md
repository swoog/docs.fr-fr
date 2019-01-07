---
title: Commande dotnet msbuild
description: La commande dotnet msbuild fournit l’accès à la ligne de commande MSbuild.
ms.date: 12/03/2018
ms.openlocfilehash: f025b5b92e57c7b804b9bdd59c8b4a4a806796da
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169077"
---
# <a name="dotnet-msbuild"></a>dotnet msbuild

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet msbuild` : Génère un projet et l’ensemble de ses dépendances.

## <a name="synopsis"></a>Résumé

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a>Description

La commande `dotnet msbuild` permet d’accéder à un outil MSBuild entièrement fonctionnel.

La commande a les mêmes fonctionnalités que le client de ligne de commande MSBuild existant pour un projet de type SDK uniquement. Les options sont identiques. Pour plus d’informations sur les options disponibles, consultez [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference).

La commande [dotnet build](dotnet-build.md) est équivalente à `dotnet msbuild -restore -target:Build`. `dotnet build` est généralement utilisée pour générer les projets, mais `dotnet msbuild` vous donne davantage de contrôle. Par exemple, si vous avez une cible spécifique que vous souhaitez exécuter (sans exécuter la cible build ), utilisez plutôt `dotnet msbuild`.

## <a name="examples"></a>Exemples

* Générer un projet et ses dépendances :

  ```console
  dotnet msbuild
  ```

* Générer un projet et ses dépendances à l’aide de la configuration Release :

  ```console
  dotnet msbuild -p:Configuration=Release
  ```

* Exécuter la cible de publication et effectuer une publication pour le RID `osx.10.11-x64` :

  ```console
  dotnet msbuild -t:Publish -p:RuntimeIdentifiers=osx.10.11-x64
  ```

* Consultez la totalité du projet avec toutes les cibles incluses par le kit SDK :

  ```console
  dotnet msbuild -pp
  ```