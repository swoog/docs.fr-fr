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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59119897"
---
# <a name="icordebugmodule2-interface"></a><span data-ttu-id="01f6d-102">ICorDebugModule2, interface</span><span class="sxs-lookup"><span data-stu-id="01f6d-102">ICorDebugModule2 Interface</span></span>

<span data-ttu-id="01f6d-103">Sert d’extension logique à l’interface ICorDebugModule.</span><span class="sxs-lookup"><span data-stu-id="01f6d-103">Serves as a logical extension to the ICorDebugModule interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="01f6d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01f6d-104">Methods</span></span>  
  
|<span data-ttu-id="01f6d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-105">Method</span></span>|<span data-ttu-id="01f6d-106">Description</span><span class="sxs-lookup"><span data-stu-id="01f6d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="01f6d-107">ApplyChanges, méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-107">ApplyChanges Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md)|<span data-ttu-id="01f6d-108">Applique les modifications dans les métadonnées et les modifications dans le code de Microsoft intermediate language (MSIL) pour le processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="01f6d-108">Applies the changes in the metadata and the changes in the Microsoft intermediate language (MSIL) code to the running process.</span></span>|  
|[<span data-ttu-id="01f6d-109">GetJITCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-109">GetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-getjitcompilerflags-method.md)|<span data-ttu-id="01f6d-110">Obtient les indicateurs qui contrôlent la compilation juste-à-temps (JIT) pour ce `ICorDebugModule2`.</span><span class="sxs-lookup"><span data-stu-id="01f6d-110">Gets the flags that control the just-in-time (JIT) compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="01f6d-111">ResolveAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-111">ResolveAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-resolveassembly-method.md)|<span data-ttu-id="01f6d-112">Résout l’assembly référencé par le jeton de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="01f6d-112">Resolves the assembly referenced by the specified metadata token.</span></span>|  
|[<span data-ttu-id="01f6d-113">SetJITCompilerFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-113">SetJITCompilerFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md)|<span data-ttu-id="01f6d-114">Définit les indicateurs qui contrôlent la compilation JIT pour ce `ICorDebugModule2`.</span><span class="sxs-lookup"><span data-stu-id="01f6d-114">Sets the flags that control the JIT compilation for this `ICorDebugModule2`.</span></span>|  
|[<span data-ttu-id="01f6d-115">SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="01f6d-115">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjmcstatus-method.md)|<span data-ttu-id="01f6d-116">Définit l’état uniquement mon Code (JMC) de toutes les méthodes de toutes les classes dans ce `ICorDebugModule2` à la valeur spécifiée, à l’exception de celles figurant dans le `pTokens` tableau, il définit la valeur opposée.</span><span class="sxs-lookup"><span data-stu-id="01f6d-116">Sets the Just My Code (JMC) status of all methods of all the classes in this `ICorDebugModule2` to the specified value, except those in the `pTokens` array, which it sets to the opposite value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="01f6d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="01f6d-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01f6d-118">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="01f6d-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="01f6d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01f6d-119">Requirements</span></span>  
 <span data-ttu-id="01f6d-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="01f6d-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01f6d-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="01f6d-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="01f6d-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="01f6d-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="01f6d-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01f6d-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01f6d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01f6d-124">See also</span></span>

- [<span data-ttu-id="01f6d-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="01f6d-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
