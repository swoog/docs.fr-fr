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
ms.openlocfilehash: 90b0cba50129bc728089e41ece5a30697cfc3bc5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61763202"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="7c988-102">IGCThreadControl::SuspensionEnding, méthode</span><span class="sxs-lookup"><span data-stu-id="7c988-102">IGCThreadControl::SuspensionEnding Method</span></span>
<span data-ttu-id="7c988-103">Avertit l’hôte que le runtime est reprise des threads après un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="7c988-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7c988-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c988-104">Syntax</span></span>  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7c988-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c988-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="7c988-106">[in] La génération sur lequel un garbage collection a été effectué.</span><span class="sxs-lookup"><span data-stu-id="7c988-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7c988-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7c988-107">Remarks</span></span>  
 <span data-ttu-id="7c988-108">Ne replanifiez pas de threads pendant le `SuspensionEnding` rappel.</span><span class="sxs-lookup"><span data-stu-id="7c988-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c988-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c988-109">Requirements</span></span>  
 <span data-ttu-id="7c988-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c988-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c988-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="7c988-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7c988-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7c988-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7c988-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c988-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c988-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c988-114">See also</span></span>

- [<span data-ttu-id="7c988-115">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="7c988-115">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
