---
title: ICorThreadpool::CorCreateTimer, méthode
ms.date: 03/30/2017
api_name:
- ICorThreadpool.CorCreateTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCreateTimer
helpviewer_keywords:
- CorCreateTimer method [.NET Framework hosting]
- ICorThreadpool::CorCreateTimer method [.NET Framework hosting]
ms.assetid: 0d56ef25-30f1-4499-8a1f-76e7654ec614
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7dfa1dd15f38263ffdfef594ab030867b3fed1de
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436775"
---
# <a name="icorthreadpoolcorcreatetimer-method"></a><span data-ttu-id="f2e83-102">ICorThreadpool::CorCreateTimer, méthode</span><span class="sxs-lookup"><span data-stu-id="f2e83-102">ICorThreadpool::CorCreateTimer Method</span></span>
<span data-ttu-id="f2e83-103">Cette m&#233;thode prend en charge l'infrastructure .NET Framework et n'est pas destin&#233;e &#224; &#234;tre utilis&#233;e directement &#224; partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="f2e83-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2e83-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2e83-104">Syntax</span></span>  
  
```  
HRESULT CorCreateTimer (  
    [in]  HANDLE*             phNewTimer,  
    [in]  WAITORTIMERCALLBACK Callback,  
    [in]  PVOID               Parameter,  
    [in]  DWORD               DueTime,  
    [in]  DWORD               Period,  
    [out] BOOL*               result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="f2e83-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f2e83-105">Requirements</span></span>  
 <span data-ttu-id="f2e83-106">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f2e83-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2e83-107">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f2e83-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f2e83-108">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2e83-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2e83-109">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2e83-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2e83-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2e83-110">See Also</span></span>  
 [<span data-ttu-id="f2e83-111">ICorThreadpool, interface</span><span class="sxs-lookup"><span data-stu-id="f2e83-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
