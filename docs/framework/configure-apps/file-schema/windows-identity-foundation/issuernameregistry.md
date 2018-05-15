---
title: '&lt;issuerNameRegistry&gt;'
ms.date: 03/30/2017
ms.assetid: 58b39d12-c953-40c4-88af-d7eb3343ca28
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: b695cc6d66e5b9e45bb6a5fd22d594bc22ea3cba
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltissuernameregistrygt"></a><span data-ttu-id="f9228-102">&lt;issuerNameRegistry&gt;</span><span class="sxs-lookup"><span data-stu-id="f9228-102">&lt;issuerNameRegistry&gt;</span></span>
<span data-ttu-id="f9228-103">Configure le Registre de nom de l’émetteur qui est utilisé par les gestionnaires de la collection du Gestionnaire de jetons.</span><span class="sxs-lookup"><span data-stu-id="f9228-103">Configures the issuer name registry that is used by handlers in the token handler collection.</span></span>  
  
 <span data-ttu-id="f9228-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="f9228-104">\<system.identityModel></span></span>  
<span data-ttu-id="f9228-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f9228-105">\<identityConfiguration></span></span>  
<span data-ttu-id="f9228-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="f9228-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="f9228-107">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f9228-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="f9228-108">\<issuerNameRegistry ></span><span class="sxs-lookup"><span data-stu-id="f9228-108">\<issuerNameRegistry></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9228-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9228-109">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f9228-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f9228-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f9228-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f9228-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f9228-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="f9228-112">Attributes</span></span>  
  
|<span data-ttu-id="f9228-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="f9228-113">Attribute</span></span>|<span data-ttu-id="f9228-114">Description</span><span class="sxs-lookup"><span data-stu-id="f9228-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f9228-115">type</span><span class="sxs-lookup"><span data-stu-id="f9228-115">type</span></span>|<span data-ttu-id="f9228-116">Un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="f9228-116">A type that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="f9228-117">Pour plus d’informations sur la façon de spécifier une personnalisée `type`, voir [références de Type personnalisé].</span><span class="sxs-lookup"><span data-stu-id="f9228-117">For more information about how to specify a custom `type`, see [Custom Type References].</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f9228-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f9228-118">Child Elements</span></span>  
  
