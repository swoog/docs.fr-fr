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
ms.openlocfilehash: 85116244ad21842fab025ddd48106deef75f210b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166970"
---
# <a name="iclrruntimehoststop-method"></a><span data-ttu-id="7a894-102">ICLRRuntimeHost::Stop, méthode</span><span class="sxs-lookup"><span data-stu-id="7a894-102">ICLRRuntimeHost::Stop Method</span></span>
<span data-ttu-id="7a894-103">Arrête l’exécution du code par le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="7a894-103">Stops the execution of code by the common language runtime (CLR).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="7a894-104">Cette méthode ne pas libérer les ressources à l’hôte, décharger des domaines d’application ou détruire des threads.</span><span class="sxs-lookup"><span data-stu-id="7a894-104">This method does not release resources to the host, unload application domains, or destroy threads.</span></span> <span data-ttu-id="7a894-105">Vous devez terminer le processus pour libérer ces ressources.</span><span class="sxs-lookup"><span data-stu-id="7a894-105">You must terminate the process to release these resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a894-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a894-106">Syntax</span></span>  
  
```  
HRESULT Stop();  
```  
  
## <a name="return-value"></a><span data-ttu-id="7a894-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7a894-107">Return Value</span></span>  
  
|<span data-ttu-id="7a894-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7a894-108">HRESULT</span></span>|<span data-ttu-id="7a894-109">Description</span><span class="sxs-lookup"><span data-stu-id="7a894-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7a894-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a894-110">S_OK</span></span>|`Stop` <span data-ttu-id="7a894-111">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="7a894-111">returned successfully.</span></span>|  
|<span data-ttu-id="7a894-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="7a894-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="7a894-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="7a894-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="7a894-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="7a894-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="7a894-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="7a894-115">The call timed out.</span></span>|  
|<span data-ttu-id="7a894-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="7a894-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="7a894-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="7a894-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="7a894-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="7a894-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="7a894-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="7a894-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="7a894-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7a894-120">E_FAIL</span></span>|<span data-ttu-id="7a894-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7a894-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="7a894-122">Si une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="7a894-122">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="7a894-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="7a894-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7a894-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a894-124">Requirements</span></span>  
 <span data-ttu-id="7a894-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a894-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a894-126">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="7a894-126">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7a894-127">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7a894-127">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="7a894-128">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7a894-128">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7a894-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a894-129">See also</span></span>

- [<span data-ttu-id="7a894-130">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="7a894-130">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
