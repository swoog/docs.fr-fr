---
title: <add> de <allowedAudienceUris>
ms.date: 03/30/2017
ms.assetid: 4e7b7637-e0ea-4a91-988f-6b6ef28d9fc3
ms.openlocfilehash: a18305d2981b1a1c8cf56a9dfcbb14ab3ce1ff92
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64607219"
---
# <a name="add-of-allowedaudienceuris"></a><span data-ttu-id="bec13-102">\<add> of \<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="bec13-102">\<add> of \<allowedAudienceUris></span></span>
<span data-ttu-id="bec13-103">Ajoute un URI cible pour lequel le jeton de sécurité <xref:System.IdentityModel.Tokens.SamlSecurityToken> peut être visé pour être considéré comme valide par une instance de <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span><span class="sxs-lookup"><span data-stu-id="bec13-103">Adds a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>  
  
 <span data-ttu-id="bec13-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bec13-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="bec13-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="bec13-105">\<behaviors></span></span>  
<span data-ttu-id="bec13-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="bec13-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="bec13-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="bec13-107">\<behavior></span></span>  
<span data-ttu-id="bec13-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="bec13-108">\<serviceCredentials></span></span>  
<span data-ttu-id="bec13-109">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="bec13-109">\<issuedTokenAuthentication></span></span>  
<span data-ttu-id="bec13-110">\<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="bec13-110">\<allowedAudienceUris></span></span>  
<span data-ttu-id="bec13-111">\<Ajouter > élément pour \<allowedAudienceUris ></span><span class="sxs-lookup"><span data-stu-id="bec13-111">\<add> element for \<allowedAudienceUris></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bec13-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bec13-112">Syntax</span></span>  
  
