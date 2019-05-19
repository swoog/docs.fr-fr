---
title: Commande dotnet remove package
description: La commande dotnet remove package est une option pratique pour supprimer une référence de package NuGet d’un projet.
ms.date: 05/29/2018
ms.openlocfilehash: cbdeacff78ef20c9a73010e10a771a724b23792e
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632433"
---
# <a name="dotnet-remove-package"></a>dotnet remove package

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet remove package` : Supprime une référence de package d’un fichier projet.

## <a name="synopsis"></a>Résumé

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet remove package` est une option pratique pour supprimer une référence de package NuGet d’un projet.

## <a name="arguments"></a>Arguments

`PROJECT`

Spécifie le nom du fichier projet. Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.

`PACKAGE_NAME`

Référence de package à supprimer.

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.

## <a name="examples"></a>Exemples

Supprime le package NuGet `Newtonsoft.Json` d’un projet dans le répertoire actuel :

`dotnet remove package Newtonsoft.Json`
