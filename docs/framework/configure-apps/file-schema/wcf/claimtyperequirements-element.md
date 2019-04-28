---
title: <claimTypeRequirements>, élément
ms.date: 03/30/2017
ms.assetid: a26efe73-4bad-4731-8cad-27f00d54354b
ms.openlocfilehash: 236ae880fff24f7ccbf5d6c9c03c0208d446688f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704399"
---
# <a name="claimtyperequirements-element"></a><span data-ttu-id="a55bf-102">\<claimTypeRequirements> element</span><span class="sxs-lookup"><span data-stu-id="a55bf-102">\<claimTypeRequirements> element</span></span>
<span data-ttu-id="a55bf-103">Spécifie une collection de types de revendications requis.</span><span class="sxs-lookup"><span data-stu-id="a55bf-103">Specifies a collection of required claim types.</span></span>  
  
 <span data-ttu-id="a55bf-104">Dans un scénario fédéré, les services déclarent les spécifications relatives aux informations d'identification entrantes.</span><span class="sxs-lookup"><span data-stu-id="a55bf-104">In a federated scenario, services state the requirements on incoming credentials.</span></span> <span data-ttu-id="a55bf-105">Par exemple, ces informations d'identification doivent posséder un jeu de types de revendications défini.</span><span class="sxs-lookup"><span data-stu-id="a55bf-105">For example, the incoming credentials must possess a certain set of claim types.</span></span> <span data-ttu-id="a55bf-106">Chaque élément enfant de la collection indique les types de revendications requis et facultatifs censés apparaître dans les informations d'identification fédérées.</span><span class="sxs-lookup"><span data-stu-id="a55bf-106">Each child element in this collection specifies the types of required and optional claims expected to appear in a federated credential.</span></span>  
  
 <span data-ttu-id="a55bf-107">Une exigence de type de revendication se compose de l’URI du type de revendication requis dans le jeton émis avec un paramètre booléen qui indique si ce type de revendication est requis ou facultatif dans le jeton émis.</span><span class="sxs-lookup"><span data-stu-id="a55bf-107">A claim type requirement consists of the URI of the claim type requested in the issued token along with a Boolean parameter that indicates whether that claim type is required in the issued token, or is optional.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a55bf-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a55bf-108">See also</span></span>

- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement.ClaimTypeRequirements%2A>
- <xref:System.ServiceModel.Configuration.ClaimTypeElementCollection>
- <xref:System.ServiceModel.Configuration.ClaimTypeElement>
- <xref:System.ServiceModel.Configuration.SecurityElementBase.IssuedTokenParameters%2A>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="a55bf-109">Identité du service et authentification</span><span class="sxs-lookup"><span data-stu-id="a55bf-109">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [<span data-ttu-id="a55bf-110">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="a55bf-110">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="a55bf-111">Fonctionnalités de sécurité avec des liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="a55bf-111">Security Capabilities with Custom Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [<span data-ttu-id="a55bf-112">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="a55bf-112">Federation and Issued Tokens</span></span>](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [<span data-ttu-id="a55bf-113">\<add></span><span class="sxs-lookup"><span data-stu-id="a55bf-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-claimtyperequirements.md)
- [<span data-ttu-id="a55bf-114">Liaisons</span><span class="sxs-lookup"><span data-stu-id="a55bf-114">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="a55bf-115">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="a55bf-115">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="a55bf-116">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="a55bf-116">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="a55bf-117">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="a55bf-117">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="a55bf-118">Guide pratique pour Créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="a55bf-118">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [<span data-ttu-id="a55bf-119">Sécurité de liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="a55bf-119">Custom Binding Security</span></span>](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
