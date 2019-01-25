---
title: ICLRTask::Abort, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.Abort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::Abort
helpviewer_keywords:
- ICLRTask::Abort method [.NET Framework hosting]
- Abort method, ICLRTask interface [.NET Framework hosting]
ms.assetid: b3594b5f-2e41-4e36-9096-3586276a138c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9164e64c56a8a4ae908a3d06f878b399550703f9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715398"
---
# <a name="iclrtaskabort-method"></a><span data-ttu-id="bd1f8-102">ICLRTask::Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="bd1f8-102">ICLRTask::Abort Method</span></span>
<span data-ttu-id="bd1f8-103">Demande que le common language runtime (CLR) abandonne la tâche qui en cours [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) représente l’instance.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-103">Requests that the common language runtime (CLR) abort the task that the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd1f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd1f8-104">Syntax</span></span>  
  
```  
HRESULT Abort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="bd1f8-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bd1f8-105">Return Value</span></span>  
  
|<span data-ttu-id="bd1f8-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bd1f8-106">HRESULT</span></span>|<span data-ttu-id="bd1f8-107">Description</span><span class="sxs-lookup"><span data-stu-id="bd1f8-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bd1f8-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd1f8-108">S_OK</span></span>|<span data-ttu-id="bd1f8-109">`Abort` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-109">`Abort` returned successfully.</span></span>|  
|<span data-ttu-id="bd1f8-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bd1f8-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bd1f8-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bd1f8-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bd1f8-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bd1f8-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-113">The call timed out.</span></span>|  
|<span data-ttu-id="bd1f8-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bd1f8-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bd1f8-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bd1f8-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bd1f8-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bd1f8-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bd1f8-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bd1f8-118">E_FAIL</span></span>|<span data-ttu-id="bd1f8-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bd1f8-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bd1f8-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bd1f8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="bd1f8-122">Remarks</span></span>  
 <span data-ttu-id="bd1f8-123">Le CLR lève une <xref:System.Threading.ThreadAbortException> lorsque l’hôte appelle la méthode `Abort`.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-123">The CLR raises a <xref:System.Threading.ThreadAbortException> when the host calls `Abort`.</span></span> <span data-ttu-id="bd1f8-124">Il retourne immédiatement après l’initialisation des informations sur l’exception, sans attendre pour le code de l’utilisateur, telles que les finaliseurs ou les mécanismes de gestion des exceptions à exécuter.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-124">It returns immediately after the exception information is initialized, without waiting for user code, such as finalizers or exception handling mechanisms, to execute.</span></span> <span data-ttu-id="bd1f8-125">Les appels à `Abort` retournent donc rapidement.</span><span class="sxs-lookup"><span data-stu-id="bd1f8-125">Calls to `Abort` thus return quickly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd1f8-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bd1f8-126">Requirements</span></span>  
 <span data-ttu-id="bd1f8-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bd1f8-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd1f8-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bd1f8-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bd1f8-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bd1f8-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bd1f8-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd1f8-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd1f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd1f8-131">See also</span></span>
- [<span data-ttu-id="bd1f8-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="bd1f8-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="bd1f8-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bd1f8-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="bd1f8-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="bd1f8-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="bd1f8-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bd1f8-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
