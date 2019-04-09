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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59179710"
---
# <a name="icordebugmodulebreakpoint-interface"></a><span data-ttu-id="c468c-102">ICorDebugModuleBreakpoint, interface</span><span class="sxs-lookup"><span data-stu-id="c468c-102">ICorDebugModuleBreakpoint Interface</span></span>

<span data-ttu-id="c468c-103">Fournit l’accès à des modules spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c468c-103">Provides access to specific modules.</span></span> <span data-ttu-id="c468c-104">Cette interface est une sous-classe de l’interface ICorDebugBreakpoint.</span><span class="sxs-lookup"><span data-stu-id="c468c-104">This interface is a subclass of the ICorDebugBreakpoint interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c468c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c468c-105">Methods</span></span>  
  
|<span data-ttu-id="c468c-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="c468c-106">Method</span></span>|<span data-ttu-id="c468c-107">Description</span><span class="sxs-lookup"><span data-stu-id="c468c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c468c-108">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="c468c-108">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodulebreakpoint-getmodule-method.md)|<span data-ttu-id="c468c-109">Obtient un pointeur d’interface vers un ICorDebugModule qui fait référence au module où ce point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="c468c-109">Gets an interface pointer to an ICorDebugModule that references the module where this breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c468c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c468c-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c468c-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="c468c-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c468c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c468c-112">Requirements</span></span>  
 <span data-ttu-id="c468c-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c468c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c468c-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c468c-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c468c-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c468c-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c468c-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c468c-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c468c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c468c-117">See also</span></span>

- [<span data-ttu-id="c468c-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c468c-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
