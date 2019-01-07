---
title: Commande dotnet nuget locals
description: La commande dotnet nuget locals efface ou répertorie les ressources NuGet locales telles que le cache de requête http, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.
author: karann-msft
ms.date: 12/04/2018
ms.openlocfilehash: d0f1c7c2e0b233c214cc48d026c19755fc047bfa
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170754"
---
# <a name="dotnet-nuget-locals"></a>dotnet nuget locals

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet nuget locals` - Efface ou liste les ressources NuGet locales.

## <a name="synopsis"></a>Résumé

```
dotnet nuget locals <CACHE_LOCATION> [(-c|--clear)|(-l|--list)] [--force-english-output]
dotnet nuget locals [-h|--help]
```

## <a name="description"></a>Description

La commande `dotnet nuget locals` efface ou liste les ressources NuGet locales dans le cache de requête HTTP, le cache temporaire ou le dossier des packages globaux à l’échelle de l’ordinateur.

## <a name="arguments"></a>Arguments

* **`CACHE_LOCATION`**

  Emplacement du cache à répertorier ou effacer. L’une des valeurs suivantes est acceptée :

  * `all` : indique que l’opération spécifiée est appliquée à tous les types de cache : le cache de requête HTTP, le cache des packages globaux et le cache temporaire.
  * `http-cache` : indique que l’opération spécifiée est appliquée uniquement au cache de requête HTTP. Les autres emplacements de cache ne sont pas affectés.
  * `global-packages` : indique que l’opération spécifiée est appliquée uniquement au cache des packages globaux. Les autres emplacements de cache ne sont pas affectés.
  * `temp` : indique que l’opération spécifiée est appliquée uniquement au cache temporaire. Les autres emplacements de cache ne sont pas affectés.

## <a name="options"></a>Options

* **`--force-english-output`**

  Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

* **`-h|--help`**

  Affiche une aide brève pour la commande.

* **`-c|--clear`**

  L’option clear exécute une opération d’effacement sur le type de cache spécifié. Le contenu des répertoires de cache est supprimé de manière récursive. Le groupe ou l’utilisateur qui effectue l’opération doit disposer de droits sur les fichiers des répertoires de cache. Sinon, une erreur s’affiche, indiquant les fichiers ou dossiers qui n’ont pas été effacés.

* **`-l|--list`**

  L’option list est utilisée pour afficher l’emplacement du type de cache spécifié.

## <a name="examples"></a>Exemples

* Afficher les chemins d’accès de tous les répertoires de cache local (le répertoire du cache HTTP, le répertoire du cache des packages globaux et le répertoire du cache temporaire) :

  ```console
  dotnet nuget locals –l all
  ```

* Affiche le chemin du répertoire du cache http local :

  ```console
  dotnet nuget locals --list http-cache
  ```

* Effacer tous les fichiers de tous les répertoires de cache local (le répertoire du cache HTTP, le répertoire du cache des packages globaux et le répertoire du cache temporaire) :

  ```console
  dotnet nuget locals --clear all
  ```

* Effacer tous les fichiers du répertoire du cache des packages globaux local :

  ```console
  dotnet nuget locals -c global-packages
  ```

* Effacer tous les fichiers du répertoire du cache temporaire local :

  ```console
  dotnet nuget locals -c temp
  ```

## <a name="troubleshooting"></a>Résolution des problèmes

Pour plus d’informations sur les problèmes et erreurs courants liés à l’utilisation de la commande `dotnet nuget locals`, consultez la page [Gestion du cache NuGet](/nuget/consume-packages/managing-the-nuget-cache).