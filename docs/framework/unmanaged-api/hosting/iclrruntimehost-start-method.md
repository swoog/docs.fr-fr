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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59172612"
---
# <a name="iclrruntimehoststart-method"></a><span data-ttu-id="8a329-102">ICLRRuntimeHost::Start, méthode</span><span class="sxs-lookup"><span data-stu-id="8a329-102">ICLRRuntimeHost::Start Method</span></span>
<span data-ttu-id="8a329-103">Initialise le common language runtime (CLR) dans un processus.</span><span class="sxs-lookup"><span data-stu-id="8a329-103">Initializes the common language runtime (CLR) into a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a329-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a329-104">Syntax</span></span>  
  
```  
HRESULT Start();  
```  
  
## <a name="return-value"></a><span data-ttu-id="8a329-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8a329-105">Return Value</span></span>  
  
|<span data-ttu-id="8a329-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8a329-106">HRESULT</span></span>|<span data-ttu-id="8a329-107">Description</span><span class="sxs-lookup"><span data-stu-id="8a329-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8a329-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a329-108">S_OK</span></span>|`Start` <span data-ttu-id="8a329-109">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="8a329-109">returned successfully.</span></span>|  
|<span data-ttu-id="8a329-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8a329-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8a329-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="8a329-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8a329-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8a329-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8a329-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="8a329-113">The call timed out.</span></span>|  
|<span data-ttu-id="8a329-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8a329-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8a329-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="8a329-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8a329-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8a329-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8a329-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="8a329-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8a329-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8a329-118">E_FAIL</span></span>|<span data-ttu-id="8a329-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8a329-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8a329-120">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="8a329-120">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8a329-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="8a329-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8a329-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8a329-122">Remarks</span></span>  
 <span data-ttu-id="8a329-123">Dans de nombreux scénarios, il n’est pas nécessaire d’appeler `Start`, car le runtime s’initialise automatiquement dès la première demande pour exécuter le code managé.</span><span class="sxs-lookup"><span data-stu-id="8a329-123">In many scenarios it is not necessary to call `Start`, because the runtime will initialize itself automatically upon the first request to run managed code.</span></span> <span data-ttu-id="8a329-124">Vous pouvez, toutefois, utiliser `Start` pour spécifier exactement quand le runtime doit être initialisé.</span><span class="sxs-lookup"><span data-stu-id="8a329-124">You can, however, use `Start` to specify exactly when the runtime should be initialized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a329-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a329-125">Requirements</span></span>  
 <span data-ttu-id="8a329-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a329-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a329-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8a329-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8a329-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8a329-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="8a329-129">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8a329-129">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8a329-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a329-130">See also</span></span>

- <xref:System.AppDomain>
- [<span data-ttu-id="8a329-131">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="8a329-131">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
