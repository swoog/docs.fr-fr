---
title: Commande dotnet build-server
description: La commande dotnet build-server interagit avec les serveurs démarrés par une build.
ms.date: 12/04/2018
ms.openlocfilehash: 7f78a0cae6e3297f3084754dc56b0da4eac38caf
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169654"
---
# <a name="dotnet-build-server"></a>dotnet build-server

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>Name

`dotnet build-server` -Interagit avec les serveurs démarrés par une build.

## <a name="synopsis"></a>Résumé

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a>Commandes

* **`shutdown`**

  Arrête les serveurs de builds démarrés à partir de dotnet. Par défaut, tous les serveurs sont arrêtés.

## <a name="options"></a>Options

* **`-h|--help`**

  Affiche une aide brève pour la commande.

* **`--msbuild`**

  Arrête le serveur de builds MSBuild.

* **`--razor`**

  Arrête le serveur de builds Razor.

* **`--vbcscompiler`**

  Arrête le serveur de builds du compilateur VB/C#.