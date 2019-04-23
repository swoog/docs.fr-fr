---
title: COR_DEBUG_STEP_RANGE, structure
ms.date: 03/30/2017
api_name:
- COR_DEBUG_STEP_RANGE
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_DEBUG_STEP_RANGE
helpviewer_keywords:
- COR_DEBUG_STEP_RANGE structure [.NET Framework debugging]
ms.assetid: 8809d00e-beaa-4dcf-b4e8-e89d0a5406b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 57d7c3256d7b52a4e55dbb5bc420b0438983d2f2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59219679"
---
# <a name="cordebugsteprange-structure"></a><span data-ttu-id="1b5c2-102">COR_DEBUG_STEP_RANGE, structure</span><span class="sxs-lookup"><span data-stu-id="1b5c2-102">COR_DEBUG_STEP_RANGE Structure</span></span>
<span data-ttu-id="1b5c2-103">Contient les informations de décalage pour une plage de code.</span><span class="sxs-lookup"><span data-stu-id="1b5c2-103">Contains the offset information for a range of code.</span></span>  
  
 <span data-ttu-id="1b5c2-104">Cette structure est utilisée par le [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1b5c2-104">This structure is used by the [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b5c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b5c2-105">Syntax</span></span>  
  
```  
typedef struct {  
    ULONG32 startOffset;  
    ULONG32 endOffset;  
} COR_DEBUG_STEP_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="1b5c2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1b5c2-106">Members</span></span>  
  
|<span data-ttu-id="1b5c2-107">Membre</span><span class="sxs-lookup"><span data-stu-id="1b5c2-107">Member</span></span>|<span data-ttu-id="1b5c2-108">Description</span><span class="sxs-lookup"><span data-stu-id="1b5c2-108">Description</span></span>|  
|------------|-----------------|  
|`startOffset`|<span data-ttu-id="1b5c2-109">Le décalage du début de la plage.</span><span class="sxs-lookup"><span data-stu-id="1b5c2-109">The offset of the beginning of the range.</span></span>|  
|`endOffset`|<span data-ttu-id="1b5c2-110">Le décalage de la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="1b5c2-110">The offset of the end of the range.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1b5c2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b5c2-111">Requirements</span></span>  
 <span data-ttu-id="1b5c2-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b5c2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b5c2-113">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="1b5c2-113">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="1b5c2-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1b5c2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1b5c2-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b5c2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b5c2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b5c2-116">See also</span></span>

- [<span data-ttu-id="1b5c2-117">StepRange, méthode</span><span class="sxs-lookup"><span data-stu-id="1b5c2-117">StepRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md)
- [<span data-ttu-id="1b5c2-118">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="1b5c2-118">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="1b5c2-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="1b5c2-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
