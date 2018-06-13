---
title: CoordinatorRecoveryLogEntryCorrupt
ms.date: 03/30/2017
ms.assetid: 3cd0c3e3-84c8-4d43-a561-a8851c78e565
ms.openlocfilehash: 3f51d1269f5ca89f4f02257c8accef3423aa7eb5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33472681"
---
# <a name="coordinatorrecoverylogentrycorrupt"></a><span data-ttu-id="25739-102">CoordinatorRecoveryLogEntryCorrupt</span><span class="sxs-lookup"><span data-stu-id="25739-102">CoordinatorRecoveryLogEntryCorrupt</span></span>
<span data-ttu-id="25739-103">ID : 139</span><span class="sxs-lookup"><span data-stu-id="25739-103">Id: 139</span></span>  
  
 <span data-ttu-id="25739-104">Gravité : Erreur</span><span class="sxs-lookup"><span data-stu-id="25739-104">Severity: Error</span></span>  
  
 <span data-ttu-id="25739-105">Catégorie : TransactionBridge</span><span class="sxs-lookup"><span data-stu-id="25739-105">Category: TransactionBridge</span></span>  
  
## <a name="description"></a><span data-ttu-id="25739-106">Description</span><span class="sxs-lookup"><span data-stu-id="25739-106">Description</span></span>  
 <span data-ttu-id="25739-107">Cet événement indique qu'une entrée de journal de récupération de coordinateur a été endommagée et n'a pas pu être désérialisée.</span><span class="sxs-lookup"><span data-stu-id="25739-107">This event indicates that a  coordinator recovery log entry was corrupt and could not be deserialized.</span></span> <span data-ttu-id="25739-108">Cette erreur risque d'entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="25739-108">Data loss may result from this error.</span></span> <span data-ttu-id="25739-109">L’événement répertorie l’ID de transaction, les données de récupération (encodage Base64), l’exception, le nom de processus et l’ID de processus.</span><span class="sxs-lookup"><span data-stu-id="25739-109">The event lists the Transaction ID, Recovery data (Base64 encoded), exception, process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25739-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25739-110">See Also</span></span>  
 [<span data-ttu-id="25739-111">Journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="25739-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)  
 [<span data-ttu-id="25739-112">Informations de référence générales sur les événements</span><span class="sxs-lookup"><span data-stu-id="25739-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
