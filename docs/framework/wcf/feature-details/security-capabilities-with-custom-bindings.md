---
title: Fonctionnalités de sécurité avec des liaisons personnalisées
ms.date: 03/30/2017
ms.assetid: a2425679-484a-4e6c-9c98-7da7304f1516
ms.openlocfilehash: 25d203fa706eeb0d0ccf1eaf4367ffa5bd7b83aa
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157272"
---
# <a name="security-capabilities-with-custom-bindings"></a>Fonctionnalités de sécurité avec des liaisons personnalisées
Vous pouvez effectuer la plupart des tâches de sécurité courantes en utilisant l'une des liaisons fournies par le système. Toutefois, si vous avez besoin de plus de contrôle, vous pouvez créer une liaison personnalisée à l'aide de <xref:System.ServiceModel.Channels.SecurityBindingElement>, comme expliqué dans les rubriques suivantes. Pour plus d’informations sur les liaisons personnalisées, consultez [liaisons personnalisées](../../../../docs/framework/wcf/extending/custom-bindings.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Modes d'authentification SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)  
 Décrit les modes d’authentification possibles avec une liaison personnalisée.  
  
 [Procédure : créer une liaison personnalisée à l’aide de SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)  
 Décrit les étapes de base pour créer une liaison personnalisée avec un élément de sécurité.  
  
 [Procédure : créer un SecurityBindingElement pour un mode d’authentification spécifié](../../../../docs/framework/wcf/feature-details/how-to-create-a-securitybindingelement-for-a-specified-authentication-mode.md)  
 Décrit comment créer un élément de sécurité pour un mode d'authentification spécifié.  
  
 [Procédure : désactiver des sessions sécurisées sur un WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)  
 Décrit comment désactiver des sessions sécurisées lors de la création d'un service FS.  
  
 [Procédure : activer la détection de réexécution des messages](../../../../docs/framework/wcf/feature-details/how-to-enable-message-replay-detection.md)  
 Décrit comment déterminer le moment où une attaque par relecture se produit.  
  
 [Procédure : créer des informations d’identification de prise en charge](../../../../docs/framework/wcf/feature-details/how-to-create-a-supporting-credential.md)  
 Décrit comment fournir des informations d'identification de prise en charge à un service, si ce dernier en a besoin.  
  
 [Procédure : configurer une confirmation de signature](../../../../docs/framework/wcf/feature-details/how-to-set-up-a-signature-confirmation.md)  
 Décrit les étapes permettant de confirmer des signatures lors de la signature numérique de messages.  
  
 [Procédure : définir une inclinaison de l’horloge maximale](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)  
 Décrit comment définir la différence de temps maximale autorisée entre un service et un client.  
  
 [Procédure : désactiver le chiffrement des signatures numériques](../../../../docs/framework/wcf/feature-details/how-to-disable-encryption-of-digital-signatures.md)  
 Décrit les avantages de la désactivation du chiffrement des signatures numériques en matière de performances.  
  
## <a name="reference"></a>Référence  
 <xref:System.ServiceModel.Channels.SecurityBindingElement>  
  
 [\<security>](../../../../docs/framework/configure-apps/file-schema/wcf/security-of-custombinding.md)  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Fonctionnement des niveaux de protection](../../../../docs/framework/wcf/understanding-protection-level.md)  
  
 [Sécurisation des services et des clients](../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
  
## <a name="see-also"></a>Voir aussi

- [Liaisons et sécurité](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)
- [Vue d'ensemble de la sécurité](../../../../docs/framework/wcf/feature-details/security-overview.md)
- [Liaisons fournies par le système](../../../../docs/framework/wcf/system-provided-bindings.md)
