---
title: ICorDebugMDA::GetOSThreadId, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetOSThreadId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetOSThreadId
helpviewer_keywords:
- ICorDebugMDA::GetOSThreadId method [.NET Framework debugging]
- GetOSThreadId method [.NET Framework debugging]
ms.assetid: 7ca7c364-ade4-4219-b434-9f6ae2359be6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e67e3bc3477e078a4f1d963cdd768676503dc953
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607661"
---
# <a name="icordebugmdagetosthreadid-method"></a><span data-ttu-id="0c7de-102">ICorDebugMDA::GetOSThreadId, méthode</span><span class="sxs-lookup"><span data-stu-id="0c7de-102">ICorDebugMDA::GetOSThreadId Method</span></span>
<span data-ttu-id="0c7de-103">Obtient l’identificateur de thread de système d’exploitation (se) sur lequel l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md) s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0c7de-103">Gets the operating system (OS) thread identifier upon which the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md) is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c7de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c7de-104">Syntax</span></span>  
  
```  
HRESULT GetOSThreadId (  
    [out] DWORD    *pOsTid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0c7de-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c7de-105">Parameters</span></span>  
 `pOsTid`  
 <span data-ttu-id="0c7de-106">[out] Pointeur vers l’identificateur du thread du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0c7de-106">[out] A pointer to the OS thread identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0c7de-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0c7de-107">Remarks</span></span>  
 <span data-ttu-id="0c7de-108">Le thread de système d’exploitation est utilisé au lieu d’un ICorDebugThread pour les situations dans lesquelles un MDA est déclenché sur un thread natif ou sur un thread managé qui n’a pas encore entré le code managé.</span><span class="sxs-lookup"><span data-stu-id="0c7de-108">The OS thread is used instead of an ICorDebugThread to allow for situations in which an MDA is fired either on a native thread or on a managed thread that has not yet entered managed code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c7de-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c7de-109">Requirements</span></span>  
 <span data-ttu-id="0c7de-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c7de-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c7de-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0c7de-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0c7de-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c7de-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c7de-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c7de-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c7de-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7de-114">See also</span></span>
- [<span data-ttu-id="0c7de-115">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="0c7de-115">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [<span data-ttu-id="0c7de-116">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="0c7de-116">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
