---
ms.openlocfilehash: 497ac09e5c9a10470d3ae1932d7e3dc114d121dd
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632014"
---
> [!NOTE]
> À compter de .NET Core 2.0, vous ne devez pas exécuter [`dotnet restore`](~/docs/core/tools/dotnet-restore.md), car il est exécuté implicitement par toutes les commandes qui nécessitent une restauration, comme `dotnet build` et `dotnet run`. Cette commande reste néanmoins valide dans certains scénarios où une restauration explicite est nécessaire, comme des [builds d’intégration continue dans Azure DevOps Services](/azure/devops/build-release/apps/aspnet/build-aspnet-core) ou dans les systèmes de génération qui doivent contrôler explicitement le moment auquel la restauration se produit.
>
> Cette commande prend également en charge les options de `dotnet restore` quand elles sont passées sous leur forme longue (par exemple `--source`). Les options sous forme abrégée, comme `-s`, ne sont pas prises en charge.
