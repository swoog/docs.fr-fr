---
title: Négociation et délais de sécurité
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: a02c9d7b42eadf9a5ce9af8022fe292d6c23249c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59180640"
---
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="dfee0-102">Négociation et délais de sécurité</span><span class="sxs-lookup"><span data-stu-id="dfee0-102">Security Negotiation and Timeouts</span></span>
<span data-ttu-id="dfee0-103">Lorsque les clients et les services s’authentifient, Windows Communication Foundation (WCF) prend en charge un mode où les informations d’identification de service sont négociée dans le cadre de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="dfee0-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="dfee0-104">Dans un tel cas, un échange potentiellement multi-segment intervient entre le client et le service. Il permet la propagation des informations d'identification du service vers le client.</span><span class="sxs-lookup"><span data-stu-id="dfee0-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="dfee0-105">La propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> contrôle le délai nécessaire à l'exécution de cet échange.</span><span class="sxs-lookup"><span data-stu-id="dfee0-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="dfee0-106">Toutefois, ce délai est appliqué uniquement lorsque l'échange nécessite plusieurs demandes-réponses.</span><span class="sxs-lookup"><span data-stu-id="dfee0-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="dfee0-107">Lorsque la négociation s'effectue en une seule boucle, ce délai n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="dfee0-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfee0-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfee0-108">See also</span></span>

- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="dfee0-109">Guide pratique pour Ensemble une variation d’horloge maximale</span><span class="sxs-lookup"><span data-stu-id="dfee0-109">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
