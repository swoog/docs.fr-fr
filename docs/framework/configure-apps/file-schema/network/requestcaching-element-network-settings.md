---
title: '&lt;requestCaching&gt; élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requestCaching
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching
helpviewer_keywords:
- requestCaching element
- <requestCaching> element
ms.assetid: 9962a2fe-cbda-41a6-9377-571811eaea84
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 9c0c8d80182931f9ac14e687a337b7be55a5a9a5
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltrequestcachinggt-element-network-settings"></a><span data-ttu-id="1b0f7-102">&lt;requestCaching&gt; élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="1b0f7-102">&lt;requestCaching&gt; Element (Network Settings)</span></span>
<span data-ttu-id="1b0f7-103">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-103">Controls the caching mechanism for network requests.</span></span>  
  
 <span data-ttu-id="1b0f7-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="1b0f7-104">\<configuration></span></span>  
<span data-ttu-id="1b0f7-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="1b0f7-105">\<system.net></span></span>  
<span data-ttu-id="1b0f7-106">\<requestCaching ></span><span class="sxs-lookup"><span data-stu-id="1b0f7-106">\<requestCaching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b0f7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b0f7-107">Syntax</span></span>  
  
```xml  
      <requestCaching>  
        isPrivateCache ="true|false"  
        disableAllCaching="true|false"  
        defaultPolicyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
        unspecifiedMaximumAge= "d.hh.mm.ss">  
          <defaultHttpCachePolicy> … </defaultHttpCachePolicy>  
          <defaultFtpCachePolicy> … </defaultFtpCachePolicy>  
      </requestCaching>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1b0f7-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1b0f7-108">Attributes and Elements</span></span>  
 <span data-ttu-id="1b0f7-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1b0f7-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="1b0f7-110">Attributes</span></span>  
  
|<span data-ttu-id="1b0f7-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="1b0f7-111">Attribute</span></span>|<span data-ttu-id="1b0f7-112">Description</span><span class="sxs-lookup"><span data-stu-id="1b0f7-112">Description</span></span>|  
|---------------|-----------------|  
|`isPrivateCache`|<span data-ttu-id="1b0f7-113">Spécifie si le cache fournit une isolation entre les informations des différents utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-113">Specifies whether the cache provides isolation between the information of different users.</span></span> <span data-ttu-id="1b0f7-114">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-114">The default value is `true`.</span></span> <span data-ttu-id="1b0f7-115">Cette valeur doit être `false` pour les applications de couche intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-115">This value should be `false` for middle tier applications.</span></span>|  
|`disableAllCaching`|<span data-ttu-id="1b0f7-116">Spécifie que la mise en cache est désactivée pour toutes les réponses Web et ne peut pas être modifié par programmation.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-116">Specifies that caching is disabled for all Web responses, and cannot be overridden programmatically.</span></span>|  
|`defaultPolicyLevel`|<span data-ttu-id="1b0f7-117">Une des valeurs dans l’énumération <xref:System.Net.Cache.RequestCacheLevel>.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-117">One of the values in the <xref:System.Net.Cache.RequestCacheLevel> enumeration.</span></span> <span data-ttu-id="1b0f7-118">La valeur par défaut est `BypassCache`.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-118">The default value is `BypassCache`.</span></span>|  
|`unspecifiedMaximumAge`|<span data-ttu-id="1b0f7-119">Spécifie la durée par défaut après lequel le contenu est marqué comme ayant expiré.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-119">Specifies the default time after which content is marked as expired.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="1b0f7-120">PolicyLevel qui n’est attribut</span><span class="sxs-lookup"><span data-stu-id="1b0f7-120">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="1b0f7-121">Value</span><span class="sxs-lookup"><span data-stu-id="1b0f7-121">Value</span></span>|<span data-ttu-id="1b0f7-122">Description</span><span class="sxs-lookup"><span data-stu-id="1b0f7-122">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="1b0f7-123">Retourne la ressource mise en cache si la ressource est actualisée, la longueur du contenu est précise et d’expiration, modification et les attributs de la longueur de contenu sont présents.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-123">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="1b0f7-124">Retourne la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-124">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="1b0f7-125">Retourne la ressource mise en cache si la longueur du contenu est présente et qu’il correspond à la taille de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-125">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="1b0f7-126">Retourne la ressource mise en cache si la longueur du contenu est fournie et correspond à la taille de l’entrée ; Sinon, la ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-126">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="1b0f7-127">Retourne la ressource mise en cache si l’horodatage de la ressource mise en cache est identique à celui de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, stocké dans le cache et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-127">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and is returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="1b0f7-128">Télécharge la ressource à partir du serveur, il stocke dans le cache et retourne la ressource à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-128">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="1b0f7-129">Si une ressource mise en cache existe, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-129">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="1b0f7-130">La ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-130">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="1b0f7-131">Satisfait une demande à l’aide de la copie mise en cache de la ressource si l’horodatage est le même que l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, présenté à l’appelant et est stockée dans le cache,</span><span class="sxs-lookup"><span data-stu-id="1b0f7-131">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and is stored in the cache,</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1b0f7-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1b0f7-132">Child Elements</span></span>  
  
|<span data-ttu-id="1b0f7-133">Élément</span><span class="sxs-lookup"><span data-stu-id="1b0f7-133">Element</span></span>|<span data-ttu-id="1b0f7-134">Description</span><span class="sxs-lookup"><span data-stu-id="1b0f7-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1b0f7-135">defaultHttpCachePolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f7-135">defaultHttpCachePolicy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaulthttpcachepolicy-element-network-settings.md)|<span data-ttu-id="1b0f7-136">Élément facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-136">Optional element.</span></span><br /><br /> <span data-ttu-id="1b0f7-137">Décrit si la mise en cache HTTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-137">Describes whether HTTP caching is active and describes the default caching policy.</span></span>|  
|[<span data-ttu-id="1b0f7-138">\<defaultFtpCachePolicy >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="1b0f7-138">\<defaultFtpCachePolicy> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultftpcachepolicy-element-network-settings.md)|<span data-ttu-id="1b0f7-139">Élément facultatif.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-139">Optional element.</span></span><br /><br /> <span data-ttu-id="1b0f7-140">Décrit si la mise en cache FTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-140">Describes whether FTP caching is active and describes the default caching policy.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="1b0f7-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1b0f7-141">Parent Elements</span></span>  
  
|<span data-ttu-id="1b0f7-142">Élément</span><span class="sxs-lookup"><span data-stu-id="1b0f7-142">Element</span></span>|<span data-ttu-id="1b0f7-143">Description</span><span class="sxs-lookup"><span data-stu-id="1b0f7-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1b0f7-144">System.NET</span><span class="sxs-lookup"><span data-stu-id="1b0f7-144">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="1b0f7-145">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-145">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="1b0f7-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="1b0f7-146">Example</span></span>  
 <span data-ttu-id="1b0f7-147">L’exemple suivant montre comment désactiver toute mise en cache.</span><span class="sxs-lookup"><span data-stu-id="1b0f7-147">The following example shows how to disable all caching.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching  
      disableAllCaching="true"  
    />  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1b0f7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b0f7-148">See Also</span></span>  
 <xref:System.Net.Cache?displayProperty=nameWithType>  
 [<span data-ttu-id="1b0f7-149">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="1b0f7-149">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
