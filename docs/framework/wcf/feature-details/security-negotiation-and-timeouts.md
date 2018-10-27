---
title: Négociation et délais de sécurité
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: dfabdb05c7658e3cf9eb5b325597360bbc0bb588
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50037796"
---
# <a name="security-negotiation-and-timeouts"></a>Négociation et délais de sécurité
Lorsque les clients et les services s’authentifient, Windows Communication Foundation (WCF) prend en charge un mode où les informations d’identification de service sont négociée dans le cadre de l’authentification. Dans un tel cas, un échange potentiellement multi-segment intervient entre le client et le service. Il permet la propagation des informations d'identification du service vers le client. La propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> contrôle le délai nécessaire à l'exécution de cet échange. Toutefois, ce délai est appliqué uniquement lorsque l'échange nécessite plusieurs demandes-réponses. Lorsque la négociation s'effectue en une seule boucle, ce délai n'est pas utilisé.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>  
 [Guide pratique pour définir une variation d’horloge maximale](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
