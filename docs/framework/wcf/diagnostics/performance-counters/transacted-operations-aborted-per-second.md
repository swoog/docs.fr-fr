---
title: Nombre d'opérations traitées abandonnées par seconde
ms.date: 03/30/2017
ms.assetid: 19fc993f-2b3d-4898-852e-3b98ec2153a5
ms.openlocfilehash: 6369fea6def5ebb6b62274caed31d5fb63b3b0e1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43500557"
---
# <a name="transacted-operations-aborted-per-second"></a><span data-ttu-id="e3c75-102">Nombre d'opérations traitées abandonnées par seconde</span><span class="sxs-lookup"><span data-stu-id="e3c75-102">Transacted Operations Aborted Per Second</span></span>
<span data-ttu-id="e3c75-103">Nom du compteur : nombre d'opérations traitées abandonnées par seconde.</span><span class="sxs-lookup"><span data-stu-id="e3c75-103">Counter Name: Transacted Operations Aborted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e3c75-104">Description</span><span class="sxs-lookup"><span data-stu-id="e3c75-104">Description</span></span>  
 <span data-ttu-id="e3c75-105">Nombre d’opérations transactionnelles abandonnées dans ce service par seconde.</span><span class="sxs-lookup"><span data-stu-id="e3c75-105">Number of transactional operations that have been aborted in this service in a second.</span></span>  
  
 <span data-ttu-id="e3c75-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="e3c75-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="e3c75-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="e3c75-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
