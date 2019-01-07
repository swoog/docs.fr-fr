---
title: Commande dotnet help
description: La commande dotnet help affiche une documentation en ligne plus détaillée pour la commande spécifiée.
ms.date: 12/04/2018
ms.openlocfilehash: 44274b698ed83bd3cdb58787f433eeb5c555bc6d
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53168950"
---
# <a name="dotnet-help-reference"></a>dotnet help reference

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-2plus.md)]

## <a name="name"></a>Name

`dotnet help` : affiche une documentation en ligne plus détaillée pour la commande spécifiée.

## <a name="synopsis"></a>Résumé

`dotnet help <COMMAND_NAME> [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet help` ouvre la page de référence sur docs.microsoft.com pour afficher des informations plus détaillées sur la commande spécifiée.

## <a name="arguments"></a>Arguments

* **`COMMAND_NAME`**

  Nom de la commande CLI .NET Core. Pour obtenir la liste des commandes CLI valides, consultez [Commandes CLI](index.md#cli-commands).

## <a name="options"></a>Options

* **`-h|--help`**

  Affiche une aide brève pour la commande.

## <a name="examples"></a>Exemples

* Ouvre la page de documentation de la commande [dotnet new](dotnet-new.md) :

  ```console
  dotnet help new
  ```