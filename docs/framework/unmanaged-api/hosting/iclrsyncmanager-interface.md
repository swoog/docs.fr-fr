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
ms.openlocfilehash: d3e4affa363083ce55ac3764c26412a0d60ba3f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59203091"
---
# <a name="iclrsyncmanager-interface"></a><span data-ttu-id="90536-102">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="90536-102">ICLRSyncManager Interface</span></span>
<span data-ttu-id="90536-103">Définit des méthodes qui permettent à l’hôte pour obtenir des informations sur les tâches demandées et pour détecter les blocages dans son implémentation de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="90536-103">Defines methods that allow the host to get information about requested tasks and to detect deadlocks in its synchronization implementation.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="90536-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="90536-104">Methods</span></span>  
  
|<span data-ttu-id="90536-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="90536-105">Method</span></span>|<span data-ttu-id="90536-106">Description</span><span class="sxs-lookup"><span data-stu-id="90536-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="90536-107">CreateRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="90536-107">CreateRWLockOwnerIterator Method</span></span>](iclrsyncmanager-createrwlockowneriterator-method.md)|<span data-ttu-id="90536-108">Demande que le common language runtime (CLR) crée un itérateur pour l’hôte à utiliser pour déterminer l’ensemble de tâches en attente sur un verrou de lecteur-writer.</span><span class="sxs-lookup"><span data-stu-id="90536-108">Requests that the common language runtime (CLR) create an iterator for the host to use to determine the set of tasks waiting on a reader-writer lock.</span></span>|  
|[<span data-ttu-id="90536-109">DeleteRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="90536-109">DeleteRWLockOwnerIterator Method</span></span>](iclrsyncmanager-deleterwlockowneriterator-method.md)|<span data-ttu-id="90536-110">Demande que le CLR détruise un itérateur qui a été créé par un appel à `CreateRWLockOwnerIterator`.</span><span class="sxs-lookup"><span data-stu-id="90536-110">Requests that the CLR destroy an iterator that was created by a call to `CreateRWLockOwnerIterator`.</span></span>|  
|[<span data-ttu-id="90536-111">GetMonitorOwner, méthode</span><span class="sxs-lookup"><span data-stu-id="90536-111">GetMonitorOwner Method</span></span>](iclrsyncmanager-getmonitorowner-method.md)|<span data-ttu-id="90536-112">Obtient la tâche qui possède le moniteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="90536-112">Gets the task that owns the specified monitor.</span></span>|  
|[<span data-ttu-id="90536-113">GetRWLockOwnerNext, méthode</span><span class="sxs-lookup"><span data-stu-id="90536-113">GetRWLockOwnerNext Method</span></span>](iclrsyncmanager-getrwlockownernext-method.md)|<span data-ttu-id="90536-114">Obtient la tâche suivante qui attend le verrou de lecteur-writer actuel.</span><span class="sxs-lookup"><span data-stu-id="90536-114">Gets the next task that is waiting on the current reader-writer lock.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="90536-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90536-115">Requirements</span></span>  
 <span data-ttu-id="90536-116">**Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="90536-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="90536-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="90536-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="90536-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="90536-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="90536-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="90536-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="90536-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90536-120">See also</span></span>

- <xref:System.Threading.Thread>
- [<span data-ttu-id="90536-121">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="90536-121">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)
- [<span data-ttu-id="90536-122">Threading managé et non managé</span><span class="sxs-lookup"><span data-stu-id="90536-122">Managed and Unmanaged Threading</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))
- [<span data-ttu-id="90536-123">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="90536-123">Hosting Interfaces</span></span>](hosting-interfaces.md)
