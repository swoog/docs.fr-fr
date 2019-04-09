---
title: ICorDebugModule2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugModule2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2
helpviewer_keywords:
- ICorDebugModule2 interface [.NET Framework debugging]
ms.assetid: 0847e64f-fdbe-4c96-8168-da20fdc84d80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3fb1bf3f61c78f4eb157b93363b1c06b25bee04
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59119897"
---
# <a name="icordebugmodule2-interface"></a><span data-ttu-id="3a05c-102">ICorDebugModule2, interface</span><span class="sxs-lookup"><span data-stu-id="3a05c-102">ICorDebugModule2 Interface</span></span>

<span data-ttu-id="3a05c-103">Sert d’extension logique à l’interface ICorDebugModule.</span><span class="sxs-lookup"><span data-stu-id="3a05c-103">Serves as a logical extension to the ICorDebugModule interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3a05c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a05c-104">Methods</span></span>  
  
|<span data-ttu-id="3a05c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-105">Method</span></span>|<span data-ttu-id="3a05c-106">Description</span><span class="sxs-lookup"><span data-stu-id="3a05c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3a05c-107">ApplyChanges, méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-107">ApplyChanges Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md)|<span data-ttu-id="3a05c-108">Applique les modifications dans les métadonnées et les modifications dans le code de Microsoft intermediate language (MSIL) pour le processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3a05c-108">Applies the changes in the metadata and the changes in the Microsoft intermediate language (MSIL) code to the running process.</span></span>|  
|[<span data-ttu-id="3a05c-109">GetJITCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-109">GetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-getjitcompilerflags-method.md)|<span data-ttu-id="3a05c-110">Obtient les indicateurs qui contrôlent la compilation juste-à-temps (JIT) pour ce `ICorDebugModule2`.</span><span class="sxs-lookup"><span data-stu-id="3a05c-110">Gets the flags that control the just-in-time (JIT) compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="3a05c-111">ResolveAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-111">ResolveAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-resolveassembly-method.md)|<span data-ttu-id="3a05c-112">Résout l’assembly référencé par le jeton de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a05c-112">Resolves the assembly referenced by the specified metadata token.</span></span>|  
|[<span data-ttu-id="3a05c-113">SetJITCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-113">SetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md)|<span data-ttu-id="3a05c-114">Définit les indicateurs qui contrôlent la compilation JIT pour ce `ICorDebugModule2`.</span><span class="sxs-lookup"><span data-stu-id="3a05c-114">Sets the flags that control the JIT compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="3a05c-115">SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="3a05c-115">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjmcstatus-method.md)|<span data-ttu-id="3a05c-116">Définit l’état uniquement mon Code (JMC) de toutes les méthodes de toutes les classes dans ce `ICorDebugModule2` à la valeur spécifiée, à l’exception de celles figurant dans le `pTokens` tableau, il définit la valeur opposée.</span><span class="sxs-lookup"><span data-stu-id="3a05c-116">Sets the Just My Code (JMC) status of all methods of all the classes in this `ICorDebugModule2` to the specified value, except those in the `pTokens` array, which it sets to the opposite value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a05c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3a05c-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3a05c-118">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="3a05c-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a05c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a05c-119">Requirements</span></span>  
 <span data-ttu-id="3a05c-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a05c-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a05c-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3a05c-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3a05c-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3a05c-122">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3a05c-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3a05c-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3a05c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a05c-124">See also</span></span>

- [<span data-ttu-id="3a05c-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3a05c-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
