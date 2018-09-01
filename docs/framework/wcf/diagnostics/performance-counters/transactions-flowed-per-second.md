---
title: Transactions passées par seconde
ms.date: 03/30/2017
ms.assetid: b9f661e1-576c-48fc-9fdf-91853e0749e8
ms.openlocfilehash: e77aef4cfff1e64f112e720183675dfb7aa25d27
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43392934"
---
# <a name="transactions-flowed-per-second"></a><span data-ttu-id="45ad8-102">Transactions passées par seconde</span><span class="sxs-lookup"><span data-stu-id="45ad8-102">Transactions Flowed Per Second</span></span>
<span data-ttu-id="45ad8-103">Nom du compteur : transactions passées par seconde</span><span class="sxs-lookup"><span data-stu-id="45ad8-103">Counter Name:  Transactions Flowed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="45ad8-104">Description</span><span class="sxs-lookup"><span data-stu-id="45ad8-104">Description</span></span>  
 <span data-ttu-id="45ad8-105">Nombre de transactions transmises à cette opération en une seconde.</span><span class="sxs-lookup"><span data-stu-id="45ad8-105">Number of transactions flowed to this operation in a second.</span></span> <span data-ttu-id="45ad8-106">Ce compteur est incrémenté à chaque fois qu’un ID de transaction est présent dans un message envoyé à l’opération.</span><span class="sxs-lookup"><span data-stu-id="45ad8-106">This counter is incremented any time a transaction ID is present in a message that is sent to the operation.</span></span>  
  
 <span data-ttu-id="45ad8-107">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="45ad8-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="45ad8-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="45ad8-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
