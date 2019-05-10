---
title: ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode (méthode)
ms.date: 03/30/2017
dev_langs:
- cpp
ms.assetid: b3af44ec-7d41-425b-aed9-0c4379e5cbe9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f390bced01428f2d94b4cebcc26e1d773bda2191
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64613786"
---
# <a name="icordebugprocess8enableexceptioncallbacksoutsideofmycode-method"></a><span data-ttu-id="a35fd-102">ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode (méthode)</span><span class="sxs-lookup"><span data-stu-id="a35fd-102">ICorDebugProcess8::EnableExceptionCallbacksOutsideOfMyCode Method</span></span>
<span data-ttu-id="a35fd-103">[Prise en charge dans [!INCLUDE[net_v46](../../../../includes/net-v46-md.md)] et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="a35fd-103">[Supported in the [!INCLUDE[net_v46](../../../../includes/net-v46-md.md)] and later versions]</span></span>  
  
 <span data-ttu-id="a35fd-104">Active ou désactive certains types de [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) rappels d’exception.</span><span class="sxs-lookup"><span data-stu-id="a35fd-104">Enables or disables certain types of [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) exception callbacks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a35fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a35fd-105">Syntax</span></span>  
  
```cpp
HRESULT EnableExceptionCallbacksOutsideOfMyCode(  
   [in] BOOL enableExceptionsOutsideOfJMC  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a35fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a35fd-106">Parameters</span></span>  
 `enableExceptionsOutsideOfJMC`  
 <span data-ttu-id="a35fd-107">[in]</span><span class="sxs-lookup"><span data-stu-id="a35fd-107">[in]</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a35fd-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a35fd-108">Remarks</span></span>  
 <span data-ttu-id="a35fd-109">Si la valeur de `enableExceptionsOutsideOfJMC` est `false` :</span><span class="sxs-lookup"><span data-stu-id="a35fd-109">If the value of `enableExceptionsOutsideOfJMC` is `false`:</span></span>  
  
- <span data-ttu-id="a35fd-110">Une exception DEBUG_EXCEPTION_FIRST_CHANCE pas entraîne un rappel au débogueur.</span><span class="sxs-lookup"><span data-stu-id="a35fd-110">A DEBUG_EXCEPTION_FIRST_CHANCE exception will not result in a callback to the debugger.</span></span>  
  
- <span data-ttu-id="a35fd-111">Une exception DEBUG_EXCEPTION_CATCH_HANDLER_FOUND pas entraîne un rappel au débogueur si l’exception s’échappe jamais dans le code utilisateur (autrement dit, le chemin d’origine vers un gestionnaire d’exceptions n’a aucune méthode marquée JustMyCode ou JMC).</span><span class="sxs-lookup"><span data-stu-id="a35fd-111">A DEBUG_EXCEPTION_CATCH_HANDLER_FOUND exception will not result in a callback to the debugger if the exception never escapes into user code (that is, the path from an exception origin to an exception handler has no methods marked as JustMyCode, or JMC).</span></span>  
  
 <span data-ttu-id="a35fd-112">La valeur par défaut de `enableExceptionsOutsideOfJMC` est `true`.</span><span class="sxs-lookup"><span data-stu-id="a35fd-112">The default value of `enableExceptionsOutsideOfJMC` is `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a35fd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a35fd-113">Requirements</span></span>  
 <span data-ttu-id="a35fd-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a35fd-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a35fd-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a35fd-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a35fd-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a35fd-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a35fd-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a35fd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a35fd-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a35fd-118">See also</span></span>

- [<span data-ttu-id="a35fd-119">ICorDebugProcess8, interface</span><span class="sxs-lookup"><span data-stu-id="a35fd-119">ICorDebugProcess8 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess8-interface.md)
- [<span data-ttu-id="a35fd-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a35fd-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
