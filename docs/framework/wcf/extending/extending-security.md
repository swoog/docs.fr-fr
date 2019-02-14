---
title: Extension de la sécurité
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], extending
ms.assetid: a015a040-9fdf-4147-9ea9-f83b570be1d4
ms.openlocfilehash: 698d65d951ed7adad5aa32e874befb15a3b24d12
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56261425"
---
# <a name="extending-security"></a><span data-ttu-id="8e233-102">Extension de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8e233-102">Extending Security</span></span>
<span data-ttu-id="8e233-103">Pour prendre en charge de nouveaux types de revendications et jetons personnalisés, vous pouvez étendre l’infrastructure de sécurité de Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="8e233-103">To accommodate new claim types and custom tokens, you can extend the security infrastructure of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="8e233-104">Les rubriques de cette section vous montrent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="8e233-104">The topics in this section show you how this is done.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8e233-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8e233-105">In This Section</span></span>  
  
 [<span data-ttu-id="8e233-106">Informations d’identification personnalisées et validation d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="8e233-106">Custom Credential and Credential Validation</span></span>](../../../../docs/framework/wcf/extending/custom-credential-and-credential-validation.md)  
 <span data-ttu-id="8e233-107">Explique comment le modèle d'identité est utilisé lors de la validation d'informations d'identification personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8e233-107">Explains how the Identity Model is used when validating custom credentials.</span></span>  
  
 [<span data-ttu-id="8e233-108">Jetons personnalisés</span><span class="sxs-lookup"><span data-stu-id="8e233-108">Custom Tokens</span></span>](../../../../docs/framework/wcf/extending/custom-tokens.md)  
 <span data-ttu-id="8e233-109">Les jetons émis par un service de jeton de sécurité sont en général des jetons SAML.</span><span class="sxs-lookup"><span data-stu-id="8e233-109">Issued tokens from a Security Token Service (STS) are typically SAML tokens.</span></span> <span data-ttu-id="8e233-110">Cette rubrique explique comment créer un type de jeton personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8e233-110">This topic explains how to create a custom token type.</span></span>  
  
 [<span data-ttu-id="8e233-111">Autorisation personnalisée</span><span class="sxs-lookup"><span data-stu-id="8e233-111">Custom Authorization</span></span>](../../../../docs/framework/wcf/extending/custom-authorization.md)  
 <span data-ttu-id="8e233-112">Explique comment implémenter une autorisation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8e233-112">Explains how to implement custom authorization.</span></span>  
  
 [<span data-ttu-id="8e233-113">Substitution de l’identité d’un service pour l’authentification</span><span class="sxs-lookup"><span data-stu-id="8e233-113">Overriding the Identity of a Service for Authentication</span></span>](../../../../docs/framework/wcf/extending/overriding-the-identity-of-a-service-for-authentication.md)  
 <span data-ttu-id="8e233-114">Décrit comment remplacer l'identité d'un service pour l'authentification.</span><span class="sxs-lookup"><span data-stu-id="8e233-114">Describes how to override the identity of a service for authentication.</span></span>  
  
 [<span data-ttu-id="8e233-115">Guide pratique pour Créer un vérificateur d’identité Client personnalisés</span><span class="sxs-lookup"><span data-stu-id="8e233-115">How to: Create a Custom Client Identity Verifier</span></span>](../../../../docs/framework/wcf/extending/how-to-create-a-custom-client-identity-verifier.md)  
 <span data-ttu-id="8e233-116">Montre comment valider une identité de point de terminaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8e233-116">Demonstrates how to validate a custom endpoint identity.</span></span>  
  
 [<span data-ttu-id="8e233-117">Guide pratique pour Utiliser des certificats X.509 distincts pour la signature et chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e233-117">How to: Use Separate X.509 Certificates for Signing and Encryption</span></span>](../../../../docs/framework/wcf/extending/how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 <span data-ttu-id="8e233-118">Les messages sont généralement signés et chiffrés à l'aide d'un certificat unique.</span><span class="sxs-lookup"><span data-stu-id="8e233-118">Messages are typically signed and encrypted with a single certificate.</span></span> <span data-ttu-id="8e233-119">Cette rubrique explique comment deux certificats peuvent être utilisés, s'ils sont requis.</span><span class="sxs-lookup"><span data-stu-id="8e233-119">This topic explains how two certificates can be used, when required.</span></span>  
  
 [<span data-ttu-id="8e233-120">Guide pratique pour Remplacer le fournisseur de services de chiffrement par clé privée d’un certificat X.509</span><span class="sxs-lookup"><span data-stu-id="8e233-120">How to: Change the Cryptographic Provider for an X.509 Certificate's Private Key</span></span>](../../../../docs/framework/wcf/extending/change-cryptographic-provider-x509-certificate-private-key.md)  
 <span data-ttu-id="8e233-121">Explique comment modifier le fournisseur de services de chiffrement utilisé pour fournir la clé privée d’un certificat X.509 et comment intégrer le fournisseur dans l’infrastructure Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="8e233-121">Explains how to change the cryptographic provider used to provide an X.509 certificate's private key and how to integrate the provider into the Windows Communication Foundation (WCF) framework.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="8e233-122">Référence</span><span class="sxs-lookup"><span data-stu-id="8e233-122">Reference</span></span>  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
## <a name="related-sections"></a><span data-ttu-id="8e233-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e233-123">Related Sections</span></span>  
 [<span data-ttu-id="8e233-124">Sécurité</span><span class="sxs-lookup"><span data-stu-id="8e233-124">Security</span></span>](../../../../docs/framework/wcf/feature-details/security.md)  
  
 [<span data-ttu-id="8e233-125">Programmation WCF de base</span><span class="sxs-lookup"><span data-stu-id="8e233-125">Basic WCF Programming</span></span>](../../../../docs/framework/wcf/basic-wcf-programming.md)  
  
## <a name="see-also"></a><span data-ttu-id="8e233-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e233-126">See also</span></span>
- [<span data-ttu-id="8e233-127">Vue d’ensemble de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8e233-127">Security Overview</span></span>](../../../../docs/framework/wcf/feature-details/security-overview.md)
