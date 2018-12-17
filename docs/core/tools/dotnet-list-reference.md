---
title: Commande dotnet list reference - Interface CLI .NET Core
description: La commande dotnet list reference est une option pratique pour lister des références entre projets.
ms.date: 12/03/2018
ms.openlocfilehash: 58b4e07abfe95d1febdd54d117825ecedf502e61
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152597"
---
# <a name="dotnet-list-reference"></a>dotnet list reference

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet list reference` : répertorie des références entre projets.

## <a name="synopsis"></a>Résumé

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet list reference` est pratique pour lister les références à un projet ou à une solution donné.

## <a name="arguments"></a>Arguments

* **`PROJECT`**

  Spécifie le fichier projet à utiliser pour répertorier les références. Si aucun fichier n’est spécifié, la commande recherche un fichier projet dans le répertoire actif.

## <a name="options"></a>Options

* **`-h|--help`**

  Affiche une aide brève pour la commande.

## <a name="examples"></a>Exemples

* Lister les références de projet pour le projet spécifié :

  ```console
  dotnet list app/app.csproj reference
  ```

* Lister les références de projet du projet dans le répertoire actuel :

  ```console
  dotnet list reference
  ```