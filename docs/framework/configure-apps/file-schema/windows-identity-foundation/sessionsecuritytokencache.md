---
title: <sessionSecurityTokenCache>
ms.date: 03/30/2017
ms.assetid: d43e676c-0153-485c-ab31-0257a2db7507
author: BrucePerlerMS
ms.openlocfilehash: 5c68fe618f965f364a3716c3bc65de5e165b12ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207797"
---
# <a name="sessionsecuritytokencache"></a><span data-ttu-id="ab6db-101">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="ab6db-101">\<sessionSecurityTokenCache></span></span>
<span data-ttu-id="ab6db-102">Inscrit un cache pour les jetons de session avec un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ab6db-102">Registers a cache for session tokens with a service or a security token handler collection.</span></span>  
  
 <span data-ttu-id="ab6db-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="ab6db-103">\<system.identityModel></span></span>  
<span data-ttu-id="ab6db-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="ab6db-104">\<identityConfiguration></span></span>  
<span data-ttu-id="ab6db-105">\<caches></span><span class="sxs-lookup"><span data-stu-id="ab6db-105">\<caches></span></span>  
<span data-ttu-id="ab6db-106">\<sessionSecurityTokenCache></span><span class="sxs-lookup"><span data-stu-id="ab6db-106">\<sessionSecurityTokenCache></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab6db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab6db-107">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ab6db-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ab6db-108">Attributes and Elements</span></span>  
 <span data-ttu-id="ab6db-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ab6db-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ab6db-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="ab6db-110">Attributes</span></span>  
  
|<span data-ttu-id="ab6db-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="ab6db-111">Attribute</span></span>|<span data-ttu-id="ab6db-112">Description</span><span class="sxs-lookup"><span data-stu-id="ab6db-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="ab6db-113">type</span><span class="sxs-lookup"><span data-stu-id="ab6db-113">type</span></span>|<span data-ttu-id="ab6db-114">Un type qui dérive de la <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> classe.</span><span class="sxs-lookup"><span data-stu-id="ab6db-114">A type that derives from the <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache> class.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ab6db-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ab6db-115">Child Elements</span></span>  
 <span data-ttu-id="ab6db-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ab6db-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ab6db-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ab6db-117">Parent Elements</span></span>  
  
|<span data-ttu-id="ab6db-118">Élément</span><span class="sxs-lookup"><span data-stu-id="ab6db-118">Element</span></span>|<span data-ttu-id="ab6db-119">Description</span><span class="sxs-lookup"><span data-stu-id="ab6db-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ab6db-120">\<caches></span><span class="sxs-lookup"><span data-stu-id="ab6db-120">\<caches></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/caches.md)|<span data-ttu-id="ab6db-121">Inscrit le met en cache utilisé par un service ou une collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ab6db-121">Registers the caches used by a service or a security token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ab6db-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="ab6db-122">Example</span></span>  
 <span data-ttu-id="ab6db-123">Le code XML suivant illustre la configuration d’un cache personnalisé pour contenir les jetons de sécurité de session (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span><span class="sxs-lookup"><span data-stu-id="ab6db-123">The following XML shows the configuration of a custom cache for holding session security tokens (<xref:System.IdentityModel.Tokens.SessionSecurityToken>).</span></span> <span data-ttu-id="ab6db-124">La configuration est extraite la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="ab6db-124">The configuration is taken from the `ClaimsAwareWebFarm` sample.</span></span> <span data-ttu-id="ab6db-125">Pour plus d’informations sur cet exemple, consultez [Index exemple de Code WIF](../../../../../docs/framework/security/wif-code-sample-index.md).</span><span class="sxs-lookup"><span data-stu-id="ab6db-125">For more information about this sample, see [WIF Code Sample Index](../../../../../docs/framework/security/wif-code-sample-index.md).</span></span>  
  
```xml  
<caches>  
  <sessionSecurityTokenCache type="CacheLibrary.SharedSessionSecurityTokenCache, CacheLibrary">  
    <!--cacheServiceAddress points to the centralized session security token cache service running in the web farm.-->  
    <cacheServiceAddress url="http://localhost:4161/SessionSecurityTokenCacheService.svc" />  
  </sessionSecurityTokenCache>  
</caches>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ab6db-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab6db-126">See also</span></span>

- <xref:System.IdentityModel.Tokens.SessionSecurityTokenCache>
