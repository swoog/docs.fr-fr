---
title: Informations d’identification personnalisées et validation d’informations d’identification
ms.date: 03/30/2017
helpviewer_keywords:
- credentials [WCF], custom
- credentials [WCF]
- custom credentials [WCF]
- credential validation [WCF]
- credentials [WCF], validation
ms.assetid: da831bec-e281-4d44-b343-437b5eef688e
ms.openlocfilehash: 3b1ff700010f471a4d9be117f363083b6cbed493
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210631"
---
# <a name="custom-credential-and-credential-validation"></a><span data-ttu-id="422e6-102">Informations d’identification personnalisées et validation d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="422e6-102">Custom Credential and Credential Validation</span></span>
<span data-ttu-id="422e6-103">Sécurité dans Windows Communication Foundation (WCF) est basée sur l’échange d’informations d’identification entre les clients et services.</span><span class="sxs-lookup"><span data-stu-id="422e6-103">Security in Windows Communication Foundation (WCF) is based on the exchange of credentials between services and clients.</span></span> <span data-ttu-id="422e6-104">La plupart des besoins en matière de sécurité peuvent être satisfaits à l'aide de types d'informations d'identification communs, tels que Windows (Kerberos), le nom d'utilisateur et les mots de passe et les certificats.</span><span class="sxs-lookup"><span data-stu-id="422e6-104">Most security scenarios can be satisfied using common credential types, such as Windows (Kerberos), username and passwords, and certificates.</span></span> <span data-ttu-id="422e6-105">Toutefois, si un nouveau type d'informations d'identification est requis, les rubriques de cette section expliquent comment gérer et valider des types nouveaux.</span><span class="sxs-lookup"><span data-stu-id="422e6-105">However, if a new type of credential is required, the topics in this section explain how to handle and validate new types.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="422e6-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="422e6-106">In This Section</span></span>  
 [<span data-ttu-id="422e6-107">Procédure : créer un service qui utilise un validateur de certificat personnalisé</span><span class="sxs-lookup"><span data-stu-id="422e6-107">How to: Create a Service that Employs a Custom Certificate Validator</span></span>](../../../../docs/framework/wcf/extending/how-to-create-a-service-that-employs-a-custom-certificate-validator.md)  
 <span data-ttu-id="422e6-108">Explique comment personnaliser la validation de WCF en héritant de la <xref:System.IdentityModel.Selectors.X509CertificateValidator> classe.</span><span class="sxs-lookup"><span data-stu-id="422e6-108">Explains how to customize WCF validation by inheriting from the <xref:System.IdentityModel.Selectors.X509CertificateValidator> class.</span></span>  
  
 [<span data-ttu-id="422e6-109">Procédure pas à pas : création d’informations d’identification de client et de service personnalisées</span><span class="sxs-lookup"><span data-stu-id="422e6-109">Walkthrough: Creating Custom Client and Service Credentials</span></span>](../../../../docs/framework/wcf/extending/walkthrough-creating-custom-client-and-service-credentials.md)  
 <span data-ttu-id="422e6-110">Montre comment étendre le <xref:System.ServiceModel.Description.ClientCredentials> et <xref:System.ServiceModel.Description.ServiceCredentials> classes pour prendre en charge de nouvelles informations d’identification de types.</span><span class="sxs-lookup"><span data-stu-id="422e6-110">Demonstrates how to extend the <xref:System.ServiceModel.Description.ClientCredentials> and <xref:System.ServiceModel.Description.ServiceCredentials> classes to accommodate new credential types.</span></span> <span data-ttu-id="422e6-111">Il s'agit du premier volet d'une série de rubriques qui permettent de créer des types d'informations d'identification personnalisés.</span><span class="sxs-lookup"><span data-stu-id="422e6-111">This is first in a series of topics that enable creation of custom credential types.</span></span>  
  
 [<span data-ttu-id="422e6-112">Procédure : créer un fournisseur de jetons de sécurité personnalisé</span><span class="sxs-lookup"><span data-stu-id="422e6-112">How to: Create a Custom Security Token Provider</span></span>](../../../../docs/framework/wcf/extending/how-to-create-a-custom-security-token-provider.md)  
 <span data-ttu-id="422e6-113">Explique comment créer un fournisseur de jetons de sécurité pour gérer de nouveaux types d'informations d'identification et retourner de nouveaux jetons pour les informations d'authentification.</span><span class="sxs-lookup"><span data-stu-id="422e6-113">Explains how to create a security token provider to handle new credential types and return new tokens for the credential.</span></span> <span data-ttu-id="422e6-114">Il s'agit de la deuxième rubrique de la série.</span><span class="sxs-lookup"><span data-stu-id="422e6-114">This is the second topic in the series.</span></span>  
  
 [<span data-ttu-id="422e6-115">Procédure : créer un authentificateur de jetons de sécurité personnalisé</span><span class="sxs-lookup"><span data-stu-id="422e6-115">How to: Create a Custom Security Token Authenticator</span></span>](../../../../docs/framework/wcf/extending/how-to-create-a-custom-security-token-authenticator.md)  
 <span data-ttu-id="422e6-116">Explique comment créer un authentificateur personnalisé pour authentifier un nouveau type d'informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="422e6-116">Explains how to create a custom authenticator to authenticate a new credential type.</span></span> <span data-ttu-id="422e6-117">Il s'agit de la troisième rubrique de la série.</span><span class="sxs-lookup"><span data-stu-id="422e6-117">This is the third topic in the series.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="422e6-118">Référence</span><span class="sxs-lookup"><span data-stu-id="422e6-118">Reference</span></span>  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
 <xref:System.IdentityModel.Selectors.X509CertificateValidator>  
  
 <xref:System.ServiceModel.Description.ClientCredentials>  
  
 <xref:System.ServiceModel.Description.ServiceCredentials>  
  
## <a name="related-sections"></a><span data-ttu-id="422e6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="422e6-119">Related Sections</span></span>  
 [<span data-ttu-id="422e6-120">Authentification</span><span class="sxs-lookup"><span data-stu-id="422e6-120">Authentication</span></span>](../../../../docs/framework/wcf/feature-details/authentication-in-wcf.md)  
  
 [<span data-ttu-id="422e6-121">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="422e6-121">Federation and Issued Tokens</span></span>](../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)  
  
 [<span data-ttu-id="422e6-122">Autorisation</span><span class="sxs-lookup"><span data-stu-id="422e6-122">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="422e6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="422e6-123">See also</span></span>

- [<span data-ttu-id="422e6-124">Sécurité</span><span class="sxs-lookup"><span data-stu-id="422e6-124">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)
