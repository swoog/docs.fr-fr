---
title: IHostThreadPoolManager::QueueUserWorkItem, méthode
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.QueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::QueueUserWorkItem
helpviewer_keywords:
- IHostThreadPoolManager::QueueUserWorkItem method [.NET Framework hosting]
- QueueUserWorkItem method [.NET Framework hosting]
ms.assetid: 41602053-8670-4827-9d61-cbfcba509b9c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3faa3762612e4d1fc608291a393e9eb2e79fe67e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616847"
---
# <a name="ihostthreadpoolmanagerqueueuserworkitem-method"></a><span data-ttu-id="2ff7c-102">IHostThreadPoolManager::QueueUserWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="2ff7c-102">IHostThreadPoolManager::QueueUserWorkItem Method</span></span>
<span data-ttu-id="2ff7c-103">Files d’attente d’une fonction pour l’exécution et spécifie un objet contenant les données à utiliser par cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-103">Queues a function for execution, and specifies an object containing data to be used by that function.</span></span> <span data-ttu-id="2ff7c-104">La fonction s’exécute lorsqu’un thread devienne disponible.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-104">The function executes when a thread becomes available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ff7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ff7c-105">Syntax</span></span>  
  
```  
HRESULT QueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID Context,  
    [in] ULONG Flags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2ff7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ff7c-106">Parameters</span></span>  
 `Function`  
 <span data-ttu-id="2ff7c-107">[in] Un pointeur de fonction qui représente la fonction à exécuter.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-107">[in] A function pointer that represents the function to execute.</span></span>  
  
 `Context`  
 <span data-ttu-id="2ff7c-108">[in] Objet qui contient les données à utiliser par `Function`.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-108">[in] An object that contains data to be used by `Function`.</span></span>  
  
 `Flags`  
 <span data-ttu-id="2ff7c-109">[in] Un des indicateurs de valeurs, comme défini pour Win32 `QueueUserWorkItem` (méthode), qui contrôle l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-109">[in] One of the flags values, as defined for the Win32 `QueueUserWorkItem` method, that control execution.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2ff7c-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2ff7c-110">Return Value</span></span>  
  
|<span data-ttu-id="2ff7c-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2ff7c-111">HRESULT</span></span>|<span data-ttu-id="2ff7c-112">Description</span><span class="sxs-lookup"><span data-stu-id="2ff7c-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2ff7c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ff7c-113">S_OK</span></span>|<span data-ttu-id="2ff7c-114">`QueueUserWorkItem` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-114">`QueueUserWorkItem` returned successfully.</span></span>|  
|<span data-ttu-id="2ff7c-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="2ff7c-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="2ff7c-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="2ff7c-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="2ff7c-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="2ff7c-118">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-118">The call timed out.</span></span>|  
|<span data-ttu-id="2ff7c-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="2ff7c-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="2ff7c-120">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="2ff7c-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="2ff7c-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="2ff7c-122">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="2ff7c-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="2ff7c-123">E_FAIL</span></span>|<span data-ttu-id="2ff7c-124">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="2ff7c-125">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="2ff7c-126">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2ff7c-127">Notes</span><span class="sxs-lookup"><span data-stu-id="2ff7c-127">Remarks</span></span>  
 <span data-ttu-id="2ff7c-128">`QueueUserWorkItem` files d’attente d’un élément de travail à un thread de travail dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-128">`QueueUserWorkItem` queues a work item to a worker thread in the thread pool.</span></span> <span data-ttu-id="2ff7c-129">Ses types de signature et de paramètres sont identiques à ceux de la fonction Win32 correspondante, qui porte le même nom.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-129">Its signature and parameter types are identical to those of the corresponding Win32 function, which has the same name.</span></span> <span data-ttu-id="2ff7c-130">Pour plus d’informations, consultez la documentation de la plateforme de Windows.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-130">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2ff7c-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2ff7c-131">Requirements</span></span>  
 <span data-ttu-id="2ff7c-132">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2ff7c-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2ff7c-133">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2ff7c-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2ff7c-134">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2ff7c-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2ff7c-135">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2ff7c-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ff7c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ff7c-136">See also</span></span>
- <xref:System.Threading.ThreadPool.QueueUserWorkItem%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="2ff7c-137">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="2ff7c-137">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
