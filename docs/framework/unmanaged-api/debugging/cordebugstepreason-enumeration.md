---
title: CorDebugStepReason, énumération
ms.date: 03/30/2017
api_name:
- CorDebugStepReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugStepReason
helpviewer_keywords:
- CorDebugStepReason enumeration [.NET Framework debugging]
ms.assetid: fe248069-b33c-48e1-a777-06ac9b239c54
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3ce2b23306e7e38f3982f8d5a4b377aa2f9547c4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59186249"
---
# <a name="cordebugstepreason-enumeration"></a><span data-ttu-id="24ac6-102">CorDebugStepReason, énumération</span><span class="sxs-lookup"><span data-stu-id="24ac6-102">CorDebugStepReason Enumeration</span></span>
<span data-ttu-id="24ac6-103">Indique le résultat d'une étape individuelle.</span><span class="sxs-lookup"><span data-stu-id="24ac6-103">Indicates the outcome of an individual step.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24ac6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24ac6-104">Syntax</span></span>  
  
```  
typedef enum CorDebugStepReason {  
    STEP_NORMAL,  
    STEP_RETURN,  
    STEP_CALL,  
    STEP_EXCEPTION_FILTER,  
    STEP_EXCEPTION_HANDLER,  
    STEP_INTERCEPT,  
    STEP_EXIT  
} CorDebugStepReason;  
```  
  
## <a name="members"></a><span data-ttu-id="24ac6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="24ac6-105">Members</span></span>  
  
|<span data-ttu-id="24ac6-106">Membre</span><span class="sxs-lookup"><span data-stu-id="24ac6-106">Member</span></span>|<span data-ttu-id="24ac6-107">Description</span><span class="sxs-lookup"><span data-stu-id="24ac6-107">Description</span></span>|  
|------------|-----------------|  
|`STEP_NORMAL`|<span data-ttu-id="24ac6-108">Exécution pas à pas s’est terminée normalement, dans la même fonction.</span><span class="sxs-lookup"><span data-stu-id="24ac6-108">Stepping completed normally, within the same function.</span></span>|  
|`STEP_RETURN`|<span data-ttu-id="24ac6-109">Exécution pas à pas a continué normalement, une fois que la fonction est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="24ac6-109">Stepping continued normally, after the function returned.</span></span>|  
|`STEP_CALL`|<span data-ttu-id="24ac6-110">Exécution pas à pas a continué normalement, au début d’une fonction qui vient d’être appelée.</span><span class="sxs-lookup"><span data-stu-id="24ac6-110">Stepping continued normally, at the beginning of a newly called function.</span></span>|  
|`STEP_EXCEPTION_FILTER`|<span data-ttu-id="24ac6-111">Une exception a été générée et le contrôle a été passé à un filtre d’exception.</span><span class="sxs-lookup"><span data-stu-id="24ac6-111">An exception was generated and control was passed to an exception filter.</span></span>|  
|`STEP_EXCEPTION_HANDLER`|<span data-ttu-id="24ac6-112">Une exception a été générée et le contrôle a été passé à un gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="24ac6-112">An exception was generated and control was passed to an exception handler.</span></span>|  
|`STEP_INTERCEPT`|<span data-ttu-id="24ac6-113">Contrôle a été passé à un intercepteur.</span><span class="sxs-lookup"><span data-stu-id="24ac6-113">Control was passed to an interceptor.</span></span>|  
|`STEP_EXIT`|<span data-ttu-id="24ac6-114">Le thread est arrêté avant la fin de l’étape.</span><span class="sxs-lookup"><span data-stu-id="24ac6-114">The thread exited before the step was completed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24ac6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24ac6-115">Requirements</span></span>  
 <span data-ttu-id="24ac6-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="24ac6-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24ac6-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24ac6-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24ac6-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24ac6-118">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="24ac6-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="24ac6-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="24ac6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24ac6-120">See also</span></span>

- [<span data-ttu-id="24ac6-121">StepComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="24ac6-121">StepComplete Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md)
- [<span data-ttu-id="24ac6-122">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="24ac6-122">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
