---
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: f3474fc1bb0ed0d11df6289ed6470447d815f5ce
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33475749"
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a><span data-ttu-id="1ccf1-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span><span class="sxs-lookup"><span data-stu-id="1ccf1-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span></span>
<span data-ttu-id="1ccf1-103">Une exception s'est produite en fermant les connexions dans ce pool de connexions.</span><span class="sxs-lookup"><span data-stu-id="1ccf1-103">An exception occurred while closing the connections in this connection pool.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1ccf1-104">Description</span><span class="sxs-lookup"><span data-stu-id="1ccf1-104">Description</span></span>  
 <span data-ttu-id="1ccf1-105">Ce suivi de niveau d’erreur indique qu’une erreur s’est produite en fermant les pools de connexion utilisés par la connexion de Windows Communication Foundation (WCF) de fonctionnalité de regroupement.</span><span class="sxs-lookup"><span data-stu-id="1ccf1-105">This error level trace indicates that an error has occurred while closing the connection pools used by Windows Communication Foundation (WCF)’s connection pooling feature.</span></span> <span data-ttu-id="1ccf1-106">L'une des raisons possibles est l'échec de la fermeture d'une connexion en groupe, ou d'un jeu de connexions en groupe, dans CloseTimeout.</span><span class="sxs-lookup"><span data-stu-id="1ccf1-106">One possible reason for this is an unsuccessful closure of a pooled connection, or a set of pooled connections within the CloseTimeout.</span></span> <span data-ttu-id="1ccf1-107">Lorsque cette exception est levée, toutes les connexions ouvertes restantes dans ce pool sont abandonnées ; les connexions ouvertes dans d'autres pools sont abandonnées.</span><span class="sxs-lookup"><span data-stu-id="1ccf1-107">When this exception is thrown, any remaining unclosed connections within that pool are aborted; unclosed connections within other pools are abandoned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ccf1-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ccf1-108">See Also</span></span>  
 [<span data-ttu-id="1ccf1-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="1ccf1-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="1ccf1-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="1ccf1-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="1ccf1-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="1ccf1-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
