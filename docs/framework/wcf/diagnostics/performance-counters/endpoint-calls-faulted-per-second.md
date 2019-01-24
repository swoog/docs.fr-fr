---
title: 'Point de terminaison : Appels ayant renvoyé une erreur par seconde'
ms.date: 03/30/2017
ms.assetid: 9840fc0a-0e4d-4638-96fd-40e3ab9e4667
ms.openlocfilehash: 3b5c881c4ce7772e197bfc1a5603636b0975143c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517654"
---
# <a name="endpoint-calls-faulted-per-second"></a><span data-ttu-id="63977-102">Point de terminaison : Appels ayant renvoyé une erreur par seconde</span><span class="sxs-lookup"><span data-stu-id="63977-102">Endpoint: Calls Faulted Per Second</span></span>
<span data-ttu-id="63977-103">Nom du compteur : Appels erronés par seconde.</span><span class="sxs-lookup"><span data-stu-id="63977-103">Counter Name: Calls Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="63977-104">Description</span><span class="sxs-lookup"><span data-stu-id="63977-104">Description</span></span>  
 <span data-ttu-id="63977-105">Nombre d'appels qui ont retourné des erreurs à ce point de terminaison en une seconde.</span><span class="sxs-lookup"><span data-stu-id="63977-105">Number of calls that have returned faults to this endpoint in a second.</span></span>  
  
 <span data-ttu-id="63977-106">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="63977-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="63977-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="63977-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="63977-108">Dans les applications Windows Communication Foundation (WCF), les méthodes de service communiquent des informations d’erreur de traitement à l’aide de messages d’erreur SOAP.</span><span class="sxs-lookup"><span data-stu-id="63977-108">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="63977-109">Les erreurs SOAP sont des types de message inclus dans les métadonnées d'une opération de service et créent, par conséquent, un contrat d'erreur permettant aux clients d'améliorer la fiabilité ou l'interactivité de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="63977-109">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="63977-110">Les erreurs SOAP étant exprimées aux clients dans un format XML, elles sont très interopérables.</span><span class="sxs-lookup"><span data-stu-id="63977-110">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63977-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63977-111">See also</span></span>
- [<span data-ttu-id="63977-112">Spécification et gestion des erreurs dans les contrats et les services</span><span class="sxs-lookup"><span data-stu-id="63977-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
