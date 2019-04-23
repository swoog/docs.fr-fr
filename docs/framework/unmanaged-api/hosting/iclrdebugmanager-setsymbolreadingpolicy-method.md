---
title: ICLRDebugManager::SetSymbolReadingPolicy, méthode
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.SetSymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::SetSymbolReadingPolicy
helpviewer_keywords:
- ICLRDebugManager, SetSymbolREadingPolicy method
- SetSymbolReadingPolicy method [.NET Framework hosting]
- ICLRDebugManager::SetSymbolReadingPolicy method [.NET Framework hosting]
ms.assetid: bd921fa2-d377-4d79-acfc-64c38d4dcae9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2dc3d350f5c97736b3b65c814a668195aceef2b0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132819"
---
# <a name="iclrdebugmanagersetsymbolreadingpolicy-method"></a><span data-ttu-id="d65ac-102">ICLRDebugManager::SetSymbolReadingPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="d65ac-102">ICLRDebugManager::SetSymbolReadingPolicy Method</span></span>
<span data-ttu-id="d65ac-103">Définit la stratégie pour la lecture des fichiers de programme (PDB) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d65ac-103">Sets the policy for reading program database (PDB) files.</span></span> <span data-ttu-id="d65ac-104">La stratégie détermine si les informations sur les fichiers et les numéros de ligne sont incluses dans les piles des appels.</span><span class="sxs-lookup"><span data-stu-id="d65ac-104">The policy determines whether information about line numbers and files is included in call stacks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d65ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d65ac-105">Syntax</span></span>  
  
```  
HRESULT SetSymbolReadingPolicy (  
    [in] ESymbolReadingPolicy policy  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d65ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d65ac-106">Parameters</span></span>  
 `policy`  
 <span data-ttu-id="d65ac-107">[in] Un membre de la [ESymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/esymbolreadingpolicy-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="d65ac-107">[in] A member of the [ESymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/esymbolreadingpolicy-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d65ac-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d65ac-108">Return Value</span></span>  
  
|<span data-ttu-id="d65ac-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d65ac-109">HRESULT</span></span>|<span data-ttu-id="d65ac-110">Description</span><span class="sxs-lookup"><span data-stu-id="d65ac-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d65ac-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d65ac-111">S_OK</span></span>|<span data-ttu-id="d65ac-112">`SetSymbolReadingPolicy` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="d65ac-112">`SetSymbolReadingPolicy` returned successfully.</span></span>|  
|<span data-ttu-id="d65ac-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d65ac-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d65ac-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="d65ac-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d65ac-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d65ac-115">E_FAIL</span></span>|<span data-ttu-id="d65ac-116">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d65ac-116">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d65ac-117">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="d65ac-117">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d65ac-118">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="d65ac-118">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d65ac-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d65ac-119">Requirements</span></span>  
 <span data-ttu-id="d65ac-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d65ac-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d65ac-121">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d65ac-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d65ac-122">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d65ac-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d65ac-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d65ac-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d65ac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d65ac-124">See also</span></span>

- [<span data-ttu-id="d65ac-125">ICLRDebugManager, interface</span><span class="sxs-lookup"><span data-stu-id="d65ac-125">ICLRDebugManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)
