---
title: '&lt;Caches&gt;'
ms.date: 03/30/2017
ms.assetid: 4651091b-3a20-40d8-b293-4408c0710143
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 2a9766b826eb7a708b4b4e99b6bd984f9fc76812
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32755212"
---
# <a name="ltcachesgt"></a><span data-ttu-id="412f2-102">&lt;Caches&gt;</span><span class="sxs-lookup"><span data-stu-id="412f2-102">&lt;caches&gt;</span></span>
<span data-ttu-id="412f2-103">Inscrit le met en cache utilisés pour les jetons de session et de la détection de relecture de jetons.</span><span class="sxs-lookup"><span data-stu-id="412f2-103">Registers the caches used for session tokens and token replay detection.</span></span>  
  
 <span data-ttu-id="412f2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="412f2-104">\<system.identityModel></span></span>  
<span data-ttu-id="412f2-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="412f2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="412f2-106">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="412f2-106">\<caches></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="412f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="412f2-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="412f2-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="412f2-108">Attributes and Elements</span></span>  
 <span data-ttu-id="412f2-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="412f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="412f2-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="412f2-110">Attributes</span></span>  
 <span data-ttu-id="412f2-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="412f2-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="412f2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="412f2-112">Child Elements</span></span>  
  
|<span data-ttu-id="412f2-113">Élément</span><span class="sxs-lookup"><span data-stu-id="412f2-113">Element</span></span>|<span data-ttu-id="412f2-114">Description</span><span class="sxs-lookup"><span data-stu-id="412f2-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="412f2-115">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="412f2-115">\<sessionSecurityTokenCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessionsecuritytokencache.md)|<span data-ttu-id="412f2-116">Inscrit un cache pour les jetons de session avec un service ou d’une collection de gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="412f2-116">Registers a cache for session tokens with a service or a security token handler collection.</span></span>|  
|[<span data-ttu-id="412f2-117">\<tokenReplayCache ></span><span class="sxs-lookup"><span data-stu-id="412f2-117">\<tokenReplayCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md)|<span data-ttu-id="412f2-118">Inscrit un cache de relecture de jetons avec un service ou d’une collection de gestionnaire de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="412f2-118">Registers a token replay cache with a service or a security token handler collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="412f2-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="412f2-119">Parent Elements</span></span>  
  
|<span data-ttu-id="412f2-120">Élément</span><span class="sxs-lookup"><span data-stu-id="412f2-120">Element</span></span>|<span data-ttu-id="412f2-121">Description</span><span class="sxs-lookup"><span data-stu-id="412f2-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="412f2-122">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="412f2-122">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="412f2-123">Spécifie les paramètres d’identité au niveau du service.</span><span class="sxs-lookup"><span data-stu-id="412f2-123">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="412f2-124">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="412f2-124">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="412f2-125">Fournit des gestionnaires de jetons de configuration pour une collection de sécurité.</span><span class="sxs-lookup"><span data-stu-id="412f2-125">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="412f2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="412f2-126">Remarks</span></span>  
 <span data-ttu-id="412f2-127">A `<caches>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de regroupement de gestionnaire de jetons de sécurité sous le `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="412f2-127">A `<caches>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="412f2-128">Paramètres sur une collection de gestionnaire de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="412f2-128">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="412f2-129">Le `<caches>` élément est représenté par la <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> classe.</span><span class="sxs-lookup"><span data-stu-id="412f2-129">The `<caches>` element is represented by the <xref:System.IdentityModel.Configuration.IdentityModelCachesElement> class.</span></span> <span data-ttu-id="412f2-130">Les caches configurés sont représentées par la <xref:System.IdentityModel.Configuration.IdentityModelCaches> classe.</span><span class="sxs-lookup"><span data-stu-id="412f2-130">The configured caches are represented by the <xref:System.IdentityModel.Configuration.IdentityModelCaches> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="412f2-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="412f2-131">Example</span></span>  
 <span data-ttu-id="412f2-132">Le code XML suivant illustre la configuration d’un cache personnalisé destiné à accueillir des jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="412f2-132">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="412f2-133">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="412f2-133">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```
