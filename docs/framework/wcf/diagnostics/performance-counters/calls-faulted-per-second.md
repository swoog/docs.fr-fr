---
title: Appels ayant renvoyé une erreur par seconde
ms.date: 03/30/2017
ms.assetid: 81c88073-8e32-4520-a71a-2c56b71ee515
ms.openlocfilehash: dd35e4096ab4e2740c638903975af085b01a1fbf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640119"
---
# <a name="calls-faulted-per-second"></a><span data-ttu-id="b1d14-102">Appels ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="b1d14-102">Calls Faulted Per Second</span></span>
<span data-ttu-id="b1d14-103">Nom du compteur : Appels ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="b1d14-103">Counter Name: Calls Faulted Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="b1d14-104">Description</span><span class="sxs-lookup"><span data-stu-id="b1d14-104">Description</span></span>  
 <span data-ttu-id="b1d14-105">Nombre d'appels qui ont retourné des erreurs pour cette opération en une seconde.</span><span class="sxs-lookup"><span data-stu-id="b1d14-105">Number of calls that returned faults to this operation in a second.</span></span>  
  
 <span data-ttu-id="b1d14-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="b1d14-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="b1d14-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="b1d14-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="b1d14-108">Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="b1d14-108">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="b1d14-109">Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="b1d14-109">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="b1d14-110">Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.</span><span class="sxs-lookup"><span data-stu-id="b1d14-110">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1d14-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1d14-111">See also</span></span>
- [<span data-ttu-id="b1d14-112">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="b1d14-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
