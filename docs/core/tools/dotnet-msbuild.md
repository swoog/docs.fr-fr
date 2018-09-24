---
title: Commande dotnet msbuild - Interface CLI .NET Core
description: La commande dotnet msbuild fournit l’accès à la ligne de commande MSbuild.
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 76165590478b0e76d19d546c87e012da4716b6db
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46578894"
---
# <a name="dotnet-msbuild"></a>dotnet msbuild

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet msbuild` : Génère un projet et l’ensemble de ses dépendances.

## <a name="synopsis"></a>Résumé

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a>Description

La commande `dotnet msbuild` permet d’accéder à un outil MSBuild entièrement fonctionnel.

La commande a les mêmes fonctionnalités que le client de ligne de commande MSBuild existant. Les options sont identiques. Pour plus d’informations sur les options disponibles, consultez [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference).

## <a name="examples"></a>Exemples

Générer un projet et ses dépendances :

`dotnet msbuild`

Générer un projet et ses dépendances à l’aide de la configuration Release :

`dotnet msbuild -p:Configuration=Release`

Exécuter la cible de publication et effectuer une publication pour le RID `osx.10.11-x64` :

`dotnet msbuild -t:Publish -p:RuntimeIdentifiers=osx.10.11-x64`

Consultez la totalité du projet avec toutes les cibles incluses par le kit SDK :

`dotnet msbuild -pp`
