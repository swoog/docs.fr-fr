---
title: ICorDebugProcess6::ProcessStateChanged, méthode
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb134b7d188c2fb966b53e4520a7fb825f11e428
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54612045"
---
# <a name="icordebugprocess6processstatechanged-method"></a><span data-ttu-id="25050-102">ICorDebugProcess6::ProcessStateChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="25050-102">ICorDebugProcess6::ProcessStateChanged Method</span></span>
<span data-ttu-id="25050-103">Avertit [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="25050-103">Notifies [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25050-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25050-104">Syntax</span></span>  
  
```  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="25050-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25050-105">Parameters</span></span>  
 `change`  
 <span data-ttu-id="25050-106">[in] Un membre de la [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) énumération</span><span class="sxs-lookup"><span data-stu-id="25050-106">[in] A member of the [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) enumeration</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="25050-107">Notes</span><span class="sxs-lookup"><span data-stu-id="25050-107">Remarks</span></span>  
 <span data-ttu-id="25050-108">Le débogueur appelle cette méthode pour notifier [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="25050-108">The debugger calls this method to notify [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="25050-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="25050-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25050-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="25050-110">Requirements</span></span>  
 <span data-ttu-id="25050-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="25050-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="25050-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="25050-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="25050-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="25050-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="25050-114">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="25050-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25050-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25050-115">See also</span></span>
- [<span data-ttu-id="25050-116">ICorDebugProcess6, interface</span><span class="sxs-lookup"><span data-stu-id="25050-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)
- [<span data-ttu-id="25050-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="25050-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
