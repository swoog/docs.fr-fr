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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198242"
---
# <a name="icorthreadpoolcorsetmaxthreads-method"></a><span data-ttu-id="1c550-102">ICorThreadpool::CorSetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="1c550-102">ICorThreadpool::CorSetMaxThreads Method</span></span>
<span data-ttu-id="1c550-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="1c550-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c550-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c550-104">Syntax</span></span>  
  
```  
HRESULT CorSetMaxThreads (  
    [in] DWORD MaxWorkerThreads,  
    [in] DWORD MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="1c550-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c550-105">Requirements</span></span>  
 <span data-ttu-id="1c550-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c550-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c550-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1c550-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1c550-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1c550-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="1c550-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1c550-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1c550-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c550-110">See also</span></span>

- [<span data-ttu-id="1c550-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="1c550-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
