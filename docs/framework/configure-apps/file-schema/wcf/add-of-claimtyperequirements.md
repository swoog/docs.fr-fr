---
title: '&lt;add&gt; de &lt;claimTypeRequirements&gt;'
ms.date: 03/30/2017
ms.assetid: c68e83c9-39e8-4264-b1ce-b6a9eb5b98aa
ms.openlocfilehash: b4f9275fdc36ea3c7ba79c6609f039c3b1f4c3ed
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-of-ltclaimtyperequirementsgt"></a><span data-ttu-id="c9d72-102">&lt;add&gt; de &lt;claimTypeRequirements&gt;</span><span class="sxs-lookup"><span data-stu-id="c9d72-102">&lt;add&gt; of &lt;claimTypeRequirements&gt;</span></span>
<span data-ttu-id="c9d72-103">Spécifie les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="c9d72-103">Specifies the types of required and optional claims expected to appear in the federated credential.</span></span> <span data-ttu-id="c9d72-104">Par exemple, les services déclarent les exigences relatives aux informations d’identification entrantes devant posséder un certain jeu de types de revendications.</span><span class="sxs-lookup"><span data-stu-id="c9d72-104">For example, services state the requirements on incoming credentials, which must possess a certain set of claim types.</span></span>  
  
 <span data-ttu-id="c9d72-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="c9d72-105">\<system.serviceModel></span></span>  
<span data-ttu-id="c9d72-106">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="c9d72-106">\<bindings></span></span>  
<span data-ttu-id="c9d72-107">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="c9d72-107">\<customBinding></span></span>  
<span data-ttu-id="c9d72-108">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="c9d72-108">\<binding></span></span>  
<span data-ttu-id="c9d72-109">\<sécurité ></span><span class="sxs-lookup"><span data-stu-id="c9d72-109">\<security></span></span>  
<span data-ttu-id="c9d72-110">\<issuedTokenParameters ></span><span class="sxs-lookup"><span data-stu-id="c9d72-110">\<issuedTokenParameters></span></span>  
<span data-ttu-id="c9d72-111">\<claimTypeRequirements ></span><span class="sxs-lookup"><span data-stu-id="c9d72-111">\<claimTypeRequirements></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9d72-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d72-112">Syntax</span></span>  
  
