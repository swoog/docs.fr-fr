---
title: '&lt;sessionSecurityTokenCache&gt;'
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: b812673ac1c015adde357d3c0707d85643aad3e9
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47401368"
---
# <a name="ltsessionsecuritytokencachegt"></a><span data-ttu-id="dff08-102">&lt;sessionSecurityTokenCache&gt;</span><span class="sxs-lookup"><span data-stu-id="dff08-102">&lt;sessionSecurityTokenCache&gt;</span></span>
<span data-ttu-id="dff08-103">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="dff08-103">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="dff08-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="dff08-104">\<system.identityModel></span></span>  
<span data-ttu-id="dff08-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="dff08-105">\<identityConfiguration></span></span>  
<span data-ttu-id="dff08-106">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="dff08-106">\<caches></span></span>  
<span data-ttu-id="dff08-107">\<sessionSecurityTokenCache ></span><span class="sxs-lookup"><span data-stu-id="dff08-107">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dff08-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff08-108">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dff08-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dff08-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dff08-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dff08-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dff08-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="dff08-111">Attributes</span></span>  
  
|<span data-ttu-id="dff08-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="dff08-112">Attribute</span></span>|<span data-ttu-id="dff08-113">Description</span><span class="sxs-lookup"><span data-stu-id="dff08-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="dff08-114">type</span><span class="sxs-lookup"><span data-stu-id="dff08-114">type</span></span>|<span data-ttu-id="dff08-115">Un type qui dérive de la <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> classe.</span><span class="sxs-lookup"><span data-stu-id="dff08-115">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dff08-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dff08-116">Child Elements</span></span>  
 <span data-ttu-id="dff08-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dff08-117">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dff08-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dff08-118">Parent Elements</span></span>  
  
|<span data-ttu-id="dff08-119">Élément</span><span class="sxs-lookup"><span data-stu-id="dff08-119">Element</span></span>|<span data-ttu-id="dff08-120">Description</span><span class="sxs-lookup"><span data-stu-id="dff08-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dff08-121">\<met en cache ></span><span class="sxs-lookup"><span data-stu-id="dff08-121">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="dff08-122">Inscrit le met en cache utilisé par un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="dff08-122">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dff08-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="dff08-123">Example</span></span>  
 <span data-ttu-id="dff08-124">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="dff08-124">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="dff08-125">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="dff08-125">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="dff08-126">Pour plus d’informations sur cet exemple, consultez [Index exemple de Code WIF](../../../../../docs/framework/security/wif-code-sample-index.md).</span><span class="sxs-lookup"><span data-stu-id="dff08-126">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="dff08-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff08-127">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
