---
title: 'Point de terminaison : appels de sécurité non autorisés'
ms.date: 03/30/2017
ms.assetid: d25095ff-9ff0-4c69-a674-4e6a9fe3f4dc
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: b449aaad65f01a5f4835f8335543220383543984
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33471254"
---
# <a name="endpoint-security-calls-not-authorized"></a><span data-ttu-id="1ba1b-102">Point de terminaison : appels de sécurité non autorisés</span><span class="sxs-lookup"><span data-stu-id="1ba1b-102">Endpoint: Security Calls Not Authorized</span></span>
<span data-ttu-id="1ba1b-103">Nom du compteur : Appels de sécurité non autorisés.</span><span class="sxs-lookup"><span data-stu-id="1ba1b-103">Counter Name: Security Calls Not Authorized.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1ba1b-104">Description</span><span class="sxs-lookup"><span data-stu-id="1ba1b-104">Description</span></span>  
 <span data-ttu-id="1ba1b-105">Ce compteur est incrémenté lorsque la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> retourne la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="1ba1b-105">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span> <span data-ttu-id="1ba1b-106">Il indique que le message entrant provient d'un utilisateur valide et qu'il est correctement protégé, mais que l'utilisateur n'est pas autorisé à exécuter des tâches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1ba1b-106">It indicates that the incoming message is from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>
