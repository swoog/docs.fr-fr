---
title: ICorDebugProcess6::ProcessStateChanged, méthode
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a4dcee3b396d9533f3169db1ea54a6cdc6086c8c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166139"
---
# <a name="icordebugprocess6processstatechanged-method"></a><span data-ttu-id="eda4e-102">ICorDebugProcess6::ProcessStateChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="eda4e-102">ICorDebugProcess6::ProcessStateChanged Method</span></span>
<span data-ttu-id="eda4e-103">Avertit [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eda4e-103">Notifies [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eda4e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eda4e-104">Syntax</span></span>  
  
```  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eda4e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eda4e-105">Parameters</span></span>  
 `change`  
 <span data-ttu-id="eda4e-106">[in] Un membre de la [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) énumération</span><span class="sxs-lookup"><span data-stu-id="eda4e-106">[in] A member of the [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) enumeration</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eda4e-107">Notes</span><span class="sxs-lookup"><span data-stu-id="eda4e-107">Remarks</span></span>  
 <span data-ttu-id="eda4e-108">Le débogueur appelle cette méthode pour notifier [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eda4e-108">The debugger calls this method to notify [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="eda4e-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="eda4e-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eda4e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eda4e-110">Requirements</span></span>  
 <span data-ttu-id="eda4e-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eda4e-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eda4e-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="eda4e-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="eda4e-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eda4e-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eda4e-114">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eda4e-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eda4e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eda4e-115">See also</span></span>

- [<span data-ttu-id="eda4e-116">ICorDebugProcess6, interface</span><span class="sxs-lookup"><span data-stu-id="eda4e-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)
- [<span data-ttu-id="eda4e-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="eda4e-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
