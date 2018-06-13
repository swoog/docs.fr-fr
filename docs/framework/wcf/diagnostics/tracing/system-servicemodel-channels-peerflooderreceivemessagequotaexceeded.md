---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 5c1e6c51ffd5aeafe65a67c8989f554ebf0824d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33478915"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a><span data-ttu-id="b5eaa-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span><span class="sxs-lookup"><span data-stu-id="b5eaa-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span></span>
<span data-ttu-id="b5eaa-103">Le taux de réception entrant des messages est trop élevé.</span><span class="sxs-lookup"><span data-stu-id="b5eaa-103">The inbound receive rate of messages is too high.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b5eaa-104">Description</span><span class="sxs-lookup"><span data-stu-id="b5eaa-104">Description</span></span>  
 <span data-ttu-id="b5eaa-105">Ce suivi se produit lors de la tentative de traitement des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="b5eaa-105">This trace occurs when attempting to process inbound messages.</span></span> <span data-ttu-id="b5eaa-106">Un message n'a pas pu être transmis à un voisin spécifique en raison du dépassement du quota défini pour ce voisin.</span><span class="sxs-lookup"><span data-stu-id="b5eaa-106">A message could not be forwarded to a specific neighbor because the quota set for that neighbor has been exceeded.</span></span> <span data-ttu-id="b5eaa-107">Ce cas se produit lorsqu'un voisin qui ne répond pas ne peut pas effacer un journal des travaux en souffrance avec messages en attente pour ce voisin.</span><span class="sxs-lookup"><span data-stu-id="b5eaa-107">This occurs when an unresponsive neighbor fails to clear a backlog of messages pending for that neighbor.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="b5eaa-108">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="b5eaa-108">Troubleshooting</span></span>  
 <span data-ttu-id="b5eaa-109">Réduisez le taux auquel les messages sont envoyés dans la maille.</span><span class="sxs-lookup"><span data-stu-id="b5eaa-109">Reduce the rate at which messages are sent within the mesh.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5eaa-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5eaa-110">See Also</span></span>  
 [<span data-ttu-id="b5eaa-111">Suivi</span><span class="sxs-lookup"><span data-stu-id="b5eaa-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="b5eaa-112">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="b5eaa-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="b5eaa-113">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="b5eaa-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
