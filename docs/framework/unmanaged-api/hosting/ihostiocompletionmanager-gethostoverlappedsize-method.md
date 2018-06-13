---
title: IHostIoCompletionManager::GetHostOverlappedSize, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.GetHostOverlappedSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::GetHostOverlappedSize
helpviewer_keywords:
- IHostIoCompletionManager::GetHostOverlappedSize method [.NET Framework hosting]
- GetHostOverlappedSize method [.NET Framework hosting]
ms.assetid: 2902578b-d5e2-4f8d-a103-0c7b6dceda9e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6713fdb822babf607752c1823a32dae43a7d567e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439596"
---
# <a name="ihostiocompletionmanagergethostoverlappedsize-method"></a><span data-ttu-id="c3c9f-102">IHostIoCompletionManager::GetHostOverlappedSize, méthode</span><span class="sxs-lookup"><span data-stu-id="c3c9f-102">IHostIoCompletionManager::GetHostOverlappedSize Method</span></span>
<span data-ttu-id="c3c9f-103">Obtient la taille des données personnalisées que l’hôte projette d’ajouter aux demandes d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-103">Gets the size of any custom data the host intends to append to I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3c9f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3c9f-104">Syntax</span></span>  
  
```  
HRESULT GetHostOverlappedSize (  
    [out] DWORD *pcbSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c3c9f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3c9f-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="c3c9f-106">[out] Un pointeur vers le nombre d’octets que le common language runtime (CLR) doit allouer en plus de la taille de Win32 `OVERLAPPED` objet.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-106">[out] A pointer to the number of bytes that the common language runtime (CLR) should allocate in addition to the size of the Win32 `OVERLAPPED` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c3c9f-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c3c9f-107">Return Value</span></span>  
  
|<span data-ttu-id="c3c9f-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c3c9f-108">HRESULT</span></span>|<span data-ttu-id="c3c9f-109">Description</span><span class="sxs-lookup"><span data-stu-id="c3c9f-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c3c9f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3c9f-110">S_OK</span></span>|<span data-ttu-id="c3c9f-111">`GetHostOverlappedSize` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-111">`GetHostOverlappedSize` returned successfully.</span></span>|  
|<span data-ttu-id="c3c9f-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c3c9f-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c3c9f-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c3c9f-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c3c9f-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c3c9f-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-115">The call timed out.</span></span>|  
|<span data-ttu-id="c3c9f-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c3c9f-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c3c9f-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c3c9f-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c3c9f-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c3c9f-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c3c9f-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c3c9f-120">E_FAIL</span></span>|<span data-ttu-id="c3c9f-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c3c9f-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c3c9f-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c3c9f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c3c9f-124">Remarks</span></span>  
 <span data-ttu-id="c3c9f-125">Tous les appels d’e/s asynchrones aux API de plateforme Windows prennent Win32 `OVERLAPPED` objet, qui fournit des informations telles que la position du pointeur.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-125">All asynchronous I/O calls to Windows Platform APIs take a Win32 `OVERLAPPED` object, which provides information such as the file pointer position.</span></span> <span data-ttu-id="c3c9f-126">Pour conserver l’état, les applications qui effectuent des appels d’e/s asynchrones généralement ajouter des données personnalisées à la structure.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-126">To maintain state, applications that make asynchronous I/O calls typically add custom data to the structure.</span></span> <span data-ttu-id="c3c9f-127">`GetHostOverlappedSize` et [IHostIoCompletionManager::InitializeHostOverlapped](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md) permettent à l’hôte d’inclure ces données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-127">`GetHostOverlappedSize` and [IHostIoCompletionManager::InitializeHostOverlapped](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md) provide an opportunity for the host to include such custom data.</span></span>  
  
 <span data-ttu-id="c3c9f-128">Le CLR appelle la `GetHostOverlappedSize` méthode pour déterminer la taille des données personnalisées qui a l’intention de l’ordinateur hôte à ajouter à la `OVERLAPPED` objet.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-128">The CLR calls the `GetHostOverlappedSize` method to determine the size of the custom data that the host intends to append to the `OVERLAPPED` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c3c9f-129">`GetHostOverlappedSize` est appelé une seule fois.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-129">`GetHostOverlappedSize` is called only once.</span></span> <span data-ttu-id="c3c9f-130">Données personnalisées de l’ordinateur hôte doivent être la même taille pour chaque demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-130">The host's custom data must be the same size for every I/O request.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="c3c9f-131">La taille de la `OVERLAPPED` objet lui-même n’est pas inclus dans la valeur de `pcbSize`.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-131">The size of the `OVERLAPPED` object itself is not included in the value of `pcbSize`.</span></span>  
  
 <span data-ttu-id="c3c9f-132">Pour plus d’informations sur la `OVERLAPPED` de la structure, consultez la documentation de la plateforme Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c9f-132">For more information about the `OVERLAPPED` structure, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3c9f-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3c9f-133">Requirements</span></span>  
 <span data-ttu-id="c3c9f-134">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3c9f-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3c9f-135">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c3c9f-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c3c9f-136">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c3c9f-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c3c9f-137">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3c9f-137">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3c9f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3c9f-138">See Also</span></span>  
 <xref:System.Threading.NativeOverlapped>  
 [<span data-ttu-id="c3c9f-139">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="c3c9f-139">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)  
 [<span data-ttu-id="c3c9f-140">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="c3c9f-140">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
