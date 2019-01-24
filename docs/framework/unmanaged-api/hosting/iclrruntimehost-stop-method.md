---
title: ICLRRuntimeHost::Stop, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.Stop
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::Stop
helpviewer_keywords:
- ICLRRuntimeHost::Stop method [.NET Framework hosting]
- Stop method, ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: b8fd7daf-8f8d-4ad7-92ae-019db244cec1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 71d4167d17b20c08c2cbc62d2ac0c1cddd88e527
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54634433"
---
# <a name="iclrruntimehoststop-method"></a><span data-ttu-id="ec0bf-102">ICLRRuntimeHost::Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="ec0bf-102">ICLRRuntimeHost::Stop Method</span></span>
<span data-ttu-id="ec0bf-103">Arrête l’exécution du code par le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="ec0bf-103">Stops the execution of code by the common language runtime (CLR).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ec0bf-104">Cette méthode ne pas libérer les ressources à l’hôte, décharger des domaines d’application ou détruire des threads.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-104">This method does not release resources to the host, unload application domains, or destroy threads.</span></span> <span data-ttu-id="ec0bf-105">Vous devez terminer le processus pour libérer ces ressources.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-105">You must terminate the process to release these resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec0bf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec0bf-106">Syntax</span></span>  
  
```  
HRESULT Stop();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ec0bf-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec0bf-107">Return Value</span></span>  
  
|<span data-ttu-id="ec0bf-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ec0bf-108">HRESULT</span></span>|<span data-ttu-id="ec0bf-109">Description</span><span class="sxs-lookup"><span data-stu-id="ec0bf-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ec0bf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec0bf-110">S_OK</span></span>|<span data-ttu-id="ec0bf-111">`Stop` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-111">`Stop` returned successfully.</span></span>|  
|<span data-ttu-id="ec0bf-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ec0bf-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="ec0bf-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="ec0bf-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ec0bf-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="ec0bf-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-115">The call timed out.</span></span>|  
|<span data-ttu-id="ec0bf-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="ec0bf-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="ec0bf-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="ec0bf-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="ec0bf-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="ec0bf-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="ec0bf-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ec0bf-120">E_FAIL</span></span>|<span data-ttu-id="ec0bf-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="ec0bf-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="ec0bf-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="ec0bf-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ec0bf-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ec0bf-124">Requirements</span></span>  
 <span data-ttu-id="ec0bf-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec0bf-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec0bf-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ec0bf-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ec0bf-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ec0bf-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ec0bf-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ec0bf-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec0bf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec0bf-129">See also</span></span>
- [<span data-ttu-id="ec0bf-130">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="ec0bf-130">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
