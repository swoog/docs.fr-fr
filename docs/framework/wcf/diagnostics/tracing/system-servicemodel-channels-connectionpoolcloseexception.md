---
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: 3dd28276cd3a39497c0387f5b9d0adec23d07c37
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666831"
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a><span data-ttu-id="cb87f-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span><span class="sxs-lookup"><span data-stu-id="cb87f-102">System.ServiceModel.Channels.ConnectionPoolCloseException</span></span>
<span data-ttu-id="cb87f-103">Une exception s'est produite en fermant les connexions dans ce pool de connexions.</span><span class="sxs-lookup"><span data-stu-id="cb87f-103">An exception occurred while closing the connections in this connection pool.</span></span>  
  
## <a name="description"></a><span data-ttu-id="cb87f-104">Description</span><span class="sxs-lookup"><span data-stu-id="cb87f-104">Description</span></span>  
 <span data-ttu-id="cb87f-105">Ce suivi de niveau d’erreur indique qu’une erreur s’est produite lors de la fermeture les pools de connexions utilisés par la connexion de Windows Communication Foundation (WCF) de fonctionnalité de regroupement.</span><span class="sxs-lookup"><span data-stu-id="cb87f-105">This error level trace indicates that an error has occurred while closing the connection pools used by Windows Communication Foundation (WCF)’s connection pooling feature.</span></span> <span data-ttu-id="cb87f-106">L'une des raisons possibles est l'échec de la fermeture d'une connexion en groupe, ou d'un jeu de connexions en groupe, dans CloseTimeout.</span><span class="sxs-lookup"><span data-stu-id="cb87f-106">One possible reason for this is an unsuccessful closure of a pooled connection, or a set of pooled connections within the CloseTimeout.</span></span> <span data-ttu-id="cb87f-107">Lorsque cette exception est levée, toutes les connexions ouvertes restantes dans ce pool sont abandonnées ; les connexions ouvertes dans d'autres pools sont abandonnées.</span><span class="sxs-lookup"><span data-stu-id="cb87f-107">When this exception is thrown, any remaining unclosed connections within that pool are aborted; unclosed connections within other pools are abandoned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb87f-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb87f-108">See also</span></span>

- [<span data-ttu-id="cb87f-109">Suivi</span><span class="sxs-lookup"><span data-stu-id="cb87f-109">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="cb87f-110">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="cb87f-110">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="cb87f-111">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="cb87f-111">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
