---
title: <add>
ms.date: 03/30/2017
ms.assetid: 4712a888-f154-4395-8887-ef14a88a6497
author: BrucePerlerMS
ms.openlocfilehash: 34643d10ef1ed2e87152e5013634e62859e0594e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791766"
---
# <a name="add"></a><span data-ttu-id="d1a09-101">\<add></span><span class="sxs-lookup"><span data-stu-id="d1a09-101">\<add></span></span>
<span data-ttu-id="d1a09-102">Ajoute le Gestionnaire de jetons de sécurité spécifié à la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="d1a09-102">Adds the specified security token handler to the token handler collection.</span></span>  
  
 <span data-ttu-id="d1a09-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="d1a09-103">\<system.identityModel></span></span>  
<span data-ttu-id="d1a09-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="d1a09-104">\<identityConfiguration></span></span>  
<span data-ttu-id="d1a09-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="d1a09-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="d1a09-106">\<add></span><span class="sxs-lookup"><span data-stu-id="d1a09-106">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1a09-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1a09-107">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type=xs:string>  
        <optionalConfigurationElement>  
        </optionalConfigurationElement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1a09-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d1a09-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d1a09-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d1a09-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1a09-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d1a09-110">Attributes</span></span>  
  
|<span data-ttu-id="d1a09-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="d1a09-111">Attribute</span></span>|<span data-ttu-id="d1a09-112">Description</span><span class="sxs-lookup"><span data-stu-id="d1a09-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="d1a09-113">type</span><span class="sxs-lookup"><span data-stu-id="d1a09-113">type</span></span>|<span data-ttu-id="d1a09-114">Le nom de type CLR de gestionnaire de jetons à ajouter.</span><span class="sxs-lookup"><span data-stu-id="d1a09-114">The CLR type name of the token handler to be added.</span></span> <span data-ttu-id="d1a09-115">Pour plus d’informations sur la façon de spécifier le `type` d’attribut, consultez [références de Type personnalisé](https://docs.microsoft.com/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).</span><span class="sxs-lookup"><span data-stu-id="d1a09-115">For more information about how to specify the `type` attribute, see [Custom Type References](https://docs.microsoft.com/previous-versions/windows-identity-foundation/gg638728(v=msdn.10)#custom-type-references).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d1a09-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d1a09-116">Child Elements</span></span>  
  
|<span data-ttu-id="d1a09-117">Élément</span><span class="sxs-lookup"><span data-stu-id="d1a09-117">Element</span></span>|<span data-ttu-id="d1a09-118">Description</span><span class="sxs-lookup"><span data-stu-id="d1a09-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1a09-119">\<samlSecurityTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="d1a09-119">\<samlSecurityTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/samlsecuritytokenrequirement.md)|<span data-ttu-id="d1a09-120">Fournit une configuration pour le <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> (classe), la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe ou une classe dérivée d’un de ces classes.</span><span class="sxs-lookup"><span data-stu-id="d1a09-120">Provides configuration for the <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler> class, the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class, or a derived class of either of these classes.</span></span>|  
|[<span data-ttu-id="d1a09-121">\<sessionTokenRequirement></span><span class="sxs-lookup"><span data-stu-id="d1a09-121">\<sessionTokenRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/sessiontokenrequirement.md)|<span data-ttu-id="d1a09-122">Fournit une configuration pour la <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="d1a09-122">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>|  
|[<span data-ttu-id="d1a09-123">\<userNameSecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="d1a09-123">\<userNameSecurityTokenHandlerRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/usernamesecuritytokenhandlerrequirement.md)|<span data-ttu-id="d1a09-124">Fournit une configuration pour la <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="d1a09-124">Provides configuration for the <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler> class or derived classes.</span></span>|  
|[<span data-ttu-id="d1a09-125">\<x509SecurityTokenHandlerRequirement></span><span class="sxs-lookup"><span data-stu-id="d1a09-125">\<x509SecurityTokenHandlerRequirement></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/x509securitytokenhandlerrequirement.md)|<span data-ttu-id="d1a09-126">Fournit une configuration facultative pour le <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> classe ou les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="d1a09-126">Provides optional configuration for the <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler> class or derived classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d1a09-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d1a09-127">Parent Elements</span></span>  
  
