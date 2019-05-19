---
ms.openlocfilehash: 975edd1bda507b46da353db788d9730560f9b573
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632110"
---
> [!NOTE]
> À partir du kit SDK .NET Core 2.0, vous n’avez pas à exécuter [`dotnet restore`](~/docs/core/tools/dotnet-restore.md), car il est exécuté implicitement par toutes les commandes qui réclament une restauration, comme `dotnet new`, `dotnet build` et `dotnet run`.
> Cette commande reste néanmoins valide dans certains scénarios où une restauration explicite est nécessaire, comme des [builds d’intégration continue dans Azure DevOps Services](https://docs.microsoft.com/azure/devops/build-release/apps/aspnet/build-aspnet-core) ou dans les systèmes de génération qui doivent contrôler explicitement le moment auquel la restauration se produit.
