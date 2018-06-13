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
ms.openlocfilehash: c25f39cf64f462ac319803354e6a2a54ea482b9e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436934"
---
# <a name="icorthreadpoolcorgetmaxthreads-method"></a><span data-ttu-id="c43ac-102">ICorThreadpool::CorGetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="c43ac-102">ICorThreadpool::CorGetMaxThreads Method</span></span>
<span data-ttu-id="c43ac-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="c43ac-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c43ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c43ac-104">Syntax</span></span>  
  
```  
HRESULT CorGetMaxThreads (  
    [out] DWORD *MaxWorkerThreads,  
    [out] DWORD *MaxIOCompletionThreads  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="c43ac-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c43ac-105">Requirements</span></span>  
 <span data-ttu-id="c43ac-106">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c43ac-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c43ac-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c43ac-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c43ac-108">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c43ac-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c43ac-109">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c43ac-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c43ac-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c43ac-110">See Also</span></span>  
 [<span data-ttu-id="c43ac-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="c43ac-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
