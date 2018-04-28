---
title: Commande dotnet msbuild - Interface CLI .NET Core
description: La commande dotnet msbuild fournit l’accès à la ligne de commande MSbuild.
author: mairaw
ms.author: mairaw
ms.date: 08/14/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 9e6f8b3063b4cd2a3a36cae8839d6f83e0466e03
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-msbuild"></a><span data-ttu-id="10b64-103">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="10b64-103">dotnet msbuild</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="10b64-104">Name</span><span class="sxs-lookup"><span data-stu-id="10b64-104">Name</span></span>

<span data-ttu-id="10b64-105">`dotnet msbuild` : Génère un projet et l’ensemble de ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="10b64-105">`dotnet msbuild` - Builds a project and all of its dependencies.</span></span>

## <a name="synopsis"></a><span data-ttu-id="10b64-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="10b64-106">Synopsis</span></span>

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a><span data-ttu-id="10b64-107">Description</span><span class="sxs-lookup"><span data-stu-id="10b64-107">Description</span></span>

<span data-ttu-id="10b64-108">La commande `dotnet msbuild` permet d’accéder à un outil MSBuild entièrement fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="10b64-108">The `dotnet msbuild` command allows access to a fully functional MSBuild.</span></span>

<span data-ttu-id="10b64-109">La commande a les mêmes fonctionnalités que le client de ligne de commande MSBuild existant.</span><span class="sxs-lookup"><span data-stu-id="10b64-109">The command has the exact same capabilities as existing MSBuild command-line client.</span></span> <span data-ttu-id="10b64-110">Les options sont identiques.</span><span class="sxs-lookup"><span data-stu-id="10b64-110">The options are all the same.</span></span> <span data-ttu-id="10b64-111">Utilisez les [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference) pour obtenir des informations sur les options disponibles.</span><span class="sxs-lookup"><span data-stu-id="10b64-111">Use the [MSBuild Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference) to obtain information on the available options.</span></span> 

## <a name="examples"></a><span data-ttu-id="10b64-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="10b64-112">Examples</span></span>

<span data-ttu-id="10b64-113">Générer un projet et ses dépendances :</span><span class="sxs-lookup"><span data-stu-id="10b64-113">Build a project and its dependencies:</span></span>

`dotnet msbuild`

<span data-ttu-id="10b64-114">Générer un projet et ses dépendances à l’aide de la configuration Release :</span><span class="sxs-lookup"><span data-stu-id="10b64-114">Build a project and its dependencies using Release configuration:</span></span>

`dotnet msbuild /p:Configuration=Release`

<span data-ttu-id="10b64-115">Exécuter la cible de publication et effectuer une publication pour le RID `osx.10.11-x64` :</span><span class="sxs-lookup"><span data-stu-id="10b64-115">Run the publish target and publish for the `osx.10.11-x64` RID:</span></span>

`dotnet msbuild /t:Publish /p:RuntimeIdentifiers=osx.10.11-x64`

<span data-ttu-id="10b64-116">Consultez la totalité du projet avec toutes les cibles incluses par le kit SDK :</span><span class="sxs-lookup"><span data-stu-id="10b64-116">See the whole project with all targets included by the SDK:</span></span>

`dotnet msbuild /pp`
