---
title: IHostTaskManager::GetStackGuarantee, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetStackGuarantee
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetStackGuarantee
helpviewer_keywords:
- GetStackGuarantee method [.NET Framework hosting]
- IHostTaskManager::GetStackGuarantee method [.NET Framework hosting]
ms.assetid: 8176d732-c25c-4520-811d-e3310f339947
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 100bb73356379d2f251513bbbed0cf1e90752ff5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494370"
---
# <a name="ihosttaskmanagergetstackguarantee-method"></a><span data-ttu-id="1684c-102">IHostTaskManager::GetStackGuarantee, méthode</span><span class="sxs-lookup"><span data-stu-id="1684c-102">IHostTaskManager::GetStackGuarantee Method</span></span>
<span data-ttu-id="1684c-103">Obtient la quantité d’espace de pile qui est garanti pour être disponible après qu’une opération de pile se termine, mais avant la fermeture d’un processus.</span><span class="sxs-lookup"><span data-stu-id="1684c-103">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1684c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1684c-104">Syntax</span></span>  
  
```  
HRESULT GetStackGuarantee(  
    [out] ULONG *pGuarantee  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1684c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1684c-105">Parameters</span></span>  
 `pGuarantee`  
 <span data-ttu-id="1684c-106">[out] Pointeur vers le nombre d’octets qui sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="1684c-106">[out] A pointer to the number of bytes that are available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1684c-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1684c-107">Requirements</span></span>  
 <span data-ttu-id="1684c-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1684c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1684c-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1684c-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1684c-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1684c-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1684c-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1684c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1684c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1684c-112">See also</span></span>
- [<span data-ttu-id="1684c-113">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="1684c-113">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
