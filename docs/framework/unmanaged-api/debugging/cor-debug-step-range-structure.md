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
ms.openlocfilehash: 45340a26b3351ca03b453fbcdb626de199bd6d19
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54710363"
---
# <a name="cordebugsteprange-structure"></a><span data-ttu-id="64aff-102">COR_DEBUG_STEP_RANGE, structure</span><span class="sxs-lookup"><span data-stu-id="64aff-102">COR_DEBUG_STEP_RANGE Structure</span></span>
<span data-ttu-id="64aff-103">Contient les informations de décalage pour une plage de code.</span><span class="sxs-lookup"><span data-stu-id="64aff-103">Contains the offset information for a range of code.</span></span>  
  
 <span data-ttu-id="64aff-104">Cette structure est utilisée par le [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="64aff-104">This structure is used by the [ICorDebugStepper::StepRange](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64aff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64aff-105">Syntax</span></span>  
  
```  
typedef struct {  
    ULONG32 startOffset;  
    ULONG32 endOffset;  
} COR_DEBUG_STEP_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="64aff-106">Membres</span><span class="sxs-lookup"><span data-stu-id="64aff-106">Members</span></span>  
  
|<span data-ttu-id="64aff-107">Membre</span><span class="sxs-lookup"><span data-stu-id="64aff-107">Member</span></span>|<span data-ttu-id="64aff-108">Description</span><span class="sxs-lookup"><span data-stu-id="64aff-108">Description</span></span>|  
|------------|-----------------|  
|`startOffset`|<span data-ttu-id="64aff-109">Le décalage du début de la plage.</span><span class="sxs-lookup"><span data-stu-id="64aff-109">The offset of the beginning of the range.</span></span>|  
|`endOffset`|<span data-ttu-id="64aff-110">Le décalage de la fin de la plage.</span><span class="sxs-lookup"><span data-stu-id="64aff-110">The offset of the end of the range.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="64aff-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="64aff-111">Requirements</span></span>  
 <span data-ttu-id="64aff-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64aff-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64aff-113">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="64aff-113">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="64aff-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="64aff-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="64aff-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64aff-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64aff-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64aff-116">See also</span></span>
- [<span data-ttu-id="64aff-117">StepRange, méthode</span><span class="sxs-lookup"><span data-stu-id="64aff-117">StepRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-steprange-method.md)
- [<span data-ttu-id="64aff-118">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="64aff-118">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="64aff-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="64aff-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
