---
title: CoordinatorRecoveryLogEntryCorrupt
ms.date: 03/30/2017
ms.assetid: 3cd0c3e3-84c8-4d43-a561-a8851c78e565
ms.openlocfilehash: faf4a07badb71588c601cd9390e4d8e3f187e629
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61969648"
---
# <a name="coordinatorrecoverylogentrycorrupt"></a><span data-ttu-id="05129-102">CoordinatorRecoveryLogEntryCorrupt</span><span class="sxs-lookup"><span data-stu-id="05129-102">CoordinatorRecoveryLogEntryCorrupt</span></span>
<span data-ttu-id="05129-103">Id : 139</span><span class="sxs-lookup"><span data-stu-id="05129-103">Id: 139</span></span>  
  
 <span data-ttu-id="05129-104">Gravité : Error</span><span class="sxs-lookup"><span data-stu-id="05129-104">Severity: Error</span></span>  
  
 <span data-ttu-id="05129-105">Catégorie : TransactionBridge</span><span class="sxs-lookup"><span data-stu-id="05129-105">Category: TransactionBridge</span></span>  
  
## <a name="description"></a><span data-ttu-id="05129-106">Description</span><span class="sxs-lookup"><span data-stu-id="05129-106">Description</span></span>  
 <span data-ttu-id="05129-107">Cet événement indique qu'une entrée de journal de récupération de coordinateur a été endommagée et n'a pas pu être désérialisée.</span><span class="sxs-lookup"><span data-stu-id="05129-107">This event indicates that a  coordinator recovery log entry was corrupt and could not be deserialized.</span></span> <span data-ttu-id="05129-108">Cette erreur risque d'entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="05129-108">Data loss may result from this error.</span></span> <span data-ttu-id="05129-109">L’événement répertorie l’ID de transaction, les données de récupération (encodage Base64), l’exception, le nom de processus et l’ID de processus.</span><span class="sxs-lookup"><span data-stu-id="05129-109">The event lists the Transaction ID, Recovery data (Base64 encoded), exception, process name and process ID.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05129-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05129-110">See also</span></span>

- [<span data-ttu-id="05129-111">Journalisation des événements</span><span class="sxs-lookup"><span data-stu-id="05129-111">Event Logging</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/index.md)
- [<span data-ttu-id="05129-112">Informations de référence générales sur les événements</span><span class="sxs-lookup"><span data-stu-id="05129-112">Events General Reference</span></span>](../../../../../docs/framework/wcf/diagnostics/event-logging/events-general-reference.md)
