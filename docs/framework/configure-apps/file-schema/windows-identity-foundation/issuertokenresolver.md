---
title: '&lt;issuerTokenResolver&gt;'
ms.date: 03/30/2017
ms.assetid: f74392f6-3f5b-4880-bd8a-3a9130d31e65
author: BrucePerlerMS
ms.openlocfilehash: eefd18c206b7f013c3a423df424c795583c0dde8
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075243"
---
# <a name="ltissuertokenresolvergt"></a><span data-ttu-id="49356-102">&lt;issuerTokenResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="49356-102">&lt;issuerTokenResolver&gt;</span></span>
<span data-ttu-id="49356-103">Inscrit le résolveur de jeton de l’émetteur qui est utilisé par les gestionnaires dans la collection de gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="49356-103">Registers the issuer token resolver that is used by handlers in the token handler collection.</span></span> <span data-ttu-id="49356-104">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="49356-104">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span>  
  
 <span data-ttu-id="49356-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="49356-105">\<system.identityModel></span></span>  
<span data-ttu-id="49356-106">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="49356-106">\<identityConfiguration></span></span>  
<span data-ttu-id="49356-107">\<securityTokenHandlers></span><span class="sxs-lookup"><span data-stu-id="49356-107">\<securityTokenHandlers></span></span>  
<span data-ttu-id="49356-108">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="49356-108">\<securityTokenHandlerConfiguration></span></span>  
<span data-ttu-id="49356-109">\<issuerTokenResolver ></span><span class="sxs-lookup"><span data-stu-id="49356-109">\<issuerTokenResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49356-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49356-110">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="49356-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="49356-111">Attributes and Elements</span></span>  
 <span data-ttu-id="49356-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="49356-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="49356-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="49356-113">Attributes</span></span>  
  
|<span data-ttu-id="49356-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="49356-114">Attribute</span></span>|<span data-ttu-id="49356-115">Description</span><span class="sxs-lookup"><span data-stu-id="49356-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="49356-116">type</span><span class="sxs-lookup"><span data-stu-id="49356-116">type</span></span>|<span data-ttu-id="49356-117">Spécifie le type du programme de résolution de jeton de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="49356-117">Specifies the type of the issuer token resolver.</span></span> <span data-ttu-id="49356-118">Doit être le <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe ou un type qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="49356-118">Must be either the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class or a type that derives from the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class.</span></span> <span data-ttu-id="49356-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="49356-119">Required.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="49356-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="49356-120">Child Elements</span></span>  
 <span data-ttu-id="49356-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="49356-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="49356-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="49356-122">Parent Elements</span></span>  
  
