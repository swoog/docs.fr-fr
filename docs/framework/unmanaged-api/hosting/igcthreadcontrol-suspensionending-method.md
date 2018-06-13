---
title: IGCThreadControl::SuspensionEnding, méthode
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d0986645a8ce4076c27f39f2ae8004ef20bb4bdb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437750"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="611c7-102">IGCThreadControl::SuspensionEnding, méthode</span><span class="sxs-lookup"><span data-stu-id="611c7-102">IGCThreadControl::SuspensionEnding Method</span></span>
<span data-ttu-id="611c7-103">Avertit l’hôte que le runtime est la reprise de threads après un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="611c7-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="611c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="611c7-104">Syntax</span></span>  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="611c7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="611c7-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="611c7-106">[in] La génération sur lequel une opération garbage collection a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="611c7-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="611c7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="611c7-107">Remarks</span></span>  
 <span data-ttu-id="611c7-108">Ne replanifiez pas de threads pendant le `SuspensionEnding` rappel.</span><span class="sxs-lookup"><span data-stu-id="611c7-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="611c7-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="611c7-109">Requirements</span></span>  
 <span data-ttu-id="611c7-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="611c7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="611c7-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="611c7-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="611c7-112">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="611c7-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="611c7-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="611c7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="611c7-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="611c7-114">See Also</span></span>  
 [<span data-ttu-id="611c7-115">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="611c7-115">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
