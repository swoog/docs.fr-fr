---
title: 'Point de terminaison : transactions passées par seconde'
ms.date: 03/30/2017
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
ms.openlocfilehash: 79f50b6706facd040ec2d325c676f210d5327bf8
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44175015"
---
# <a name="endpoint-transactions-flowed-per-second"></a><span data-ttu-id="c433f-102">Point de terminaison : transactions passées par seconde</span><span class="sxs-lookup"><span data-stu-id="c433f-102">Endpoint: Transactions Flowed Per Second</span></span>
<span data-ttu-id="c433f-103">Nom du compteur : transactions passées par seconde.</span><span class="sxs-lookup"><span data-stu-id="c433f-103">Counter Name: Transactions Flowed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="c433f-104">Description</span><span class="sxs-lookup"><span data-stu-id="c433f-104">Description</span></span>  
 <span data-ttu-id="c433f-105">Nombre de transactions transférées vers les opérations au niveau de ce point de terminaison en une seconde.</span><span class="sxs-lookup"><span data-stu-id="c433f-105">Number of transactions flowed to operations at this endpoint in a second.</span></span> <span data-ttu-id="c433f-106">Ce compteur est incrémenté à chaque ID de transaction présent dans un message envoyé vers le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c433f-106">This counter is incremented any time a transaction ID is present in a message sent to the endpoint.</span></span>  
  
 <span data-ttu-id="c433f-107">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="c433f-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="c433f-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="c433f-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
