---
title: ICorDebugCode2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugCode2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode2
helpviewer_keywords:
- ICorDebugCode2 interface [.NET Framework debugging]
ms.assetid: 9321903b-7dea-40d8-ba32-99016c00cc46
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dce3e3e4baeaa351c5ed1d9e5ca2c03631c3fce4
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56964265"
---
# <a name="icordebugcode2-interface"></a><span data-ttu-id="95e94-102">ICorDebugCode2, interface</span><span class="sxs-lookup"><span data-stu-id="95e94-102">ICorDebugCode2 Interface</span></span>

<span data-ttu-id="95e94-103">Fournit des méthodes qui étendent les capacités de « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="95e94-103">Provides methods that extend the capabilities of "ICorDebugCode".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="95e94-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95e94-104">Methods</span></span>  
  
|<span data-ttu-id="95e94-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="95e94-105">Method</span></span>|<span data-ttu-id="95e94-106">Description</span><span class="sxs-lookup"><span data-stu-id="95e94-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="95e94-107">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="95e94-107">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)|<span data-ttu-id="95e94-108">Obtient les segments de code composée de cet objet de code.</span><span class="sxs-lookup"><span data-stu-id="95e94-108">Gets the chunks of code that this code object is composed of.</span></span>|  
|[<span data-ttu-id="95e94-109">GetCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="95e94-109">GetCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcompilerflags-method.md)|<span data-ttu-id="95e94-110">Obtient les indicateurs qui spécifient les conditions sous lesquelles cet objet de code a été soit juste-à-temps (JIT) compilé ou généré à l’aide du Générateur d’images natives (Ngen.exe).</span><span class="sxs-lookup"><span data-stu-id="95e94-110">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95e94-111">Notes</span><span class="sxs-lookup"><span data-stu-id="95e94-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="95e94-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="95e94-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95e94-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95e94-113">Requirements</span></span>  
 <span data-ttu-id="95e94-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="95e94-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95e94-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="95e94-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="95e94-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="95e94-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="95e94-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95e94-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95e94-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95e94-118">See also</span></span>

- [<span data-ttu-id="95e94-119">ICorDebugCode3, interface</span><span class="sxs-lookup"><span data-stu-id="95e94-119">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
- [<span data-ttu-id="95e94-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="95e94-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
