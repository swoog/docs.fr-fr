---
title: Commande dotnet build-server - CLI .NET Core
description: La commande dotnet build-server interagit avec les serveurs démarrés par une build.
ms.date: 12/04/2018
ms.openlocfilehash: 2746ade12cc819089258483e84a8c0f02a64c755
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53125676"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="ac2c8-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="ac2c8-103">dotnet build-server</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="ac2c8-104">Name</span><span class="sxs-lookup"><span data-stu-id="ac2c8-104">Name</span></span>

<span data-ttu-id="ac2c8-105">`dotnet build-server` -Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ac2c8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac2c8-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="ac2c8-107">Commandes</span><span class="sxs-lookup"><span data-stu-id="ac2c8-107">Commands</span></span>

* **`shutdown`**

  <span data-ttu-id="ac2c8-108">Arrête les serveurs de builds démarrés à partir de dotnet.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="ac2c8-109">Par défaut, tous les serveurs sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="ac2c8-110">Options</span><span class="sxs-lookup"><span data-stu-id="ac2c8-110">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="ac2c8-111">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-111">Prints out a short help for the command.</span></span>

* **`--msbuild`**

  <span data-ttu-id="ac2c8-112">Arrête le serveur de builds MSBuild.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-112">Shuts down the MSBuild build server.</span></span>

* **`--razor`**

  <span data-ttu-id="ac2c8-113">Arrête le serveur de builds Razor.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-113">Shuts down the Razor build server.</span></span>

* **`--vbcscompiler`**

  <span data-ttu-id="ac2c8-114">Arrête le serveur de builds du compilateur VB/C#.</span><span class="sxs-lookup"><span data-stu-id="ac2c8-114">Shuts down the VB/C# compiler build server.</span></span>