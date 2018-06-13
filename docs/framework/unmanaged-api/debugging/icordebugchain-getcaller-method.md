---
title: ICorDebugChain::GetCaller, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCaller
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCaller
helpviewer_keywords:
- ICorDebugChain::GetCaller method [.NET Framework debugging]
- GetCaller method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: d0b8ab4b-d7d2-4fa0-945f-3d2b87e7e991
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a0b5d702e9718ce6ac537beae67fc190b152b9f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405141"
---
# <a name="icordebugchaingetcaller-method"></a><span data-ttu-id="e9249-102">ICorDebugChain::GetCaller, méthode</span><span class="sxs-lookup"><span data-stu-id="e9249-102">ICorDebugChain::GetCaller Method</span></span>
<span data-ttu-id="e9249-103">Obtient la chaîne qui a appelé cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e9249-103">Gets the chain that called this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9249-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9249-104">Syntax</span></span>  
  
```  
HRESULT GetCaller (  
    [out] ICorDebugChain      **ppChain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e9249-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9249-105">Parameters</span></span>  
 `ppChain`  
 <span data-ttu-id="e9249-106">[out] Pointeur vers l’adresse d’un objet ICorDebugChain qui représente la chaîne d’appel.</span><span class="sxs-lookup"><span data-stu-id="e9249-106">[out] A pointer to the address of an ICorDebugChain object that represents the calling chain.</span></span>  
  
 <span data-ttu-id="e9249-107">Si cette chaîne a été appelée spontanément (comme ce serait le cas si cette chaîne ou le débogueur initialisé la pile des appels), `ppChain` sera null.</span><span class="sxs-lookup"><span data-stu-id="e9249-107">If this chain was spontaneously called (as would be the case if this chain or the debugger initialized the call stack), `ppChain` will be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e9249-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e9249-108">Remarks</span></span>  
 <span data-ttu-id="e9249-109">La chaîne d’appels peut être sur un autre thread, si l’appel a été marshalé à travers les threads.</span><span class="sxs-lookup"><span data-stu-id="e9249-109">The calling chain may be on a different thread, if the call was marshaled across threads.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9249-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e9249-110">Requirements</span></span>  
 <span data-ttu-id="e9249-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e9249-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e9249-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e9249-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e9249-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e9249-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e9249-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9249-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
