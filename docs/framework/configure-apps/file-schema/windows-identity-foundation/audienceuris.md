---
title: '&lt;audienceUris&gt;'
ms.date: 03/30/2017
ms.assetid: 7a3d8515-d756-4afe-a22d-07cbe2217ee3
author: BrucePerlerMS
ms.openlocfilehash: af138a4da49a48ed43e1bc8f2c2c81c56892feed
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48034478"
---
# <a name="ltaudienceurisgt"></a><span data-ttu-id="56833-102">&lt;audienceUris&gt;</span><span class="sxs-lookup"><span data-stu-id="56833-102">&lt;audienceUris&gt;</span></span>
<span data-ttu-id="56833-103">Spécifie le jeu d’URI qui sont des identificateurs acceptables de la partie de confiance (RP).</span><span class="sxs-lookup"><span data-stu-id="56833-103">Specifies the set of URIs that are acceptable identifiers of the relying party (RP).</span></span> <span data-ttu-id="56833-104">Jetons ne seront pas acceptés, sauf si elles sont limitées pour un des URI d’audience autorisés.</span><span class="sxs-lookup"><span data-stu-id="56833-104">Tokens will not be accepted unless they are scoped for one of the allowed audience URIs.</span></span>  
  
 <span data-ttu-id="56833-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="56833-105">\<system.identityModel></span></span>  
<span data-ttu-id="56833-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="56833-106">\<identityConfiguration></span></span>  
<span data-ttu-id="56833-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="56833-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="56833-108">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="56833-108">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="56833-109">\<audienceUris ></span><span class="sxs-lookup"><span data-stu-id="56833-109">\<audienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56833-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56833-110">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <audienceUris mode=xs:string>  
          <add value=xs:string />  
          <clear />  
          <remove value=xs:string />  
        </audienceUris>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="56833-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="56833-111">Attributes and Elements</span></span>  
 <span data-ttu-id="56833-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="56833-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="56833-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="56833-113">Attributes</span></span>  
  
|<span data-ttu-id="56833-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="56833-114">Attribute</span></span>|<span data-ttu-id="56833-115">Description</span><span class="sxs-lookup"><span data-stu-id="56833-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="56833-116">mode</span><span class="sxs-lookup"><span data-stu-id="56833-116">mode</span></span>|<span data-ttu-id="56833-117">Un <xref:System.IdentityModel.Selectors.AudienceUriMode> valeur qui spécifie si la restriction d’audience doit être appliquée à un jeton entrant.</span><span class="sxs-lookup"><span data-stu-id="56833-117">An <xref:System.IdentityModel.Selectors.AudienceUriMode> value that specifies whether the audience restriction should be applied to an incoming token.</span></span> <span data-ttu-id="56833-118">Les valeurs possibles sont « », « Jamais » et toujours « BearerKeyOnly ».</span><span class="sxs-lookup"><span data-stu-id="56833-118">The possible values are "Always", "Never", and "BearerKeyOnly".</span></span> <span data-ttu-id="56833-119">La valeur par défaut est « Toujours ».</span><span class="sxs-lookup"><span data-stu-id="56833-119">The default is "Always".</span></span> <span data-ttu-id="56833-120">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="56833-120">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="56833-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="56833-121">Child Elements</span></span>  
  
|<span data-ttu-id="56833-122">Élément</span><span class="sxs-lookup"><span data-stu-id="56833-122">Element</span></span>|<span data-ttu-id="56833-123">Description</span><span class="sxs-lookup"><span data-stu-id="56833-123">Description</span></span>|  
|-------------|-----------------|  
|`<add value=xs:string>`|<span data-ttu-id="56833-124">Ajoute l’URI spécifié par le `value` d’attribut à la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="56833-124">Adds the URI specified by the `value` attribute to the audienceUris collection.</span></span> <span data-ttu-id="56833-125">L'attribut `value` est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="56833-125">The `value` attribute is required.</span></span> <span data-ttu-id="56833-126">L’URI respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="56833-126">The URI is case-sensitive.</span></span>|  
|`<clear>`|<span data-ttu-id="56833-127">Efface la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="56833-127">Clears the audienceUris collection.</span></span> <span data-ttu-id="56833-128">Tous les identificateurs sont supprimés de la collection.</span><span class="sxs-lookup"><span data-stu-id="56833-128">All identifiers are removed from the collection.</span></span>|  
|`<remove value=xs:string>`|<span data-ttu-id="56833-129">Supprime l’URI spécifié par le `value` attribut à partir de la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="56833-129">Removes the URI specified by the `value` attribute from the audienceUris collection.</span></span> <span data-ttu-id="56833-130">L'attribut `value` est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="56833-130">The `value` attribute is required.</span></span> <span data-ttu-id="56833-131">L’URI respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="56833-131">The URI is case-sensitive.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="56833-132">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="56833-132">Parent Elements</span></span>  
  
|<span data-ttu-id="56833-133">Élément</span><span class="sxs-lookup"><span data-stu-id="56833-133">Element</span></span>|<span data-ttu-id="56833-134">Description</span><span class="sxs-lookup"><span data-stu-id="56833-134">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="56833-135">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="56833-135">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="56833-136">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="56833-136">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="56833-137">Notes</span><span class="sxs-lookup"><span data-stu-id="56833-137">Remarks</span></span>  
 <span data-ttu-id="56833-138">Par défaut, la collection est vide. Utilisez `<add>`, `<clear>`, et `<remove>` éléments à modifier la collection.</span><span class="sxs-lookup"><span data-stu-id="56833-138">By default, the collection is empty; use `<add>`, `<clear>`, and `<remove>` elements to modify the collection.</span></span> <span data-ttu-id="56833-139"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> et <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objets utilisent les valeurs dans la collection d’URI d’audience pour configurer toutes autorisée audience restrictions URI dans <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objets.</span><span class="sxs-lookup"><span data-stu-id="56833-139"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> and <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objects use the values in the audience URI collection to configure any allowed audience URI restrictions in <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objects.</span></span>  
  
 <span data-ttu-id="56833-140">Le `<audienceUris>` élément est représenté par la <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="56833-140">The `<audienceUris>` element is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> class.</span></span> <span data-ttu-id="56833-141">Un URI individuel ajouté à la collection est représenté par la <xref:System.IdentityModel.Configuration.AudienceUriElement> classe.</span><span class="sxs-lookup"><span data-stu-id="56833-141">An individual URI added to the collection is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="56833-142">L’utilisation de la `<audienceUris>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="56833-142">The use of the `<audienceUris>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="56833-143">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="56833-143">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="56833-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="56833-144">Example</span></span>  
 <span data-ttu-id="56833-145">Le code XML suivant montre comment configurer l’URI d’audience acceptable pour une application.</span><span class="sxs-lookup"><span data-stu-id="56833-145">The following XML shows how to configure the acceptable audience URIs for an application.</span></span> <span data-ttu-id="56833-146">Cet exemple configure un URI unique.</span><span class="sxs-lookup"><span data-stu-id="56833-146">This example configures a single URI.</span></span> <span data-ttu-id="56833-147">Jetons de portée pour cet URI seront acceptés, toutes les autres sont rejetées.</span><span class="sxs-lookup"><span data-stu-id="56833-147">Tokens scoped for this URI will be accepted, all others will be rejected.</span></span>  
  
```xml  
<audienceUris>  
  <add value="http://localhost:19851/"/>  
</audienceUris>  
```
