---
title: ICorDebugManagedCallback::ExitThread, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ExitThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ExitThread
helpviewer_keywords:
- ExitThread method [.NET Framework debugging]
- ICorDebugManagedCallback::ExitThread method [.NET Framework debugging]
ms.assetid: 62db708b-6cf0-45c5-b897-4b5c75bd2505
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 37815d8aead1ec89826c13db6f012f2cd17bc792
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988180"
---
# <a name="icordebugmanagedcallbackexitthread-method"></a><span data-ttu-id="c5686-102">ICorDebugManagedCallback::ExitThread, méthode</span><span class="sxs-lookup"><span data-stu-id="c5686-102">ICorDebugManagedCallback::ExitThread Method</span></span>
<span data-ttu-id="c5686-103">Notifie le débogueur qu’un thread qui exécutait le code managé s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="c5686-103">Notifies the debugger that a thread that was executing managed code has exited.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5686-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5686-104">Syntax</span></span>  
  
```  
HRESULT ExitThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5686-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5686-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="c5686-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant le thread managé.</span><span class="sxs-lookup"><span data-stu-id="c5686-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the managed thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="c5686-107">[in] Pointeur vers un objet ICorDebugThread qui représente le thread managé.</span><span class="sxs-lookup"><span data-stu-id="c5686-107">[in] A pointer to an ICorDebugThread object that represents the managed thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c5686-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c5686-108">Remarks</span></span>  
 <span data-ttu-id="c5686-109">Une fois le `ExitThread` rappel est déclenché, le thread n’apparaît plus dans les énumérations de thread.</span><span class="sxs-lookup"><span data-stu-id="c5686-109">Once the `ExitThread` callback is fired, the thread will no longer appear in thread enumerations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5686-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5686-110">Requirements</span></span>  
 <span data-ttu-id="c5686-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c5686-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5686-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c5686-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c5686-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c5686-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c5686-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c5686-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5686-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5686-115">See also</span></span>

- [<span data-ttu-id="c5686-116">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="c5686-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
