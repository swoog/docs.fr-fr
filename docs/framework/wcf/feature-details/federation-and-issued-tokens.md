---
title: Fédération et jetons émis
ms.date: 03/30/2017
helpviewer_keywords:
- WCF, federation
- issued tokens [WCF]
- federation [WCF], issued tokens
ms.assetid: 4c31ee7d-a820-4067-8b84-a83049021bb6
ms.openlocfilehash: 5ea30c2e9593f289c91a47cc082becf47dedc450
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072779"
---
# <a name="federation-and-issued-tokens"></a><span data-ttu-id="9555f-102">Fédération et jetons émis</span><span class="sxs-lookup"><span data-stu-id="9555f-102">Federation and Issued Tokens</span></span>
<span data-ttu-id="9555f-103">Avec Windows Communication Foundation (WCF), vous pouvez créer des clients qui communiquent en toute sécurité avec les services qui implémentent les spécifications WS-Federation et WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="9555f-103">With Windows Communication Foundation (WCF), you can create clients that communicate securely with services that implement the WS-Federation and WS-Trust specifications.</span></span> <span data-ttu-id="9555f-104">Ces spécifications utilisent XML, SOAP et WSDL (Web Services Description Language) pour fournir des mécanismes permettant d'activer l'authentification et l'autorisation sur différents domaines de confiance.</span><span class="sxs-lookup"><span data-stu-id="9555f-104">The specifications use XML, SOAP, and Web Services Description Language (WSDL) to provide mechanisms that enable authentication and authorization across different trust realms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9555f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9555f-105">In This Section</span></span>  
 [<span data-ttu-id="9555f-106">Fédération</span><span class="sxs-lookup"><span data-stu-id="9555f-106">Federation</span></span>](../../../../docs/framework/wcf/feature-details/federation.md)  
 <span data-ttu-id="9555f-107">Fournit une vue d'ensemble de la fédération.</span><span class="sxs-lookup"><span data-stu-id="9555f-107">Provides an overview of federation.</span></span>  
  
 [<span data-ttu-id="9555f-108">Fédération et confiance</span><span class="sxs-lookup"><span data-stu-id="9555f-108">Federation and Trust</span></span>](../../../../docs/framework/wcf/feature-details/federation-and-trust.md)  
 <span data-ttu-id="9555f-109">Répertorie les problèmes de conception dont il convient d'être informé lors de la création de services ou de clients fédérés.</span><span class="sxs-lookup"><span data-stu-id="9555f-109">Lists the design issues to be aware of when creating federated services or clients.</span></span>  
  
 [<span data-ttu-id="9555f-110">Procédure : créer un client fédéré</span><span class="sxs-lookup"><span data-stu-id="9555f-110">How to: Create a Federated Client</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)  
 <span data-ttu-id="9555f-111">Décrit les principes fondamentaux de création d’un client fédéré avec WCF.</span><span class="sxs-lookup"><span data-stu-id="9555f-111">Describes the basics of creating a federated client with WCF.</span></span>  
  
 [<span data-ttu-id="9555f-112">Procédure : configurer des informations d’identification sur un service de fédération</span><span class="sxs-lookup"><span data-stu-id="9555f-112">How to: Configure Credentials on a Federation Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)  
 <span data-ttu-id="9555f-113">Décrit les étapes de création d'un service fédéré.</span><span class="sxs-lookup"><span data-stu-id="9555f-113">Describes the steps of creating a federated service.</span></span>  
  
 [<span data-ttu-id="9555f-114">Procédure : créer un WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="9555f-114">How to: Create a WSFederationHttpBinding</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)  
 <span data-ttu-id="9555f-115">Décrit comment configurer des clients et des services qui utilisent `WSFederationHttpBinding`.</span><span class="sxs-lookup"><span data-stu-id="9555f-115">Describes how to configure clients and services that use the `WSFederationHttpBinding`.</span></span>  
  
 [<span data-ttu-id="9555f-116">Procédure : créer un service d’émission de jeton de sécurité</span><span class="sxs-lookup"><span data-stu-id="9555f-116">How to: Create a Security Token Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-token-service.md)  
 <span data-ttu-id="9555f-117">Décrit les étapes de création d'un service d'émission de jeton de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9555f-117">Describes the steps of creating a security token service.</span></span>  
  
 [<span data-ttu-id="9555f-118">Jetons SAML (Security Assertions Markup Language) et revendications</span><span class="sxs-lookup"><span data-stu-id="9555f-118">Security Assertions Markup Language (SAML) Tokens and Claims</span></span>](../../../../docs/framework/wcf/feature-details/saml-tokens-and-claims.md)  
 <span data-ttu-id="9555f-119">Décrit les jetons SAML (Security Assertions Markup Language), qui sont extensibles et vous permettent de créer des types de revendications enrichies.</span><span class="sxs-lookup"><span data-stu-id="9555f-119">Describes Security Assertions Markup Language (SAML) tokens, which are extensible and enable you to create rich claim types.</span></span>  
  
 [<span data-ttu-id="9555f-120">Procédure : configurer un émetteur local</span><span class="sxs-lookup"><span data-stu-id="9555f-120">How to: Configure a Local Issuer</span></span>](../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)  
 <span data-ttu-id="9555f-121">Décrit comment créer un émetteur local de jetons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9555f-121">Describes how to create a local issuer of security tokens.</span></span>  
  
 [<span data-ttu-id="9555f-122">Procédure : désactiver des sessions sécurisées sur un WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="9555f-122">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)  
 <span data-ttu-id="9555f-123">Décrit comment désactiver des sessions sécurisées sur `WSFederationHttpBinding`.</span><span class="sxs-lookup"><span data-stu-id="9555f-123">Describes how to disable secure sessions on a `WSFederationHttpBinding`.</span></span> <span data-ttu-id="9555f-124">La désactivation de sessions sécurisées est nécessaire lors de la création d'une batterie de serveurs Web qui requiert une session pour chaque client.</span><span class="sxs-lookup"><span data-stu-id="9555f-124">Disabling secure sessions is necessary when creating a Web farm that requires a session for each client.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="9555f-125">Référence</span><span class="sxs-lookup"><span data-stu-id="9555f-125">Reference</span></span>  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.IdentityModel.Tokens.SamlSecurityToken>  
  
 <xref:System.ServiceModel.Security.IssuedTokenClientCredential>  
  
 <xref:System.ServiceModel.Security.IssuedTokenServiceCredential>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenProvider>  
  
 <xref:System.ServiceModel.WSFederationHttpBinding>  
  
## <a name="see-also"></a><span data-ttu-id="9555f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9555f-126">See also</span></span>

- [<span data-ttu-id="9555f-127">Autorisation</span><span class="sxs-lookup"><span data-stu-id="9555f-127">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)
- [<span data-ttu-id="9555f-128">Jetons personnalisés</span><span class="sxs-lookup"><span data-stu-id="9555f-128">Custom Tokens</span></span>](../../../../docs/framework/wcf/extending/custom-tokens.md)
- [<span data-ttu-id="9555f-129">Modèle de sécurité pour Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="9555f-129">Security Model for Windows Server App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
