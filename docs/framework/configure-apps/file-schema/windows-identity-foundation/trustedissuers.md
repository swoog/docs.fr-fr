---
title: <trustedIssuers>
ms.date: 03/30/2017
ms.assetid: d818c917-07b4-40db-9801-8676561859fd
author: BrucePerlerMS
ms.openlocfilehash: cebfc2f3598f32f233db6039dfe82076d2ffce46
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59221702"
---
# <a name="trustedissuers"></a><span data-ttu-id="b6bbf-101">\<trustedIssuers></span><span class="sxs-lookup"><span data-stu-id="b6bbf-101">\<trustedIssuers></span></span>
<span data-ttu-id="b6bbf-102">Configure la liste des certificats d’émetteurs approuvés utilisés par le Registre des noms d’émetteurs basé sur la configuration (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).</span><span class="sxs-lookup"><span data-stu-id="b6bbf-102">Configures the list of trusted issuer certificates used by the configuration-based issuer name registry (<xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>).</span></span>  
  
 <span data-ttu-id="b6bbf-103">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="b6bbf-103">\<system.identityModel></span></span>  
<span data-ttu-id="b6bbf-104">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="b6bbf-104">\<identityConfiguration></span></span>  
<span data-ttu-id="b6bbf-105">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="b6bbf-105">\<securityTokenHandlers></span></span>  
<span data-ttu-id="b6bbf-106">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="b6bbf-106">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="b6bbf-107">\<issuerNameRegistry></span><span class="sxs-lookup"><span data-stu-id="b6bbf-107">\<issuerNameRegistry></span></span>  
<span data-ttu-id="b6bbf-108">\<trustedIssuers></span><span class="sxs-lookup"><span data-stu-id="b6bbf-108">\<trustedIssuers></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6bbf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6bbf-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerNameRegistry>  
          <trustedIssuers>  
            <add thumbprint=xs:string name=xs:string>  
            <clear>  
            <remove thumbprint=xs:string>  
          </trustedIssuers>  
        </issuerNameRegistry>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b6bbf-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b6bbf-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b6bbf-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b6bbf-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b6bbf-112">Attributes</span></span>  
 <span data-ttu-id="b6bbf-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-113">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b6bbf-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6bbf-114">Child Elements</span></span>  
  
|<span data-ttu-id="b6bbf-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b6bbf-115">Element</span></span>|<span data-ttu-id="b6bbf-116">Description</span><span class="sxs-lookup"><span data-stu-id="b6bbf-116">Description</span></span>|  
|-------------|-----------------|  
|`<add thumbprint=xs:string name=xs:string>`|<span data-ttu-id="b6bbf-117">Ajoute un certificat à la collection des émetteurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-117">Adds a certificate to the collection of trusted issuers.</span></span> <span data-ttu-id="b6bbf-118">Le certificat est spécifié avec la `thumbprint` attribut.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-118">The certificate is specified with the `thumbprint` attribute.</span></span> <span data-ttu-id="b6bbf-119">Cet attribut est obligatoire et doit contenir le formulaire ASN.1 codé de l’empreinte du certificat.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-119">This attribute is required and should contain the ASN.1 encoded form of the certificate thumbprint.</span></span> <span data-ttu-id="b6bbf-120">Le `name` attribut est facultatif et peut être utilisé pour spécifier un nom convivial pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-120">The `name` attribute is optional and can be used to specify a friendly name for the certificate.</span></span>|  
|`<clear>`|<span data-ttu-id="b6bbf-121">Efface tous les certificats à partir de la collection des émetteurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-121">Clears all certificates from the collection of trusted issuers.</span></span>|  
|`<remove thumbprint=xs:string>`|<span data-ttu-id="b6bbf-122">Supprime un certificat à partir de la collection des émetteurs approuvés.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-122">Removes a certificate from the collection of trusted issuers.</span></span> <span data-ttu-id="b6bbf-123">Le certificat est spécifié avec la `thumbprint` attribut.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-123">The certificate is specified with the `thumbprint` attribute.</span></span> <span data-ttu-id="b6bbf-124">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-124">This attribute is required.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b6bbf-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b6bbf-125">Parent Elements</span></span>  
  
