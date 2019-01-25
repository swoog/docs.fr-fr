---
title: System.ServiceModel.Channels.FailedPipeConnect
ms.date: 03/30/2017
ms.assetid: 9a827e0f-fb91-46bb-bd54-926d4b74d8a6
ms.openlocfilehash: 22d2605c3c96c0e030f9e435293de42094965cb7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627942"
---
# <a name="systemservicemodelchannelsfailedpipeconnect"></a><span data-ttu-id="1d3b7-102">System.ServiceModel.Channels.FailedPipeConnect</span><span class="sxs-lookup"><span data-stu-id="1d3b7-102">System.ServiceModel.Channels.FailedPipeConnect</span></span>
<span data-ttu-id="1d3b7-103">Une tentative de connexion au point de terminaison du canal nommé a échoué.</span><span class="sxs-lookup"><span data-stu-id="1d3b7-103">An attempt to connect to the named pipe endpoint failed.</span></span> <span data-ttu-id="1d3b7-104">Une autre tentative est effectuée dans le délai d'attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="1d3b7-104">Another attempt is made within the specified timeout period.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1d3b7-105">Description</span><span class="sxs-lookup"><span data-stu-id="1d3b7-105">Description</span></span>  
 <span data-ttu-id="1d3b7-106">Ce suivi d'informations indique l'échec d'une connexion à un point de terminaison de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="1d3b7-106">This informational trace indicates a failure to connect to a named pipe endpoint.</span></span> <span data-ttu-id="1d3b7-107">Cela peut se produire si le point de terminaison de canal nommé est introuvable ou occupé.</span><span class="sxs-lookup"><span data-stu-id="1d3b7-107">This could happen if the named pipe endpoint is not found or is busy.</span></span> <span data-ttu-id="1d3b7-108">D'autres tentatives sont effectuées, chacune séparée par un bref lapse de temps jusqu'à ce que l'une réussisse ou que OpenTimeout expire.</span><span class="sxs-lookup"><span data-stu-id="1d3b7-108">Additional attempts are made, each separated by a short amount of time, until one succeeds or the OpenTimeout expires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d3b7-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d3b7-109">See also</span></span>
- [<span data-ttu-id="1d3b7-110">Suivi</span><span class="sxs-lookup"><span data-stu-id="1d3b7-110">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)
- [<span data-ttu-id="1d3b7-111">Utilisation du suivi pour résoudre les problèmes posés par votre application</span><span class="sxs-lookup"><span data-stu-id="1d3b7-111">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="1d3b7-112">Administration et diagnostics</span><span class="sxs-lookup"><span data-stu-id="1d3b7-112">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