```xml  
<claimTypeRequirements>  
      <add claimType="URI"  
           isOptional="Boolean" />  
</claimTypeRequirements>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c9d72-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c9d72-113">Attributes and Elements</span></span>  
 <span data-ttu-id="c9d72-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c9d72-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c9d72-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="c9d72-115">Attributes</span></span>  
  
|<span data-ttu-id="c9d72-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="c9d72-116">Attribute</span></span>|<span data-ttu-id="c9d72-117">Description</span><span class="sxs-lookup"><span data-stu-id="c9d72-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="c9d72-118">claimType</span><span class="sxs-lookup"><span data-stu-id="c9d72-118">claimType</span></span>|<span data-ttu-id="c9d72-119">URI définissant le type d'une revendication.</span><span class="sxs-lookup"><span data-stu-id="c9d72-119">A URI that defines the type of a claim.</span></span> <span data-ttu-id="c9d72-120">Par exemple, pour acheter un produit d'un site Web, l'utilisateur doit présenter une carte de crédit valide avec limite de crédit suffisante.</span><span class="sxs-lookup"><span data-stu-id="c9d72-120">For example, to purchase a product from a Web site, the user must present a valid credit card with sufficient credit limit.</span></span> <span data-ttu-id="c9d72-121">Le type de revendication est l'URI de la carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="c9d72-121">The claim type would be the credit card URI.</span></span>|  
|<span data-ttu-id="c9d72-122">isOptional</span><span class="sxs-lookup"><span data-stu-id="c9d72-122">isOptional</span></span>|<span data-ttu-id="c9d72-123">Valeur booléenne indiquant si l'opération concerne une revendication facultative.</span><span class="sxs-lookup"><span data-stu-id="c9d72-123">A Boolean value that specifies if this is for an optional claim.</span></span> <span data-ttu-id="c9d72-124">Affectez à cet attribut la valeur `false` si c'est une revendication requise.</span><span class="sxs-lookup"><span data-stu-id="c9d72-124">Set this attribute to `false` if this is a required claim.</span></span><br /><br /> <span data-ttu-id="c9d72-125">Vous pouvez utiliser cet attribut lorsque le service demande certaines informations sans pour autant les exiger.</span><span class="sxs-lookup"><span data-stu-id="c9d72-125">You can use this attribute when the service asks for some information but does not require it.</span></span> <span data-ttu-id="c9d72-126">Par exemple, si vous décidez que l'utilisateur doit indiquer ses prénom, nom et adresse mais pas forcément son numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="c9d72-126">For example, if you require the user to enter his/her first name, last name and address, but decide that phone number is optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="c9d72-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c9d72-127">Child Elements</span></span>  
 <span data-ttu-id="c9d72-128">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c9d72-128">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="c9d72-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c9d72-129">Parent Elements</span></span>  
  
|<span data-ttu-id="c9d72-130">Élément</span><span class="sxs-lookup"><span data-stu-id="c9d72-130">Element</span></span>|<span data-ttu-id="c9d72-131">Description</span><span class="sxs-lookup"><span data-stu-id="c9d72-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c9d72-132">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="c9d72-132">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)|<span data-ttu-id="c9d72-133">Spécifie une collection de types de revendications requis.</span><span class="sxs-lookup"><span data-stu-id="c9d72-133">Specifies a collection of required claim types.</span></span><br /><br /> <span data-ttu-id="c9d72-134">Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="c9d72-134">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="c9d72-135">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="c9d72-135">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="c9d72-136">Chaque élément de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d’identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="c9d72-136">Each element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c9d72-137">Notes</span><span class="sxs-lookup"><span data-stu-id="c9d72-137">Remarks</span></span>  
 <span data-ttu-id="c9d72-138">Dans un scénario fédéré, les services déclarent les exigences relatives aux informations d’identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="c9d72-138">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="c9d72-139">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="c9d72-139">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="c9d72-140">Cette spécification est explicitée dans une stratégie de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c9d72-140">This requirement is manifested in a security policy.</span></span> <span data-ttu-id="c9d72-141">Lorsqu’un client requiert des informations d’identification à partir d’un service fédéré (CardSpace, par exemple), il indique ces exigences dans une demande de jeton (RequestSecurityToken) afin que le service fédéré puisse publier ces informations et répondre aux exigences.</span><span class="sxs-lookup"><span data-stu-id="c9d72-141">When a client requests credentials from a federated service (for example, CardSpace), it puts the requirements into a token request (RequestSecurityToken) so that the federated service can issue the credentials that satisfy the requirements accordingly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9d72-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9d72-142">Example</span></span>  
 <span data-ttu-id="c9d72-143">La configuration suivante ajoute deux exigences de type de revendication à une liaison de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c9d72-143">The following configuration adds two claim type requirements to a security binding.</span></span>  
  
```xml  
<bindings>  
    <wsFederationHttpBinding>  
      <binding name="myFederatedBinding">  
        <security mode="Message">  
          <message issuedTokenType="urn:oasis:names:tc:SAML:1.0:assertion">  
            <claimTypeRequirements>  
              <add claimType=  
"http://schemas.microsoft.com/ws/2005/05/identity/claims/EmailAddress"/>  
              <add claimType=  
"http://schemas.microsoft.com/ws/2005/05/identity/claims/UserName"    
optional="true" />  
            </claims>  
          </message>  
        </security>  
      </binding>  
    </wsFederationHttpBinding>  
</bindings>  
```  
  
## <a name="see-also"></a><span data-ttu-id="c9d72-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d72-144">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.ClaimTypeRequirement>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="c9d72-145">\<claimTypeRequirements></span><span class="sxs-lookup"><span data-stu-id="c9d72-145">\<claimTypeRequirements></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/claimtyperequirements-element.md)  
 [<span data-ttu-id="c9d72-146">Liaisons</span><span class="sxs-lookup"><span data-stu-id="c9d72-146">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="c9d72-147">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="c9d72-147">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="c9d72-148">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="c9d72-148">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="c9d72-149">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="c9d72-149">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="c9d72-150">Guide pratique pour créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="c9d72-150">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="c9d72-151">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="c9d72-151">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
