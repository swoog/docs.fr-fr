---
title: Commande dotnet list reference - Interface CLI .NET Core
description: La commande dotnet list reference est une option pratique pour lister des références entre projets.
author: mairaw
ms.author: mairaw
ms.date: 08/14/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 946d3d523443fbe673b95dba95dbca327fde1699
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-list-reference"></a><span data-ttu-id="afb6b-103">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="afb6b-103">dotnet list reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="afb6b-104">Name</span><span class="sxs-lookup"><span data-stu-id="afb6b-104">Name</span></span>

<span data-ttu-id="afb6b-105">`dotnet list reference` : Répertorie des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="afb6b-105">`dotnet list reference` - Lists project to project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="afb6b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="afb6b-106">Synopsis</span></span>

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a><span data-ttu-id="afb6b-107">Description</span><span class="sxs-lookup"><span data-stu-id="afb6b-107">Description</span></span>

<span data-ttu-id="afb6b-108">La commande `dotnet list reference` est une option pratique pour répertorier des références de projet pour un projet donné.</span><span class="sxs-lookup"><span data-stu-id="afb6b-108">The `dotnet list reference` command provides a convenient option to list project references for a given project.</span></span>

## <a name="arguments"></a><span data-ttu-id="afb6b-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="afb6b-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="afb6b-110">Spécifie le fichier projet à utiliser pour répertorier les références.</span><span class="sxs-lookup"><span data-stu-id="afb6b-110">Specifies the project file to use for listing references.</span></span> <span data-ttu-id="afb6b-111">Si aucun fichier n’est spécifié, la commande recherche un fichier projet dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="afb6b-111">If not specified, the command will search the current directory for a project file.</span></span>

## <a name="options"></a><span data-ttu-id="afb6b-112">Options</span><span class="sxs-lookup"><span data-stu-id="afb6b-112">Options</span></span>

`-h|--help`

<span data-ttu-id="afb6b-113">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="afb6b-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="afb6b-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="afb6b-114">Examples</span></span>

<span data-ttu-id="afb6b-115">Lister les références de projet pour le projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="afb6b-115">List the project references for the specified project:</span></span>

`dotnet list app/app.csproj reference`

<span data-ttu-id="afb6b-116">Lister les références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="afb6b-116">List the project references for the project in the current directory:</span></span>

`dotnet list reference`
