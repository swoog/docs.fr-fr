---
title: ICorThreadpool::CorSetMaxThreads, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorSetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSetMaxThreads
helpviewer_keywords:
- ICorThreadpool::CorSetMaxThreads method [.NET Framework hosting]
- CorSetMaxThreads method [.NET Framework hosting]
ms.assetid: 4a846238-df4e-4060-ba3b-5173f6a51e85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b7cbc14c1b84ae5605f7aaed688acbedbb51d056
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437129"
---
# <a name="icorthreadpoolcorsetmaxthreads-method"></a><span data-ttu-id="4493c-102">ICorThreadpool::CorSetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="4493c-102">ICorThreadpool::CorSetMaxThreads Method</span></span>
<span data-ttu-id="4493c-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="4493c-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4493c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4493c-104">Syntax</span></span>  
  
```  
HRESULT CorSetMaxThreads (  
    [in] DWORD MaxWorkerThreads,  
    [in] DWORD MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="4493c-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4493c-105">Requirements</span></span>  
 <span data-ttu-id="4493c-106">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4493c-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4493c-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="4493c-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4493c-108">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4493c-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4493c-109">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4493c-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4493c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4493c-110">See Also</span></span>  
 [<span data-ttu-id="4493c-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="4493c-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
