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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750109"
---
# <a name="icordebugcode2-interface"></a><span data-ttu-id="7bd2d-102">ICorDebugCode2, interface</span><span class="sxs-lookup"><span data-stu-id="7bd2d-102">ICorDebugCode2 Interface</span></span>

<span data-ttu-id="7bd2d-103">Fournit des méthodes qui étendent les capacités de « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="7bd2d-103">Provides methods that extend the capabilities of "ICorDebugCode".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7bd2d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7bd2d-104">Methods</span></span>  
  
|<span data-ttu-id="7bd2d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7bd2d-105">Method</span></span>|<span data-ttu-id="7bd2d-106">Description</span><span class="sxs-lookup"><span data-stu-id="7bd2d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7bd2d-107">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="7bd2d-107">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)|<span data-ttu-id="7bd2d-108">Obtient les segments de code composée de cet objet de code.</span><span class="sxs-lookup"><span data-stu-id="7bd2d-108">Gets the chunks of code that this code object is composed of.</span></span>|  
|[<span data-ttu-id="7bd2d-109">GetCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="7bd2d-109">GetCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcompilerflags-method.md)|<span data-ttu-id="7bd2d-110">Obtient les indicateurs qui spécifient les conditions sous lesquelles cet objet de code a été soit juste-à-temps (JIT) compilé ou généré à l’aide du Générateur d’images natives (Ngen.exe).</span><span class="sxs-lookup"><span data-stu-id="7bd2d-110">Gets the flags that specify the conditions under which this code object was either just-in-time (JIT) compiled or generated using the native image generator (Ngen.exe).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7bd2d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7bd2d-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7bd2d-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="7bd2d-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7bd2d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bd2d-113">Requirements</span></span>  
 <span data-ttu-id="7bd2d-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7bd2d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7bd2d-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7bd2d-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7bd2d-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7bd2d-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7bd2d-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7bd2d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bd2d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bd2d-118">See also</span></span>

- [<span data-ttu-id="7bd2d-119">ICorDebugCode3, interface</span><span class="sxs-lookup"><span data-stu-id="7bd2d-119">ICorDebugCode3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode3-interface.md)
- [<span data-ttu-id="7bd2d-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7bd2d-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
