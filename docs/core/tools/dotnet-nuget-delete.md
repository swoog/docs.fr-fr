---
title: Commande dotnet nuget delete - Interface CLI .NET Core
description: La commande nuget-dotnet-delete supprime ou retire un package du serveur.
author: karann-msft
ms.author: mairaw
ms.date: 06/01/2018
ms.openlocfilehash: 1b58136d0bc04947f0a5baba320e5e6b3e45e2f1
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34728412"
---
# <a name="dotnet-nuget-delete"></a><span data-ttu-id="0eb4f-103">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="0eb4f-103">dotnet nuget delete</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="0eb4f-104">Name</span><span class="sxs-lookup"><span data-stu-id="0eb4f-104">Name</span></span>

<span data-ttu-id="0eb4f-105">`dotnet nuget delete` -Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-105">`dotnet nuget delete` - Deletes or unlists a package from the server.</span></span>

## <a name="synopsis"></a><span data-ttu-id="0eb4f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0eb4f-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="0eb4f-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="0eb4f-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--no-service-endpoint]
    [--non-interactive] [-s|--source]
dotnet nuget delete [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="0eb4f-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb4f-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--non-interactive]
    [-s|--source]
dotnet nuget delete [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="0eb4f-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="0eb4f-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet nuget delete [<PACKAGE_NAME> <PACKAGE_VERSION>] [--force-english-output] [-k|--api-key] [--non-interactive]
    [-s|--source]
dotnet nuget delete [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="0eb4f-110">Description</span><span class="sxs-lookup"><span data-stu-id="0eb4f-110">Description</span></span>

<span data-ttu-id="0eb4f-111">La commande `dotnet nuget delete` supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-111">The `dotnet nuget delete` command deletes or unlists a package from the server.</span></span> <span data-ttu-id="0eb4f-112">Pour [nuget.org](https://www.nuget.org/), l’action consiste à supprimer le package de la liste.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-112">For [nuget.org](https://www.nuget.org/), the action is to unlist the package.</span></span>

## <a name="arguments"></a><span data-ttu-id="0eb4f-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="0eb4f-113">Arguments</span></span>

`PACKAGE_NAME`

<span data-ttu-id="0eb4f-114">Nom/ID du package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-114">Name/ID of the package to delete.</span></span>

`PACKAGE_VERSION`

<span data-ttu-id="0eb4f-115">Version du package à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-115">Version of the package to delete.</span></span>

## <a name="options"></a><span data-ttu-id="0eb4f-116">Options</span><span class="sxs-lookup"><span data-stu-id="0eb4f-116">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="0eb4f-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="0eb4f-117">.NET Core 2.1</span></span>](#tab/netcore21)

`--force-english-output`

 <span data-ttu-id="0eb4f-118">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-118">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="0eb4f-119">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-119">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="0eb4f-120">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-120">The API key for the server.</span></span>

<span data-ttu-id="0eb4f-121">`--no-service-endpoint` N’ajoute pas « api/v2/package » à l’URL source.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-121">`--no-service-endpoint` Doesn't append "api/v2/package" to the source URL.</span></span>

`--non-interactive`

<span data-ttu-id="0eb4f-122">Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-122">Doesn't prompt for user input or confirmations.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="0eb4f-123">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-123">Specifies the server URL.</span></span> <span data-ttu-id="0eb4f-124">Les URL prises en charge pour nuget.org incluent `http://www.nuget.org`, `http://www.nuget.org/api/v3` et `http://www.nuget.org/api/v2/package`.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-124">Supported URLs for nuget.org include `http://www.nuget.org`, `http://www.nuget.org/api/v3`, and `http://www.nuget.org/api/v2/package`.</span></span> <span data-ttu-id="0eb4f-125">Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-125">For private feeds, replace the host name (for example, `%hostname%/api/v3`).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="0eb4f-126">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="0eb4f-126">.NET Core 2.0</span></span>](#tab/netcore20)

`--force-english-output`

 <span data-ttu-id="0eb4f-127">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-127">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="0eb4f-128">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-128">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="0eb4f-129">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-129">The API key for the server.</span></span>

`--non-interactive`

<span data-ttu-id="0eb4f-130">Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-130">Doesn't prompt for user input or confirmations.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="0eb4f-131">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-131">Specifies the server URL.</span></span> <span data-ttu-id="0eb4f-132">Les URL prises en charge pour nuget.org incluent `http://www.nuget.org`, `http://www.nuget.org/api/v3` et `http://www.nuget.org/api/v2/package`.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-132">Supported URLs for nuget.org include `http://www.nuget.org`, `http://www.nuget.org/api/v3`, and `http://www.nuget.org/api/v2/package`.</span></span> <span data-ttu-id="0eb4f-133">Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-133">For private feeds, replace the host name (for example, `%hostname%/api/v3`).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="0eb4f-134">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="0eb4f-134">.NET Core 1.x</span></span>](#tab/netcore1x)

`--force-english-output`

 <span data-ttu-id="0eb4f-135">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-135">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="0eb4f-136">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-136">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="0eb4f-137">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-137">The API key for the server.</span></span>

`--non-interactive`

<span data-ttu-id="0eb4f-138">Ne demande pas de saisie ou de confirmation de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-138">Doesn't prompt for user input or confirmations.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="0eb4f-139">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-139">Specifies the server URL.</span></span> <span data-ttu-id="0eb4f-140">Les URL prises en charge pour nuget.org incluent `http://www.nuget.org`, `http://www.nuget.org/api/v3` et `http://www.nuget.org/api/v2/package`.</span><span class="sxs-lookup"><span data-stu-id="0eb4f-140">Supported URLs for nuget.org include `http://www.nuget.org`, `http://www.nuget.org/api/v3`, and `http://www.nuget.org/api/v2/package`.</span></span> <span data-ttu-id="0eb4f-141">Pour les flux privés, remplacez le nom d’hôte (par exemple, `%hostname%/api/v3`).</span><span class="sxs-lookup"><span data-stu-id="0eb4f-141">For private feeds, replace the host name (for example, `%hostname%/api/v3`).</span></span>

---

## <a name="examples"></a><span data-ttu-id="0eb4f-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="0eb4f-142">Examples</span></span>

<span data-ttu-id="0eb4f-143">Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` :</span><span class="sxs-lookup"><span data-stu-id="0eb4f-143">Deletes version 1.0 of package `Microsoft.AspNetCore.Mvc`:</span></span>

`dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0`

<span data-ttu-id="0eb4f-144">Supprime la version 1.0 du package `Microsoft.AspNetCore.Mvc` sans inviter l’utilisateur à fournir ses informations d’identification ou d’autres données :</span><span class="sxs-lookup"><span data-stu-id="0eb4f-144">Deletes version 1.0 of package `Microsoft.AspNetCore.Mvc`, not prompting user for credentials or other input:</span></span>

`dotnet nuget delete Microsoft.AspNetCore.Mvc 1.0 --non-interactive`
