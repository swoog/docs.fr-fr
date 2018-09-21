---
title: 'Service : appels de sécurité non autorisés par seconde'
ms.date: 03/30/2017
ms.assetid: 1eeade5a-ea62-4757-b1f9-1b1b1746abd1
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: f2c921991f059d7dfe5661dfe688ec9675d0d5fe
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46528224"
---
# <a name="service-security-calls-not-authorized-per-second"></a><span data-ttu-id="5c852-102">Service : appels de sécurité non autorisés par seconde</span><span class="sxs-lookup"><span data-stu-id="5c852-102">Service: Security Calls Not Authorized Per Second</span></span>
<span data-ttu-id="5c852-103">Nom du compteur : appels de sécurité non autorisés par seconde.</span><span class="sxs-lookup"><span data-stu-id="5c852-103">Counter name: Security Calls Not Authorized Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="5c852-104">Description</span><span class="sxs-lookup"><span data-stu-id="5c852-104">Description</span></span>  
 <span data-ttu-id="5c852-105">Nombre de messages entrants par seconde qui proviennent d’un utilisateur valide et sont correctement protégés, mais pour lesquels l’utilisateur n’est pas autorisé à effectuer des tâches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5c852-105">Number of incoming messages in one second, which are from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="5c852-106">Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="5c852-106">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span>  
  
 <span data-ttu-id="5c852-107">Ce compteur est de type de compteur de performances [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkId=94649), dont la valeur est calculée à l’aide de la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="5c852-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkId=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="5c852-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="5c852-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
