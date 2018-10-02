---
title: '&lt;paramètres&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 9d6189c736e1f2843a986c3a96f8547e9a231db0
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47862683"
---
# <a name="ltsettingsgt-element-network-settings"></a><span data-ttu-id="5d23a-102">&lt;paramètres&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="5d23a-102">&lt;settings&gt; Element (Network Settings)</span></span>
<span data-ttu-id="5d23a-103">Configure les options réseau de base pour l’espace de noms <xref:System.Net?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5d23a-103">Configures basic network options for the <xref:System.Net?displayProperty=nameWithType> namespace.</span></span>  
  
 <span data-ttu-id="5d23a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="5d23a-104">\<configuration></span></span>  
<span data-ttu-id="5d23a-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="5d23a-105">\<system.net></span></span>  
<span data-ttu-id="5d23a-106">\<Paramètres ></span><span class="sxs-lookup"><span data-stu-id="5d23a-106">\<settings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5d23a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d23a-107">Syntax</span></span>  
  
```xml  
<settings>  
  <httpListener> … </httpListener>  
  <httpWebRequest> … </httpWebRequest>  
  <ipv6> … </ipv6>  
  <performanceCounters> … </performanceCounters>  
  <servicePointManager> … </servicePointManager>  
  <socket> … </socket>  
  <webProxyScript> … </webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5d23a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5d23a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="5d23a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5d23a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5d23a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="5d23a-110">Attributes</span></span>  
 <span data-ttu-id="5d23a-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5d23a-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="5d23a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5d23a-112">Child Elements</span></span>  
  
|<span data-ttu-id="5d23a-113">Élément</span><span class="sxs-lookup"><span data-stu-id="5d23a-113">Element</span></span>|<span data-ttu-id="5d23a-114">Description</span><span class="sxs-lookup"><span data-stu-id="5d23a-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5d23a-115">httpListener</span><span class="sxs-lookup"><span data-stu-id="5d23a-115">httpListener</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httplistener-element-network-settings.md)|<span data-ttu-id="5d23a-116">Personnalise les paramètres utilisés par la <xref:System.Net.HttpListener> classe.</span><span class="sxs-lookup"><span data-stu-id="5d23a-116">Customizes parameters used by the <xref:System.Net.HttpListener> class.</span></span>|  
|[<span data-ttu-id="5d23a-117">httpWebRequest</span><span class="sxs-lookup"><span data-stu-id="5d23a-117">httpWebRequest</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httpwebrequest-element-network-settings.md)|<span data-ttu-id="5d23a-118">Personnalise les paramètres de la demande Web.</span><span class="sxs-lookup"><span data-stu-id="5d23a-118">Customizes Web request parameters.</span></span>|  
|[<span data-ttu-id="5d23a-119">IPv6</span><span class="sxs-lookup"><span data-stu-id="5d23a-119">ipv6</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/ipv6-element-network-settings.md)|<span data-ttu-id="5d23a-120">Permet d’Internet Protocol version 6 (IPv6) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="5d23a-120">Enables Internet Protocol version 6 (IPv6) support.</span></span>|  
|[<span data-ttu-id="5d23a-121">\<performanceCounter >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="5d23a-121">\<performanceCounter> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/performancecounter-element-network-settings.md)|<span data-ttu-id="5d23a-122">Active les compteurs de performances réseau.</span><span class="sxs-lookup"><span data-stu-id="5d23a-122">Enables network performance counters.</span></span>|  
|[<span data-ttu-id="5d23a-123">servicePointManager</span><span class="sxs-lookup"><span data-stu-id="5d23a-123">servicePointManager</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/servicepointmanager-element-network-settings.md)|<span data-ttu-id="5d23a-124">Configure les connexions aux ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="5d23a-124">Configures connections to network resources.</span></span>|  
|[<span data-ttu-id="5d23a-125">Socket</span><span class="sxs-lookup"><span data-stu-id="5d23a-125">socket</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/socket-element-network-settings.md)|<span data-ttu-id="5d23a-126">Spécifie si les opérations de socket utilisent des ports de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5d23a-126">Specifies whether socket operations use completion ports.</span></span>|  
|[<span data-ttu-id="5d23a-127">\<webProxyScript >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="5d23a-127">\<webProxyScript> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webproxyscript-element-network-settings.md)|<span data-ttu-id="5d23a-128">Configure les caractéristiques du script utilisé pour découvrir les proxys Web.</span><span class="sxs-lookup"><span data-stu-id="5d23a-128">Configures the characteristics of the script used to discover Web proxies.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="5d23a-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5d23a-129">Parent Elements</span></span>  
  
|<span data-ttu-id="5d23a-130">Élément</span><span class="sxs-lookup"><span data-stu-id="5d23a-130">Element</span></span>|<span data-ttu-id="5d23a-131">Description</span><span class="sxs-lookup"><span data-stu-id="5d23a-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5d23a-132">System.NET</span><span class="sxs-lookup"><span data-stu-id="5d23a-132">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="5d23a-133">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="5d23a-133">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5d23a-134">Notes</span><span class="sxs-lookup"><span data-stu-id="5d23a-134">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="5d23a-135">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="5d23a-135">Configuration Files</span></span>  
 <span data-ttu-id="5d23a-136">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="5d23a-136">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d23a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d23a-137">See Also</span></span>  
 <xref:System.Net?displayProperty=nameWithType>  
 [<span data-ttu-id="5d23a-138">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="5d23a-138">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
