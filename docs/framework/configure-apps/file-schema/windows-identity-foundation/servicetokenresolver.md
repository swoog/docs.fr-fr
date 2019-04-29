---
title: <serviceTokenResolver>
ms.date: 03/30/2017
ms.assetid: 6e9001e1-e064-4f47-84b2-46225c177746
author: BrucePerlerMS
ms.openlocfilehash: 1143717882652fc8a03947327b5f1ea89dde7373
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793807"
---
# <a name="servicetokenresolver"></a><span data-ttu-id="73caa-101">\<serviceTokenResolver></span><span class="sxs-lookup"><span data-stu-id="73caa-101">\<serviceTokenResolver></span></span>
<span data-ttu-id="73caa-102">Inscrit le résolveur de jeton de service qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="73caa-102">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="73caa-103">Le programme de résolution de jeton de service est utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="73caa-103">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span>  
  
 <span data-ttu-id="73caa-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="73caa-104">\<system.identityModel></span></span>  
<span data-ttu-id="73caa-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="73caa-105">\<identityConfiguration></span></span>  
<span data-ttu-id="73caa-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="73caa-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="73caa-107">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="73caa-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="73caa-108">\<serviceTokenResolver></span><span class="sxs-lookup"><span data-stu-id="73caa-108">\<serviceTokenResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73caa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73caa-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <serviceTokenResolver type=xs:string>  
        </serviceTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="73caa-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="73caa-110">Attributes and Elements</span></span>  
 <span data-ttu-id="73caa-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="73caa-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="73caa-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="73caa-112">Attributes</span></span>  
  
|<span data-ttu-id="73caa-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="73caa-113">Attribute</span></span>|<span data-ttu-id="73caa-114">Description</span><span class="sxs-lookup"><span data-stu-id="73caa-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="73caa-115">type</span><span class="sxs-lookup"><span data-stu-id="73caa-115">type</span></span>|<span data-ttu-id="73caa-116">Spécifie le type du programme de résolution de jeton de service.</span><span class="sxs-lookup"><span data-stu-id="73caa-116">Specifies the type of the service token resolver.</span></span> <span data-ttu-id="73caa-117">Soit le <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type ou un type qui dérive de la <xref:System.IdentityModel.Selectors.SecurityTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="73caa-117">Either the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type or a type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span> <span data-ttu-id="73caa-118">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="73caa-118">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span> <span data-ttu-id="73caa-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="73caa-119">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="73caa-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="73caa-120">Child Elements</span></span>  
 <span data-ttu-id="73caa-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="73caa-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="73caa-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="73caa-122">Parent Elements</span></span>  
  
|<span data-ttu-id="73caa-123">Élément</span><span class="sxs-lookup"><span data-stu-id="73caa-123">Element</span></span>|<span data-ttu-id="73caa-124">Description</span><span class="sxs-lookup"><span data-stu-id="73caa-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="73caa-125">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="73caa-125">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="73caa-126">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="73caa-126">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="73caa-127">Notes</span><span class="sxs-lookup"><span data-stu-id="73caa-127">Remarks</span></span>  
 <span data-ttu-id="73caa-128">Le programme de résolution de jeton de service peut être utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="73caa-128">The service token resolver can be used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="73caa-129">Il est utilisé pour récupérer la clé qui doit être utilisée pour déchiffrer les jetons entrants.</span><span class="sxs-lookup"><span data-stu-id="73caa-129">It is used to retrieve the key that should be used to decrypt incoming tokens.</span></span> <span data-ttu-id="73caa-130">Vous devez spécifier le `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="73caa-130">You must specify the `type` attribute.</span></span> <span data-ttu-id="73caa-131">Le type spécifié peut être soit <xref:System.IdentityModel.Selectors.SecurityTokenResolver> ou un type personnalisé qui dérive de la <xref:System.IdentityModel.Selectors.SecurityTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="73caa-131">The type specified can be either <xref:System.IdentityModel.Selectors.SecurityTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span>  
  
 <span data-ttu-id="73caa-132">Certains gestionnaires de jetons permettent de spécifier les paramètres de résolution de jetons de service dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="73caa-132">Some token handlers allow you to specify service token resolver settings in configuration.</span></span> <span data-ttu-id="73caa-133">Les paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="73caa-133">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="73caa-134">En spécifiant le `<serviceTokenResolver>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="73caa-134">Specifying the `<serviceTokenResolver>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="73caa-135">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="73caa-135">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73caa-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="73caa-136">Example</span></span>  
  
```xml  
<serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
```
