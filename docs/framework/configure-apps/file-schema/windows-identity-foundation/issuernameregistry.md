---
title: '&lt;issuerNameRegistry&gt;'
ms.date: 03/30/2017
ms.assetid: 58b39d12-c953-40c4-88af-d7eb3343ca28
author: BrucePerlerMS
ms.openlocfilehash: de3ceb5d84d17307c69e9155834a0a584e6920a1
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48845422"
---
# <a name="ltissuernameregistrygt"></a><span data-ttu-id="a1460-102">&lt;issuerNameRegistry&gt;</span><span class="sxs-lookup"><span data-stu-id="a1460-102">&lt;issuerNameRegistry&gt;</span></span>
<span data-ttu-id="a1460-103">Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="a1460-103">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span>  
  
 <span data-ttu-id="a1460-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="a1460-104">\<system.identityModel></span></span>  
<span data-ttu-id="a1460-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a1460-105">\<identityConfiguration></span></span>  
<span data-ttu-id="a1460-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="a1460-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="a1460-107">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a1460-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="a1460-108">\<issuerNameRegistry ></span><span class="sxs-lookup"><span data-stu-id="a1460-108">\<issuerNameRegistry></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1460-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1460-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry type=xs:string>  
          <optionalCustomConfigurationElements />  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a1460-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a1460-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a1460-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a1460-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a1460-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a1460-112">Attributes</span></span>  
  
|<span data-ttu-id="a1460-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a1460-113">Attribute</span></span>|<span data-ttu-id="a1460-114">Description</span><span class="sxs-lookup"><span data-stu-id="a1460-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a1460-115">type</span><span class="sxs-lookup"><span data-stu-id="a1460-115">type</span></span>|<span data-ttu-id="a1460-116">Un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="a1460-116">A type that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="a1460-117">Pour plus d’informations sur la façon de spécifier une personnalisée `type`, consultez [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="a1460-117">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a1460-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a1460-118">Child Elements</span></span>  
  
|<span data-ttu-id="a1460-119">Élément</span><span class="sxs-lookup"><span data-stu-id="a1460-119">Element</span></span>|<span data-ttu-id="a1460-120">Description</span><span class="sxs-lookup"><span data-stu-id="a1460-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1460-121">\<trustedIssuers ></span><span class="sxs-lookup"><span data-stu-id="a1460-121">\<trustedIssuers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)|<span data-ttu-id="a1460-122">Lorsque le `type` attribut spécifie le Registre des noms d’émetteurs basé sur la configuration (le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe), la [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="a1460-122">When the `type` attribute specifies the configuration-based issuer name registry (the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class), the [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element must be specified.</span></span> <span data-ttu-id="a1460-123">Le [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément peut prendre `<add>`, `<clear>`, ou `<remove>` éléments comme des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="a1460-123">The [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element can take `<add>`, `<clear>`, or `<remove>` elements as child elements.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a1460-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a1460-124">Parent Elements</span></span>  
  
|<span data-ttu-id="a1460-125">Élément</span><span class="sxs-lookup"><span data-stu-id="a1460-125">Element</span></span>|<span data-ttu-id="a1460-126">Description</span><span class="sxs-lookup"><span data-stu-id="a1460-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a1460-127">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a1460-127">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="a1460-128">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="a1460-128">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a1460-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a1460-129">Remarks</span></span>  
 <span data-ttu-id="a1460-130">Tous les jetons d’émetteur sont validés à l’aide d’un registre des noms d’émetteur.</span><span class="sxs-lookup"><span data-stu-id="a1460-130">All issuer tokens are validated using an issuer name registry.</span></span> <span data-ttu-id="a1460-131">Il s’agit d’un objet qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="a1460-131">This is an object that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="a1460-132">Le Registre des noms d’émetteur est utilisé pour associer un nom mnémonique avec le matériel de chiffrement qui est nécessaire pour vérifier les signatures des jetons produits par l’émetteur correspondant.</span><span class="sxs-lookup"><span data-stu-id="a1460-132">The issuer name registry is used to associate a mnemonic name to the cryptographic material that is needed to verify the signatures of tokens produced by the corresponding issuer.</span></span> <span data-ttu-id="a1460-133">Le Registre des noms d’émetteur gère une liste d’émetteurs approuvés par l’application de confiance (RP).</span><span class="sxs-lookup"><span data-stu-id="a1460-133">The issuer name registry maintains a list of issuers that are trusted by the relying party (RP) application.</span></span> <span data-ttu-id="a1460-134">Le type du Registre de nom de l’émetteur est spécifié à l’aide de la `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="a1460-134">The type of the issuer name registry is specified using the `type` attribute.</span></span> <span data-ttu-id="a1460-135">Le `<issuerNameRegistry>` élément peut avoir un ou plusieurs éléments enfants qui fournissent la configuration pour le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="a1460-135">The `<issuerNameRegistry>` element can have one or more child elements that provide configuration for the specified type.</span></span> <span data-ttu-id="a1460-136">Vous fournissez la logique qui traite ces éléments enfants en substituant le <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="a1460-136">You provide the logic that processes these child elements by overriding the <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> method.</span></span>  
  
 <span data-ttu-id="a1460-137">WIF fournit un émetteur unique type de Registre de nom dès le départ, le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="a1460-137">WIF provides a single issuer name registry type out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="a1460-138">Cette classe utilise un ensemble de certificats d’émetteurs approuvés qui sont spécifiés dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="a1460-138">This class uses a set of trusted issuer certificates that are specified in configuration.</span></span> <span data-ttu-id="a1460-139">Il requiert un élément de configuration enfant, `<trustedIssuers>`, sous lequel la collection de certificats d’émetteurs approuvés est configurée.</span><span class="sxs-lookup"><span data-stu-id="a1460-139">It requires a child configuration element, `<trustedIssuers>`, under which the collection of trusted issuer certificates is configured.</span></span> <span data-ttu-id="a1460-140">Approuvé de certificats sont spécifiés à l’aide de l’ASN.1 forme codée de l’empreinte de certificat et est ajouté ou supprimé de la collection à l’aide de `<add>`, `<clear>`, ou `<remove>` éléments.</span><span class="sxs-lookup"><span data-stu-id="a1460-140">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added or removed from the collection by using `<add>`, `<clear>`, or `<remove>` elements.</span></span>  
  
 <span data-ttu-id="a1460-141">Le `<issuerNameRegistry>` élément est représenté par la <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> classe.</span><span class="sxs-lookup"><span data-stu-id="a1460-141">The `<issuerNameRegistry>` element is represented by the <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a1460-142">En spécifiant le `<issuerNameRegistry>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a1460-142">Specifying the `<issuerNameRegistry>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="a1460-143">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="a1460-143">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1460-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="a1460-144">Example</span></span>  
 <span data-ttu-id="a1460-145">Le code XML suivant montre comment spécifier l’émetteur de la configuration en fonction du Registre des noms.</span><span class="sxs-lookup"><span data-stu-id="a1460-145">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB … 1EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a1460-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1460-146">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.IssuerNameRegistry>  
 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
