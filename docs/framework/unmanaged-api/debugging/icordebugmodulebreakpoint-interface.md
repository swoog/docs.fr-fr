---
title: ICorDebugModuleBreakpoint Interface1
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
ms.openlocfilehash: c04d5f779306a67e389f768cefdf633f3d72f0ee
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416135"
---
# <a name="icordebugmodulebreakpoint-interface1"></a><span data-ttu-id="8690f-102">ICorDebugModuleBreakpoint Interface1</span><span class="sxs-lookup"><span data-stu-id="8690f-102">ICorDebugModuleBreakpoint Interface1</span></span>
<span data-ttu-id="8690f-103">Fournit l’accès à des modules spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8690f-103">Provides access to specific modules.</span></span> <span data-ttu-id="8690f-104">Cette interface est une sous-classe de l’interface ICorDebugBreakpoint.</span><span class="sxs-lookup"><span data-stu-id="8690f-104">This interface is a subclass of the ICorDebugBreakpoint interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8690f-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8690f-105">Methods</span></span>  
  
|<span data-ttu-id="8690f-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="8690f-106">Method</span></span>|<span data-ttu-id="8690f-107">Description</span><span class="sxs-lookup"><span data-stu-id="8690f-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8690f-108">GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="8690f-108">GetModule Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodulebreakpoint-getmodule-method.md)|<span data-ttu-id="8690f-109">Obtient un pointeur d’interface vers un ICorDebugModule qui référence le module où ce point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="8690f-109">Gets an interface pointer to an ICorDebugModule that references the module where this breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8690f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8690f-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8690f-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="8690f-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8690f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8690f-112">Requirements</span></span>  
 <span data-ttu-id="8690f-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8690f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8690f-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8690f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8690f-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8690f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8690f-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8690f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8690f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8690f-117">See Also</span></span>  
 [<span data-ttu-id="8690f-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8690f-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
