---
title: Commande dotnet help
description: La commande dotnet help affiche une documentation en ligne plus détaillée pour la commande spécifiée.
ms.date: 12/04/2018
ms.openlocfilehash: 8694494720cdb9a540754fdf79eeb99d5dbe61ef
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65631986"
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
