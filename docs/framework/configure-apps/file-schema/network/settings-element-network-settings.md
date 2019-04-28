---
title: <settings>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#settings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings
helpviewer_keywords:
- settings element
- <settings> element
ms.assetid: 189ce989-c39b-427d-b004-6b82a668b931
ms.openlocfilehash: a1733803d1f5a5bf64aeb69d0360cef3de3b3a69
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674413"
---
# <a name="settings-element-network-settings"></a><span data-ttu-id="95298-102">\<Paramètres >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="95298-102">\<settings> Element (Network Settings)</span></span>
<span data-ttu-id="95298-103">Configure les options réseau de base pour l’espace de noms <xref:System.Net?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="95298-103">Configures basic network options for the <xref:System.Net?displayProperty=nameWithType> namespace.</span></span>  
  
 <span data-ttu-id="95298-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="95298-104">\<configuration></span></span>  
<span data-ttu-id="95298-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="95298-105">\<system.net></span></span>  
<span data-ttu-id="95298-106">\<settings></span><span class="sxs-lookup"><span data-stu-id="95298-106">\<settings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95298-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95298-107">Syntax</span></span>  
  
```xml  
<settings>  
  <httpListener>...</httpListener>  
  <httpWebRequest>...</httpWebRequest>  
  <ipv6>...</ipv6>  
  <performanceCounters>...</performanceCounters>  
  <servicePointManager>...</servicePointManager>  
  <socket>...</socket>  
  <webProxyScript>...</webProxyScript>  
</settings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="95298-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="95298-108">Attributes and Elements</span></span>  
 <span data-ttu-id="95298-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="95298-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="95298-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="95298-110">Attributes</span></span>  
 <span data-ttu-id="95298-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="95298-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="95298-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="95298-112">Child Elements</span></span>  
  
|<span data-ttu-id="95298-113">Élément</span><span class="sxs-lookup"><span data-stu-id="95298-113">Element</span></span>|<span data-ttu-id="95298-114">Description</span><span class="sxs-lookup"><span data-stu-id="95298-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95298-115">httpListener</span><span class="sxs-lookup"><span data-stu-id="95298-115">httpListener</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httplistener-element-network-settings.md)|<span data-ttu-id="95298-116">Personnalise les paramètres utilisés par la <xref:System.Net.HttpListener> classe.</span><span class="sxs-lookup"><span data-stu-id="95298-116">Customizes parameters used by the <xref:System.Net.HttpListener> class.</span></span>|  
|[<span data-ttu-id="95298-117">httpWebRequest</span><span class="sxs-lookup"><span data-stu-id="95298-117">httpWebRequest</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/httpwebrequest-element-network-settings.md)|<span data-ttu-id="95298-118">Personnalise les paramètres de la demande Web.</span><span class="sxs-lookup"><span data-stu-id="95298-118">Customizes Web request parameters.</span></span>|  
|[<span data-ttu-id="95298-119">ipv6</span><span class="sxs-lookup"><span data-stu-id="95298-119">ipv6</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/ipv6-element-network-settings.md)|<span data-ttu-id="95298-120">Permet d’Internet Protocol version 6 (IPv6) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="95298-120">Enables Internet Protocol version 6 (IPv6) support.</span></span>|  
|[<span data-ttu-id="95298-121">\<performanceCounter >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="95298-121">\<performanceCounter> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/performancecounter-element-network-settings.md)|<span data-ttu-id="95298-122">Active les compteurs de performances réseau.</span><span class="sxs-lookup"><span data-stu-id="95298-122">Enables network performance counters.</span></span>|  
|[<span data-ttu-id="95298-123">servicePointManager</span><span class="sxs-lookup"><span data-stu-id="95298-123">servicePointManager</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/servicepointmanager-element-network-settings.md)|<span data-ttu-id="95298-124">Configure les connexions aux ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="95298-124">Configures connections to network resources.</span></span>|  
|[<span data-ttu-id="95298-125">socket</span><span class="sxs-lookup"><span data-stu-id="95298-125">socket</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/socket-element-network-settings.md)|<span data-ttu-id="95298-126">Spécifie si les opérations de socket utilisent des ports de terminaison.</span><span class="sxs-lookup"><span data-stu-id="95298-126">Specifies whether socket operations use completion ports.</span></span>|  
|[<span data-ttu-id="95298-127">\<webProxyScript >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="95298-127">\<webProxyScript> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webproxyscript-element-network-settings.md)|<span data-ttu-id="95298-128">Configure les caractéristiques du script utilisé pour découvrir les proxys Web.</span><span class="sxs-lookup"><span data-stu-id="95298-128">Configures the characteristics of the script used to discover Web proxies.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="95298-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="95298-129">Parent Elements</span></span>  
  
|<span data-ttu-id="95298-130">Élément</span><span class="sxs-lookup"><span data-stu-id="95298-130">Element</span></span>|<span data-ttu-id="95298-131">Description</span><span class="sxs-lookup"><span data-stu-id="95298-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="95298-132">system.net</span><span class="sxs-lookup"><span data-stu-id="95298-132">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="95298-133">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="95298-133">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95298-134">Notes</span><span class="sxs-lookup"><span data-stu-id="95298-134">Remarks</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="95298-135">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="95298-135">Configuration Files</span></span>  
 <span data-ttu-id="95298-136">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="95298-136">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95298-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95298-137">See also</span></span>

- <xref:System.Net?displayProperty=nameWithType>
- [<span data-ttu-id="95298-138">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="95298-138">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
