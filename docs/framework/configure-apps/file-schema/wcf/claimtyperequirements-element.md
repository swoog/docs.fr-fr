---
title: '&lt;claimTypeRequirements&gt;, élément'
ms.date: 03/30/2017
ms.assetid: a26efe73-4bad-4731-8cad-27f00d54354b
ms.openlocfilehash: 3a8bacf4dad2140e3d162cca89c6bd3ecf54b41f
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32748013"
---
# <a name="ltclaimtyperequirementsgt-element"></a><span data-ttu-id="3929a-102">&lt;claimTypeRequirements&gt;, élément</span><span class="sxs-lookup"><span data-stu-id="3929a-102">&lt;claimTypeRequirements&gt; element</span></span>
<span data-ttu-id="3929a-103">Spécifie une collection de types de revendications requis.</span><span class="sxs-lookup"><span data-stu-id="3929a-103">Specifies a collection of required claim types.</span></span>  
  
 <span data-ttu-id="3929a-104">Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="3929a-104">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="3929a-105">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="3929a-105">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="3929a-106">Chaque élément enfant de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="3929a-106">Each child element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>  
  
 <span data-ttu-id="3929a-107">Une exigence de type de revendication se compose de l’URI du type de revendication requis dans le jeton émis avec un paramètre booléen qui indique si ce type de revendication est requis ou facultatif dans le jeton émis.</span><span class="sxs-lookup"><span data-stu-id="3929a-107">A claim type requirement consists of the URI of the claim type requested in the issued token along with a Boolean parameter that indicates whether that claim type is required in the issued token, or is optional.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3929a-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3929a-108">See Also</span></span>  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ClaimTypeElement>  
 <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="3929a-109">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="3929a-109">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="3929a-110">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="3929a-110">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="3929a-111">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="3929a-111">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)  
 [<span data-ttu-id="3929a-112">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="3929a-112">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
 [<span data-ttu-id="3929a-113">\<add></span><span class="sxs-lookup"><span data-stu-id="3929a-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-claimtyperequirements.md)  
 [<span data-ttu-id="3929a-114">Liaisons</span><span class="sxs-lookup"><span data-stu-id="3929a-114">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="3929a-115">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="3929a-115">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="3929a-116">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="3929a-116">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="3929a-117">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="3929a-117">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)  
 [<span data-ttu-id="3929a-118">Guide pratique pour créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="3929a-118">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 [<span data-ttu-id="3929a-119">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="3929a-119">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