|<span data-ttu-id="d1a09-128">Élément</span><span class="sxs-lookup"><span data-stu-id="d1a09-128">Element</span></span>|<span data-ttu-id="d1a09-129">Description</span><span class="sxs-lookup"><span data-stu-id="d1a09-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1a09-130">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="d1a09-130">\<securityTokenHandlers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlers.md)|<span data-ttu-id="d1a09-131">Spécifie une collection de gestionnaires de jetons de sécurité qui sont inscrits avec le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d1a09-131">Specifies a collection of security token handlers that are registered with the endpoint.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1a09-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d1a09-132">Remarks</span></span>  
 <span data-ttu-id="d1a09-133">Le `<add>` élément peut prendre un seul élément enfant qui spécifie la configuration pour le Gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="d1a09-133">The `<add>` element can take a single child element that specifies the configuration for the token handler.</span></span> <span data-ttu-id="d1a09-134">Cela dépend de la classe de gestionnaire référencée ou non par le biais du `type` attribut de la `<add>` élément prend en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d1a09-134">This is dependent on whether the handler class referenced through the `type` attribute of the `<add>` element provides support for this feature.</span></span> <span data-ttu-id="d1a09-135">Les classes de gestionnaire de jetons qui fournissent cette fonctionnalité doivent exposer un constructeur qui accepte un <xref:System.Xml.XmlElement> objet.</span><span class="sxs-lookup"><span data-stu-id="d1a09-135">Token handler classes that provide this feature must expose a constructor that takes an <xref:System.Xml.XmlElement> object.</span></span>  
  
```  
public class CustomTokenHandler : Microsoft.IdentityModel.Tokens.SecurityTokenHandler  
{  
    public CustomTokenHandler( XmlElement customConfig )  
    {  
    }  
}  
```  
  
 <span data-ttu-id="d1a09-136">Plusieurs des classes de gestionnaire de jetons de sécurité intégrés ne fournissent pas cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d1a09-136">Several of the built-in security token handler classes do provide this functionality.</span></span> <span data-ttu-id="d1a09-137">Ces classes sont <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, et <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>.</span><span class="sxs-lookup"><span data-stu-id="d1a09-137">These classes are <xref:System.IdentityModel.Tokens.SamlSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, <xref:System.IdentityModel.Services.Tokens.MembershipUserNameSecurityTokenHandler>, <xref:System.IdentityModel.Tokens.X509SecurityTokenHandler>, and <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler>.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d1a09-138">La collection de gestionnaires de jetons ne peut contenir qu’un seul gestionnaire de tout type donné.</span><span class="sxs-lookup"><span data-stu-id="d1a09-138">The token handler collection can only contain a single handler of any given type.</span></span> <span data-ttu-id="d1a09-139">Cela signifie, par exemple, que si vous souhaitez ajouter un gestionnaire qui est dérivé de la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> classe à la collection, vous devez d’abord supprimer la <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, qui n’est présent par défaut, à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="d1a09-139">This means, for example, that if you want to add a handler that is derived from the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler> class to the collection, you must first remove the <xref:System.IdentityModel.Tokens.Saml2SecurityTokenHandler>, which is present by default, from the collection.</span></span> <span data-ttu-id="d1a09-140">Vous pouvez utiliser la [ \<Supprimer >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md) élément à supprimer un gestionnaire unique à partir de la collection ou utilisez le [ \<Effacer >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md) élément à supprimer tous les gestionnaires de la collection.</span><span class="sxs-lookup"><span data-stu-id="d1a09-140">You can use the [\<remove>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/remove.md) element to remove a single handler from the collection or use the [\<clear>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/clear.md) element to remove all handlers from the collection.</span></span>  
  
 <span data-ttu-id="d1a09-141">Les paramètres spécifiés sur un gestionnaire de remplacent les paramètres équivalents spécifiés sur la collection de gestionnaires de jetons sous le [ \<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) élément et ceux spécifiés au niveau du service sous le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément.</span><span class="sxs-lookup"><span data-stu-id="d1a09-141">Settings specified on a handler override equivalent settings specified on the token handler collection under the [\<securityTokenHandlerConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md) element and those specified at the service-level under the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1a09-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="d1a09-142">Example</span></span>  
 <span data-ttu-id="d1a09-143">Le code XML suivant illustre l’utilisation de la `<add>` et `<remove>` éléments pour remplacer le Gestionnaire de jetons de session par défaut par un gestionnaire de jetons de session personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d1a09-143">The following XML shows the use of the `<add>` and `<remove>` elements to replace the default session token handler with a custom session token handler.</span></span> <span data-ttu-id="d1a09-144">Le code XML provient de la `ClaimsAwareWebFarm` exemple.</span><span class="sxs-lookup"><span data-stu-id="d1a09-144">The XML is taken from the `ClaimsAwareWebFarm` sample.</span></span>  
  
```xml  
<securityTokenHandlers>  
  <remove type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
  <add type="System.IdentityModel.Services.Tokens.MachineKeySessionSecurityTokenHandler, System.IdentityModel.Services, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
</securityTokenHandlers>  
```
