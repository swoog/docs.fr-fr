---
title: Fédération et jetons émis
ms.date: 03/30/2017
helpviewer_keywords:
- WCF, federation
- issued tokens [WCF]
- federation [WCF], issued tokens
ms.assetid: 4c31ee7d-a820-4067-8b84-a83049021bb6
ms.openlocfilehash: 513d68f49e4182979b492fa67e65860aee96e09a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54699413"
---
# <a name="federation-and-issued-tokens"></a>Fédération et jetons émis
Avec Windows Communication Foundation (WCF), vous pouvez créer des clients qui communiquent en toute sécurité avec les services qui implémentent les spécifications WS-Federation et WS-Trust. Ces spécifications utilisent XML, SOAP et WSDL (Web Services Description Language) pour fournir des mécanismes permettant d'activer l'authentification et l'autorisation sur différents domaines de confiance.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Fédération](../../../../docs/framework/wcf/feature-details/federation.md)  
 Fournit une vue d'ensemble de la fédération.  
  
 [Fédération et confiance](../../../../docs/framework/wcf/feature-details/federation-and-trust.md)  
 Répertorie les problèmes de conception dont il convient d'être informé lors de la création de services ou de clients fédérés.  
  
 [Guide pratique pour Créer un Client fédéré](../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)  
 Décrit les principes fondamentaux de création d’un client fédéré avec WCF.  
  
 [Guide pratique pour Configurer les informations d’identification sur un Service de fédération](../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)  
 Décrit les étapes de création d'un service fédéré.  
  
 [Guide pratique pour Créer une liaison WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)  
 Décrit comment configurer des clients et des services qui utilisent `WSFederationHttpBinding`.  
  
 [Guide pratique pour Créer un Service de jeton de sécurité](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-token-service.md)  
 Décrit les étapes de création d'un service d'émission de jeton de sécurité.  
  
 [Jetons SAML (Security Assertions Markup Language) et revendications](../../../../docs/framework/wcf/feature-details/saml-tokens-and-claims.md)  
 Décrit les jetons SAML (Security Assertions Markup Language), qui sont extensibles et vous permettent de créer des types de revendications enrichies.  
  
 [Guide pratique pour Configurer un émetteur Local](../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)  
 Décrit comment créer un émetteur local de jetons de sécurité.  
  
 [Guide pratique pour Désactiver des Sessions sécurisées sur une liaison WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)  
 Décrit comment désactiver des sessions sécurisées sur `WSFederationHttpBinding`. La désactivation de sessions sécurisées est nécessaire lors de la création d'une batterie de serveurs Web qui requiert une session pour chaque client.  
  
## <a name="reference"></a>Référence  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.IdentityModel.Tokens.SamlSecurityToken>  
  
 <xref:System.ServiceModel.Security.IssuedTokenClientCredential>  
  
 <xref:System.ServiceModel.Security.IssuedTokenServiceCredential>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenProvider>  
  
 <xref:System.ServiceModel.WSFederationHttpBinding>  
  
## <a name="see-also"></a>Voir aussi
- [Autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)
- [Jetons personnalisés](../../../../docs/framework/wcf/extending/custom-tokens.md)
- [Modèle de sécurité pour Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
