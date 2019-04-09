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
ms.openlocfilehash: 57efd4f29ba7e28adf1af03030d7f83eb32c1c2b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59139774"
---
# <a name="iclrtaskabort-method"></a><span data-ttu-id="ec539-102">ICLRTask::Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="ec539-102">ICLRTask::Abort Method</span></span>
<span data-ttu-id="ec539-103">Demande que le common language runtime (CLR) abandonne la tâche qui en cours [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) représente l’instance.</span><span class="sxs-lookup"><span data-stu-id="ec539-103">Requests that the common language runtime (CLR) abort the task that the current [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec539-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec539-104">Syntax</span></span>  
  
```  
HRESULT Abort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ec539-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec539-105">Return Value</span></span>  
  
|<span data-ttu-id="ec539-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ec539-106">HRESULT</span></span>|<span data-ttu-id="ec539-107">Description</span><span class="sxs-lookup"><span data-stu-id="ec539-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ec539-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec539-108">S_OK</span></span>|`Abort` <span data-ttu-id="ec539-109">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec539-109">returned successfully.</span></span>|  
|<span data-ttu-id="ec539-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ec539-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ec539-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec539-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ec539-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ec539-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ec539-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="ec539-113">The call timed out.</span></span>|  
|<span data-ttu-id="ec539-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ec539-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ec539-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="ec539-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ec539-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ec539-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ec539-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="ec539-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ec539-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ec539-118">E_FAIL</span></span>|<span data-ttu-id="ec539-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ec539-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ec539-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="ec539-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ec539-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="ec539-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ec539-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ec539-122">Remarks</span></span>  
 <span data-ttu-id="ec539-123">Le CLR lève une <xref:System.Threading.ThreadAbortException> lorsque l’hôte appelle la méthode `Abort`.</span><span class="sxs-lookup"><span data-stu-id="ec539-123">The CLR raises a <xref:System.Threading.ThreadAbortException> when the host calls `Abort`.</span></span> <span data-ttu-id="ec539-124">Il retourne immédiatement après l’initialisation des informations sur l’exception, sans attendre pour le code de l’utilisateur, telles que les finaliseurs ou les mécanismes de gestion des exceptions à exécuter.</span><span class="sxs-lookup"><span data-stu-id="ec539-124">It returns immediately after the exception information is initialized, without waiting for user code, such as finalizers or exception handling mechanisms, to execute.</span></span> <span data-ttu-id="ec539-125">Les appels à `Abort` retournent donc rapidement.</span><span class="sxs-lookup"><span data-stu-id="ec539-125">Calls to `Abort` thus return quickly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ec539-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec539-126">Requirements</span></span>  
 <span data-ttu-id="ec539-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec539-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec539-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ec539-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ec539-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ec539-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="ec539-130">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ec539-130">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ec539-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec539-131">See also</span></span>

- [<span data-ttu-id="ec539-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="ec539-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="ec539-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="ec539-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="ec539-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="ec539-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="ec539-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="ec539-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
