---
title: Commande dotnet build-server
description: La commande dotnet build-server interagit avec les serveurs démarrés par une build.
ms.date: 04/24/2019
ms.openlocfilehash: fa663bc045e8abfc3375a0226be7d16331b49740
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632095"
---
# <a name="dotnet-build-server"></a><span data-ttu-id="e4138-103">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="e4138-103">dotnet build-server</span></span>

<span data-ttu-id="e4138-104">**Cet article s’applique à : ✓** SDK .NET Core 2.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="e4138-104">**This article applies to: ✓** .NET Core 2.1 SDK and later versions</span></span>

<!-- todo: uncomment when all CLI commands are reviewed
[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]
-->

## <a name="name"></a><span data-ttu-id="e4138-105">Name</span><span class="sxs-lookup"><span data-stu-id="e4138-105">Name</span></span>

<span data-ttu-id="e4138-106">`dotnet build-server` -Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="e4138-106">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="e4138-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e4138-107">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="e4138-108">Commandes</span><span class="sxs-lookup"><span data-stu-id="e4138-108">Commands</span></span>

* **`shutdown`**

  <span data-ttu-id="e4138-109">Arrête les serveurs de builds démarrés à partir de dotnet.</span><span class="sxs-lookup"><span data-stu-id="e4138-109">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="e4138-110">Par défaut, tous les serveurs sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="e4138-110">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="e4138-111">Options</span><span class="sxs-lookup"><span data-stu-id="e4138-111">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="e4138-112">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="e4138-112">Prints out a short help for the command.</span></span>

* **`--msbuild`**

  <span data-ttu-id="e4138-113">Arrête le serveur de builds MSBuild.</span><span class="sxs-lookup"><span data-stu-id="e4138-113">Shuts down the MSBuild build server.</span></span>

* **`--razor`**

  <span data-ttu-id="e4138-114">Arrête le serveur de builds Razor.</span><span class="sxs-lookup"><span data-stu-id="e4138-114">Shuts down the Razor build server.</span></span>

* **`--vbcscompiler`**

  <span data-ttu-id="e4138-115">Arrête le serveur de builds du compilateur VB/C#.</span><span class="sxs-lookup"><span data-stu-id="e4138-115">Shuts down the VB/C# compiler build server.</span></span>
