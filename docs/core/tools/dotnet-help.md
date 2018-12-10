---
title: Commande dotnet help - Interface CLI .NET Core
description: La commande dotnet help affiche une documentation en ligne plus détaillée pour la commande spécifiée.
ms.date: 12/04/2018
ms.openlocfilehash: 60d1cc706ca5c78fa3be877bd679888181213e88
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152173"
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