---
title: Commande dotnet remove package - Interface CLI .NET Core
description: La commande dotnet remove package est une option pratique pour supprimer une référence de package NuGet d’un projet.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: ed6086bfdfadaa06494c857fc74687f1273af971
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696856"
---
# <a name="dotnet-remove-package"></a><span data-ttu-id="f4c85-103">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="f4c85-103">dotnet remove package</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="f4c85-104">Name</span><span class="sxs-lookup"><span data-stu-id="f4c85-104">Name</span></span>

<span data-ttu-id="f4c85-105">`dotnet remove package` : Supprime une référence de package d’un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="f4c85-105">`dotnet remove package` - Removes package reference from a project file.</span></span>

## <a name="synopsis"></a><span data-ttu-id="f4c85-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f4c85-106">Synopsis</span></span>

`dotnet remove [<PROJECT>] package <PACKAGE_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="f4c85-107">Description</span><span class="sxs-lookup"><span data-stu-id="f4c85-107">Description</span></span>

<span data-ttu-id="f4c85-108">La commande `dotnet remove package` est une option pratique pour supprimer une référence de package NuGet d’un projet.</span><span class="sxs-lookup"><span data-stu-id="f4c85-108">The `dotnet remove package` command provides a convenient option to remove a NuGet package reference from a project.</span></span>

## <a name="arguments"></a><span data-ttu-id="f4c85-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="f4c85-109">Arguments</span></span>

`PROJECT`

<span data-ttu-id="f4c85-110">Spécifie le nom du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="f4c85-110">Specifies the project file.</span></span> <span data-ttu-id="f4c85-111">Si aucun fichier n’est spécifié, la commande en recherche un dans le répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="f4c85-111">If not specified, the command searches the current directory for one.</span></span>

`PACKAGE_NAME`

<span data-ttu-id="f4c85-112">Référence de package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f4c85-112">The package reference to remove.</span></span>

## <a name="options"></a><span data-ttu-id="f4c85-113">Options</span><span class="sxs-lookup"><span data-stu-id="f4c85-113">Options</span></span>

`-h|--help`

<span data-ttu-id="f4c85-114">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="f4c85-114">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="f4c85-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="f4c85-115">Examples</span></span>

<span data-ttu-id="f4c85-116">Supprime le package NuGet `Newtonsoft.Json` d’un projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="f4c85-116">Removes `Newtonsoft.Json` NuGet package from a project in the current directory:</span></span>

`dotnet remove package Newtonsoft.Json`