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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59144415"
---
# <a name="igcthreadcontrolsuspensionending-method"></a><span data-ttu-id="83478-102">IGCThreadControl::SuspensionEnding, méthode</span><span class="sxs-lookup"><span data-stu-id="83478-102">IGCThreadControl::SuspensionEnding Method</span></span>
<span data-ttu-id="83478-103">Avertit l’hôte que le runtime est reprise des threads après un garbage collection ou une suspension.</span><span class="sxs-lookup"><span data-stu-id="83478-103">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83478-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83478-104">Syntax</span></span>  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83478-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83478-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="83478-106">[in] La génération sur lequel un garbage collection a été effectué.</span><span class="sxs-lookup"><span data-stu-id="83478-106">[in] The generation on which a garbage collection has been performed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="83478-107">Notes</span><span class="sxs-lookup"><span data-stu-id="83478-107">Remarks</span></span>  
 <span data-ttu-id="83478-108">Ne replanifiez pas de threads pendant le `SuspensionEnding` rappel.</span><span class="sxs-lookup"><span data-stu-id="83478-108">Do not reschedule any threads during the `SuspensionEnding` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83478-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83478-109">Requirements</span></span>  
 <span data-ttu-id="83478-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83478-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83478-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="83478-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83478-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83478-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="83478-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="83478-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="83478-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83478-114">See also</span></span>

- [<span data-ttu-id="83478-115">IGCThreadControl, interface</span><span class="sxs-lookup"><span data-stu-id="83478-115">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
