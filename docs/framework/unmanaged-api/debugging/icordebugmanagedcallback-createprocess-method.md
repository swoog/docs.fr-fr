---
title: ICorDebugManagedCallback::CreateProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.CreateProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::CreateProcess
helpviewer_keywords:
- ICorDebugManagedCallback::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: 8e89d5ee-e4e3-4738-8302-0b7d1cf4846e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7693111427f3181adcd2127ad5ecb2a317e30921
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515613"
---
# <a name="icordebugmanagedcallbackcreateprocess-method"></a><span data-ttu-id="aed47-102">ICorDebugManagedCallback::CreateProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="aed47-102">ICorDebugManagedCallback::CreateProcess Method</span></span>
<span data-ttu-id="aed47-103">Notifie le débogueur lorsqu’un processus a été joint ou démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="aed47-103">Notifies the debugger when a process has been attached or started for the first time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aed47-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aed47-104">Syntax</span></span>  
  
```  
HRESULT CreateProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aed47-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aed47-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="aed47-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus qui a été joint ou démarré.</span><span class="sxs-lookup"><span data-stu-id="aed47-106">[in] A pointer to an ICorDebugProcess object that represents the process that has been attached or started.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aed47-107">Notes</span><span class="sxs-lookup"><span data-stu-id="aed47-107">Remarks</span></span>  
 <span data-ttu-id="aed47-108">Cette méthode n’est pas appelée jusqu'à ce que le common language runtime est initialisé.</span><span class="sxs-lookup"><span data-stu-id="aed47-108">This method is not called until the common language runtime is initialized.</span></span> <span data-ttu-id="aed47-109">La plupart de la [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) méthodes retourneront CORDBG_E_NOTREADY avant le `CreateProcess` rappel.</span><span class="sxs-lookup"><span data-stu-id="aed47-109">Most of the [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) methods will return CORDBG_E_NOTREADY before the `CreateProcess` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aed47-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aed47-110">Requirements</span></span>  
 <span data-ttu-id="aed47-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aed47-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aed47-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aed47-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aed47-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aed47-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aed47-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aed47-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aed47-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aed47-115">See also</span></span>
- [<span data-ttu-id="aed47-116">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="aed47-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
