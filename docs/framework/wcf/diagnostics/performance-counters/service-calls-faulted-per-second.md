---
title: 'Service : appels ayant renvoyé une erreur par seconde'
ms.date: 03/30/2017
ms.assetid: 94247356-2b29-4b50-b639-91ca8c1cf3a9
ms.openlocfilehash: 86eddc62fb9aec8eced49ae70865583f3a50eb85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33474098"
---
# <a name="service-calls-faulted-per-second"></a><span data-ttu-id="8b8f2-102">Service : appels ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="8b8f2-102">Service: Calls Faulted Per Second</span></span>
<span data-ttu-id="8b8f2-103">Nom du compteur : appels ayant renvoyé une erreur par seconde.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-103">Counter Name: Calls Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8b8f2-104">Description</span><span class="sxs-lookup"><span data-stu-id="8b8f2-104">Description</span></span>  
 <span data-ttu-id="8b8f2-105">Nombre d'appels qui ont retourné des erreurs à ce service en une seconde.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-105">Number of calls that have returned faults to this service in a second.</span></span>  
  
 <span data-ttu-id="8b8f2-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="8b8f2-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="8b8f2-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="8b8f2-108">Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-108">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="8b8f2-109">Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-109">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="8b8f2-110">Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.</span><span class="sxs-lookup"><span data-stu-id="8b8f2-110">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b8f2-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b8f2-111">See Also</span></span>  
 [<span data-ttu-id="8b8f2-112">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="8b8f2-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
