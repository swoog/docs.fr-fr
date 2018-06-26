---
title: Commande dotnet remove reference - Interface CLI .NET Core
description: La commande dotnet remove reference est une option pratique pour supprimer des références entre projets.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: b281b255be7f49a99a6b4928c340cd4fb085f085
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696229"
---
# <a name="dotnet-remove-reference"></a>dotnet remove reference

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet remove reference` - Supprime des références entre projets.

## <a name="synopsis"></a>Résumé

`dotnet remove [<PROJECT>] reference [-f|--framework] <PROJECT_REFERENCES> [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet remove reference` est une option pratique pour supprimer des références de projet d’un projet.

## <a name="arguments"></a>Arguments

`PROJECT`

Fichier projet cible. Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.

`PROJECT_REFERENCES`

Références entre projets (P2P) à supprimer. Vous pouvez spécifier un ou plusieurs projets. Les [modèles Glob](https://en.wikipedia.org/wiki/Glob_(programming)) sont pris en charge sur les terminaux Unix/Linux.

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.

`-f|--framework <FRAMEWORK>`

Ne supprime une référence que quand [framework](../../standard/frameworks.md) spécifique est ciblé.

## <a name="examples"></a>Exemples

Supprimer une référence de projet du projet spécifié :

`dotnet remove app/app.csproj reference lib/lib.csproj`

Supprimer plusieurs références de projet du projet dans le répertoire actuel :

`dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj`

Supprimer plusieurs références de projet à l’aide du modèle Glob sous Unix/Linux :

`dotnet remove app/app.csproj reference **/*.csproj`
