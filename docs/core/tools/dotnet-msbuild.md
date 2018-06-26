---
title: Commande dotnet msbuild - Interface CLI .NET Core
description: La commande dotnet msbuild fournit l’accès à la ligne de commande MSbuild.
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 58aac2a5314758b8711c0b014154022168fb671c
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696843"
---
# <a name="dotnet-msbuild"></a><span data-ttu-id="68ee8-103">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="68ee8-103">dotnet msbuild</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="68ee8-104">Name</span><span class="sxs-lookup"><span data-stu-id="68ee8-104">Name</span></span>

<span data-ttu-id="68ee8-105">`dotnet msbuild` : Génère un projet et l’ensemble de ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="68ee8-105">`dotnet msbuild` - Builds a project and all of its dependencies.</span></span>

## <a name="synopsis"></a><span data-ttu-id="68ee8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="68ee8-106">Synopsis</span></span>

`dotnet msbuild <msbuild_arguments> [-h]`

## <a name="description"></a><span data-ttu-id="68ee8-107">Description</span><span class="sxs-lookup"><span data-stu-id="68ee8-107">Description</span></span>

<span data-ttu-id="68ee8-108">La commande `dotnet msbuild` permet d’accéder à un outil MSBuild entièrement fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="68ee8-108">The `dotnet msbuild` command allows access to a fully functional MSBuild.</span></span>

<span data-ttu-id="68ee8-109">La commande a les mêmes fonctionnalités que le client de ligne de commande MSBuild existant.</span><span class="sxs-lookup"><span data-stu-id="68ee8-109">The command has the exact same capabilities as existing MSBuild command-line client.</span></span> <span data-ttu-id="68ee8-110">Les options sont identiques.</span><span class="sxs-lookup"><span data-stu-id="68ee8-110">The options are all the same.</span></span> <span data-ttu-id="68ee8-111">Pour plus d’informations sur les options disponibles, consultez [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference).</span><span class="sxs-lookup"><span data-stu-id="68ee8-111">For more information about the available options, see the [MSBuild Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference).</span></span>

## <a name="examples"></a><span data-ttu-id="68ee8-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="68ee8-112">Examples</span></span>

<span data-ttu-id="68ee8-113">Générer un projet et ses dépendances :</span><span class="sxs-lookup"><span data-stu-id="68ee8-113">Build a project and its dependencies:</span></span>

`dotnet msbuild`

<span data-ttu-id="68ee8-114">Générer un projet et ses dépendances à l’aide de la configuration Release :</span><span class="sxs-lookup"><span data-stu-id="68ee8-114">Build a project and its dependencies using Release configuration:</span></span>

`dotnet msbuild /p:Configuration=Release`

<span data-ttu-id="68ee8-115">Exécuter la cible de publication et effectuer une publication pour le RID `osx.10.11-x64` :</span><span class="sxs-lookup"><span data-stu-id="68ee8-115">Run the publish target and publish for the `osx.10.11-x64` RID:</span></span>

`dotnet msbuild /t:Publish /p:RuntimeIdentifiers=osx.10.11-x64`

<span data-ttu-id="68ee8-116">Consultez la totalité du projet avec toutes les cibles incluses par le kit SDK :</span><span class="sxs-lookup"><span data-stu-id="68ee8-116">See the whole project with all targets included by the SDK:</span></span>

`dotnet msbuild /pp`
