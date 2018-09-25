---
title: '&lt;Caches&gt;'
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: a91a389e53354e4f5b26e1510fc2f025300d65cc
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47084239"
---
# <a name="ltcachesgt"></a><span data-ttu-id="cc193-102">&lt;Caches&gt;</span><span class="sxs-lookup"><span data-stu-id="cc193-102">&lt;caches&gt;</span></span>
<span data-ttu-id="cc193-103">Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.</span><span class="sxs-lookup"><span data-stu-id="cc193-103">Registers the caches used for session tokens and token replay detection.</span></span>  
  
 <span data-ttu-id="cc193-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="cc193-104">\<system.identityModel></span></span>  
<span data-ttu-id="cc193-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="cc193-105">\<identityConfiguration></span></span>  
<span data-ttu-id="cc193-106">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="cc193-106">\<caches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc193-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc193-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cc193-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cc193-108">Attributes and Elements</span></span>  
 <span data-ttu-id="cc193-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cc193-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cc193-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="cc193-110">Attributes</span></span>  
 <span data-ttu-id="cc193-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cc193-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="cc193-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cc193-112">Child Elements</span></span>  
  
|<span data-ttu-id="cc193-113">Élément</span><span class="sxs-lookup"><span data-stu-id="cc193-113">Element</span></span>|<span data-ttu-id="cc193-114">Description</span><span class="sxs-lookup"><span data-stu-id="cc193-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cc193-115">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="cc193-115">\<sessionSecurityTokenCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|<span data-ttu-id="cc193-116">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cc193-116">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[<span data-ttu-id="cc193-117">\<tokenReplayCache ></span><span class="sxs-lookup"><span data-stu-id="cc193-117">\<tokenReplayCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|<span data-ttu-id="cc193-118">Inscrit un cache de relecture de jetons avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cc193-118">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="cc193-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cc193-119">Parent Elements</span></span>  
  
|<span data-ttu-id="cc193-120">Élément</span><span class="sxs-lookup"><span data-stu-id="cc193-120">Element</span></span>|<span data-ttu-id="cc193-121">Description</span><span class="sxs-lookup"><span data-stu-id="cc193-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cc193-122">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="cc193-122">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="cc193-123">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="cc193-123">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="cc193-124">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="cc193-124">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="cc193-125">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="cc193-125">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc193-126">Notes</span><span class="sxs-lookup"><span data-stu-id="cc193-126">Remarks</span></span>  
 <span data-ttu-id="cc193-127">Un `<caches>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="cc193-127">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="cc193-128">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="cc193-128">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="cc193-129">Le `<caches>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> classe.</span><span class="sxs-lookup"><span data-stu-id="cc193-129">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="cc193-130">Caches configurés sont représentées par la <xref:System.IdentityModel.Configuration.IdentityModelCaches> classe.</span><span class="sxs-lookup"><span data-stu-id="cc193-130">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cc193-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc193-131">Example</span></span>  
 <span data-ttu-id="cc193-132">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="cc193-132">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="cc193-133">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="cc193-133">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
