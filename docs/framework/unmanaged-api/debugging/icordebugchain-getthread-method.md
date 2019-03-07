---
title: ICorDebugChain::GetThread, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugChain interface [.NET Framework debugging]
- ICorDebugChain::GetThread method [.NET Framework debugging]
ms.assetid: b3390319-6366-418c-ba80-b552ac4dfc1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ab2b584b4a3e9bef17110f3084dc93efb2e5167
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481649"
---
# <a name="icordebugchaingetthread-method"></a><span data-ttu-id="d5344-102">ICorDebugChain::GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="d5344-102">ICorDebugChain::GetThread Method</span></span>
<span data-ttu-id="d5344-103">Obtient le thread physique cette chaîne d’appel est partie.</span><span class="sxs-lookup"><span data-stu-id="d5344-103">Gets the physical thread this call chain is part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5344-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5344-104">Syntax</span></span>  
  
```  
HRESULT GetThread (  
    [out] ICorDebugThread    **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5344-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5344-105">Parameters</span></span>  
 `ppThread`  
 <span data-ttu-id="d5344-106">[out] Un pointeur vers un objet ICorDebugThread qui représente le thread physique fait partie de cette chaîne d’appel.</span><span class="sxs-lookup"><span data-stu-id="d5344-106">[out] A pointer to an ICorDebugThread object that represents the physical thread this call chain is part of.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5344-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d5344-107">Requirements</span></span>  
 <span data-ttu-id="d5344-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d5344-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5344-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d5344-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d5344-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5344-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d5344-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5344-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
