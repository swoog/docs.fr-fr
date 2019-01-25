---
title: ICorThreadpool::CorCallOrQueueUserWorkItem, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCallOrQueueUserWorkItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCallOrQueueUserWorkItem
helpviewer_keywords:
- ICorThreadpool::CorCallOrQueueUserWorkItem method [.NET Framework hosting]
- CorCallOrQueueUserWorkItem method [.NET Framework hosting]
ms.assetid: a2081223-84ca-4331-a8d3-9352f422f3e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 11afa2900ef2db857942e95d0b184f99b1e9c947
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54741806"
---
# <a name="icorthreadpoolcorcallorqueueuserworkitem-method"></a><span data-ttu-id="6fcbb-102">ICorThreadpool::CorCallOrQueueUserWorkItem, méthode</span><span class="sxs-lookup"><span data-stu-id="6fcbb-102">ICorThreadpool::CorCallOrQueueUserWorkItem Method</span></span>
<span data-ttu-id="6fcbb-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fcbb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fcbb-104">Syntax</span></span>  
  
```  
HRESULT CorCallOrQueueUserWorkItem (  
    [in] LPTHREAD_START_ROUTINE Function,  
    [in] PVOID                  Context,  
    [out] BOOL*                 result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="6fcbb-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6fcbb-105">Requirements</span></span>  
 <span data-ttu-id="6fcbb-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6fcbb-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6fcbb-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6fcbb-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6fcbb-108">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6fcbb-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6fcbb-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6fcbb-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fcbb-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fcbb-110">See also</span></span>
- [<span data-ttu-id="6fcbb-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="6fcbb-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
