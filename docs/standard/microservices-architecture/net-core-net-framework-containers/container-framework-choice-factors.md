---
title: 'Table de décision : versions de .NET Framework à utiliser pour Docker'
description: Architecture de microservices .NET pour les applications .NET en conteneur | Table de décision, versions de .NET Framework à utiliser pour Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: 8044e3064ac372750c174d8b47c3f7a63d6bbd0b
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149053"
---
# <a name="decision-table-net-frameworks-to-use-for-docker"></a><span data-ttu-id="9133d-104">Table de décision : versions de .NET Framework à utiliser pour Docker</span><span class="sxs-lookup"><span data-stu-id="9133d-104">Decision table: .NET frameworks to use for Docker</span></span>

<span data-ttu-id="9133d-105">La table de décision ci-dessous vous indique s’il convient d’utiliser .NET Framework ou .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9133d-105">The following decision table summarizes whether to use .NET Framework or .NET Core.</span></span> <span data-ttu-id="9133d-106">N’oubliez pas que pour les conteneurs Linux, vous avez besoin d’hôtes Docker basés sur Linux (machines virtuelles ou serveurs) et que pour les conteneurs Windows, vous avez besoin d’hôtes Docker basés sur Windows Server (machines virtuelles ou serveurs).</span><span class="sxs-lookup"><span data-stu-id="9133d-106">Remember that for Linux containers, you need Linux-based Docker hosts (VMs or servers) and that for Windows Containers you need Windows Server based Docker hosts (VMs or servers).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9133d-107">Vos machines de développement exécuteront un hôte Docker, Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="9133d-107">Your development machines will run one Docker host, either Linux or Windows.</span></span> <span data-ttu-id="9133d-108">Les microservices connexes que vous souhaitez exécuter et tester ensemble dans une solution devront tous s’exécuter sur la même plateforme de conteneur.</span><span class="sxs-lookup"><span data-stu-id="9133d-108">Related microservices that you want to run and test together in one solution will all need to run on the same container platform.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9133d-109"><strong>Architecture / Type d’application</strong></span><span class="sxs-lookup"><span data-stu-id="9133d-109"><strong>Architecture / App Type</strong></span></span></th>
<th><span data-ttu-id="9133d-110"><strong>Conteneurs Linux</strong></span><span class="sxs-lookup"><span data-stu-id="9133d-110"><strong>Linux containers</strong></span></span></th>
<th><span data-ttu-id="9133d-111"><strong>Conteneurs Windows</strong></span><span class="sxs-lookup"><span data-stu-id="9133d-111"><strong>Windows Containers</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9133d-112">Microservices sur des conteneurs</span><span class="sxs-lookup"><span data-stu-id="9133d-112">Microservices on containers</span></span></td>
<td><span data-ttu-id="9133d-113">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-113">.NET Core</span></span></td>
<td><span data-ttu-id="9133d-114">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-114">.NET Core</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9133d-115">Application monolithique</span><span class="sxs-lookup"><span data-stu-id="9133d-115">Monolithic app</span></span></td>
<td><span data-ttu-id="9133d-116">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-116">.NET Core</span></span></td>
<td><p><span data-ttu-id="9133d-117">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-117">.NET Framework</span></span></p>
<p><span data-ttu-id="9133d-118">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-118">.NET Core</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9133d-119">Performances et scalabilité de pointe</span><span class="sxs-lookup"><span data-stu-id="9133d-119">Best-in-class performance and scalability</span></span></td>
<td><span data-ttu-id="9133d-120">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-120">.NET Core</span></span></td>
<td><span data-ttu-id="9133d-121">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-121">.NET Core</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9133d-122">Migration d’application existante Windows Server (« brown-field ») vers des conteneurs</span><span class="sxs-lookup"><span data-stu-id="9133d-122">Windows Server legacy app ("brown-field") migration to containers</span></span></td>
<td>--</td>
<td><span data-ttu-id="9133d-123">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-123">.NET Framework</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9133d-124">Développement basé sur un nouveau conteneur (« green-field »)</span><span class="sxs-lookup"><span data-stu-id="9133d-124">New container-based development ("green-field")</span></span></td>
<td><span data-ttu-id="9133d-125">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-125">.NET Core</span></span></td>
<td><span data-ttu-id="9133d-126">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-126">.NET Core</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9133d-127">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-127">ASP.NET Core</span></span></td>
<td><span data-ttu-id="9133d-128">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-128">.NET Core</span></span></td>
<td><p><span data-ttu-id="9133d-129">.NET Core (recommandé)</span><span class="sxs-lookup"><span data-stu-id="9133d-129">.NET Core (recommended)</span></span></p>
<p><span data-ttu-id="9133d-130">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-130">.NET Framework</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9133d-131">ASP.NET 4 (MVC 5, API web 2 et Web Forms)</span><span class="sxs-lookup"><span data-stu-id="9133d-131">ASP.NET 4 (MVC 5, Web API 2, and Web Forms)</span></span></td>
<td>--</td>
<td><span data-ttu-id="9133d-132">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-132">.NET Framework</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9133d-133">Services SignalR</span><span class="sxs-lookup"><span data-stu-id="9133d-133">SignalR services</span></span></td>
<td><span data-ttu-id="9133d-134">.NET Core 2.1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9133d-134">.NET Core 2.1 or higher version</span></span></td>
<td><p><span data-ttu-id="9133d-135">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-135">.NET Framework</span></span></p>
<p><span data-ttu-id="9133d-136">.NET Core 2.1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9133d-136">.NET Core 2.1 or higher version</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9133d-137">WCF, WF et autres frameworks existants</span><span class="sxs-lookup"><span data-stu-id="9133d-137">WCF, WF, and other legacy frameworks</span></span></td>
<td><span data-ttu-id="9133d-138">WCF dans .NET Core (uniquement la bibliothèque cliente WCF)</span><span class="sxs-lookup"><span data-stu-id="9133d-138">WCF in .NET Core (only the WCF client library)</span></span></td>
<td><p><span data-ttu-id="9133d-139">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-139">.NET Framework</span></span></p>
<p><span data-ttu-id="9133d-140">WCF dans .NET Core (uniquement la bibliothèque cliente WCF)</span><span class="sxs-lookup"><span data-stu-id="9133d-140">WCF in .NET Core (only the WCF client library)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9133d-141">Consommation des services Azure</span><span class="sxs-lookup"><span data-stu-id="9133d-141">Consumption of Azure services</span></span></td>
<td><p><span data-ttu-id="9133d-142">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-142">.NET Core</span></span></p>
<p><span data-ttu-id="9133d-143">(tous les services Azure fourniront les SDK clients pour .NET Core)</span><span class="sxs-lookup"><span data-stu-id="9133d-143">(eventually all Azure services will provide client SDKs for .NET Core)</span></span></p></td>
<td><p><span data-ttu-id="9133d-144">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="9133d-144">.NET Framework</span></span></p>
<p><span data-ttu-id="9133d-145">.NET Core</span><span class="sxs-lookup"><span data-stu-id="9133d-145">.NET Core</span></span></p>
<p><span data-ttu-id="9133d-146">(tous les services Azure fourniront les SDK clients pour .NET Core)</span><span class="sxs-lookup"><span data-stu-id="9133d-146">(eventually all Azure services will provide client SDKs for .NET Core)</span></span></p></td>
</tr>
</tbody>
</table>

>[!div class="step-by-step"]
><span data-ttu-id="9133d-147">[Précédent](net-framework-container-scenarios.md)
>[Suivant](net-container-os-targets.md)</span><span class="sxs-lookup"><span data-stu-id="9133d-147">[Previous](net-framework-container-scenarios.md)
[Next](net-container-os-targets.md)</span></span>