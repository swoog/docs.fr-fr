---
title: '&lt;serviceTokenResolver&gt;'
ms.date: 03/30/2017
ms.assetid: 6e9001e1-e064-4f47-84b2-46225c177746
author: BrucePerlerMS
ms.openlocfilehash: d4b64e2c88e153834b7cf5a83bd6258b6dfd471f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075296"
---
# <a name="ltservicetokenresolvergt"></a><span data-ttu-id="eadfe-102">&lt;serviceTokenResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="eadfe-102">&lt;serviceTokenResolver&gt;</span></span>
<span data-ttu-id="eadfe-103">Inscrit le résolveur de jeton de service qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="eadfe-103">Registers the service token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="eadfe-104">Le programme de résolution de jeton de service est utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="eadfe-104">The service token resolver is used to resolve the encryption token on incoming tokens and messages.</span></span>  
  
 <span data-ttu-id="eadfe-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="eadfe-105">\<system.identityModel></span></span>  
<span data-ttu-id="eadfe-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="eadfe-106">\<identityConfiguration></span></span>  
<span data-ttu-id="eadfe-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="eadfe-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="eadfe-108">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="eadfe-108">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="eadfe-109">\<serviceTokenResolver ></span><span class="sxs-lookup"><span data-stu-id="eadfe-109">\<serviceTokenResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eadfe-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eadfe-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eadfe-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eadfe-111">Attributes and Elements</span></span>  
 <span data-ttu-id="eadfe-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eadfe-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eadfe-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="eadfe-113">Attributes</span></span>  
  
|<span data-ttu-id="eadfe-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="eadfe-114">Attribute</span></span>|<span data-ttu-id="eadfe-115">Description</span><span class="sxs-lookup"><span data-stu-id="eadfe-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="eadfe-116">type</span><span class="sxs-lookup"><span data-stu-id="eadfe-116">type</span></span>|<span data-ttu-id="eadfe-117">Spécifie le type du programme de résolution de jeton de service.</span><span class="sxs-lookup"><span data-stu-id="eadfe-117">Specifies the type of the service token resolver.</span></span> <span data-ttu-id="eadfe-118">Soit le <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type ou un type qui dérive de la <xref:System.IdentityModel.Selectors.SecurityTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="eadfe-118">Either the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> type or a type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span> <span data-ttu-id="eadfe-119">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="eadfe-119">For more information about how to specify the `type` attribute, see [Custom Type References].</span></span> <span data-ttu-id="eadfe-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eadfe-120">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="eadfe-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eadfe-121">Child Elements</span></span>  
 <span data-ttu-id="eadfe-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eadfe-122">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eadfe-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eadfe-123">Parent Elements</span></span>  
  
|<span data-ttu-id="eadfe-124">Élément</span><span class="sxs-lookup"><span data-stu-id="eadfe-124">Element</span></span>|<span data-ttu-id="eadfe-125">Description</span><span class="sxs-lookup"><span data-stu-id="eadfe-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eadfe-126">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="eadfe-126">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="eadfe-127">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="eadfe-127">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eadfe-128">Notes</span><span class="sxs-lookup"><span data-stu-id="eadfe-128">Remarks</span></span>  
 <span data-ttu-id="eadfe-129">Le programme de résolution de jeton de service peut être utilisé pour résoudre le jeton de chiffrement sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="eadfe-129">The service token resolver can be used to resolve the encryption token on incoming tokens and messages.</span></span> <span data-ttu-id="eadfe-130">Il est utilisé pour récupérer la clé qui doit être utilisée pour déchiffrer les jetons entrants.</span><span class="sxs-lookup"><span data-stu-id="eadfe-130">It is used to retrieve the key that should be used to decrypt incoming tokens.</span></span> <span data-ttu-id="eadfe-131">Vous devez spécifier le `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="eadfe-131">You must specify the `type` attribute.</span></span> <span data-ttu-id="eadfe-132">Le type spécifié peut être soit <xref:System.IdentityModel.Selectors.SecurityTokenResolver> ou un type personnalisé qui dérive de la <xref:System.IdentityModel.Selectors.SecurityTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="eadfe-132">The type specified can be either <xref:System.IdentityModel.Selectors.SecurityTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Selectors.SecurityTokenResolver> class.</span></span>  
  
 <span data-ttu-id="eadfe-133">Certains gestionnaires de jetons permettent de spécifier les paramètres de résolution de jetons de service dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="eadfe-133">Some token handlers allow you to specify service token resolver settings in configuration.</span></span> <span data-ttu-id="eadfe-134">Les paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eadfe-134">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="eadfe-135">En spécifiant le `<serviceTokenResolver>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="eadfe-135">Specifying the `<serviceTokenResolver>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="eadfe-136">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="eadfe-136">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eadfe-137">Exemple</span><span class="sxs-lookup"><span data-stu-id="eadfe-137">Example</span></span>  
  
```xml  
<serviceTokenResolver type="MyNamespace.CustomTokenResolver, MyAssembly" />  
```
