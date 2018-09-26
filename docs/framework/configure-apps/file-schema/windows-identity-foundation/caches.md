---
title: '&lt;Caches&gt;'
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: a91a389e53354e4f5b26e1510fc2f025300d65cc
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47192678"
---
# <a name="ltcachesgt"></a><span data-ttu-id="97c5a-102">&lt;Caches&gt;</span><span class="sxs-lookup"><span data-stu-id="97c5a-102">&lt;caches&gt;</span></span>
<span data-ttu-id="97c5a-103">Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.</span><span class="sxs-lookup"><span data-stu-id="97c5a-103">Registers the caches used for session tokens and token replay detection.</span></span>  
  
 <span data-ttu-id="97c5a-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="97c5a-104">\<system.identityModel></span></span>  
<span data-ttu-id="97c5a-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="97c5a-105">\<identityConfiguration></span></span>  
<span data-ttu-id="97c5a-106">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="97c5a-106">\<caches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97c5a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97c5a-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="97c5a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="97c5a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="97c5a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="97c5a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="97c5a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="97c5a-110">Attributes</span></span>  
 <span data-ttu-id="97c5a-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="97c5a-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="97c5a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="97c5a-112">Child Elements</span></span>  
  
|<span data-ttu-id="97c5a-113">Élément</span><span class="sxs-lookup"><span data-stu-id="97c5a-113">Element</span></span>|<span data-ttu-id="97c5a-114">Description</span><span class="sxs-lookup"><span data-stu-id="97c5a-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="97c5a-115">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="97c5a-115">\<sessionSecurityTokenCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|<span data-ttu-id="97c5a-116">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="97c5a-116">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[<span data-ttu-id="97c5a-117">\<tokenReplayCache ></span><span class="sxs-lookup"><span data-stu-id="97c5a-117">\<tokenReplayCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|<span data-ttu-id="97c5a-118">Inscrit un cache de relecture de jetons avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="97c5a-118">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="97c5a-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="97c5a-119">Parent Elements</span></span>  
  
|<span data-ttu-id="97c5a-120">Élément</span><span class="sxs-lookup"><span data-stu-id="97c5a-120">Element</span></span>|<span data-ttu-id="97c5a-121">Description</span><span class="sxs-lookup"><span data-stu-id="97c5a-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="97c5a-122">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="97c5a-122">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="97c5a-123">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="97c5a-123">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="97c5a-124">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="97c5a-124">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="97c5a-125">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="97c5a-125">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="97c5a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="97c5a-126">Remarks</span></span>  
 <span data-ttu-id="97c5a-127">Un `<caches>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="97c5a-127">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="97c5a-128">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="97c5a-128">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="97c5a-129">Le `<caches>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> classe.</span><span class="sxs-lookup"><span data-stu-id="97c5a-129">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="97c5a-130">Caches configurés sont représentées par la <xref:System.IdentityModel.Configuration.IdentityModelCaches> classe.</span><span class="sxs-lookup"><span data-stu-id="97c5a-130">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="97c5a-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="97c5a-131">Example</span></span>  
 <span data-ttu-id="97c5a-132">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="97c5a-132">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="97c5a-133">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="97c5a-133">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
