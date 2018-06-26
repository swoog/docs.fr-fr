---
title: Commande dotnet build-server - CLI .NET Core
description: La commande dotnet build-server interagit avec les serveurs démarrés par une build.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 929b8d74aa5f3f0ad73b108be8a5bf22f86e30d6
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696252"
---
# <a name="dotnet-build"></a><span data-ttu-id="a1046-103">dotnet-build</span><span class="sxs-lookup"><span data-stu-id="a1046-103">dotnet-build</span></span>

[!INCLUDE [topic-appliesto-net-core-21plus](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a><span data-ttu-id="a1046-104">Name</span><span class="sxs-lookup"><span data-stu-id="a1046-104">Name</span></span>

<span data-ttu-id="a1046-105">`dotnet build-server` -Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="a1046-105">`dotnet build-server` - Interacts with servers started by a build.</span></span>

## <a name="synopsis"></a><span data-ttu-id="a1046-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a1046-106">Synopsis</span></span>

```
dotnet build-server shutdown [--msbuild] [--razor] [--vbcscompiler]
dotnet build-server shutdown [-h|--help]
dotnet build-server [-h|--help]
```

## <a name="commands"></a><span data-ttu-id="a1046-107">Commandes</span><span class="sxs-lookup"><span data-stu-id="a1046-107">Commands</span></span>

`shutdown`

<span data-ttu-id="a1046-108">Arrête les serveurs de builds démarrés à partir de dotnet.</span><span class="sxs-lookup"><span data-stu-id="a1046-108">Shuts down build servers that are started from dotnet.</span></span> <span data-ttu-id="a1046-109">Par défaut, tous les serveurs sont arrêtés.</span><span class="sxs-lookup"><span data-stu-id="a1046-109">By default, all servers are shut down.</span></span>

## <a name="options"></a><span data-ttu-id="a1046-110">Options</span><span class="sxs-lookup"><span data-stu-id="a1046-110">Options</span></span>

`-h|--help`

<span data-ttu-id="a1046-111">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a1046-111">Prints out a short help for the command.</span></span>

`--msbuild`

<span data-ttu-id="a1046-112">Arrête le serveur de builds MSBuild.</span><span class="sxs-lookup"><span data-stu-id="a1046-112">Shuts down the MSBuild build server.</span></span>

`--razor`

<span data-ttu-id="a1046-113">Arrête le serveur de builds Razor.</span><span class="sxs-lookup"><span data-stu-id="a1046-113">Shuts down the Razor build server.</span></span>

`--vbcscompiler`

<span data-ttu-id="a1046-114">Arrête le serveur de builds du compilateur VB/C#.</span><span class="sxs-lookup"><span data-stu-id="a1046-114">Shuts down the VB/C# compiler build server.</span></span>
