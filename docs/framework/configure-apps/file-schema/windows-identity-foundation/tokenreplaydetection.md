---
title: '&lt;tokenReplayDetection&gt;'
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: bd2272cb83dc0183d5008cfa178e11783f51ca2d
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47205927"
---
# <a name="lttokenreplaydetectiongt"></a><span data-ttu-id="de46b-102">&lt;tokenReplayDetection&gt;</span><span class="sxs-lookup"><span data-stu-id="de46b-102">&lt;tokenReplayDetection&gt;</span></span>
<span data-ttu-id="de46b-103">Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons.</span><span class="sxs-lookup"><span data-stu-id="de46b-103">Enables token replay detection and specifies the expiration time for tokens.</span></span>  
  
 <span data-ttu-id="de46b-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="de46b-104">\<system.identityModel></span></span>  
<span data-ttu-id="de46b-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="de46b-105">\<identityConfiguration></span></span>  
<span data-ttu-id="de46b-106">\<tokenReplayDetection ></span><span class="sxs-lookup"><span data-stu-id="de46b-106">\<tokenReplayDetection></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de46b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de46b-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a><span data-ttu-id="de46b-108">Type</span><span class="sxs-lookup"><span data-stu-id="de46b-108">Type</span></span>  
 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="de46b-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="de46b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="de46b-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="de46b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="de46b-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="de46b-111">Attributes</span></span>  
  
|<span data-ttu-id="de46b-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="de46b-112">Attribute</span></span>|<span data-ttu-id="de46b-113">Description</span><span class="sxs-lookup"><span data-stu-id="de46b-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="de46b-114">enabled</span><span class="sxs-lookup"><span data-stu-id="de46b-114">enabled</span></span>|<span data-ttu-id="de46b-115">Une valeur qui spécifie si la détection de relecture de jetons est activée ; détection de relecture « true » pour activer un jeton.</span><span class="sxs-lookup"><span data-stu-id="de46b-115">A value that specifies whether token replay detection is enabled; "true" to enable token replay detection.</span></span>|  
|<span data-ttu-id="de46b-116">expirationPeriod</span><span class="sxs-lookup"><span data-stu-id="de46b-116">expirationPeriod</span></span>|<span data-ttu-id="de46b-117">Un <xref:System.TimeSpan> qui spécifie la quantité maximale de temps avant qu’un élément est considéré comme expiré et supprimé du cache.</span><span class="sxs-lookup"><span data-stu-id="de46b-117">A <xref:System.TimeSpan> that specifies the maximum amount of time before an item is considered expired and removed from the cache.</span></span>  <span data-ttu-id="de46b-118">Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="de46b-118">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="de46b-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="de46b-119">Child Elements</span></span>  
 <span data-ttu-id="de46b-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="de46b-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="de46b-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="de46b-121">Parent Elements</span></span>  
  
|<span data-ttu-id="de46b-122">Élément</span><span class="sxs-lookup"><span data-stu-id="de46b-122">Element</span></span>|<span data-ttu-id="de46b-123">Description</span><span class="sxs-lookup"><span data-stu-id="de46b-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="de46b-124">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="de46b-124">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="de46b-125">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="de46b-125">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="de46b-126">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="de46b-126">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="de46b-127">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="de46b-127">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="de46b-128">Notes</span><span class="sxs-lookup"><span data-stu-id="de46b-128">Remarks</span></span>  
 <span data-ttu-id="de46b-129">Un `<tokenReplayDetection>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="de46b-129">A `<tokenReplayDetection>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="de46b-130">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="de46b-130">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="de46b-131">Le type du cache de relecture de jetons est spécifié par le [ \<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) élément.</span><span class="sxs-lookup"><span data-stu-id="de46b-131">The type of the token replay cache is specified by the [\<tokenReplayCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) element.</span></span>
