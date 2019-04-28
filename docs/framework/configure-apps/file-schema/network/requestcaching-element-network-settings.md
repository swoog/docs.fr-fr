---
title: <requestCaching>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#requestCaching
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/requestCaching
helpviewer_keywords:
- requestCaching element
- <requestCaching> element
ms.assetid: 9962a2fe-cbda-41a6-9377-571811eaea84
ms.openlocfilehash: af290e4b9258a08425a15e297ff538502edea916
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61674426"
---
# <a name="requestcaching-element-network-settings"></a><span data-ttu-id="b445a-102">\<requestCaching>, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="b445a-102">\<requestCaching> Element (Network Settings)</span></span>
<span data-ttu-id="b445a-103">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="b445a-103">Controls the caching mechanism for network requests.</span></span>  
  
 <span data-ttu-id="b445a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b445a-104">\<configuration></span></span>  
<span data-ttu-id="b445a-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="b445a-105">\<system.net></span></span>  
<span data-ttu-id="b445a-106">\<requestCaching></span><span class="sxs-lookup"><span data-stu-id="b445a-106">\<requestCaching></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b445a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b445a-107">Syntax</span></span>  
  
```xml  
<requestCaching  
  isPrivateCache ="true|false"  
  disableAllCaching="true|false"  
  defaultPolicyLevel="BypassCache|Default|CacheOnly|CacheIfAvailable|Revalidate|Reload|NoCacheNoStore|Revalidate"  
  unspecifiedMaximumAge= "d.hh.mm.ss">  
    <defaultHttpCachePolicy>...</defaultHttpCachePolicy>  
    <defaultFtpCachePolicy>...</defaultFtpCachePolicy>  
</requestCaching>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b445a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b445a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b445a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b445a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b445a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b445a-110">Attributes</span></span>  
  
|<span data-ttu-id="b445a-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="b445a-111">Attribute</span></span>|<span data-ttu-id="b445a-112">Description</span><span class="sxs-lookup"><span data-stu-id="b445a-112">Description</span></span>|  
|---------------|-----------------|  
|`isPrivateCache`|<span data-ttu-id="b445a-113">Spécifie si le cache fournit une isolation entre les informations d’utilisateurs différents.</span><span class="sxs-lookup"><span data-stu-id="b445a-113">Specifies whether the cache provides isolation between the information of different users.</span></span> <span data-ttu-id="b445a-114">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="b445a-114">The default value is `true`.</span></span> <span data-ttu-id="b445a-115">Cette valeur doit être `false` pour les applications de couche intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="b445a-115">This value should be `false` for middle tier applications.</span></span>|  
|`disableAllCaching`|<span data-ttu-id="b445a-116">Spécifie que la mise en cache est désactivée pour toutes les réponses Web et ne peut pas être substituée par programmation.</span><span class="sxs-lookup"><span data-stu-id="b445a-116">Specifies that caching is disabled for all Web responses, and cannot be overridden programmatically.</span></span>|  
|`defaultPolicyLevel`|<span data-ttu-id="b445a-117">Une des valeurs dans l’énumération <xref:System.Net.Cache.RequestCacheLevel>.</span><span class="sxs-lookup"><span data-stu-id="b445a-117">One of the values in the <xref:System.Net.Cache.RequestCacheLevel> enumeration.</span></span> <span data-ttu-id="b445a-118">La valeur par défaut est `BypassCache`.</span><span class="sxs-lookup"><span data-stu-id="b445a-118">The default value is `BypassCache`.</span></span>|  
|`unspecifiedMaximumAge`|<span data-ttu-id="b445a-119">Spécifie la durée par défaut après lequel le contenu est marqué comme ayant expiré.</span><span class="sxs-lookup"><span data-stu-id="b445a-119">Specifies the default time after which content is marked as expired.</span></span>|  
  
## <a name="policylevel-attribute"></a><span data-ttu-id="b445a-120">policyLevel attribut</span><span class="sxs-lookup"><span data-stu-id="b445a-120">policyLevel Attribute</span></span>  
  
|<span data-ttu-id="b445a-121">Value</span><span class="sxs-lookup"><span data-stu-id="b445a-121">Value</span></span>|<span data-ttu-id="b445a-122">Description</span><span class="sxs-lookup"><span data-stu-id="b445a-122">Description</span></span>|  
|-----------|-----------------|  
|`Default`|<span data-ttu-id="b445a-123">Retourne la ressource mise en cache si la ressource est actualisée, la longueur du contenu est précise, et l’expiration, la modification et attributs de la longueur du contenu sont présents.</span><span class="sxs-lookup"><span data-stu-id="b445a-123">Returns the cached resource if the resource is fresh, the content length is accurate, and the expiration, modification, and content length attributes are present.</span></span>|  
|`BypassCache`|<span data-ttu-id="b445a-124">Retourne la ressource à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="b445a-124">Returns the resource from the server.</span></span>|  
|`CacheOnly`|<span data-ttu-id="b445a-125">Retourne la ressource mise en cache si la longueur du contenu est présente et qu’il correspond à la taille d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b445a-125">Returns the cached resource if the content length is present and matches the entry size.</span></span>|  
|`CacheIfAvailable`|<span data-ttu-id="b445a-126">Retourne la ressource mise en cache si la longueur du contenu est fournie et correspond à la taille d’entrée ; Sinon, la ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b445a-126">Returns the cached resource if the content length is provided and matches the entry size; otherwise, the resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="b445a-127">Retourne la ressource mise en cache si l’horodatage de la ressource mise en cache est identique à l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, stocké dans le cache et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b445a-127">Returns the cached resource if the timestamp of the cached resource is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, stored in the cache, and is returned to the caller.</span></span>|  
|`Reload`|<span data-ttu-id="b445a-128">Télécharge la ressource à partir du serveur, il stocke dans le cache et retourne la ressource à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b445a-128">Downloads the resource from the server, stores it in the cache, and returns the resource to the caller.</span></span>|  
|`NoCacheNoStore`|<span data-ttu-id="b445a-129">Si une ressource mise en cache existe, elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="b445a-129">If a cached resource exists, it is deleted.</span></span> <span data-ttu-id="b445a-130">La ressource est téléchargée à partir du serveur et est retournée à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b445a-130">The resource is downloaded from the server and is returned to the caller.</span></span>|  
|`Revalidate`|<span data-ttu-id="b445a-131">Satisfait une demande à l’aide de la copie mise en cache de la ressource si l’horodatage est le même que l’horodatage de la ressource sur le serveur ; Sinon, la ressource est téléchargée à partir du serveur, présenté à l’appelant et est stockée dans le cache,</span><span class="sxs-lookup"><span data-stu-id="b445a-131">Satisfies a request by using the cached copy of the resource if the timestamp is the same as the timestamp of the resource on the server; otherwise, the resource is downloaded from the server, presented to the caller, and is stored in the cache,</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b445a-132">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b445a-132">Child Elements</span></span>  
  
|<span data-ttu-id="b445a-133">Élément</span><span class="sxs-lookup"><span data-stu-id="b445a-133">Element</span></span>|<span data-ttu-id="b445a-134">Description</span><span class="sxs-lookup"><span data-stu-id="b445a-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b445a-135">defaultHttpCachePolicy</span><span class="sxs-lookup"><span data-stu-id="b445a-135">defaultHttpCachePolicy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaulthttpcachepolicy-element-network-settings.md)|<span data-ttu-id="b445a-136">Élément facultatif.</span><span class="sxs-lookup"><span data-stu-id="b445a-136">Optional element.</span></span><br /><br /> <span data-ttu-id="b445a-137">Décrit si la mise en cache HTTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="b445a-137">Describes whether HTTP caching is active and describes the default caching policy.</span></span>|  
|[<span data-ttu-id="b445a-138">\<defaultFtpCachePolicy >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="b445a-138">\<defaultFtpCachePolicy> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultftpcachepolicy-element-network-settings.md)|<span data-ttu-id="b445a-139">Élément facultatif.</span><span class="sxs-lookup"><span data-stu-id="b445a-139">Optional element.</span></span><br /><br /> <span data-ttu-id="b445a-140">Décrit si la mise en cache FTP est active et décrit la valeur par défaut, la mise en cache de stratégie.</span><span class="sxs-lookup"><span data-stu-id="b445a-140">Describes whether FTP caching is active and describes the default caching policy.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b445a-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b445a-141">Parent Elements</span></span>  
  
|<span data-ttu-id="b445a-142">Élément</span><span class="sxs-lookup"><span data-stu-id="b445a-142">Element</span></span>|<span data-ttu-id="b445a-143">Description</span><span class="sxs-lookup"><span data-stu-id="b445a-143">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b445a-144">system.net</span><span class="sxs-lookup"><span data-stu-id="b445a-144">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="b445a-145">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="b445a-145">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b445a-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="b445a-146">Example</span></span>  
 <span data-ttu-id="b445a-147">L’exemple suivant montre comment désactiver toute mise en cache.</span><span class="sxs-lookup"><span data-stu-id="b445a-147">The following example shows how to disable all caching.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <requestCaching  
      disableAllCaching="true"  
    />  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b445a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b445a-148">See also</span></span>

- <xref:System.Net.Cache?displayProperty=nameWithType>
- [<span data-ttu-id="b445a-149">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="b445a-149">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
