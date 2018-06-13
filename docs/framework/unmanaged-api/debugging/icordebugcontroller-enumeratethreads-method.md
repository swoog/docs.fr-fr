---
title: ICorDebugController::EnumerateThreads, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.EnumerateThreads
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::EnumerateThreads
helpviewer_keywords:
- ICorDebugController::EnumerateThreads method [.NET Framework debugging]
- EnumerateThreads method [.NET Framework debugging]
ms.assetid: 73f536f6-4668-4a4a-b3e4-ac7df862d5be
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f8276e2a8fd1bdc546add2ae1ca5d96298186c7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412829"
---
# <a name="icordebugcontrollerenumeratethreads-method"></a><span data-ttu-id="1ce50-102">ICorDebugController::EnumerateThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="1ce50-102">ICorDebugController::EnumerateThreads Method</span></span>
<span data-ttu-id="1ce50-103">Obtient un énumérateur pour les threads managés actifs dans le processus.</span><span class="sxs-lookup"><span data-stu-id="1ce50-103">Gets an enumerator for the active managed threads in the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ce50-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ce50-104">Syntax</span></span>  
  
```  
HRESULT EnumerateThreads (  
    [out] ICorDebugThreadEnum **ppThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ce50-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ce50-105">Parameters</span></span>  
 `ppThreads`  
 <span data-ttu-id="1ce50-106">[out] Pointeur vers l’adresse d’un objet « ICorDebugThreadEnum » qui représente un énumérateur pour tous les threads managés qui sont actifs dans le processus.</span><span class="sxs-lookup"><span data-stu-id="1ce50-106">[out] A pointer to the address of an "ICorDebugThreadEnum" object that represents an enumerator for all managed threads that are active in the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ce50-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1ce50-107">Remarks</span></span>  
 <span data-ttu-id="1ce50-108">Un thread est considéré comme actif une fois la [ICorDebugManagedCallback::CreateThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createthread-method.md) du rappel et avant la [ICorDebugManagedCallback::ExitThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitthread-method.md) du rappel .</span><span class="sxs-lookup"><span data-stu-id="1ce50-108">A thread is considered active after the [ICorDebugManagedCallback::CreateThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createthread-method.md) callback has been dispatched and before the [ICorDebugManagedCallback::ExitThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitthread-method.md) callback has been dispatched.</span></span> <span data-ttu-id="1ce50-109">Un thread managé ne peut pas nécessairement des frames managés sur sa pile.</span><span class="sxs-lookup"><span data-stu-id="1ce50-109">A managed thread may not necessarily have any managed frames on its stack.</span></span> <span data-ttu-id="1ce50-110">Les threads peuvent être énumérés avant même que le [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="1ce50-110">Threads can be enumerated even before the [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) callback.</span></span> <span data-ttu-id="1ce50-111">L’énumération sera naturellement vide.</span><span class="sxs-lookup"><span data-stu-id="1ce50-111">The enumeration will naturally be empty.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ce50-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1ce50-112">Requirements</span></span>  
 <span data-ttu-id="1ce50-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ce50-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ce50-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1ce50-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1ce50-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ce50-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ce50-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ce50-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ce50-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ce50-117">See Also</span></span>  
 
