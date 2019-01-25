---
title: ICLRSyncManager, interface
ms.date: 03/30/2017
api_name:
- ICLRSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager
helpviewer_keywords:
- ICLRSyncManager interface [.NET Framework hosting]
ms.assetid: a49f9d80-1c76-4ddd-8c49-34f913a5c596
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b949466c5557415ec06bac601380675beed7fd1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549861"
---
# <a name="iclrsyncmanager-interface"></a><span data-ttu-id="5ae87-102">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="5ae87-102">ICLRSyncManager Interface</span></span>
<span data-ttu-id="5ae87-103">Définit des méthodes qui permettent à l’hôte pour obtenir des informations sur les tâches demandées et pour détecter les blocages dans son implémentation de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5ae87-103">Defines methods that allow the host to get information about requested tasks and to detect deadlocks in its synchronization implementation.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5ae87-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5ae87-104">Methods</span></span>  
  
|<span data-ttu-id="5ae87-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ae87-105">Method</span></span>|<span data-ttu-id="5ae87-106">Description</span><span class="sxs-lookup"><span data-stu-id="5ae87-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5ae87-107">CreateRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="5ae87-107">CreateRWLockOwnerIterator Method</span></span>](iclrsyncmanager-createrwlockowneriterator-method.md)|<span data-ttu-id="5ae87-108">Demande que le common language runtime (CLR) crée un itérateur pour l’hôte à utiliser pour déterminer l’ensemble de tâches en attente sur un verrou de lecteur-writer.</span><span class="sxs-lookup"><span data-stu-id="5ae87-108">Requests that the common language runtime (CLR) create an iterator for the host to use to determine the set of tasks waiting on a reader-writer lock.</span></span>|  
|[<span data-ttu-id="5ae87-109">DeleteRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="5ae87-109">DeleteRWLockOwnerIterator Method</span></span>](iclrsyncmanager-deleterwlockowneriterator-method.md)|<span data-ttu-id="5ae87-110">Demande que le CLR détruise un itérateur qui a été créé par un appel à `CreateRWLockOwnerIterator`.</span><span class="sxs-lookup"><span data-stu-id="5ae87-110">Requests that the CLR destroy an iterator that was created by a call to `CreateRWLockOwnerIterator`.</span></span>|  
|[<span data-ttu-id="5ae87-111">GetMonitorOwner, méthode</span><span class="sxs-lookup"><span data-stu-id="5ae87-111">GetMonitorOwner Method</span></span>](iclrsyncmanager-getmonitorowner-method.md)|<span data-ttu-id="5ae87-112">Obtient la tâche qui possède le moniteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="5ae87-112">Gets the task that owns the specified monitor.</span></span>|  
|[<span data-ttu-id="5ae87-113">GetRWLockOwnerNext, méthode</span><span class="sxs-lookup"><span data-stu-id="5ae87-113">GetRWLockOwnerNext Method</span></span>](iclrsyncmanager-getrwlockownernext-method.md)|<span data-ttu-id="5ae87-114">Obtient la tâche suivante qui attend le verrou de lecteur-writer actuel.</span><span class="sxs-lookup"><span data-stu-id="5ae87-114">Gets the next task that is waiting on the current reader-writer lock.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5ae87-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5ae87-115">Requirements</span></span>  
 <span data-ttu-id="5ae87-116">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ae87-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ae87-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5ae87-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5ae87-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ae87-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5ae87-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ae87-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ae87-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ae87-120">See also</span></span>
- <xref:System.Threading.Thread>
- [<span data-ttu-id="5ae87-121">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="5ae87-121">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- <span data-ttu-id="5ae87-122">[Threading managé et non managé](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="5ae87-122">[Managed and Unmanaged Threading](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))</span></span>
- [<span data-ttu-id="5ae87-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="5ae87-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
