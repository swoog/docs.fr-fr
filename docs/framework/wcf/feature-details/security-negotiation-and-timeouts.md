---
title: Négociation et délais de sécurité
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 508d648acf148f13076327bb312d0a0b08471ac1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33497462"
---
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="e1c6c-102">Négociation et délais de sécurité</span><span class="sxs-lookup"><span data-stu-id="e1c6c-102">Security Negotiation and Timeouts</span></span>
<span data-ttu-id="e1c6c-103">Lorsque les clients et services s’authentifient, Windows Communication Foundation (WCF) prend en charge un mode dans lequel les informations d’identification de service sont négociées dans le cadre de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="e1c6c-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="e1c6c-104">Dans un tel cas, un échange potentiellement multi-segment intervient entre le client et le service. Il permet la propagation des informations d'identification du service vers le client.</span><span class="sxs-lookup"><span data-stu-id="e1c6c-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="e1c6c-105">La propriété <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> contrôle le délai nécessaire à l'exécution de cet échange.</span><span class="sxs-lookup"><span data-stu-id="e1c6c-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="e1c6c-106">Toutefois, ce délai est appliqué uniquement lorsque l'échange nécessite plusieurs demandes-réponses.</span><span class="sxs-lookup"><span data-stu-id="e1c6c-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="e1c6c-107">Lorsque la négociation s'effectue en une seule boucle, ce délai n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e1c6c-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1c6c-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1c6c-108">See Also</span></span>  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>  
 [<span data-ttu-id="e1c6c-109">Guide pratique pour définir une variation d’horloge maximale</span><span class="sxs-lookup"><span data-stu-id="e1c6c-109">How to: Set a Max Clock Skew</span></span>](../../../../docs/framework/wcf/feature-details/how-to-set-a-max-clock-skew.md)
