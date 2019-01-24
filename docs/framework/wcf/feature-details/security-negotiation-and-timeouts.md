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
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="2d0dc-102">Négociation et délais de sécurité</span><span class="sxs-lookup"><span data-stu-id="2d0dc-102">Security Negotiation and Timeouts</span></span>
<span data-ttu-id="2d0dc-103">Lorsque les clients et les services s’authentifient, Windows Communication Foundation (WCF) prend en charge un mode où les informations d’identification de service sont négociée dans le cadre de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="2d0dc-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="2d0dc-104">Dans un tel cas, un échange potentiellement multi-segment intervient entre le client et le service. Il permet la propagation des informations d'identification du service vers le client.</span><span class="sxs-lookup"><span data-stu-id="2d0dc-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="2d0dc-105">La propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> contrôle le délai nécessaire à l'exécution de cet échange.</span><span class="sxs-lookup"><span data-stu-id="2d0dc-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="2d0dc-106">Toutefois, ce délai est appliqué uniquement lorsque l'échange nécessite plusieurs demandes-réponses.</span><span class="sxs-lookup"><span data-stu-id="2d0dc-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="2d0dc-107">Lorsque la négociation s'effectue en une seule boucle, ce délai n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2d0dc-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d0dc-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d0dc-108">See also</span></span>
- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="2d0dc-109">Guide pratique pour Ensemble une variation d’horloge maximale</span><span class="sxs-lookup"><span data-stu-id="2d0dc-109">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
