---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: 024375cb114bb080c576ea033e5588526350ecdf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510089"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="9fae2-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="9fae2-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="9fae2-103">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9fae2-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="9fae2-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="9fae2-104">\<system.identityModel></span></span>  
<span data-ttu-id="9fae2-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="9fae2-105">\<identityConfiguration></span></span>  
<span data-ttu-id="9fae2-106">\<caches></span><span class="sxs-lookup"><span data-stu-id="9fae2-106">\<caches></span></span>  
<span data-ttu-id="9fae2-107">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="9fae2-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9fae2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fae2-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <caches>  
      <sessionSecurityTokenCache type=xs:string>  
      </sessionSecurityTokenCache>  
    </caches>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9fae2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9fae2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9fae2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9fae2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9fae2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="9fae2-111">Attributes</span></span>  
  
|<span data-ttu-id="9fae2-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="9fae2-112">Attribute</span></span>|<span data-ttu-id="9fae2-113">Description</span><span class="sxs-lookup"><span data-stu-id="9fae2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9fae2-114">type</span><span class="sxs-lookup"><span data-stu-id="9fae2-114">type</span></span>|<span data-ttu-id="9fae2-115">Un type qui dérive de la <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> classe.</span><span class="sxs-lookup"><span data-stu-id="9fae2-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9fae2-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9fae2-116">Child Elements</span></span>  
 <span data-ttu-id="9fae2-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9fae2-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9fae2-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9fae2-118">Parent Elements</span></span>  
  
|<span data-ttu-id="9fae2-119">Élément</span><span class="sxs-lookup"><span data-stu-id="9fae2-119">Element</span></span>|<span data-ttu-id="9fae2-120">Description</span><span class="sxs-lookup"><span data-stu-id="9fae2-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9fae2-121">\<caches></span><span class="sxs-lookup"><span data-stu-id="9fae2-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="9fae2-122">Inscrit le met en cache utilisé par un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9fae2-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9fae2-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="9fae2-123">Example</span></span>  
 <span data-ttu-id="9fae2-124">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="9fae2-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="9fae2-125">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="9fae2-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="9fae2-126">Pour plus d’informations sur cet exemple, consultez [Index exemple de Code WIF](../../../../../docs/framework/security/wif-code-sample-index.md).</span><span class="sxs-lookup"><span data-stu-id="9fae2-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9fae2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fae2-127">See also</span></span>
- <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
