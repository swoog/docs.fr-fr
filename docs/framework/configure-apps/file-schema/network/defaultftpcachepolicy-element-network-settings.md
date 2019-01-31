---
title: <defaultFtpCachePolicy>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultFtpCachePolicy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching/defaultFtpCachePolicy
helpviewer_keywords:
- <defaultFtpCachePolicy> element
- defaultFtpCachePolicy element
ms.assetid: 0eb0c5cb-dd97-484d-8614-785e88877abb
ms.openlocfilehash: eda246c93660c1a37f7db3a6a38144a44a0ae1d3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279706"
---
# <a name="defaultftpcachepolicy-element-network-settings"></a><span data-ttu-id="eb74e-102">\<defaultFtpCachePolicy >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="eb74e-102">\<defaultFtpCachePolicy> Element (Network Settings)</span></span>
<span data-ttu-id="eb74e-103">Décrit si la mise en cache FTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="eb74e-103">Describes whether FTP caching is active and describes the default caching policy.</span></span>  
  
 <span data-ttu-id="eb74e-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="eb74e-104">\<configuration></span></span>  
<span data-ttu-id="eb74e-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="eb74e-105">\<system.net></span></span>  
<span data-ttu-id="eb74e-106">\<requestCaching></span><span class="sxs-lookup"><span data-stu-id="eb74e-106">\<requestCaching></span></span>  
<span data-ttu-id="eb74e-107">\<defaultFtpCachePolicy></span><span class="sxs-lookup"><span data-stu-id="eb74e-107">\<defaultFtpCachePolicy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb74e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb74e-108">Syntax</span></span>  
  
```xml  
<defaultFtpCachePolicy  
  policyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eb74e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eb74e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="eb74e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eb74e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eb74e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb74e-111">Attributes</span></span>  
  
|<span data-ttu-id="eb74e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="eb74e-112">Attribute</span></span>|<span data-ttu-id="eb74e-113">Description</span><span class="sxs-lookup"><span data-stu-id="eb74e-113">Description</span></span>|  
|---------------|-----------------|  
|`policyLevel`|<span data-ttu-id="eb74e-114">Spécifie la mise en cache de stratégie FTP.</span><span class="sxs-lookup"><span data-stu-id="eb74e-114">Specifies the FTP caching policy.</span></span> <span data-ttu-id="eb74e-115">La valeur par défaut est `Default`.</span><span class="sxs-lookup"><span data-stu-id="eb74e-115">The default value is `Default`.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="eb74e-116">policyLevel attribut</span><span class="sxs-lookup"><span data-stu-id="eb74e-116">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="eb74e-117">Value</span><span class="sxs-lookup"><span data-stu-id="eb74e-117">Value</span></span>|<span data-ttu-id="eb74e-118">Description</span><span class="sxs-lookup"><span data-stu-id="eb74e-118">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="eb74e-119">Retourne la ressource mise en cache si la ressource est actualisée, la longueur du contenu est précise, et l’expiration, la modification et attributs de la longueur du contenu sont présents.</span><span class="sxs-lookup"><span data-stu-id="eb74e-119">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="eb74e-120">Retourne la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="eb74e-120">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="eb74e-121">Retourne la ressource mise en cache si la longueur du contenu est présente et qu’il correspond à la taille d’entrée.</span><span class="sxs-lookup"><span data-stu-id="eb74e-121">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="eb74e-122">Retourne la ressource mise en cache si la longueur du contenu est fournie et correspond à la taille d’entrée ; Sinon, la ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="eb74e-122">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="eb74e-123">Retourne la ressource mise en cache si l’horodatage de la ressource mise en cache est identique à l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, stockée dans le cache et retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="eb74e-123">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="eb74e-124">Télécharge la ressource à partir du serveur, il stocke dans le cache et retourne la ressource à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="eb74e-124">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="eb74e-125">Si une ressource mise en cache existe, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="eb74e-125">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="eb74e-126">La ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="eb74e-126">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="eb74e-127">Satisfait une demande à l’aide de la copie mise en cache de la ressource si l’horodatage est le même que l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, présentée à l’appelant et stockée dans le cache.</span><span class="sxs-lookup"><span data-stu-id="eb74e-127">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and stored in the cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eb74e-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb74e-128">Child Elements</span></span>  
 <span data-ttu-id="eb74e-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb74e-129">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eb74e-130">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eb74e-130">Parent Elements</span></span>  
  
|<span data-ttu-id="eb74e-131">Élément</span><span class="sxs-lookup"><span data-stu-id="eb74e-131">Element</span></span>|<span data-ttu-id="eb74e-132">Description</span><span class="sxs-lookup"><span data-stu-id="eb74e-132">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eb74e-133">requestCaching</span><span class="sxs-lookup"><span data-stu-id="eb74e-133">requestCaching</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)|<span data-ttu-id="eb74e-134">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="eb74e-134">Controls the caching mechanism for network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eb74e-135">Notes</span><span class="sxs-lookup"><span data-stu-id="eb74e-135">Remarks</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb74e-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb74e-136">Example</span></span>  
 <span data-ttu-id="eb74e-137">L’exemple suivant montre comment spécifier une FTP mise en cache de la stratégie de `NoCacheNoStore`.</span><span class="sxs-lookup"><span data-stu-id="eb74e-137">The following example shows how to specify an FTP caching policy of `NoCacheNoStore`.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="eb74e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb74e-138">See also</span></span>
- <xref:System.Net.Cache>
- <xref:System.Net.WebRequest>
- <xref:System.Net.Cache.RequestCacheLevel>
- [<span data-ttu-id="eb74e-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="eb74e-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