```xml  
<allowedAudienceUris>
  <add allowedAudienceUri="String" />
</allowedAudienceUris>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bec13-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bec13-113">Attributes and Elements</span></span>  
 <span data-ttu-id="bec13-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bec13-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bec13-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="bec13-115">Attributes</span></span>  
  
|<span data-ttu-id="bec13-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="bec13-116">Attribute</span></span>|<span data-ttu-id="bec13-117">Description</span><span class="sxs-lookup"><span data-stu-id="bec13-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bec13-118">allowedAudienceUri</span><span class="sxs-lookup"><span data-stu-id="bec13-118">allowedAudienceUri</span></span>|<span data-ttu-id="bec13-119">Chaîne qui contient un URI cible pour lequel le jeton de sécurité <xref:System.IdentityModel.Tokens.SamlSecurityToken> peut être visé pour être considéré comme valide par une instance de <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span><span class="sxs-lookup"><span data-stu-id="bec13-119">A string that contains a target Uri for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bec13-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bec13-120">Child Elements</span></span>  
 <span data-ttu-id="bec13-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bec13-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bec13-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bec13-122">Parent Elements</span></span>  
  
|<span data-ttu-id="bec13-123">Élément</span><span class="sxs-lookup"><span data-stu-id="bec13-123">Element</span></span>|<span data-ttu-id="bec13-124">Description</span><span class="sxs-lookup"><span data-stu-id="bec13-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bec13-125">\<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="bec13-125">\<allowedAudienceUris></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowedaudienceuris.md)|<span data-ttu-id="bec13-126">Représente une collection d’URI cibles pour lesquels le jeton de sécurité <xref:System.IdentityModel.Tokens.SamlSecurityToken> peut être visé pour être considéré comme valide par une instance de <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span><span class="sxs-lookup"><span data-stu-id="bec13-126">Represents a collection of target URIs for which the <xref:System.IdentityModel.Tokens.SamlSecurityToken> security token can be targeted for in order to be considered valid by a <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bec13-127">Notes</span><span class="sxs-lookup"><span data-stu-id="bec13-127">Remarks</span></span>  
 <span data-ttu-id="bec13-128">Vous devez utiliser cette collection dans une application fédérée qui utilise un service de jeton de sécurité (STS) qui émet des jetons de sécurité <xref:System.IdentityModel.Tokens.SamlSecurityToken>.</span><span class="sxs-lookup"><span data-stu-id="bec13-128">You should use this collection in a federated application that utilizes a security token service (STS) that issues <xref:System.IdentityModel.Tokens.SamlSecurityToken> security tokens.</span></span> <span data-ttu-id="bec13-129">Lorsque le STS émet le jeton de sécurité, il peut spécifier l'URI des services Web pour lesquels le jeton de sécurité est prévu en ajoutant un <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> au jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bec13-129">When the STS issues the security token, it can specify the URI of the Web services for which the security token is intended by adding a <xref:System.IdentityModel.Tokens.SamlAudienceRestrictionCondition> to the security token.</span></span> <span data-ttu-id="bec13-130">Cela permet au <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> du service Web destinataire de vérifier que le jeton de sécurité émis est prévu pour ce service Web en spécifiant que ce contrôle doit arriver en effectuant les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bec13-130">That allows the <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator> for the recipient Web service to verify that the issued security token is intended for this Web service by specifying that this check should happen by doing the following:</span></span>  
  
- <span data-ttu-id="bec13-131">Affectez à l'attribut `audienceUriMode` de `<issuedTokenAuthentication>` la valeur <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> ou <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>.</span><span class="sxs-lookup"><span data-stu-id="bec13-131">Set the `audienceUriMode` attribute of `<issuedTokenAuthentication>` to <xref:System.IdentityModel.Selectors.AudienceUriMode.Always> or <xref:System.IdentityModel.Selectors.AudienceUriMode.BearerKeyOnly>.</span></span>  
  
- <span data-ttu-id="bec13-132">Spécifiez le jeu d'URI valides en ajoutant les URI à cette collection.</span><span class="sxs-lookup"><span data-stu-id="bec13-132">Specify the set of valid URIs, by adding the URIs to this collection.</span></span>  
  
 <span data-ttu-id="bec13-133">Pour plus d'informations, consultez <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span><span class="sxs-lookup"><span data-stu-id="bec13-133">For more information, see <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>.</span></span>  
  
 <span data-ttu-id="bec13-134">Pour plus d’informations sur l’utilisation de cet élément de configuration, consultez [Comment : Configurer les informations d’identification sur un Service de fédération](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span><span class="sxs-lookup"><span data-stu-id="bec13-134">For more information on using this configuration element, see [How to: Configure Credentials on a Federation Service](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bec13-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bec13-135">See also</span></span>

- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AllowedAudienceUris%2A>
- <xref:System.IdentityModel.Selectors.SamlSecurityTokenAuthenticator.AudienceUriMode%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenServiceElement.AllowedAudienceUris%2A>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElementCollection>
- <xref:System.ServiceModel.Configuration.AllowedAudienceUriElement>
- <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowedAudienceUris%2A>
- [<span data-ttu-id="bec13-136">\<allowedAudienceUris></span><span class="sxs-lookup"><span data-stu-id="bec13-136">\<allowedAudienceUris></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowedaudienceuris.md)
- [<span data-ttu-id="bec13-137">\<issuedTokenAuthentication></span><span class="sxs-lookup"><span data-stu-id="bec13-137">\<issuedTokenAuthentication></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenauthentication-of-servicecredentials.md)
- [<span data-ttu-id="bec13-138">Comportements de sécurité</span><span class="sxs-lookup"><span data-stu-id="bec13-138">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [<span data-ttu-id="bec13-139">Sécurisation des services et des clients</span><span class="sxs-lookup"><span data-stu-id="bec13-139">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="bec13-140">Guide pratique pour Configurer les informations d’identification sur un Service de fédération</span><span class="sxs-lookup"><span data-stu-id="bec13-140">How to: Configure Credentials on a Federation Service</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)
