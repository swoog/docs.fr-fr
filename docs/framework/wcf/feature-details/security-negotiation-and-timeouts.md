---
title: Négociation et délais de sécurité
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: 38dce9bd6587850a5e3327600bb8bc13c48b93e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54592612"
---
# <a name="security-negotiation-and-timeouts"></a>Négociation et délais de sécurité
Lorsque les clients et les services s’authentifient, Windows Communication Foundation (WCF) prend en charge un mode où les informations d’identification de service sont négociée dans le cadre de l’authentification. Dans un tel cas, un échange potentiellement multi-segment intervient entre le client et le service. Il permet la propagation des informations d'identification du service vers le client. La propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> contrôle le délai nécessaire à l'exécution de cet échange. Toutefois, ce délai est appliqué uniquement lorsque l'échange nécessite plusieurs demandes-réponses. Lorsque la négociation s'effectue en une seule boucle, ce délai n'est pas utilisé.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [Guide pratique pour Ensemble une variation d’horloge maximale](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
