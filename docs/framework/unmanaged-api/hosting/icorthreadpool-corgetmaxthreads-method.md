---
title: ICorThreadpool::CorGetMaxThreads, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorGetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorGetMaxThreads
helpviewer_keywords:
- CorGetMaxThreads method [.NET Framework hosting]
- ICorThreadpool::CorGetMaxThreads method [.NET Framework hosting]
ms.assetid: 2861533a-cda0-47b3-b716-0d363505289b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bbf5c02972a8331b3dd5e35ffcc4213e094e532d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175732"
---
# <a name="icorthreadpoolcorgetmaxthreads-method"></a><span data-ttu-id="989a2-102">ICorThreadpool::CorGetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="989a2-102">ICorThreadpool::CorGetMaxThreads Method</span></span>
<span data-ttu-id="989a2-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="989a2-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="989a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="989a2-104">Syntax</span></span>  
  
```  
HRESULT CorGetMaxThreads (  
    [out] DWORD *MaxWorkerThreads,  
    [out] DWORD *MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="989a2-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="989a2-105">Requirements</span></span>  
 <span data-ttu-id="989a2-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="989a2-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="989a2-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="989a2-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="989a2-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="989a2-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="989a2-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="989a2-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="989a2-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="989a2-110">See also</span></span>

- [<span data-ttu-id="989a2-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="989a2-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
