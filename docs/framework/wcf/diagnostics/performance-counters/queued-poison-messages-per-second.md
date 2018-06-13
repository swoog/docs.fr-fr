---
title: Messages incohérents en file d'attente par seconde
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: 6407cce120f5d534f88a12591ea2ad09bb5130d8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473257"
---
# <a name="queued-poison-messages-per-second"></a><span data-ttu-id="06766-102">Messages incohérents en file d'attente par seconde</span><span class="sxs-lookup"><span data-stu-id="06766-102">Queued Poison Messages Per Second</span></span>
<span data-ttu-id="06766-103">Nom du compteur : Messages incohérents en file d'attente par seconde.</span><span class="sxs-lookup"><span data-stu-id="06766-103">Counter Name: Queued Poison Messages Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="06766-104">Description</span><span class="sxs-lookup"><span data-stu-id="06766-104">Description</span></span>  
 <span data-ttu-id="06766-105">Nombre de messages vers ce service marqués comme incohérents par le transport de mise en file d'attente par seconde.</span><span class="sxs-lookup"><span data-stu-id="06766-105">Number of messages that are marked poisoned by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="06766-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="06766-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="06766-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="06766-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
