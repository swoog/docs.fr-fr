---
title: '&lt;defaultFtpCachePolicy&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultFtpCachePolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching/defaultFtpCachePolicy
helpviewer_keywords:
- <defaultFtpCachePolicy> element
- defaultFtpCachePolicy element
ms.assetid: 0eb0c5cb-dd97-484d-8614-785e88877abb
author: mcleblanc
ms.author: markl
ms.openlocfilehash: e03fb02bd351058c1fcdedb8367d03318418a12c
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49316439"
---
# <a name="ltdefaultftpcachepolicygt-element-network-settings"></a><span data-ttu-id="e27e0-102">&lt;defaultFtpCachePolicy&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="e27e0-102">&lt;defaultFtpCachePolicy&gt; Element (Network Settings)</span></span>
<span data-ttu-id="e27e0-103">Décrit si la mise en cache FTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="e27e0-103">Describes whether FTP caching is active and describes the default caching policy.</span></span>  
  
 <span data-ttu-id="e27e0-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="e27e0-104">\<configuration></span></span>  
<span data-ttu-id="e27e0-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="e27e0-105">\<system.net></span></span>  
<span data-ttu-id="e27e0-106">\<requestCaching ></span><span class="sxs-lookup"><span data-stu-id="e27e0-106">\<requestCaching></span></span>  
<span data-ttu-id="e27e0-107">\<defaultFtpCachePolicy ></span><span class="sxs-lookup"><span data-stu-id="e27e0-107">\<defaultFtpCachePolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e27e0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e27e0-108">Syntax</span></span>  
  
```xml  
<defaultFtpCachePolicy  
  policyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e27e0-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e27e0-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e27e0-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e27e0-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e27e0-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="e27e0-111">Attributes</span></span>  
  
|<span data-ttu-id="e27e0-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="e27e0-112">Attribute</span></span>|<span data-ttu-id="e27e0-113">Description</span><span class="sxs-lookup"><span data-stu-id="e27e0-113">Description</span></span>|  
|---------------|-----------------|  
|`policyLevel`|<span data-ttu-id="e27e0-114">Spécifie la mise en cache de stratégie FTP.</span><span class="sxs-lookup"><span data-stu-id="e27e0-114">Specifies the FTP caching policy.</span></span> <span data-ttu-id="e27e0-115">La valeur par défaut est `Default`.</span><span class="sxs-lookup"><span data-stu-id="e27e0-115">The default value is `Default`.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="e27e0-116">policyLevel attribut</span><span class="sxs-lookup"><span data-stu-id="e27e0-116">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="e27e0-117">Value</span><span class="sxs-lookup"><span data-stu-id="e27e0-117">Value</span></span>|<span data-ttu-id="e27e0-118">Description</span><span class="sxs-lookup"><span data-stu-id="e27e0-118">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="e27e0-119">Retourne la ressource mise en cache si la ressource est actualisée, la longueur du contenu est précise, et l’expiration, la modification et attributs de la longueur du contenu sont présents.</span><span class="sxs-lookup"><span data-stu-id="e27e0-119">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="e27e0-120">Retourne la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="e27e0-120">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="e27e0-121">Retourne la ressource mise en cache si la longueur du contenu est présente et qu’il correspond à la taille d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e27e0-121">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="e27e0-122">Retourne la ressource mise en cache si la longueur du contenu est fournie et correspond à la taille d’entrée ; Sinon, la ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e27e0-122">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="e27e0-123">Retourne la ressource mise en cache si l’horodatage de la ressource mise en cache est identique à l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, stockée dans le cache et retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e27e0-123">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="e27e0-124">Télécharge la ressource à partir du serveur, il stocke dans le cache et retourne la ressource à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e27e0-124">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="e27e0-125">Si une ressource mise en cache existe, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="e27e0-125">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="e27e0-126">La ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e27e0-126">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="e27e0-127">Satisfait une demande à l’aide de la copie mise en cache de la ressource si l’horodatage est le même que l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, présentée à l’appelant et stockée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="e27e0-127">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and stored in the cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e27e0-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e27e0-128">Child Elements</span></span>  
 <span data-ttu-id="e27e0-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e27e0-129">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e27e0-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e27e0-130">Parent Elements</span></span>  
  
|<span data-ttu-id="e27e0-131">Élément</span><span class="sxs-lookup"><span data-stu-id="e27e0-131">Element</span></span>|<span data-ttu-id="e27e0-132">Description</span><span class="sxs-lookup"><span data-stu-id="e27e0-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e27e0-133">requestCaching</span><span class="sxs-lookup"><span data-stu-id="e27e0-133">requestCaching</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)|<span data-ttu-id="e27e0-134">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="e27e0-134">Controls the caching mechanism for network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e27e0-135">Notes</span><span class="sxs-lookup"><span data-stu-id="e27e0-135">Remarks</span></span>  
  
## <a name="example"></a><span data-ttu-id="e27e0-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="e27e0-136">Example</span></span>  
 <span data-ttu-id="e27e0-137">L’exemple suivant montre comment spécifier une FTP mise en cache de la stratégie de `NoCacheNoStore`.</span><span class="sxs-lookup"><span data-stu-id="e27e0-137">The following example shows how to specify an FTP caching policy of `NoCacheNoStore`.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching>  
      <defaultFtpCachePolicy  
        policyLevel="NoCacheNoStore">  
      </defaultFtpCachePolicy>  
    </requestCaching>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="e27e0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e27e0-138">See Also</span></span>  
 <xref:System.Net.Cache>  
 <xref:System.Net.WebRequest>  
 <xref:System.Net.Cache.RequestCacheLevel>  
 [<span data-ttu-id="e27e0-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="e27e0-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
