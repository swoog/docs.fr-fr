---
title: <caches>
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
ms.openlocfilehash: b1d04280ef993297102d446ba5a7db54e8404dd8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55285660"
---
# <a name="caches"></a><span data-ttu-id="c8585-101">\<caches></span><span class="sxs-lookup"><span data-stu-id="c8585-101">\<caches></span></span>
<span data-ttu-id="c8585-102">Inscrit les caches utilisés pour la détection de relecture de jetons et de jetons de session.</span><span class="sxs-lookup"><span data-stu-id="c8585-102">Registers the caches used for session tokens and token replay detection.</span></span>  
  
 <span data-ttu-id="c8585-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="c8585-103">\<system.identityModel></span></span>  
<span data-ttu-id="c8585-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="c8585-104">\<identityConfiguration></span></span>  
<span data-ttu-id="c8585-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="c8585-105">\<caches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8585-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8585-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c8585-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c8585-107">Attributes and Elements</span></span>  
 <span data-ttu-id="c8585-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c8585-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c8585-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="c8585-109">Attributes</span></span>  
 <span data-ttu-id="c8585-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c8585-110">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c8585-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c8585-111">Child Elements</span></span>  
  
|<span data-ttu-id="c8585-112">Élément</span><span class="sxs-lookup"><span data-stu-id="c8585-112">Element</span></span>|<span data-ttu-id="c8585-113">Description</span><span class="sxs-lookup"><span data-stu-id="c8585-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c8585-114">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="c8585-114">\<sessionSecurityTokenCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|<span data-ttu-id="c8585-115">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8585-115">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[<span data-ttu-id="c8585-116">\<tokenReplayCache></span><span class="sxs-lookup"><span data-stu-id="c8585-116">\<tokenReplayCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|<span data-ttu-id="c8585-117">Inscrit un cache de relecture de jetons avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8585-117">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c8585-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c8585-118">Parent Elements</span></span>  
  
|<span data-ttu-id="c8585-119">Élément</span><span class="sxs-lookup"><span data-stu-id="c8585-119">Element</span></span>|<span data-ttu-id="c8585-120">Description</span><span class="sxs-lookup"><span data-stu-id="c8585-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c8585-121">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="c8585-121">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="c8585-122">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="c8585-122">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="c8585-123">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="c8585-123">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="c8585-124">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="c8585-124">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c8585-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c8585-125">Remarks</span></span>  
 <span data-ttu-id="c8585-126">Un `<caches>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="c8585-126">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="c8585-127">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="c8585-127">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="c8585-128">Le `<caches>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> classe.</span><span class="sxs-lookup"><span data-stu-id="c8585-128">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="c8585-129">Caches configurés sont représentées par la <xref:System.IdentityModel.Configuration.IdentityModelCaches> classe.</span><span class="sxs-lookup"><span data-stu-id="c8585-129">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c8585-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8585-130">Example</span></span>  
 <span data-ttu-id="c8585-131">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="c8585-131">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="c8585-132">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="c8585-132">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
