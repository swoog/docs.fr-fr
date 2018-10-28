---
title: 'Point de terminaison : appels de sécurité non autorisés par seconde'
ms.date: 03/30/2017
ms.assetid: c8a1547b-986b-45c1-b302-dea0cd4b516d
ms.openlocfilehash: c62bec570daf8b107ca0540871eb6eac43ca2d7e
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188350"
---
# <a name="endpoint-security-calls-not-authorized-per-second"></a><span data-ttu-id="44f54-102">Point de terminaison : appels de sécurité non autorisés par seconde</span><span class="sxs-lookup"><span data-stu-id="44f54-102">Endpoint: Security Calls Not Authorized Per Second</span></span>
<span data-ttu-id="44f54-103">Nom du compteur : Appels de sécurité non autorisés par seconde.</span><span class="sxs-lookup"><span data-stu-id="44f54-103">Counter Name: Security Calls Not Authorized Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="44f54-104">Description</span><span class="sxs-lookup"><span data-stu-id="44f54-104">Description</span></span>  
 <span data-ttu-id="44f54-105">Nombre de messages entrants en une seconde qui proviennent d'un utilisateur valide et sont protégés correctement, mais pour lesquels l'utilisateur n'est pas autorisé à effectuer des tâches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="44f54-105">Number of incoming messages in a second that are from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="44f54-106">Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="44f54-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span>  
  
 <span data-ttu-id="44f54-107">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="44f54-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="44f54-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="44f54-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
