---
title: ICorThreadpool::CorQueueUserWorkItem, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorQueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorQueueUserWorkItem
helpviewer_keywords:
- ICorThreadpool::CorQueueUserWorkItem method [.NET Framework hosting]
- CorQueueUserWorkItem method [.NET Framework hosting]
ms.assetid: 29ac7898-a7c7-433e-8f79-cd5237e0bab8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 249571cbe49fdce720630e31d2da1641aa979624
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218691"
---
# <a name="icorthreadpoolcorqueueuserworkitem-method"></a><span data-ttu-id="8675f-102">ICorThreadpool::CorQueueUserWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="8675f-102">ICorThreadpool::CorQueueUserWorkItem Method</span></span>
<span data-ttu-id="8675f-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="8675f-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8675f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8675f-104">Syntax</span></span>  
  
```  
HRESULT CorQueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID                  Context,  
    [in] BOOL                   executeOnlyOnce,  
    [out] BOOL*                 result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="8675f-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8675f-105">Requirements</span></span>  
 <span data-ttu-id="8675f-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8675f-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8675f-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8675f-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8675f-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8675f-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="8675f-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8675f-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8675f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8675f-110">See also</span></span>

- [<span data-ttu-id="8675f-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="8675f-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
