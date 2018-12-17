---
title: Commande dotnet nuget delete - Interface CLI .NET Core
description: La commande nuget-dotnet-delete supprime ou retire un package du serveur.
author: karann-msft
ms.date: 12/04/2018
ms.openlocfilehash: 451352ea652b77e44dcaf731d5b6cce230d1ef78
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53126833"
---
# <a name="dotnet-nuget-delete"></a><span data-ttu-id="b6bba-103">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="b6bba-103">dotnet nuget delete</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="b6bba-104">Name</span><span class="sxs-lookup"><span data-stu-id="b6bba-104">Name</span></span>

<span data-ttu-id="b6bba-105">`dotnet nuget delete` -Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-105">`dotnet nuget delete` - Deletes or unlists a package from the server.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b6bba-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b6bba-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="b6bba-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="b6bba-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [--interactive] [-k|--api-key] [--no-service-endpoint]
    [--non-interactive] [-s|--source]
dotnet nuget delete [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="b6bba-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="b6bba-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--non-interactive]
    [-s|--source]
dotnet nuget delete [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="b6bba-109">Description</span><span class="sxs-lookup"><span data-stu-id="b6bba-109">Description</span></span>

<span data-ttu-id="b6bba-110">La commande `dotnet nuget delete` supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-110">The `dotnet nuget delete` command deletes or unlists a package from the server.</span></span> <span data-ttu-id="b6bba-111">Pour [nuget.org](https://www.nuget.org/), l’action consiste à supprimer le package de la liste.</span><span class="sxs-lookup"><span data-stu-id="b6bba-111">For [nuget.org](https://www.nuget.org/), the action is to unlist the package.</span></span>

## <a name="arguments"></a><span data-ttu-id="b6bba-112">Arguments</span><span class="sxs-lookup"><span data-stu-id="b6bba-112">Arguments</span></span>

* **`PACKAGE_NAME`**

  <span data-ttu-id="b6bba-113">Nom/ID du package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b6bba-113">Name/ID of the package to delete.</span></span>

* **`PACKAGE_VERSION`**

  <span data-ttu-id="b6bba-114">Version du package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b6bba-114">Version of the package to delete.</span></span>

## <a name="options"></a><span data-ttu-id="b6bba-115">Options</span><span class="sxs-lookup"><span data-stu-id="b6bba-115">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="b6bba-116">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="b6bba-116">.NET Core 2.x</span></span>](#tab/netcore2x)

* **`--force-english-output`**

  <span data-ttu-id="b6bba-117">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="b6bba-117">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

  <span data-ttu-id="b6bba-118">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="b6bba-118">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="b6bba-119">Autorise la commande pour bloquer et exige une action manuelle pour des opérations comme l'authentification.</span><span class="sxs-lookup"><span data-stu-id="b6bba-119">Allows the command to block and requires manual action for operations like authentication.</span></span> <span data-ttu-id="b6bba-120">Option disponible à partir du kit SDK .NET Core 2.2.</span><span class="sxs-lookup"><span data-stu-id="b6bba-120">Option available since .NET Core 2.2 SDK.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="b6bba-121">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-121">The API key for the server.</span></span>

* **`--no-service-endpoint`**

  <span data-ttu-id="b6bba-122">N’ajoute pas « api/v2/package » à l’URL source.</span><span class="sxs-lookup"><span data-stu-id="b6bba-122">Doesn't append "api/v2/package" to the source URL.</span></span> <span data-ttu-id="b6bba-123">Option disponible à partir du kit SDK .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="b6bba-123">Option available since .NET Core 2.1 SDK.</span></span>

* **`--non-interactive`**

  <span data-ttu-id="b6bba-124">Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-124">Doesn't prompt for user input or confirmations.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="b6bba-125">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-125">Specifies the server URL.</span></span> <span data-ttu-id="b6bba-126">Les URL prises en charge pour nuget.org incluent `https://www.nuget.org`, `https://www.nuget.org/api/v3` et `https://www.nuget.org/api/v2/package`.</span><span class="sxs-lookup"><span data-stu-id="b6bba-126">Supported URLs for nuget.org include `https://www.nuget.org`, `https://www.nuget.org/api/v3`, and `https://www.nuget.org/api/v2/package`.</span></span> <span data-ttu-id="b6bba-127">Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).</span><span class="sxs-lookup"><span data-stu-id="b6bba-127">For private feeds, replace the host name (for example, `%hostname%/api/v3`).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="b6bba-128">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="b6bba-128">.NET Core 1.x</span></span>](#tab/netcore1x)

* **`--force-english-output`**

  <span data-ttu-id="b6bba-129">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="b6bba-129">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

  <span data-ttu-id="b6bba-130">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="b6bba-130">Prints out a short help for the command.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="b6bba-131">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-131">The API key for the server.</span></span>

* **`--non-interactive`**

  <span data-ttu-id="b6bba-132">Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-132">Doesn't prompt for user input or confirmations.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="b6bba-133">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="b6bba-133">Specifies the server URL.</span></span> <span data-ttu-id="b6bba-134">Les URL prises en charge pour nuget.org incluent `https://www.nuget.org`, `https://www.nuget.org/api/v3` et `https://www.nuget.org/api/v2/package`.</span><span class="sxs-lookup"><span data-stu-id="b6bba-134">Supported URLs for nuget.org include `https://www.nuget.org`, `https://www.nuget.org/api/v3`, and `https://www.nuget.org/api/v2/package`.</span></span> <span data-ttu-id="b6bba-135">Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).</span><span class="sxs-lookup"><span data-stu-id="b6bba-135">For private feeds, replace the host name (for example, `%hostname%/api/v3`).</span></span>

---

## <a name="examples"></a><span data-ttu-id="b6bba-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="b6bba-136">Examples</span></span>

* <span data-ttu-id="b6bba-137">Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` :</span><span class="sxs-lookup"><span data-stu-id="b6bba-137">Deletes version 1.0 of package `Microsoft.AspNetCore.Mvc`:</span></span>

  ```console
  dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0
  ```

* <span data-ttu-id="b6bba-138">Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` sans inviter l’utilisateur à fournir ses informations d’identification ou d’autres données :</span><span class="sxs-lookup"><span data-stu-id="b6bba-138">Deletes version 1.0 of package `Microsoft.AspNetCore.Mvc`, not prompting user for credentials or other input:</span></span>

  ```console
  dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0 --non-interactive
  ```