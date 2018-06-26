---
title: Commande dotnet list reference - Interface CLI .NET Core
description: La commande dotnet list reference est une option pratique pour lister des références entre projets.
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 821e6d276af44bf984c8ac1b42b4e954dbe69556
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34697181"
---
# <a name="dotnet-list-reference"></a><span data-ttu-id="98cf9-103">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="98cf9-103">dotnet list reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="98cf9-104">Name</span><span class="sxs-lookup"><span data-stu-id="98cf9-104">Name</span></span>

<span data-ttu-id="98cf9-105">`dotnet list reference` : répertorie des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="98cf9-105">`dotnet list reference` - Lists project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="98cf9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="98cf9-106">Synopsis</span></span>

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a><span data-ttu-id="98cf9-107">Description</span><span class="sxs-lookup"><span data-stu-id="98cf9-107">Description</span></span>

<span data-ttu-id="98cf9-108">La commande `dotnet list reference` est une option pratique pour répertorier des références de projet pour un projet donné.</span><span class="sxs-lookup"><span data-stu-id="98cf9-108">The `dotnet list reference` command provides a convenient option to list project references for a given project.</span></span>

## <a name="arguments"></a><span data-ttu-id="98cf9-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="98cf9-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="98cf9-110">Spécifie le fichier projet à utiliser pour répertorier les références.</span><span class="sxs-lookup"><span data-stu-id="98cf9-110">Specifies the project file to use for listing references.</span></span> <span data-ttu-id="98cf9-111">Si aucun fichier n’est spécifié, la commande recherche un fichier projet dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="98cf9-111">If not specified, the command searches the current directory for a project file.</span></span>

## <a name="options"></a><span data-ttu-id="98cf9-112">Options</span><span class="sxs-lookup"><span data-stu-id="98cf9-112">Options</span></span>

`-h|--help`

<span data-ttu-id="98cf9-113">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="98cf9-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="98cf9-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="98cf9-114">Examples</span></span>

<span data-ttu-id="98cf9-115">Lister les références de projet pour le projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="98cf9-115">List the project references for the specified project:</span></span>

`dotnet list app/app.csproj reference`

<span data-ttu-id="98cf9-116">Lister les références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="98cf9-116">List the project references for the project in the current directory:</span></span>

`dotnet list reference`