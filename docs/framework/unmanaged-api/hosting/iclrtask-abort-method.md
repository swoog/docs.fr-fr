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
ms.openlocfilehash: 46d60ff6ab64d57ca5c7020877758657b61125ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434835"
---
# <a name="iclrtaskabort-method"></a><span data-ttu-id="2aa09-102">ICLRTask::Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="2aa09-102">ICLRTask::Abort Method</span></span>
<span data-ttu-id="2aa09-103">Demande que le common language runtime (CLR) abandonne la tâche qui en cours [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) représente l’instance.</span><span class="sxs-lookup"><span data-stu-id="2aa09-103">Requests that the common language runtime (CLR) abort the task that the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2aa09-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2aa09-104">Syntax</span></span>  
  
```  
HRESULT Abort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2aa09-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2aa09-105">Return Value</span></span>  
  
|<span data-ttu-id="2aa09-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2aa09-106">HRESULT</span></span>|<span data-ttu-id="2aa09-107">Description</span><span class="sxs-lookup"><span data-stu-id="2aa09-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2aa09-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="2aa09-108">S_OK</span></span>|<span data-ttu-id="2aa09-109">`Abort` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="2aa09-109">`Abort` returned successfully.</span></span>|  
|<span data-ttu-id="2aa09-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2aa09-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2aa09-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="2aa09-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2aa09-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2aa09-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2aa09-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="2aa09-113">The call timed out.</span></span>|  
|<span data-ttu-id="2aa09-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2aa09-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2aa09-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="2aa09-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2aa09-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2aa09-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2aa09-117">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="2aa09-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2aa09-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2aa09-118">E_FAIL</span></span>|<span data-ttu-id="2aa09-119">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2aa09-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2aa09-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="2aa09-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2aa09-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="2aa09-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2aa09-122">Notes</span><span class="sxs-lookup"><span data-stu-id="2aa09-122">Remarks</span></span>  
 <span data-ttu-id="2aa09-123">Le CLR lève une <xref:System.Threading.ThreadAbortException> lorsque l’hôte appelle la méthode `Abort`.</span><span class="sxs-lookup"><span data-stu-id="2aa09-123">The CLR raises a <xref:System.Threading.ThreadAbortException> when the host calls `Abort`.</span></span> <span data-ttu-id="2aa09-124">Il retourne immédiatement après initialisation des informations sur l’exception, sans attendre le code de l’utilisateur, telles que les finaliseurs ou les mécanismes de gestion des exceptions à exécuter.</span><span class="sxs-lookup"><span data-stu-id="2aa09-124">It returns immediately after the exception information is initialized, without waiting for user code, such as finalizers or exception handling mechanisms, to execute.</span></span> <span data-ttu-id="2aa09-125">Les appels à `Abort` retournent donc rapidement.</span><span class="sxs-lookup"><span data-stu-id="2aa09-125">Calls to `Abort` thus return quickly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2aa09-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2aa09-126">Requirements</span></span>  
 <span data-ttu-id="2aa09-127">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2aa09-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2aa09-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2aa09-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2aa09-129">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2aa09-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2aa09-130">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2aa09-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aa09-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa09-131">See Also</span></span>  
 [<span data-ttu-id="2aa09-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="2aa09-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="2aa09-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="2aa09-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="2aa09-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="2aa09-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="2aa09-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="2aa09-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
