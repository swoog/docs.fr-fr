---
title: Considérations sur la sécurité pour les sessions sécurisées
ms.date: 03/30/2017
ms.assetid: 0d5be591-9a7b-4a6f-a906-95d3abafe8db
ms.openlocfilehash: d2244ba42b1cf95f77424d32a19ebe11dd3a2a45
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59148705"
---
# <a name="security-considerations-for-secure-sessions"></a>Considérations sur la sécurité pour les sessions sécurisées
Vous devez tenir compte des éléments suivants qui affectent la sécurité lors de l'implémentation de sessions sécurisées. Pour plus d’informations sur les considérations de sécurité, consultez [considérations de sécurité](../../../../docs/framework/wcf/feature-details/security-considerations-in-wcf.md) et [meilleures pratiques pour la sécurité](../../../../docs/framework/wcf/feature-details/best-practices-for-security-in-wcf.md).  
  
## <a name="secure-sessions-and-metadata"></a>Sessions sécurisées et métadonnées  
 Lorsqu’une session sécurisée est établie et les <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters.RequireCancellation%2A> propriété est définie sur `false`, Windows Communication Foundation (WCF) envoie une `mssp:MustNotSendCancel` assertion dans le cadre des métadonnées dans le document Web Services Description Language (WSDL) pour le point de terminaison de service. L'assertion `mssp:MustNotSendCancel` informe les clients que le service ne répond pas aux demandes d'annulation de session sécurisée. Lorsque le <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters.RequireCancellation%2A> propriété est définie sur `true`, puis WCF n’émet pas un `mssp:MustNotSendCancel` assertion dans le document WSDL. Lorsqu'ils n'ont plus besoin de la session sécurisée, les clients doivent envoyer une demande d'annulation au service. Lorsqu’un client est généré à l’aide de la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md), le code client réagit en conséquence à la présence ou l’absence de la `mssp:MustNotSendCancel` assertion.  
  
## <a name="secure-conversations-and-custom-tokens"></a>Conversations sécurisées et jetons personnalisés  
 Le mélange de jetons personnalisés et de clés dérivées pose quelques problèmes en raison de la manière dont il est défini dans la spécification WS-SecureConversation. La spécification stipule que `wsse:SecurityTokenReference` est un élément facultatif qui référence le jeton dérivé : "`/wsc:DerivedKeyToken/wsse:SecurityTokenReference` Cet élément facultatif est utilisé pour spécifier le jeton de contexte de sécurité, le jeton de sécurité ou la clé/le secret partagé utilisé pour la dérivation. Si cet élément n'est pas spécifié, il est supposé que le destinataire peut déterminer la clé partagée à partir du contexte de message. Si le contexte ne peut pas être déterminé, puis une erreur telle que `wsc:UnknownDerivationSource` doit être déclenché. »  
  
 Cela signifie que si vous souhaitez qu'un jeton personnalisé soit dérivé, vous devez encapsuler son type de clause dans un élément `SecurityTokenReference`. Il est possible de désactiver la dérivation mais la valeur par défaut consiste à dériver les clés. Si vous ne parvenez pas à encapsuler la clé, la sérialisation du jeton de clé dérivé aboutit, mais la tentative de désérialisation de ce jeton lève une exception.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : désactiver des sessions sécurisées sur un WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)
- [Considérations relatives à la sécurité](../../../../docs/framework/wcf/feature-details/security-considerations-in-wcf.md)
- [Bonnes pratiques pour la sécurité](../../../../docs/framework/wcf/feature-details/best-practices-for-security-in-wcf.md)
