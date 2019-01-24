---
title: CorDebugIntercept, énumération
ms.date: 03/30/2017
api_name:
- CorDebugIntercept
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugIntercept
helpviewer_keywords:
- CorDebugIntercept enumeration [.NET Framework debugging]
ms.assetid: 3d5b642e-7ef2-428b-a5ae-509c35ed461a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d15f34c55f0ee261c65649e9d431944201c546f0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506028"
---
# <a name="cordebugintercept-enumeration"></a><span data-ttu-id="9186c-102">CorDebugIntercept, énumération</span><span class="sxs-lookup"><span data-stu-id="9186c-102">CorDebugIntercept Enumeration</span></span>
<span data-ttu-id="9186c-103">Indique les types de code qui peuvent être interceptés (c'est-à-dire pouvant faire l'objet d'un pas à pas détaillé).</span><span class="sxs-lookup"><span data-stu-id="9186c-103">Indicates the types of code that can be intercepted (that is, stepped into).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9186c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9186c-104">Syntax</span></span>  
  
```  
typedef enum CorDebugIntercept {  
    INTERCEPT_NONE                = 0x0,  
    INTERCEPT_CLASS_INIT          = 0x01,  
    INTERCEPT_EXCEPTION_FILTER    = 0x02,  
    INTERCEPT_SECURITY            = 0x04,  
    INTERCEPT_CONTEXT_POLICY      = 0x08,  
    INTERCEPT_INTERCEPTION        = 0x10,  
    INTERCEPT_ALL                 = 0xffff  
} CorDebugIntercept;  
```  
  
## <a name="members"></a><span data-ttu-id="9186c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9186c-105">Members</span></span>  
  
|<span data-ttu-id="9186c-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9186c-106">Member</span></span>|<span data-ttu-id="9186c-107">Description</span><span class="sxs-lookup"><span data-stu-id="9186c-107">Description</span></span>|  
|------------|-----------------|  
|`INTERCEPT_NONE`|<span data-ttu-id="9186c-108">Aucun code ne peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-108">No code can be intercepted.</span></span>|  
|`INTERCEPT_CLASS_INIT`|<span data-ttu-id="9186c-109">Un constructeur peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-109">A constructor can be intercepted.</span></span>|  
|`INTERCEPT_EXCEPTION_FILTER`|<span data-ttu-id="9186c-110">Un filtre d'exception peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-110">An exception filter can be intercepted.</span></span>|  
|`INTERCEPT_SECURITY`|<span data-ttu-id="9186c-111">Le code qui applique la sécurité peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-111">Code that enforces security can be intercepted.</span></span>|  
|`INTERCEPT_CONTEXT_POLICY`|<span data-ttu-id="9186c-112">Une stratégie de contexte peut être interceptée.</span><span class="sxs-lookup"><span data-stu-id="9186c-112">A context policy can be intercepted.</span></span>|  
|`INTERCEPT_INTERCEPTION`|<span data-ttu-id="9186c-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9186c-113">Not used.</span></span>|  
|`INTERCEPT_ALL`|<span data-ttu-id="9186c-114">Aucun code ne peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-114">All code can be intercepted.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9186c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9186c-115">Remarks</span></span>  
 <span data-ttu-id="9186c-116">Utilisez le [ICorDebugStepper::SetInterceptMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md) méthode pour définir les types de code qui peut être intercepté.</span><span class="sxs-lookup"><span data-stu-id="9186c-116">Use the [ICorDebugStepper::SetInterceptMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md) method to establish the types of code that can be intercepted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9186c-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9186c-117">Requirements</span></span>  
 <span data-ttu-id="9186c-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9186c-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9186c-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9186c-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9186c-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9186c-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9186c-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9186c-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9186c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9186c-122">See also</span></span>
- [<span data-ttu-id="9186c-123">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="9186c-123">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
