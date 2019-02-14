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
# <a name="extending-security"></a>Extension de la sécurité
Pour prendre en charge de nouveaux types de revendications et jetons personnalisés, vous pouvez étendre l’infrastructure de sécurité de Windows Communication Foundation (WCF). Les rubriques de cette section vous montrent comment procéder.  
  
## <a name="in-this-section"></a>Dans cette section  
  
 [Informations d’identification personnalisées et validation d’informations d’identification](../../../../docs/framework/wcf/extending/custom-credential-and-credential-validation.md)  
 Explique comment le modèle d'identité est utilisé lors de la validation d'informations d'identification personnalisées.  
  
 [Jetons personnalisés](../../../../docs/framework/wcf/extending/custom-tokens.md)  
 Les jetons émis par un service de jeton de sécurité sont en général des jetons SAML. Cette rubrique explique comment créer un type de jeton personnalisé.  
  
 [Autorisation personnalisée](../../../../docs/framework/wcf/extending/custom-authorization.md)  
 Explique comment implémenter une autorisation personnalisée.  
  
 [Substitution de l’identité d’un service pour l’authentification](../../../../docs/framework/wcf/extending/overriding-the-identity-of-a-service-for-authentication.md)  
 Décrit comment remplacer l'identité d'un service pour l'authentification.  
  
 [Guide pratique pour Créer un vérificateur d’identité Client personnalisés](../../../../docs/framework/wcf/extending/how-to-create-a-custom-client-identity-verifier.md)  
 Montre comment valider une identité de point de terminaison personnalisée.  
  
 [Guide pratique pour Utiliser des certificats X.509 distincts pour la signature et chiffrement](../../../../docs/framework/wcf/extending/how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 Les messages sont généralement signés et chiffrés à l'aide d'un certificat unique. Cette rubrique explique comment deux certificats peuvent être utilisés, s'ils sont requis.  
  
 [Guide pratique pour Remplacer le fournisseur de services de chiffrement par clé privée d’un certificat X.509](../../../../docs/framework/wcf/extending/change-cryptographic-provider-x509-certificate-private-key.md)  
 Explique comment modifier le fournisseur de services de chiffrement utilisé pour fournir la clé privée d’un certificat X.509 et comment intégrer le fournisseur dans l’infrastructure Windows Communication Foundation (WCF).  
  
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
- [Vue d’ensemble de la sécurité](../../../../docs/framework/wcf/feature-details/security-overview.md)
