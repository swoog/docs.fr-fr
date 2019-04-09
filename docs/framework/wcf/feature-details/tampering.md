---
title: Falsification
ms.date: 03/30/2017
ms.assetid: 3bad93be-60bb-4f89-96ab-a1c3dc7c0fad
ms.openlocfilehash: 7a4265c30a6713f9557de2b3d1e99c87b7dd3e58
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59107885"
---
# <a name="tampering"></a>Falsification
*Falsification* est l’action de modification d’un message ou la remise d’un message et à l’aide de ce message modifié à un usage autre que celles prévues pour.  
  
## <a name="do-not-disable-ws-addressing"></a>Ne pas désactiver WS-Addressing  
 La spécification WS-Addressing fournit des en-têtes d'adresse sur chaque message, ce qui permet au destinataire d'un message de vérifier l'expéditeur de celui-ci. Vous pouvez désactiver cette fonctionnalité en affectant <xref:System.ServiceModel.Channels.MessageVersion.Addressing%2A> à la propriété <xref:System.ServiceModel.Channels.AddressingVersion.None%2A>.  
  
 Si le mode de sécurité a la valeur Message et que WS-Addressing est désactivé, un intrus peut prendre la demande d'un client et l'envoyer à un autre service, le deuxième service n'ayant aucun moyen de détecter que le message est provenu du client d'origine. En effet, le premier service peut prétendre qu'il est un client lorsqu'il parle au deuxième service.  
  
 Pour atténuer ce risque, n'affectez jamais <xref:System.ServiceModel.Channels.MessageVersion.Addressing%2A> à la propriété <xref:System.ServiceModel.Channels.AddressingVersion.None%2A> et évitez d'utiliser <xref:System.ServiceModel.Channels.MessageVersion>, tel que la propriété statique <xref:System.ServiceModel.Channels.MessageVersion.Soap12%2A>, qui affecte <xref:System.ServiceModel.Channels.MessageVersion.Addressing%2A> à la propriété <xref:System.ServiceModel.Channels.AddressingVersion.None%2A>.  
  
## <a name="see-also"></a>Voir aussi

- [Considérations relatives à la sécurité](../../../../docs/framework/wcf/feature-details/security-considerations-in-wcf.md)
- [Divulgation d'informations](../../../../docs/framework/wcf/feature-details/information-disclosure.md)
- [Élévation de privilège](../../../../docs/framework/wcf/feature-details/elevation-of-privilege.md)
- [Refus de service](../../../../docs/framework/wcf/feature-details/denial-of-service.md)
- [Scénarios non pris en charge](../../../../docs/framework/wcf/feature-details/unsupported-scenarios.md)
- [Attaques par relecture](../../../../docs/framework/wcf/feature-details/replay-attacks.md)