|<span data-ttu-id="b6bbf-126">Élément</span><span class="sxs-lookup"><span data-stu-id="b6bbf-126">Element</span></span>|<span data-ttu-id="b6bbf-127">Description</span><span class="sxs-lookup"><span data-stu-id="b6bbf-127">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b6bbf-128">\<issuerNameRegistry></span><span class="sxs-lookup"><span data-stu-id="b6bbf-128">\<issuerNameRegistry></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/issuernameregistry.md)|<span data-ttu-id="b6bbf-129">Configure le Registre des noms d’émetteur.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-129">Configures the issuer name registry.</span></span> <span data-ttu-id="b6bbf-130">**Important :**  Le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe pour le `<trustedIssuers>` élément soit valide.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-130">**Important:**  The `type` attribute of the `<issuerNameRegistry>` element must reference the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class for the `<trustedIssuers>` element to be valid.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b6bbf-131">Notes</span><span class="sxs-lookup"><span data-stu-id="b6bbf-131">Remarks</span></span>  
 <span data-ttu-id="b6bbf-132">Windows Identity Foundation (WIF) fournit une implémentation unique de la <xref:System.IdentityModel.Tokens.IssuerNameRegistry> classe dès le départ, le <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-132">Windows Identity Foundation (WIF) provides a single implementation of the <xref:System.IdentityModel.Tokens.IssuerNameRegistry> class out of the box, the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class.</span></span> <span data-ttu-id="b6bbf-133">Le Registre des noms configuration émetteur gère une liste d’émetteurs approuvés qui est chargée à partir de la configuration.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-133">The configuration issuer name registry maintains a list of trusted issuers that is loaded from configuration.</span></span> <span data-ttu-id="b6bbf-134">La liste associe chaque nom de l’émetteur du certificat X.509 qui est nécessaire pour vérifier la signature des jetons produits par l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-134">The list associates each issuer name with the X.509 certificate that is needed to verify the signature of tokens produced by the issuer.</span></span> <span data-ttu-id="b6bbf-135">La liste des certificats d’émetteurs approuvés est spécifiée sous la `<trustedIssuers>` élément.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-135">The list of trusted issuer certificates is specified under the `<trustedIssuers>` element.</span></span> <span data-ttu-id="b6bbf-136">Chaque élément dans la liste associe un nom de l’émetteur mnémonique avec le certificat X.509 qui est nécessaire pour vérifier la signature des jetons produits par cet émetteur.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-136">Each element in the list associates a mnemonic issuer name with the X.509 certificate that is needed to verify the signature of tokens produced by that issuer.</span></span> <span data-ttu-id="b6bbf-137">Certificats de confiance sont spécifiés à l’aide de l’ASN.1 forme codée de l’empreinte de certificat et sont ajoutés de la collection à l’aide de `<add>` élément.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-137">Trusted certificates are specified using the ASN.1 encoded form of the certificate thumbprint and are added the collection by using `<add>` element.</span></span> <span data-ttu-id="b6bbf-138">Vous pouvez effacer ou supprimer des émetteurs (certificats) dans la liste à l’aide de la `<clear>` et `<remove>` éléments.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-138">You can clear or remove issuers (certificates) from the list by using the `<clear>` and `<remove>` elements.</span></span>  
  
 <span data-ttu-id="b6bbf-139">Le `type` attribut de la `<issuerNameRegistry>` élément doit faire référence à la <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> classe pour le `<trustedIssuers>` élément soit valide.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-139">The `type` attribute of the `<issuerNameRegistry>` element must reference the <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry> class for the `<trustedIssuers>` element to be valid.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6bbf-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6bbf-140">Example</span></span>  
 <span data-ttu-id="b6bbf-141">Le code XML suivant montre comment spécifier l’émetteur de la configuration en fonction du Registre des noms.</span><span class="sxs-lookup"><span data-stu-id="b6bbf-141">The following XML shows how to specify the configuration based issuer name registry.</span></span>  
  
```xml  
<issuerNameRegistry type="System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry, System.IdentityModel, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">  
  <trustedIssuers>  
    <add thumbprint="9B74CB2F32 … B1DC01EF40D0" name="LocalSTS" />  
  </trustedIssuers>  
</issuerNameRegistry>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b6bbf-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6bbf-142">See also</span></span>

- <xref:System.IdentityModel.Tokens.ConfigurationBasedIssuerNameRegistry>
- <xref:System.IdentityModel.Tokens.IssuerNameRegistry>
