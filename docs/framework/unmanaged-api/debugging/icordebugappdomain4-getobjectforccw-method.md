---
title: ICorDebugAppDomain4::GetObjectForCCW, méthode
ms.date: 03/30/2017
ms.assetid: 2cacdb85-e7b8-42e7-b310-c3e8c22e5d33
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f1089668aa19747f5f694360ebb87098e2df9ad4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405549"
---
# <a name="icordebugappdomain4getobjectforccw-method"></a><span data-ttu-id="d47ee-102">ICorDebugAppDomain4::GetObjectForCCW, méthode</span><span class="sxs-lookup"><span data-stu-id="d47ee-102">ICorDebugAppDomain4::GetObjectForCCW Method</span></span>
<span data-ttu-id="d47ee-103">Obtient un objet managé à partir d'un pointeur de wrapper CCW (COM Callable Wrapper).</span><span class="sxs-lookup"><span data-stu-id="d47ee-103">Gets a managed object from a COM callable wrapper (CCW) pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d47ee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d47ee-104">Syntax</span></span>  
  
```  
HRESULT GetObjectForCCW(  
   [in]CORDB_ADDRESS ccwPointer,   
   [out]ICorDebugValue **ppManagedObject  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d47ee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d47ee-105">Parameters</span></span>  
 `ccwPointer`  
 <span data-ttu-id="d47ee-106">[in] Pointeur vers un wrapper CCW (COM Callable Wrapper)</span><span class="sxs-lookup"><span data-stu-id="d47ee-106">[in] A COM callable wrapper (CCW) pointer.</span></span>  
  
 `ppManagedObject`  
 <span data-ttu-id="d47ee-107">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » qui représente l’objet managé qui correspond au pointeur CCW donné.</span><span class="sxs-lookup"><span data-stu-id="d47ee-107">[out] A pointer to the address of an "ICorDebugValue" object that represents the managed object that corresponds to the given CCW pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d47ee-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d47ee-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d47ee-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d47ee-109">Requirements</span></span>  
 <span data-ttu-id="d47ee-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d47ee-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d47ee-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d47ee-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d47ee-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d47ee-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d47ee-113">**Versions du .NET framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d47ee-113">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d47ee-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d47ee-114">See Also</span></span>  
 [<span data-ttu-id="d47ee-115">ICorDebugAppDomain4, interface</span><span class="sxs-lookup"><span data-stu-id="d47ee-115">ICorDebugAppDomain4 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain4-interface.md)  
 [<span data-ttu-id="d47ee-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d47ee-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
