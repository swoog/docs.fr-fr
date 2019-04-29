---
title: Authentification dans WCF
ms.date: 03/30/2017
helpviewer_keywords:
- authentication [WCF]
- security [WCF], authentication
ms.assetid: 9254d873-843d-4c6e-bea4-8184ac3e44f4
ms.openlocfilehash: ebff66e185bdca75a0150b22a16392bfd08892d3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61595957"
---
# <a name="authentication-in-wcf"></a>Authentification dans WCF
Les rubriques suivantes montrent un nombre de mécanismes différents dans Windows Communication Foundation (WCF) qui fournissent l’authentification, par exemple, l’authentification Windows, les certificats X.509 et nom d’utilisateur et mots de passe.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Utiliser le fournisseur d’appartenances ASP.NET](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-membership-provider.md)  
 Les fonctionnalités ASP.NET incluent une appartenance et un fournisseur de rôles, une base de données pour stocker des paires nom d’utilisateur/mot de passe pour l’authentification et des rôles d’utilisateur pour l’autorisation. Cette rubrique explique comment les services WCF peuvent utiliser la même base de données pour authentifier et autoriser les utilisateurs.  
  
 [Guide pratique pour Utiliser un validateur de mot de passe et le nom d’utilisateur personnalisé](../../../../docs/framework/wcf/feature-details/how-to-use-a-custom-user-name-and-password-validator.md)  
 Montre comment intégrer un validateur personnalisé de nom d'utilisateur/mot de passe.  
  
 [Identité du service et authentification](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 En tant que dispositif de protection supplémentaire, un client peut authentifier le service en spécifiant attendu *identité* du service. Si l'identité attendue et l'identité retournée par le service ne correspondent pas, l'authentification échoue.  
  
 [Négociation et délais de sécurité](../../../../docs/framework/wcf/feature-details/security-negotiation-and-timeouts.md)  
 Décrit comment utiliser la propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> de la classe <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>.  
  
 [Débogage d’erreurs d’authentification Windows](../../../../docs/framework/wcf/feature-details/debugging-windows-authentication-errors.md)  
 Traite des problèmes courants rencontrés lors de l'utilisation de l'authentification Windows.  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Scénarios de sécurité courants](../../../../docs/framework/wcf/feature-details/common-security-scenarios.md)  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la sécurité](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [Modèle de sécurité pour Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
