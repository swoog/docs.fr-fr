---
title: CorDebugSetContextFlag, énumération
ms.date: 03/30/2017
api_name:
- CorDebugSetContextFlag
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugSetContextFlag
helpviewer_keywords:
- CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: badd79926e8f039cf6b947dd6655e2cd679e3000
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406973"
---
# <a name="cordebugsetcontextflag-enumeration"></a><span data-ttu-id="46bc8-102">CorDebugSetContextFlag, énumération</span><span class="sxs-lookup"><span data-stu-id="46bc8-102">CorDebugSetContextFlag Enumeration</span></span>
<span data-ttu-id="46bc8-103">Indique si le contexte provient du frame (ou feuille) actif ou s'il a été calculé par déroulement à partir d'un autre frame.</span><span class="sxs-lookup"><span data-stu-id="46bc8-103">Indicates whether the context is from the active (or leaf) frame on the stack or has been computed by unwinding from another frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46bc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46bc8-104">Syntax</span></span>  
  
```  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="46bc8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="46bc8-105">Members</span></span>  
  
|<span data-ttu-id="46bc8-106">Membre</span><span class="sxs-lookup"><span data-stu-id="46bc8-106">Member</span></span>|<span data-ttu-id="46bc8-107">Description</span><span class="sxs-lookup"><span data-stu-id="46bc8-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="46bc8-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span><span class="sxs-lookup"><span data-stu-id="46bc8-108">SET_CONTEXT_FLAG_ACTIVE_FRAME</span></span>|<span data-ttu-id="46bc8-109">Le contexte est le contexte du thread actif.</span><span class="sxs-lookup"><span data-stu-id="46bc8-109">The context is the thread’s active context.</span></span>|  
|<span data-ttu-id="46bc8-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span><span class="sxs-lookup"><span data-stu-id="46bc8-110">SET_CONTEXT_FLAG_UNWIND_FRAME</span></span>|<span data-ttu-id="46bc8-111">Le contexte a été calculé par déroulement à partir d’un autre frame.</span><span class="sxs-lookup"><span data-stu-id="46bc8-111">The context has been computed by unwinding from another frame.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46bc8-112">Notes</span><span class="sxs-lookup"><span data-stu-id="46bc8-112">Remarks</span></span>  
 <span data-ttu-id="46bc8-113">`CorDebugSetContextFlag` Fournit des valeurs qui sont utilisées par le [ICorDebugStackWalk::SetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="46bc8-113">`CorDebugSetContextFlag` provides values that are used by the [ICorDebugStackWalk::SetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46bc8-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46bc8-114">Requirements</span></span>  
 <span data-ttu-id="46bc8-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46bc8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46bc8-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46bc8-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46bc8-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46bc8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46bc8-118">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46bc8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46bc8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46bc8-119">See Also</span></span>  
 [<span data-ttu-id="46bc8-120">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="46bc8-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="46bc8-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="46bc8-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