|<span data-ttu-id="f9228-119">Élément</span><span class="sxs-lookup"><span data-stu-id="f9228-119">Element</span></span>|<span data-ttu-id="f9228-120">Description</span><span class="sxs-lookup"><span data-stu-id="f9228-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f9228-121">\<trustedIssuers ></span><span class="sxs-lookup"><span data-stu-id="f9228-121">\<trustedIssuers></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md)|<span data-ttu-id="f9228-122">Lorsque le `type` attribut spécifie le Registre des noms en fonction de configuration de l’émetteur (le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe), la [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9228-122">When the `type` attribute specifies the configuration-based issuer name registry (the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class), the [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element must be specified.</span></span> <span data-ttu-id="f9228-123">Le [ \<trustedIssuers >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) élément peut prendre `<add>`, `<clear>`, ou `<remove>` éléments comme des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="f9228-123">The [\<trustedIssuers>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/trustedissuers.md) element can take `<add>`, `<clear>`, or `<remove>` elements as child elements.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f9228-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f9228-124">Parent Elements</span></span>  
  
|<span data-ttu-id="f9228-125">Élément</span><span class="sxs-lookup"><span data-stu-id="f9228-125">Element</span></span>|<span data-ttu-id="f9228-126">Description</span><span class="sxs-lookup"><span data-stu-id="f9228-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f9228-127">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="f9228-127">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="f9228-128">Fournit des gestionnaires de jetons de configuration pour une collection de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f9228-128">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f9228-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f9228-129">Remarks</span></span>  
 <span data-ttu-id="f9228-130">Tous les jetons d’émetteurs sont validés à l’aide d’un Registre de nom de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="f9228-130">All issuer tokens are validated using an issuer name registry.</span></span> <span data-ttu-id="f9228-131">Il s’agit d’un objet qui dérive de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="f9228-131">This is an object that derives from the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class.</span></span> <span data-ttu-id="f9228-132">Le Registre de nom d’émetteur est utilisé pour associer un nom mnémonique pour le matériel de chiffrement qui est nécessaire pour vérifier les signatures des jetons de produits par l’émetteur correspondant.</span><span class="sxs-lookup"><span data-stu-id="f9228-132">The issuer name registry is used to associate a mnemonic name to the cryptographic material that is needed to verify the signatures of tokens produced by the corresponding issuer.</span></span> <span data-ttu-id="f9228-133">Le Registre de nom d’émetteur gère une liste d’émetteurs approuvés par l’application de confiance de partie de confiance.</span><span class="sxs-lookup"><span data-stu-id="f9228-133">The issuer name registry maintains a list of issuers that are trusted by the relying party (RP) application.</span></span> <span data-ttu-id="f9228-134">Le type du Registre de nom d’émetteur est spécifié à l’aide de la `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="f9228-134">The type of the issuer name registry is specified using the `type` attribute.</span></span> <span data-ttu-id="f9228-135">Le `<issuerNameRegistry>` élément peut avoir un ou plusieurs des éléments enfants qui fournissent la configuration pour le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9228-135">The `<issuerNameRegistry>` element can have one or more child elements that provide configuration for the specified type.</span></span> <span data-ttu-id="f9228-136">Vous fournissez la logique qui traite de ces éléments enfants en substituant la <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="f9228-136">You provide the logic that processes these child elements by overriding the <xref:System.IdentityModel.Tokens.IssuerNameRegistry.LoadCustomConfiguration%2A> method.</span></span>  
  
 <span data-ttu-id="f9228-137">WIF fournit un émetteur unique type de Registre de nom utilisable, la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="f9228-137">WIF provides a single issuer name registry type out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="f9228-138">Cette classe utilise un jeu de certificats d’émetteurs approuvés qui sont spécifiés dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="f9228-138">This class uses a set of trusted issuer certificates that are specified in configuration.</span></span> <span data-ttu-id="f9228-139">Il requiert un élément de configuration enfant, `<trustedIssuers>`, sous lequel la collection de certificats d’émetteurs approuvés est configurée.</span><span class="sxs-lookup"><span data-stu-id="f9228-139">It requires a child configuration element, `<trustedIssuers>`, under which the collection of trusted issuer certificates is configured.</span></span> <span data-ttu-id="f9228-140">Approuvé les certificats sont spécifiés à l’aide de la ASN.1 forme encodée de l’empreinte numérique du certificat et est ajouté ou supprimé de la collection à l’aide de `<add>`, `<clear>`, ou `<remove>` éléments.</span><span class="sxs-lookup"><span data-stu-id="f9228-140">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added or removed from the collection by using `<add>`, `<clear>`, or `<remove>` elements.</span></span>  
  
 <span data-ttu-id="f9228-141">Le `<issuerNameRegistry>` élément est représenté par la <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> classe.</span><span class="sxs-lookup"><span data-stu-id="f9228-141">The `<issuerNameRegistry>` element is represented by the <xref:System.IdentityModel.Configuration.IssuerNameRegistryElement> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f9228-142">En spécifiant le `<issuerNameRegistry>` élément comme un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) l’élément a été déconseillée, mais est toujours prise en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="f9228-142">Specifying the `<issuerNameRegistry>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="f9228-143">Paramètres de la `<securityTokenHandlerConfiguration>` élément remplacent celles sur le `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="f9228-143">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f9228-144">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9228-144">Example</span></span>  
 <span data-ttu-id="f9228-145">Le code XML suivant montre comment spécifier l’émetteur de la configuration en fonction du Registre des noms.</span><span class="sxs-lookup"><span data-stu-id="f9228-145">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB … 1EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="f9228-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9228-146">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.IssuerNameRegistry>  
 <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
