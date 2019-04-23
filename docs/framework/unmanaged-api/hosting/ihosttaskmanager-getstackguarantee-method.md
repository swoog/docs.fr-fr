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
ms.openlocfilehash: ea1c1f998febccbc80fb10cef5a8dfd229e1987e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095943"
---
# <a name="ihosttaskmanagergetstackguarantee-method"></a><span data-ttu-id="fca75-102">IHostTaskManager::GetStackGuarantee, méthode</span><span class="sxs-lookup"><span data-stu-id="fca75-102">IHostTaskManager::GetStackGuarantee Method</span></span>
<span data-ttu-id="fca75-103">Obtient la quantité d’espace de pile qui est garanti pour être disponible après qu’une opération de pile se termine, mais avant la fermeture d’un processus.</span><span class="sxs-lookup"><span data-stu-id="fca75-103">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fca75-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fca75-104">Syntax</span></span>  
  
```  
HRESULT GetStackGuarantee(  
    [out] ULONG *pGuarantee  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fca75-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fca75-105">Parameters</span></span>  
 `pGuarantee`  
 <span data-ttu-id="fca75-106">[out] Pointeur vers le nombre d’octets qui sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="fca75-106">[out] A pointer to the number of bytes that are available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fca75-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fca75-107">Requirements</span></span>  
 <span data-ttu-id="fca75-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fca75-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fca75-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="fca75-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="fca75-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fca75-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="fca75-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fca75-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fca75-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fca75-112">See also</span></span>

- [<span data-ttu-id="fca75-113">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="fca75-113">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
