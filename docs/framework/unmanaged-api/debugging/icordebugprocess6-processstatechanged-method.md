---
title: ICorDebugProcess6::ProcessStateChanged, méthode
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bc5861762242412d7ab6f0c02f2b8f5c149f9453
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420177"
---
# <a name="icordebugprocess6processstatechanged-method"></a><span data-ttu-id="019df-102">ICorDebugProcess6::ProcessStateChanged, méthode</span><span class="sxs-lookup"><span data-stu-id="019df-102">ICorDebugProcess6::ProcessStateChanged Method</span></span>
<span data-ttu-id="019df-103">Notifie [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="019df-103">Notifies [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="019df-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="019df-104">Syntax</span></span>  
  
```  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="019df-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="019df-105">Parameters</span></span>  
 `change`  
 <span data-ttu-id="019df-106">[in] Un membre de la [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) énumération</span><span class="sxs-lookup"><span data-stu-id="019df-106">[in] A member of the [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) enumeration</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="019df-107">Notes</span><span class="sxs-lookup"><span data-stu-id="019df-107">Remarks</span></span>  
 <span data-ttu-id="019df-108">Le débogueur appelle cette méthode pour notifier [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) le processus est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="019df-108">The debugger calls this method to notify [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) that the process is running.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="019df-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="019df-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="019df-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="019df-110">Requirements</span></span>  
 <span data-ttu-id="019df-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="019df-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="019df-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="019df-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="019df-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="019df-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="019df-114">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="019df-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="019df-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="019df-115">See Also</span></span>  
 [<span data-ttu-id="019df-116">ICorDebugProcess6, interface</span><span class="sxs-lookup"><span data-stu-id="019df-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)  
 [<span data-ttu-id="019df-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="019df-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
