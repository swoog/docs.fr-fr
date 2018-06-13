---
title: Messages rejetés par le transport de mise en file d'attente par seconde
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: 31091c6c9dd04ecd7294f69f9611f25e401df724
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473443"
---
# <a name="queued-rejected-messages-per-second"></a><span data-ttu-id="a64be-102">Messages rejetés par le transport de mise en file d'attente par seconde</span><span class="sxs-lookup"><span data-stu-id="a64be-102">Queued Rejected Messages Per Second</span></span>
<span data-ttu-id="a64be-103">Nom du compteur : Messages rejetés par le transport de mise en file d'attente par seconde.</span><span class="sxs-lookup"><span data-stu-id="a64be-103">Counter Name: Queued Messages Rejected Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a64be-104">Description</span><span class="sxs-lookup"><span data-stu-id="a64be-104">Description</span></span>  
 <span data-ttu-id="a64be-105">Nombre de messages vers ce service qui ont été rejetés par le transport de mise en file d'attente en une seconde.</span><span class="sxs-lookup"><span data-stu-id="a64be-105">Number of messages that are rejected by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="a64be-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="a64be-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="a64be-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="a64be-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
