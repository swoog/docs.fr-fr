---
title: ICorDebugFunction3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFunction3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b22717b9-ead5-4eea-887e-789b52d613dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c1945e678dd62f81c698807714d0e71053d6b378
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414783"
---
# <a name="icordebugfunction3-interface"></a><span data-ttu-id="197ea-102">ICorDebugFunction3, interface</span><span class="sxs-lookup"><span data-stu-id="197ea-102">ICorDebugFunction3 Interface</span></span>
<span data-ttu-id="197ea-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="197ea-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="197ea-104">Étend logiquement l’interface ICorDebugFunction pour fournir un accès au code à partir d’une demande ReJIT.</span><span class="sxs-lookup"><span data-stu-id="197ea-104">Logically extends the ICorDebugFunction interface to provide access to code from a ReJIT request.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="197ea-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="197ea-105">Methods</span></span>  
  
|<span data-ttu-id="197ea-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="197ea-106">Method</span></span>|<span data-ttu-id="197ea-107">Description</span><span class="sxs-lookup"><span data-stu-id="197ea-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="197ea-108">GetActiveReJitRequestILCode, méthode</span><span class="sxs-lookup"><span data-stu-id="197ea-108">GetActiveReJitRequestILCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-getactiverejitrequestilcode-method.md)|<span data-ttu-id="197ea-109">Obtient un pointeur d’interface vers un [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) qui contient le langage intermédiaire d’une demande ReJIT active.</span><span class="sxs-lookup"><span data-stu-id="197ea-109">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="197ea-110">Notes</span><span class="sxs-lookup"><span data-stu-id="197ea-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="197ea-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="197ea-111">Requirements</span></span>  
 <span data-ttu-id="197ea-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="197ea-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="197ea-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="197ea-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="197ea-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="197ea-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="197ea-115">**Versions du .NET framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="197ea-115">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="197ea-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="197ea-116">See Also</span></span>  
 [<span data-ttu-id="197ea-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="197ea-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="197ea-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="197ea-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)  
 [<span data-ttu-id="197ea-119">ReJIT : Un Guide de procédures relatives</span><span class="sxs-lookup"><span data-stu-id="197ea-119">ReJIT: A How-To Guide</span></span>](http://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
