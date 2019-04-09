---
title: ICorThreadpool::CorBindIoCompletionCallback, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorBindIoCompletionCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorBindIoCompletionCallback
helpviewer_keywords:
- CorBindIoCompletionCallback method [.NET Framework hosting]
- ICorThreadpool::CorBindIoCompletionCallback method [.NET Framework hosting]
ms.assetid: 2b159225-f09c-42f1-aa7c-44087e121249
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b3faffbf9dc85c563dac84fc2e4e4d849db5d42d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59148523"
---
# <a name="icorthreadpoolcorbindiocompletioncallback-method"></a><span data-ttu-id="3aabd-102">ICorThreadpool::CorBindIoCompletionCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="3aabd-102">ICorThreadpool::CorBindIoCompletionCallback Method</span></span>
<span data-ttu-id="3aabd-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="3aabd-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aabd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aabd-104">Syntax</span></span>  
  
```  
HRESULT CorBindIoCompletionCallback (  
    [in] HANDLE                          fileHandle,  
    [in] LPOVERLAPPED_COMPLETION_ROUTINE callback  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="3aabd-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aabd-105">Requirements</span></span>  
 <span data-ttu-id="3aabd-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3aabd-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aabd-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3aabd-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3aabd-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3aabd-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="3aabd-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3aabd-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3aabd-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aabd-110">See also</span></span>

- [<span data-ttu-id="3aabd-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="3aabd-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
