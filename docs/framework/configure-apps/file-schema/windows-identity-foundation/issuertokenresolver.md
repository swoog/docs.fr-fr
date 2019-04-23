---
title: <issuerTokenResolver>
ms.date: 03/30/2017
ms.assetid: f74392f6-3f5b-4880-bd8a-3a9130d31e65
author: BrucePerlerMS
ms.openlocfilehash: 08082d2e6647f07f33df72ab79dac00c15a1cd1b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200816"
---
# <a name="issuertokenresolver"></a><span data-ttu-id="5bc1e-101">\<issuerTokenResolver></span><span class="sxs-lookup"><span data-stu-id="5bc1e-101">\<issuerTokenResolver></span></span>
<span data-ttu-id="5bc1e-102">Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-102">Registers the issuer token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="5bc1e-103">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-103">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span>  
  
 <span data-ttu-id="5bc1e-104">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="5bc1e-104">\<system.identityModel></span></span>  
<span data-ttu-id="5bc1e-105">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="5bc1e-105">\<identityConfiguration></span></span>  
<span data-ttu-id="5bc1e-106">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="5bc1e-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="5bc1e-107">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="5bc1e-107">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="5bc1e-108">\<issuerTokenResolver></span><span class="sxs-lookup"><span data-stu-id="5bc1e-108">\<issuerTokenResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bc1e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc1e-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerTokenResolver type=xs:string>  
        </issuerTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5bc1e-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5bc1e-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5bc1e-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5bc1e-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="5bc1e-112">Attributes</span></span>  
  
|<span data-ttu-id="5bc1e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="5bc1e-113">Attribute</span></span>|<span data-ttu-id="5bc1e-114">Description</span><span class="sxs-lookup"><span data-stu-id="5bc1e-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5bc1e-115">type</span><span class="sxs-lookup"><span data-stu-id="5bc1e-115">type</span></span>|<span data-ttu-id="5bc1e-116">Spécifie le type du programme de résolution de jeton de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-116">Specifies the type of the issuer token resolver.</span></span> <span data-ttu-id="5bc1e-117">Doit être le <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe ou un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-117">Must be either the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class or a type that derives from the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class.</span></span> <span data-ttu-id="5bc1e-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-118">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5bc1e-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5bc1e-119">Child Elements</span></span>  
 <span data-ttu-id="5bc1e-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5bc1e-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5bc1e-121">Parent Elements</span></span>  
  
|<span data-ttu-id="5bc1e-122">Élément</span><span class="sxs-lookup"><span data-stu-id="5bc1e-122">Element</span></span>|<span data-ttu-id="5bc1e-123">Description</span><span class="sxs-lookup"><span data-stu-id="5bc1e-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5bc1e-124">\<securityTokenHandlerConfiguration></span><span class="sxs-lookup"><span data-stu-id="5bc1e-124">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="5bc1e-125">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-125">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5bc1e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5bc1e-126">Remarks</span></span>  
 <span data-ttu-id="5bc1e-127">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-127">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span> <span data-ttu-id="5bc1e-128">Il est utilisé pour récupérer le matériel de chiffrement qui est utilisé pour la vérification de la signature.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-128">It is used to retrieve the cryptographic material that is used for checking the signature.</span></span> <span data-ttu-id="5bc1e-129">Vous devez spécifier le `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-129">You must specify the `type` attribute.</span></span> <span data-ttu-id="5bc1e-130">Le type spécifié peut être soit <xref:System.IdentityModel.Tokens.IssuerTokenResolver> ou un type personnalisé qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-130">The type specified can be either <xref:System.IdentityModel.Tokens.IssuerTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class.</span></span>  
  
 <span data-ttu-id="5bc1e-131">Certains gestionnaires de jetons permettent de spécifier les paramètres de résolution de jeton de l’émetteur dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-131">Some token handlers allow you to specify issuer token resolver settings in configuration.</span></span> <span data-ttu-id="5bc1e-132">Les paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-132">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5bc1e-133">En spécifiant le `<issuerTokenResolver>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-133">Specifying the `<issuerTokenResolver>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="5bc1e-134">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-134">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bc1e-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="5bc1e-135">Example</span></span>  
 <span data-ttu-id="5bc1e-136">Le code XML suivant montre la configuration pour un résolveur de jeton de l’émetteur est basé sur une classe personnalisée qui dérive de <xref:System.IdentityModel.Tokens.IssuerTokenResolver>.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-136">The following XML shows configuration for an issuer token resolver that is based on a custom class that derives from <xref:System.IdentityModel.Tokens.IssuerTokenResolver>.</span></span> <span data-ttu-id="5bc1e-137">Le programme de résolution de jeton gère un dictionnaire de paires clé-public qui est initialisé à partir d’un élément de configuration personnalisé (`<AddAudienceKeyPair>`) définie pour la classe.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-137">The token resolver maintains a dictionary of audience-key pairs that is initialized from a custom configuration element (`<AddAudienceKeyPair>`) defined for the class.</span></span> <span data-ttu-id="5bc1e-138">La classe substitue la <xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A> méthode pour traiter cet élément.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-138">The class overrides the <xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A> method to process this element.</span></span> <span data-ttu-id="5bc1e-139">Le remplacement est illustré dans l’exemple suivant ; Toutefois, les méthodes qu’elle appelle ne sont pas affichés par souci de concision.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-139">The override is shown in the following example; however, the methods it calls are not shown for brevity.</span></span> <span data-ttu-id="5bc1e-140">Pour obtenir un exemple complet, consultez la `CustomToken` exemple.</span><span class="sxs-lookup"><span data-stu-id="5bc1e-140">For the complete example, see the `CustomToken` sample.</span></span>  
  
```xml  
<issuerTokenResolver type="SimpleWebToken.CustomIssuerTokenResolver, SimpleWebToken">  
  <AddAudienceKeyPair  symmetricKey="wAVkldQiFypTQ+kdNdGWCYCHRcee8XmXxOvgmak8vSY=" audience="http://localhost:19851/" />  
</issuerTokenResolver>  
```  
  
## <a name="example"></a><span data-ttu-id="5bc1e-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="5bc1e-141">Example</span></span>  
  
```  
public override void LoadCustomConfiguration(System.Xml.XmlNodeList nodelist)  
{  
    foreach (XmlNode node in nodelist)  
    {  
        XmlDictionaryReader rdr = XmlDictionaryReader.CreateDictionaryReader(new XmlTextReader(new StringReader(node.OuterXml)));  
        rdr.MoveToContent();  
  
        string symmetricKey = rdr.GetAttribute("symmetricKey");  
        string audience = rdr.GetAttribute("audience");  
  
        this.AddAudienceKeyPair(audience, symmetricKey);  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="5bc1e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bc1e-142">See also</span></span>

- <xref:System.IdentityModel.Tokens.IssuerTokenResolver>
