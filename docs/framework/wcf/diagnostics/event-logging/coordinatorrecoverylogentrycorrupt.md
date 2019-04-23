---
title: CoordinatorRecoveryLogEntryCorrupt
ms.date: 03/30/2017
ms.assetid: 3cd0c3e3-84c8-4d43-a561-a8851c78e565
ms.openlocfilehash: faf4a07badb71588c601cd9390e4d8e3f187e629
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59121626"
---
# <a name="coordinatorrecoverylogentrycorrupt"></a><span data-ttu-id="c727e-102">CoordinatorRecoveryLogEntryCorrupt</span><span class="sxs-lookup"><span data-stu-id="c727e-102">CoordinatorRecoveryLogEntryCorrupt</span></span>
<span data-ttu-id="c727e-103">Id : 139</span><span class="sxs-lookup"><span data-stu-id="c727e-103">Id: 139</span></span>  
  
 <span data-ttu-id="c727e-104">Gravité : Error</span><span class="sxs-lookup"><span data-stu-id="c727e-104">Severity: Error</span></span>  
  
 <span data-ttu-id="c727e-105">Catégorie : TransactionBridge</span><span class="sxs-lookup"><span data-stu-id="c727e-105">Category: TransactionBridge</span></span>  
  
## <a name="description"></a><span data-ttu-id="c727e-106">Description</span><span class="sxs-lookup"><span data-stu-id="c727e-106">Description</span></span>  
 <span data-ttu-id="c727e-107">Cet événement indique qu'une entrée de journal de récupération de coordinateur a été endommagée et n'a pas pu être désérialisée.</span><span class="sxs-lookup"><span data-stu-id="c727e-107">This event indicates that a  coordinator recovery log entry was corrupt and could not be deserialized.</span></span> <span data-ttu-id="c727e-108">Cette erreur risque d'entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="c727e-108">Data loss may result from this error.</span></span> <span data-ttu-id="c727e-109">L’événement répertorie l’ID de transaction, les données de récupération (encodage Base64), l’exception, le nom de processus et l’ID de processus.</span><span class="sxs-lookup"><span data-stu-id="c727e-109">The event lists the Transaction ID, Recovery data (Base64 encoded), exception, process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c727e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c727e-110">See also</span></span>

- [<span data-ttu-id="c727e-111">Journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="c727e-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)
- [<span data-ttu-id="c727e-112">Informations de référence générales sur les événements</span><span class="sxs-lookup"><span data-stu-id="c727e-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
