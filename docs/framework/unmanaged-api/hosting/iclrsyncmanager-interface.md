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
ms.openlocfilehash: 1b87ccc3d6c3e957d0384499048032e35247093a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436479"
---
# <a name="iclrsyncmanager-interface"></a><span data-ttu-id="f27dd-102">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="f27dd-102">ICLRSyncManager Interface</span></span>
<span data-ttu-id="f27dd-103">Définit des méthodes qui permettent à l’hôte pour obtenir des informations sur les tâches demandées et pour détecter les blocages dans son implémentation de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="f27dd-103">Defines methods that allow the host to get information about requested tasks and to detect deadlocks in its synchronization implementation.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f27dd-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f27dd-104">Methods</span></span>  
  
|<span data-ttu-id="f27dd-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f27dd-105">Method</span></span>|<span data-ttu-id="f27dd-106">Description</span><span class="sxs-lookup"><span data-stu-id="f27dd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f27dd-107">CreateRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="f27dd-107">CreateRWLockOwnerIterator Method</span></span>](iclrsyncmanager-createrwlockowneriterator-method.md)|<span data-ttu-id="f27dd-108">Demande que le common language runtime (CLR) crée un itérateur pour l’hôte à utiliser pour déterminer l’ensemble de tâches attendant un verrou de lecteur-writer.</span><span class="sxs-lookup"><span data-stu-id="f27dd-108">Requests that the common language runtime (CLR) create an iterator for the host to use to determine the set of tasks waiting on a reader-writer lock.</span></span>|  
|[<span data-ttu-id="f27dd-109">DeleteRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="f27dd-109">DeleteRWLockOwnerIterator Method</span></span>](iclrsyncmanager-deleterwlockowneriterator-method.md)|<span data-ttu-id="f27dd-110">Demande que le CLR détruise un itérateur qui a été créé par un appel à `CreateRWLockOwnerIterator`.</span><span class="sxs-lookup"><span data-stu-id="f27dd-110">Requests that the CLR destroy an iterator that was created by a call to `CreateRWLockOwnerIterator`.</span></span>|  
|[<span data-ttu-id="f27dd-111">GetMonitorOwner, méthode</span><span class="sxs-lookup"><span data-stu-id="f27dd-111">GetMonitorOwner Method</span></span>](iclrsyncmanager-getmonitorowner-method.md)|<span data-ttu-id="f27dd-112">Obtient la tâche qui possède le moniteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f27dd-112">Gets the task that owns the specified monitor.</span></span>|  
|[<span data-ttu-id="f27dd-113">GetRWLockOwnerNext, méthode</span><span class="sxs-lookup"><span data-stu-id="f27dd-113">GetRWLockOwnerNext Method</span></span>](iclrsyncmanager-getrwlockownernext-method.md)|<span data-ttu-id="f27dd-114">Obtient la tâche suivante qui attend le verrou de lecteur-writer actuelle.</span><span class="sxs-lookup"><span data-stu-id="f27dd-114">Gets the next task that is waiting on the current reader-writer lock.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f27dd-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f27dd-115">Requirements</span></span>  
 <span data-ttu-id="f27dd-116">**Plateformes :** consultez [requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f27dd-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f27dd-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f27dd-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f27dd-118">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f27dd-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f27dd-119">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f27dd-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f27dd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f27dd-120">See Also</span></span>  
 <xref:System.Threading.Thread>  
 [<span data-ttu-id="f27dd-121">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="f27dd-121">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)  
 <span data-ttu-id="f27dd-122">[Threading managé et non managé](https://msdn.microsoft.com/library/db425c20-4b2f-4433-bf96-76071c7881e5(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="f27dd-122">[Managed and Unmanaged Threading](https://msdn.microsoft.com/library/db425c20-4b2f-4433-bf96-76071c7881e5(v=vs.100))</span></span>  
 [<span data-ttu-id="f27dd-123">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="f27dd-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
