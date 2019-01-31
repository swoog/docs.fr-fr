---
title: <audienceUris>
ms.date: 03/30/2017
ms.assetid: 7a3d8515-d756-4afe-a22d-07cbe2217ee3
author: BrucePerlerMS
ms.openlocfilehash: 556c444d5e48e27036c4b49338f6e70de7ef5c5d
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55267272"
---
# <a name="audienceuris"></a><span data-ttu-id="88121-101">\<audienceUris></span><span class="sxs-lookup"><span data-stu-id="88121-101">\<audienceUris></span></span>
<span data-ttu-id="88121-102">Spécifie le jeu d’URI qui sont des identificateurs acceptables de la partie de confiance (RP).</span><span class="sxs-lookup"><span data-stu-id="88121-102">Specifies the set of URIs that are acceptable identifiers of the relying party (RP).</span></span> <span data-ttu-id="88121-103">Jetons ne seront pas acceptés, sauf si elles sont limitées pour un des URI d’audience autorisés.</span><span class="sxs-lookup"><span data-stu-id="88121-103">Tokens will not be accepted unless they are scoped for one of the allowed audience URIs.</span></span>  
  
 <span data-ttu-id="88121-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="88121-104">\<system.identityModel></span></span>  
<span data-ttu-id="88121-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="88121-105">\<identityConfiguration></span></span>  
<span data-ttu-id="88121-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="88121-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="88121-107">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="88121-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="88121-108">\<audienceUris></span><span class="sxs-lookup"><span data-stu-id="88121-108">\<audienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88121-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88121-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="88121-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="88121-110">Attributes and Elements</span></span>  
 <span data-ttu-id="88121-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="88121-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="88121-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="88121-112">Attributes</span></span>  
  
|<span data-ttu-id="88121-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="88121-113">Attribute</span></span>|<span data-ttu-id="88121-114">Description</span><span class="sxs-lookup"><span data-stu-id="88121-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="88121-115">mode</span><span class="sxs-lookup"><span data-stu-id="88121-115">mode</span></span>|<span data-ttu-id="88121-116">Un <xref:System.IdentityModel.Selectors.AudienceUriMode> valeur qui spécifie si la restriction d’audience doit être appliquée à un jeton entrant.</span><span class="sxs-lookup"><span data-stu-id="88121-116">An <xref:System.IdentityModel.Selectors.AudienceUriMode> value that specifies whether the audience restriction should be applied to an incoming token.</span></span> <span data-ttu-id="88121-117">Les valeurs possibles sont « », « Jamais » et toujours « BearerKeyOnly ».</span><span class="sxs-lookup"><span data-stu-id="88121-117">The possible values are "Always", "Never", and "BearerKeyOnly".</span></span> <span data-ttu-id="88121-118">La valeur par défaut est « Toujours ».</span><span class="sxs-lookup"><span data-stu-id="88121-118">The default is "Always".</span></span> <span data-ttu-id="88121-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="88121-119">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="88121-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="88121-120">Child Elements</span></span>  
  
|<span data-ttu-id="88121-121">Élément</span><span class="sxs-lookup"><span data-stu-id="88121-121">Element</span></span>|<span data-ttu-id="88121-122">Description</span><span class="sxs-lookup"><span data-stu-id="88121-122">Description</span></span>|  
|-------------|-----------------|  
|`<add value=xs:string>`|<span data-ttu-id="88121-123">Ajoute l’URI spécifié par le `value` d’attribut à la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="88121-123">Adds the URI specified by the `value` attribute to the audienceUris collection.</span></span> <span data-ttu-id="88121-124">L'attribut `value` est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="88121-124">The `value` attribute is required.</span></span> <span data-ttu-id="88121-125">L’URI respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="88121-125">The URI is case-sensitive.</span></span>|  
|`<clear>`|<span data-ttu-id="88121-126">Efface la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="88121-126">Clears the audienceUris collection.</span></span> <span data-ttu-id="88121-127">Tous les identificateurs sont supprimés de la collection.</span><span class="sxs-lookup"><span data-stu-id="88121-127">All identifiers are removed from the collection.</span></span>|  
|`<remove value=xs:string>`|<span data-ttu-id="88121-128">Supprime l’URI spécifié par le `value` attribut à partir de la collection d’audienceUris.</span><span class="sxs-lookup"><span data-stu-id="88121-128">Removes the URI specified by the `value` attribute from the audienceUris collection.</span></span> <span data-ttu-id="88121-129">L'attribut `value` est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="88121-129">The `value` attribute is required.</span></span> <span data-ttu-id="88121-130">L’URI respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="88121-130">The URI is case-sensitive.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="88121-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="88121-131">Parent Elements</span></span>  
  
|<span data-ttu-id="88121-132">Élément</span><span class="sxs-lookup"><span data-stu-id="88121-132">Element</span></span>|<span data-ttu-id="88121-133">Description</span><span class="sxs-lookup"><span data-stu-id="88121-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="88121-134">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="88121-134">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="88121-135">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="88121-135">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="88121-136">Notes</span><span class="sxs-lookup"><span data-stu-id="88121-136">Remarks</span></span>  
 <span data-ttu-id="88121-137">Par défaut, la collection est vide. Utilisez `<add>`, `<clear>`, et `<remove>` éléments à modifier la collection.</span><span class="sxs-lookup"><span data-stu-id="88121-137">By default, the collection is empty; use `<add>`, `<clear>`, and `<remove>` elements to modify the collection.</span></span> <span data-ttu-id="88121-138"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> et <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objets utilisent les valeurs dans la collection d’URI d’audience pour configurer toutes autorisée audience restrictions URI dans <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objets.</span><span class="sxs-lookup"><span data-stu-id="88121-138"><xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> and <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> objects use the values in the audience URI collection to configure any allowed audience URI restrictions in <xref:System.IdentityModel.Tokens.SamlSecurityTokenRequirement> objects.</span></span>  
  
 <span data-ttu-id="88121-139">Le `<audienceUris>` élément est représenté par la <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="88121-139">The `<audienceUris>` element is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElementCollection> class.</span></span> <span data-ttu-id="88121-140">Un URI individuel ajouté à la collection est représenté par la <xref:System.IdentityModel.Configuration.AudienceUriElement> classe.</span><span class="sxs-lookup"><span data-stu-id="88121-140">An individual URI added to the collection is represented by the <xref:System.IdentityModel.Configuration.AudienceUriElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="88121-141">L’utilisation de la `<audienceUris>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="88121-141">The use of the `<audienceUris>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="88121-142">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="88121-142">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="88121-143">Exemple</span><span class="sxs-lookup"><span data-stu-id="88121-143">Example</span></span>  
 <span data-ttu-id="88121-144">Le code XML suivant montre comment configurer l’URI d’audience acceptable pour une application.</span><span class="sxs-lookup"><span data-stu-id="88121-144">The following XML shows how to configure the acceptable audience URIs for an application.</span></span> <span data-ttu-id="88121-145">Cet exemple configure un URI unique.</span><span class="sxs-lookup"><span data-stu-id="88121-145">This example configures a single URI.</span></span> <span data-ttu-id="88121-146">Jetons de portée pour cet URI seront acceptés, toutes les autres sont rejetées.</span><span class="sxs-lookup"><span data-stu-id="88121-146">Tokens scoped for this URI will be accepted, all others will be rejected.</span></span>  
  
```xml  
<audienceUris>  
  <add value="http://localhost:19851/"/>  
</audienceUris>  
```
