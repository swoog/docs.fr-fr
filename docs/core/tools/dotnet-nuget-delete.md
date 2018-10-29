---
title: Commande dotnet nuget delete - Interface CLI .NET Core
description: La commande nuget-dotnet-delete supprime ou retire un package du serveur.
author: karann-msft
ms.author: mairaw
ms.date: 06/01/2018
ms.openlocfilehash: f4aa027a465c4adea1de13853063d03e8e295411
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180876"
---
# <a name="dotnet-nuget-delete"></a>dotnet nuget delete

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet nuget delete` -Supprime ou retire un package du serveur.

## <a name="synopsis"></a>Résumé

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--no-service-endpoint]
    [--non-interactive] [-s|--source]
dotnet nuget delete [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--non-interactive]
    [-s|--source]
dotnet nuget delete [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--non-interactive]
    [-s|--source]
dotnet nuget delete [-h|--help]
```
---

## <a name="description"></a>Description

La commande `dotnet nuget delete` supprime ou retire un package du serveur. Pour [nuget.org](https://www.nuget.org/), l’action consiste à supprimer le package de la liste.

## <a name="arguments"></a>Arguments

`PACKAGE_NAME`

Nom/ID du package à supprimer.

`PACKAGE_VERSION`

Version du package à supprimer.

## <a name="options"></a>Options

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)

`--force-english-output`

 Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`--no-service-endpoint` N’ajoute pas « api/v2/package » à l’URL source.

`--non-interactive`

Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Les URL prises en charge pour nuget.org incluent `https://www.nuget.org`, `https://www.nuget.org/api/v3` et `https://www.nuget.org/api/v2/package`. Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).

# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)

`--force-english-output`

 Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`--non-interactive`

Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Les URL prises en charge pour nuget.org incluent `https://www.nuget.org`, `https://www.nuget.org/api/v3` et `https://www.nuget.org/api/v2/package`. Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

`--force-english-output`

 Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`--non-interactive`

Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Les URL prises en charge pour nuget.org incluent `https://www.nuget.org`, `https://www.nuget.org/api/v3` et `https://www.nuget.org/api/v2/package`. Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).

---

## <a name="examples"></a>Exemples

Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` :

`dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0`

Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` sans inviter l’utilisateur à fournir ses informations d’identification ou d’autres données :

`dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0 --non-interactive`
