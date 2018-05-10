---
title: Extension de la sécurité
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], extending
ms.assetid: a015a040-9fdf-4147-9ea9-f83b570be1d4
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 94aefe80674c5b4ec6fcce6a41d9b68e093f4262
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="extending-security"></a>Extension de la sécurité
Pour prendre en compte les nouveaux types de revendications et jetons personnalisés, vous pouvez étendre l’infrastructure de sécurité de Windows Communication Foundation (WCF). Les rubriques de cette section vous montrent comment procéder.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Architecture de sécurité](http://msdn.microsoft.com/library/16593476-d36a-408d-808c-ae6fd483e28f)  
 Décrit l’architecture du système de sécurité WCF.  
  
 [Informations d’identification personnalisées et validation d’informations d’identification](../../../../docs/framework/wcf/extending/custom-credential-and-credential-validation.md)  
 Explique comment le modèle d'identité est utilisé lors de la validation d'informations d'identification personnalisées.  
  
 [Jetons personnalisés](../../../../docs/framework/wcf/extending/custom-tokens.md)  
 Les jetons émis par un service de jeton de sécurité sont en général des jetons SAML. Cette rubrique explique comment créer un type de jeton personnalisé.  
  
 [Autorisation personnalisée](../../../../docs/framework/wcf/extending/custom-authorization.md)  
 Explique comment implémenter une autorisation personnalisée.  
  
 [Substitution de l’identité d’un service pour l’authentification](../../../../docs/framework/wcf/extending/overriding-the-identity-of-a-service-for-authentication.md)  
 Décrit comment remplacer l'identité d'un service pour l'authentification.  
  
 [Guide pratique pour créer un vérificateur d’identité du client personnalisé](../../../../docs/framework/wcf/extending/how-to-create-a-custom-client-identity-verifier.md)  
 Montre comment valider une identité de point de terminaison personnalisée.  
  
 [Guide pratique pour utiliser des certificats X.509 distincts pour les signatures et le chiffrement](../../../../docs/framework/wcf/extending/how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 Les messages sont généralement signés et chiffrés à l'aide d'un certificat unique. Cette rubrique explique comment deux certificats peuvent être utilisés, s'ils sont requis.  
  
 [Guide pratique pour remplacer le fournisseur de services de chiffrement par la clé privée d’un certificat X.509](../../../../docs/framework/wcf/extending/change-cryptographic-provider-x509-certificate-private-key.md)  
 Explique comment modifier le fournisseur de services de chiffrement utilisé pour fournir la clé privée d’un certificat X.509 et comment intégrer le fournisseur dans le cadre de Windows Communication Foundation (WCF).  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Sécurité](../../../../docs/framework/wcf/feature-details/security.md)  
  
 [Programmation WCF de base](../../../../docs/framework/wcf/basic-wcf-programming.md)  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de la sécurité](../../../../docs/framework/wcf/feature-details/security-overview.md)
