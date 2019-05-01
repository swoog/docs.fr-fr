---
title: ICorDebugModuleBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint
helpviewer_keywords:
- ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: 34667162-f314-475f-ae1b-ce9cb0fcbb83
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6a43a264fcaa94ce4e629d8db504e9d416f6b89
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994732"
---
# <a name="icordebugmodulebreakpoint-interface"></a><span data-ttu-id="39a7b-102">ICorDebugModuleBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="39a7b-102">ICorDebugModuleBreakpoint Interface</span></span>

<span data-ttu-id="39a7b-103">Fournit l’accès à des modules spécifiques.</span><span class="sxs-lookup"><span data-stu-id="39a7b-103">Provides access to specific modules.</span></span> <span data-ttu-id="39a7b-104">Cette interface est une sous-classe de l’interface ICorDebugBreakpoint.</span><span class="sxs-lookup"><span data-stu-id="39a7b-104">This interface is a subclass of the ICorDebugBreakpoint interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="39a7b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="39a7b-105">Methods</span></span>  
  
|<span data-ttu-id="39a7b-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="39a7b-106">Method</span></span>|<span data-ttu-id="39a7b-107">Description</span><span class="sxs-lookup"><span data-stu-id="39a7b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="39a7b-108">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="39a7b-108">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodulebreakpoint-getmodule-method.md)|<span data-ttu-id="39a7b-109">Obtient un pointeur d’interface vers un ICorDebugModule qui fait référence au module où ce point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="39a7b-109">Gets an interface pointer to an ICorDebugModule that references the module where this breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="39a7b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="39a7b-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="39a7b-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="39a7b-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39a7b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39a7b-112">Requirements</span></span>  
 <span data-ttu-id="39a7b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="39a7b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39a7b-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="39a7b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="39a7b-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="39a7b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="39a7b-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39a7b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39a7b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39a7b-117">See also</span></span>

- [<span data-ttu-id="39a7b-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="39a7b-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
