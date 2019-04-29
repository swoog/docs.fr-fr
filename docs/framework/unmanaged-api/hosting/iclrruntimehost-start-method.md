---
title: ICLRRuntimeHost::Start, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::Start
helpviewer_keywords:
- ICLRRuntimeHost::Start method [.NET Framework hosting]
- Start method, ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: c0a6dce5-0a8d-42e8-808b-6ca14df9d289
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 608612f6a0f4395092e33ce75fdbd249f19ae4f4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771831"
---
# <a name="iclrruntimehoststart-method"></a><span data-ttu-id="85193-102">ICLRRuntimeHost::Start, méthode</span><span class="sxs-lookup"><span data-stu-id="85193-102">ICLRRuntimeHost::Start Method</span></span>
<span data-ttu-id="85193-103">Initialise le common language runtime (CLR) dans un processus.</span><span class="sxs-lookup"><span data-stu-id="85193-103">Initializes the common language runtime (CLR) into a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85193-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85193-104">Syntax</span></span>  
  
```  
HRESULT Start();  
```  
  
## <a name="return-value"></a><span data-ttu-id="85193-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="85193-105">Return Value</span></span>  
  
|<span data-ttu-id="85193-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="85193-106">HRESULT</span></span>|<span data-ttu-id="85193-107">Description</span><span class="sxs-lookup"><span data-stu-id="85193-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="85193-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="85193-108">S_OK</span></span>|<span data-ttu-id="85193-109">`Start` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="85193-109">`Start` returned successfully.</span></span>|  
|<span data-ttu-id="85193-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="85193-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="85193-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="85193-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="85193-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="85193-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="85193-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="85193-113">The call timed out.</span></span>|  
|<span data-ttu-id="85193-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="85193-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="85193-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="85193-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="85193-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="85193-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="85193-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="85193-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="85193-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="85193-118">E_FAIL</span></span>|<span data-ttu-id="85193-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="85193-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="85193-120">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="85193-120">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="85193-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="85193-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="85193-122">Notes</span><span class="sxs-lookup"><span data-stu-id="85193-122">Remarks</span></span>  
 <span data-ttu-id="85193-123">Dans de nombreux scénarios, il n’est pas nécessaire d’appeler `Start`, car le runtime s’initialise automatiquement dès la première demande pour exécuter le code managé.</span><span class="sxs-lookup"><span data-stu-id="85193-123">In many scenarios it is not necessary to call `Start`, because the runtime will initialize itself automatically upon the first request to run managed code.</span></span> <span data-ttu-id="85193-124">Vous pouvez, toutefois, utiliser `Start` pour spécifier exactement quand le runtime doit être initialisé.</span><span class="sxs-lookup"><span data-stu-id="85193-124">You can, however, use `Start` to specify exactly when the runtime should be initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85193-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85193-125">Requirements</span></span>  
 <span data-ttu-id="85193-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="85193-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85193-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="85193-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="85193-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="85193-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="85193-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85193-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85193-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85193-130">See also</span></span>

- <xref:System.AppDomain>
- [<span data-ttu-id="85193-131">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="85193-131">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