|<span data-ttu-id="49356-123">Élément</span><span class="sxs-lookup"><span data-stu-id="49356-123">Element</span></span>|<span data-ttu-id="49356-124">Description</span><span class="sxs-lookup"><span data-stu-id="49356-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="49356-125">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="49356-125">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="49356-126">Fournit une configuration pour une collection de sécurité gestionnaires de jetons.</span><span class="sxs-lookup"><span data-stu-id="49356-126">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="49356-127">Notes</span><span class="sxs-lookup"><span data-stu-id="49356-127">Remarks</span></span>  
 <span data-ttu-id="49356-128">Le programme de résolution de jeton de l’émetteur est utilisé pour résoudre le jeton de signature sur les jetons et les messages entrant.</span><span class="sxs-lookup"><span data-stu-id="49356-128">The issuer token resolver is used to resolve the signing token on incoming tokens and messages.</span></span> <span data-ttu-id="49356-129">Il est utilisé pour récupérer le matériel de chiffrement qui est utilisé pour la vérification de la signature.</span><span class="sxs-lookup"><span data-stu-id="49356-129">It is used to retrieve the cryptographic material that is used for checking the signature.</span></span> <span data-ttu-id="49356-130">Vous devez spécifier le `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="49356-130">You must specify the `type` attribute.</span></span> <span data-ttu-id="49356-131">Le type spécifié peut être soit <xref:System.IdentityModel.Tokens.IssuerTokenResolver> ou un type personnalisé qui dérive de la <xref:System.IdentityModel.Tokens.IssuerTokenResolver> classe.</span><span class="sxs-lookup"><span data-stu-id="49356-131">The type specified can be either <xref:System.IdentityModel.Tokens.IssuerTokenResolver> or a custom type that derives from the <xref:System.IdentityModel.Tokens.IssuerTokenResolver> class.</span></span>  
  
 <span data-ttu-id="49356-132">Certains gestionnaires de jetons permettent de spécifier les paramètres de résolution de jeton de l’émetteur dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="49356-132">Some token handlers allow you to specify issuer token resolver settings in configuration.</span></span> <span data-ttu-id="49356-133">Les paramètres sur les gestionnaires de jetons individuels remplacent celles spécifiées sur la collection de gestionnaires de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="49356-133">Settings on individual token handlers override those specified on the security token handler collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="49356-134">En spécifiant le `<issuerTokenResolver>` en tant qu’un élément enfant de le [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) élément a été déconseillé, mais est toujours pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="49356-134">Specifying the `<issuerTokenResolver>` element as a child element of the [\<identityConfiguration>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) element has been deprecated, but is still supported for backward compatibility.</span></span> <span data-ttu-id="49356-135">Paramètres sur le `<securityTokenHandlerConfiguration>` élément remplacent ceux de la `<identityConfiguration>` élément.</span><span class="sxs-lookup"><span data-stu-id="49356-135">Settings on the `<securityTokenHandlerConfiguration>` element override those on the `<identityConfiguration>` element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="49356-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="49356-136">Example</span></span>  
 <span data-ttu-id="49356-137">Le code XML suivant montre la configuration pour un résolveur de jeton de l’émetteur est basé sur une classe personnalisée qui dérive de <xref:System.IdentityModel.Tokens.IssuerTokenResolver>.</span><span class="sxs-lookup"><span data-stu-id="49356-137">The following XML shows configuration for an issuer token resolver that is based on a custom class that derives from <xref:System.IdentityModel.Tokens.IssuerTokenResolver>.</span></span> <span data-ttu-id="49356-138">Le programme de résolution de jeton gère un dictionnaire de paires clé-public qui est initialisé à partir d’un élément de configuration personnalisé (`<AddAudienceKeyPair>`) définie pour la classe.</span><span class="sxs-lookup"><span data-stu-id="49356-138">The token resolver maintains a dictionary of audience-key pairs that is initialized from a custom configuration element (`<AddAudienceKeyPair>`) defined for the class.</span></span> <span data-ttu-id="49356-139">La classe substitue la <xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A> méthode pour traiter cet élément.</span><span class="sxs-lookup"><span data-stu-id="49356-139">The class overrides the <xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A> method to process this element.</span></span> <span data-ttu-id="49356-140">Le remplacement est illustré dans l’exemple suivant ; Toutefois, les méthodes qu’elle appelle ne sont pas affichés par souci de concision.</span><span class="sxs-lookup"><span data-stu-id="49356-140">The override is shown in the following example; however, the methods it calls are not shown for brevity.</span></span> <span data-ttu-id="49356-141">Pour obtenir un exemple complet, consultez la `CustomToken` exemple.</span><span class="sxs-lookup"><span data-stu-id="49356-141">For the complete example, see the `CustomToken` sample.</span></span>  
  
```xml  
<issuerTokenResolver type="SimpleWebToken.CustomIssuerTokenResolver, SimpleWebToken">  
  <AddAudienceKeyPair  symmetricKey="wAVkldQiFypTQ+kdNdGWCYCHRcee8XmXxOvgmak8vSY=" audience="http://localhost:19851/" />  
</issuerTokenResolver>  
```  
  
## <a name="example"></a><span data-ttu-id="49356-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="49356-142">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="49356-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49356-143">See Also</span></span>  
 <xref:System.IdentityModel.Tokens.IssuerTokenResolver>
