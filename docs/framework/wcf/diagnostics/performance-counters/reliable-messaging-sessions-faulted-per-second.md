---
title: Sessions de messagerie fiable ayant renvoyé une erreur par seconde
ms.date: 03/30/2017
ms.assetid: 8f8ca2eb-1be4-4b6a-aa78-fcd3ee145fe8
ms.openlocfilehash: c77d6a5f12dcce15dba94e2f63025a219ebcc6fd
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44077156"
---
# <a name="reliable-messaging-sessions-faulted-per-second"></a><span data-ttu-id="ad482-102">Sessions de messagerie fiable ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="ad482-102">Reliable Messaging Sessions Faulted Per Second</span></span>
<span data-ttu-id="ad482-103">Nom du compteur : Sessions de messagerie fiable ayant renvoyé une erreur par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad482-103">Counter Name: Reliable Messaging Sessions Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ad482-104">Description</span><span class="sxs-lookup"><span data-stu-id="ad482-104">Description</span></span>  
 <span data-ttu-id="ad482-105">Nombre de sessions de messagerie fiable ayant renvoyé une erreur dans ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="ad482-105">Number of reliable messaging sessions that are faulted in this service in a second.</span></span>  
  
 <span data-ttu-id="ad482-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="ad482-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="ad482-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="ad482-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
