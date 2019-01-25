---
title: ICLRErrorReportingManager::EndCustomDump, méthode
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.EndCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::EndCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::EndCustomDump method [.NET Framework hosting]
- EndCustomDump method [.NET Framework hosting]
ms.assetid: 88a5da04-8729-4108-82c4-af206a7d483e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: addf6f52ad445da372dbb04b9c408c5bfea0daf3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54660123"
---
# <a name="iclrerrorreportingmanagerendcustomdump-method"></a><span data-ttu-id="63e3b-102">ICLRErrorReportingManager::EndCustomDump, méthode</span><span class="sxs-lookup"><span data-stu-id="63e3b-102">ICLRErrorReportingManager::EndCustomDump Method</span></span>
<span data-ttu-id="63e3b-103">Supprime la configuration de vidage de pile personnalisée qui a été spécifiée dans un appel antérieur à la [ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="63e3b-103">Removes the custom stack dump configuration that was specified in an earlier call to the [ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63e3b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63e3b-104">Syntax</span></span>  
  
```  
HRESULT EndCustomDump ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="63e3b-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="63e3b-105">Return Value</span></span>  
  
|<span data-ttu-id="63e3b-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="63e3b-106">HRESULT</span></span>|<span data-ttu-id="63e3b-107">Description</span><span class="sxs-lookup"><span data-stu-id="63e3b-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="63e3b-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="63e3b-108">S_OK</span></span>|<span data-ttu-id="63e3b-109">`EndCustomDump` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="63e3b-109">`EndCustomDump` returned successfully.</span></span>|  
|<span data-ttu-id="63e3b-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="63e3b-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="63e3b-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="63e3b-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="63e3b-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="63e3b-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="63e3b-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="63e3b-113">The call timed out.</span></span>|  
|<span data-ttu-id="63e3b-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="63e3b-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="63e3b-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="63e3b-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="63e3b-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="63e3b-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="63e3b-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="63e3b-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="63e3b-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="63e3b-118">E_FAIL</span></span>|<span data-ttu-id="63e3b-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="63e3b-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="63e3b-120">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="63e3b-120">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="63e3b-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="63e3b-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="63e3b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="63e3b-122">Remarks</span></span>  
 <span data-ttu-id="63e3b-123">Le `EndCustomDump` méthode efface la configuration du vidage de pile personnalisée définie par un appel antérieur à la `BeginCustomDump` (méthode) et libère tout état associé.</span><span class="sxs-lookup"><span data-stu-id="63e3b-123">The `EndCustomDump` method clears the custom stack dump configuration set by an earlier call to the `BeginCustomDump` method and frees any associated state.</span></span> <span data-ttu-id="63e3b-124">Il doit être appelée après que le vidage de pile personnalisée est terminé.</span><span class="sxs-lookup"><span data-stu-id="63e3b-124">It should be called after the custom stack dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="63e3b-125">Échec d’appel `EndCustomDump` entraîne une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="63e3b-125">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63e3b-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63e3b-126">Requirements</span></span>  
 <span data-ttu-id="63e3b-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63e3b-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63e3b-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="63e3b-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="63e3b-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="63e3b-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="63e3b-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63e3b-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63e3b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63e3b-131">See also</span></span>
- [<span data-ttu-id="63e3b-132">CustomDumpItem, structure</span><span class="sxs-lookup"><span data-stu-id="63e3b-132">CustomDumpItem Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md)
- [<span data-ttu-id="63e3b-133">ECustomDumpFlavor, énumération</span><span class="sxs-lookup"><span data-stu-id="63e3b-133">ECustomDumpFlavor Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md)
- [<span data-ttu-id="63e3b-134">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="63e3b-134">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
