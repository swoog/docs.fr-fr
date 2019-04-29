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
ms.openlocfilehash: 48d84d5c45ea8e1af1da44480410692d46162810
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699641"
---
# <a name="icorthreadpoolcorsetmaxthreads-method"></a><span data-ttu-id="bb55c-102">ICorThreadpool::CorSetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="bb55c-102">ICorThreadpool::CorSetMaxThreads Method</span></span>
<span data-ttu-id="bb55c-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="bb55c-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb55c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb55c-104">Syntax</span></span>  
  
```  
HRESULT CorSetMaxThreads (  
    [in] DWORD MaxWorkerThreads,  
    [in] DWORD MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="bb55c-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb55c-105">Requirements</span></span>  
 <span data-ttu-id="bb55c-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bb55c-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb55c-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bb55c-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bb55c-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bb55c-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bb55c-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb55c-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb55c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb55c-110">See also</span></span>

- [<span data-ttu-id="bb55c-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="bb55c-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
