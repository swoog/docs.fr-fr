---
title: Commande dotnet list reference
description: La commande dotnet list reference est une option pratique pour lister des références entre projets.
ms.date: 12/03/2018
ms.openlocfilehash: c0b88c4a0af4469d7ddc9e0a9368bb1b2d9d20b6
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632408"
---
# <a name="dotnet-list-reference"></a><span data-ttu-id="cd133-103">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="cd133-103">dotnet list reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="cd133-104">Name</span><span class="sxs-lookup"><span data-stu-id="cd133-104">Name</span></span>

<span data-ttu-id="cd133-105">`dotnet list reference` : répertorie des références entre projets.</span><span class="sxs-lookup"><span data-stu-id="cd133-105">`dotnet list reference` - Lists project-to-project references.</span></span>

## <a name="synopsis"></a><span data-ttu-id="cd133-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="cd133-106">Synopsis</span></span>

`dotnet list [<PROJECT>] reference [-h|--help]`

## <a name="description"></a><span data-ttu-id="cd133-107">Description</span><span class="sxs-lookup"><span data-stu-id="cd133-107">Description</span></span>

<span data-ttu-id="cd133-108">La commande `dotnet list reference` est pratique pour lister les références à un projet ou à une solution donné.</span><span class="sxs-lookup"><span data-stu-id="cd133-108">The `dotnet list reference` command provides a convenient option to list project references for a given project or solution.</span></span>

## <a name="arguments"></a><span data-ttu-id="cd133-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="cd133-109">Arguments</span></span>

* **`PROJECT`**

  <span data-ttu-id="cd133-110">Spécifie le fichier projet à utiliser pour répertorier les références.</span><span class="sxs-lookup"><span data-stu-id="cd133-110">Specifies the project file to use for listing references.</span></span> <span data-ttu-id="cd133-111">Si aucun fichier n’est spécifié, la commande recherche un fichier projet dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="cd133-111">If not specified, the command searches the current directory for a project file.</span></span>

## <a name="options"></a><span data-ttu-id="cd133-112">Options</span><span class="sxs-lookup"><span data-stu-id="cd133-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="cd133-113">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="cd133-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="cd133-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="cd133-114">Examples</span></span>

* <span data-ttu-id="cd133-115">Lister les références de projet pour le projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="cd133-115">List the project references for the specified project:</span></span>

  ```console
  dotnet list app/app.csproj reference
  ```

* <span data-ttu-id="cd133-116">Lister les références de projet du projet dans le répertoire actuel :</span><span class="sxs-lookup"><span data-stu-id="cd133-116">List the project references for the project in the current directory:</span></span>

  ```console
  dotnet list reference
  ```
