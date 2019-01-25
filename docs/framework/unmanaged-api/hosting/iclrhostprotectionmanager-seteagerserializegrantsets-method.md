---
title: ICLRHostProtectionManager::SetEagerSerializeGrantSets, méthode
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager.SetEagerSerializeGrantSets
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager::SetEagerSerializeGrantSets
helpviewer_keywords:
- SetEagerSerializeGrantSets method [.NET Framework hosting]
- ICLRHostProtectionManager::SetEagerSerializeGrantSets method [.NET Framework hosting]
ms.assetid: d6158360-22b1-4ace-ad85-d830b9964783
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 948fd78ae2839bd24a44c8c0b806e32b1da7125f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729773"
---
# <a name="iclrhostprotectionmanagerseteagerserializegrantsets-method"></a><span data-ttu-id="917a8-102">ICLRHostProtectionManager::SetEagerSerializeGrantSets, méthode</span><span class="sxs-lookup"><span data-stu-id="917a8-102">ICLRHostProtectionManager::SetEagerSerializeGrantSets Method</span></span>
<span data-ttu-id="917a8-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="917a8-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="917a8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="917a8-104">Syntax</span></span>  
  
```  
HRESULT SetEagerSerializeGrantSets ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="917a8-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="917a8-105">Return Value</span></span>  
  
|<span data-ttu-id="917a8-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="917a8-106">HRESULT</span></span>|<span data-ttu-id="917a8-107">Description</span><span class="sxs-lookup"><span data-stu-id="917a8-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="917a8-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="917a8-108">S_OK</span></span>|<span data-ttu-id="917a8-109">`SetEagerSerializeGrantSets` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="917a8-109">`SetEagerSerializeGrantSets` returned successfully.</span></span>|  
|<span data-ttu-id="917a8-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="917a8-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="917a8-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="917a8-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="917a8-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="917a8-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="917a8-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="917a8-113">The call timed out.</span></span>|  
|<span data-ttu-id="917a8-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="917a8-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="917a8-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="917a8-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="917a8-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="917a8-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="917a8-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="917a8-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="917a8-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="917a8-118">E_FAIL</span></span>|<span data-ttu-id="917a8-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="917a8-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="917a8-120">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="917a8-120">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="917a8-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="917a8-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="917a8-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="917a8-122">Requirements</span></span>  
 <span data-ttu-id="917a8-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="917a8-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="917a8-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="917a8-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="917a8-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="917a8-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="917a8-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="917a8-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="917a8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="917a8-127">See also</span></span>
- [<span data-ttu-id="917a8-128">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="917a8-128">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="917a8-129">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="917a8-129">ICLRHostProtectionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-interface.md)
