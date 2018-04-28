---
title: Commande dotnet remove package - Interface CLI .NET Core
description: La commande dotnet remove package est une option pratique pour supprimer une référence de package NuGet d’un projet.
author: mairaw
ms.author: mairaw
ms.date: 08/14/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: bdb66a24526b04e8300e654a991719bb607971b8
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-remove-package"></a><span data-ttu-id="35677-103">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="35677-103">dotnet remove package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="35677-104">Name</span><span class="sxs-lookup"><span data-stu-id="35677-104">Name</span></span>

<span data-ttu-id="35677-105">`dotnet remove package` : Supprime une référence de package d’un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="35677-105">`dotnet remove package` - Removes package reference from a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="35677-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="35677-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="35677-107">Description</span><span class="sxs-lookup"><span data-stu-id="35677-107">Description</span></span>

<span data-ttu-id="35677-108">La commande `dotnet remove package` est une option pratique pour supprimer une référence de package NuGet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="35677-108">The `dotnet remove package` command provides a convenient option to remove a NuGet package reference from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="35677-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="35677-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="35677-110">Spécifie le nom du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="35677-110">Specifies the project file.</span></span> <span data-ttu-id="35677-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="35677-111">If not specified, the command will search the current directory for one.</span></span>

`PACKAGE_NAME`

<span data-ttu-id="35677-112">Référence de package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="35677-112">The package reference to remove.</span></span>

## <a name="options"></a><span data-ttu-id="35677-113">Options</span><span class="sxs-lookup"><span data-stu-id="35677-113">Options</span></span>

`-h|--help`

<span data-ttu-id="35677-114">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="35677-114">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="35677-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="35677-115">Examples</span></span>

<span data-ttu-id="35677-116">Supprime le package NuGet `Newtonsoft.Json` d’un projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="35677-116">Removes `Newtonsoft.Json` NuGet package from a project in the current directory:</span></span>

`dotnet remove package Newtonsoft.Json`
