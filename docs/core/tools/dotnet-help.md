---
title: Commande dotnet help - Interface CLI .NET Core
description: La commande dotnet help affiche une documentation en ligne plus détaillée pour la commande spécifiée.
ms.date: 12/04/2018
ms.openlocfilehash: 60d1cc706ca5c78fa3be877bd679888181213e88
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152173"
---
# <a name="dotnet-help-reference"></a><span data-ttu-id="45c22-103">dotnet help reference</span><span class="sxs-lookup"><span data-stu-id="45c22-103">dotnet help reference</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-2plus.md)]

## <a name="name"></a><span data-ttu-id="45c22-104">Name</span><span class="sxs-lookup"><span data-stu-id="45c22-104">Name</span></span>

<span data-ttu-id="45c22-105">`dotnet help` : affiche une documentation en ligne plus détaillée pour la commande spécifiée.</span><span class="sxs-lookup"><span data-stu-id="45c22-105">`dotnet help` - Shows more detailed documentation online for the specified command.</span></span>

## <a name="synopsis"></a><span data-ttu-id="45c22-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="45c22-106">Synopsis</span></span>

`dotnet help <COMMAND_NAME> [-h|--help]`

## <a name="description"></a><span data-ttu-id="45c22-107">Description</span><span class="sxs-lookup"><span data-stu-id="45c22-107">Description</span></span>

<span data-ttu-id="45c22-108">La commande `dotnet help` ouvre la page de référence sur docs.microsoft.com pour afficher des informations plus détaillées sur la commande spécifiée.</span><span class="sxs-lookup"><span data-stu-id="45c22-108">The `dotnet help` command opens up the reference page for more detailed information about the specified command at docs.microsoft.com.</span></span>

## <a name="arguments"></a><span data-ttu-id="45c22-109">Arguments</span><span class="sxs-lookup"><span data-stu-id="45c22-109">Arguments</span></span>

* **`COMMAND_NAME`**

  <span data-ttu-id="45c22-110">Nom de la commande CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="45c22-110">Name of the .NET Core CLI command.</span></span> <span data-ttu-id="45c22-111">Pour obtenir la liste des commandes CLI valides, consultez [Commandes CLI](index.md#cli-commands).</span><span class="sxs-lookup"><span data-stu-id="45c22-111">For a list of the valid CLI commands, see [CLI commands](index.md#cli-commands).</span></span>

## <a name="options"></a><span data-ttu-id="45c22-112">Options</span><span class="sxs-lookup"><span data-stu-id="45c22-112">Options</span></span>

* **`-h|--help`**

  <span data-ttu-id="45c22-113">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="45c22-113">Prints out a short help for the command.</span></span>

## <a name="examples"></a><span data-ttu-id="45c22-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="45c22-114">Examples</span></span>

* <span data-ttu-id="45c22-115">Ouvre la page de documentation de la commande [dotnet new](dotnet-new.md) :</span><span class="sxs-lookup"><span data-stu-id="45c22-115">Opens the documentation page for the [dotnet new](dotnet-new.md) command:</span></span>

  ```console
  dotnet help new
  ```