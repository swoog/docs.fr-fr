---
title: <tokenReplayDetection>
ms.date: 03/30/2017
ms.assetid: ac3f588e-5f75-4275-b969-2d492ecc3b47
author: BrucePerlerMS
ms.openlocfilehash: 4deeb1d84f2621adb7ff1b649a505138b6856ec1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283073"
---
# <a name="tokenreplaydetection"></a><span data-ttu-id="bfdc0-101">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="bfdc0-101">\<tokenReplayDetection></span></span>
<span data-ttu-id="bfdc0-102">Active la détection de relecture de jetons et spécifie le délai d’expiration pour les jetons.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-102">Enables token replay detection and specifies the expiration time for tokens.</span></span>  
  
 <span data-ttu-id="bfdc0-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="bfdc0-103">\<system.identityModel></span></span>  
<span data-ttu-id="bfdc0-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="bfdc0-104">\<identityConfiguration></span></span>  
<span data-ttu-id="bfdc0-105">\<tokenReplayDetection></span><span class="sxs-lookup"><span data-stu-id="bfdc0-105">\<tokenReplayDetection></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfdc0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfdc0-106">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <tokenReplayDetection enabled=xs:boolean expirationPeriod=TimeSpan>  
    </tokenReplayDetection>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="type"></a><span data-ttu-id="bfdc0-107">Type</span><span class="sxs-lookup"><span data-stu-id="bfdc0-107">Type</span></span>  
 <xref:System.IdentityModel.Configuration.TokenReplayDetectionElement>  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bfdc0-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bfdc0-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bfdc0-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bfdc0-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="bfdc0-110">Attributes</span></span>  
  
|<span data-ttu-id="bfdc0-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="bfdc0-111">Attribute</span></span>|<span data-ttu-id="bfdc0-112">Description</span><span class="sxs-lookup"><span data-stu-id="bfdc0-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bfdc0-113">enabled</span><span class="sxs-lookup"><span data-stu-id="bfdc0-113">enabled</span></span>|<span data-ttu-id="bfdc0-114">Une valeur qui spécifie si la détection de relecture de jetons est activée ; détection de relecture « true » pour activer un jeton.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-114">A value that specifies whether token replay detection is enabled; "true" to enable token replay detection.</span></span>|  
|<span data-ttu-id="bfdc0-115">expirationPeriod</span><span class="sxs-lookup"><span data-stu-id="bfdc0-115">expirationPeriod</span></span>|<span data-ttu-id="bfdc0-116">Un <xref:System.TimeSpan> qui spécifie la quantité maximale de temps avant qu’un élément est considéré comme expiré et supprimé du cache.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-116">A <xref:System.TimeSpan> that specifies the maximum amount of time before an item is considered expired and removed from the cache.</span></span>  <span data-ttu-id="bfdc0-117">Pour plus d’informations sur la spécification <xref:System.TimeSpan> valeurs, consultez [valeurs Timespan](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span><span class="sxs-lookup"><span data-stu-id="bfdc0-117">For more information about how to specify <xref:System.TimeSpan> values, see [Timespan Values](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/index.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bfdc0-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bfdc0-118">Child Elements</span></span>  
 <span data-ttu-id="bfdc0-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bfdc0-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bfdc0-120">Parent Elements</span></span>  
  
|<span data-ttu-id="bfdc0-121">Élément</span><span class="sxs-lookup"><span data-stu-id="bfdc0-121">Element</span></span>|<span data-ttu-id="bfdc0-122">Description</span><span class="sxs-lookup"><span data-stu-id="bfdc0-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bfdc0-123">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="bfdc0-123">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="bfdc0-124">Spécifie les paramètres de l’identité de niveau de service.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-124">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="bfdc0-125">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="bfdc0-125">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="bfdc0-126">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-126">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bfdc0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bfdc0-127">Remarks</span></span>  
 <span data-ttu-id="bfdc0-128">Un `<tokenReplayDetection>` élément peut être spécifié au niveau du service sous le `<identityConfiguration>` élément ou sur le niveau de collection de gestionnaires de jetons de sécurité sous la `<securityTokenHandlerConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-128">A `<tokenReplayDetection>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="bfdc0-129">Les paramètres sur une collection de gestionnaires de jetons remplacent celles spécifiées sur le service.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-129">Settings on a token handler collection override those specified on the service.</span></span>  
  
 <span data-ttu-id="bfdc0-130">Le type du cache de relecture de jetons est spécifié par le [ \<tokenReplayCache >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) élément.</span><span class="sxs-lookup"><span data-stu-id="bfdc0-130">The type of the token replay cache is specified by the [\<tokenReplayCache>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/tokenreplaycache.md) element.</span></span>
