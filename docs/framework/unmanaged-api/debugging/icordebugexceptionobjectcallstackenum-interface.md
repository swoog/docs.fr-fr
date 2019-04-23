---
title: ICorDebugExceptionObjectCallStackEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectCallStackEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectCallStackEnum
helpviewer_keywords:
- ICorDebugExceptionObjectCallStackEnum interface [.NET Framework debugging]
ms.assetid: 39dffa18-c71b-48c4-b11d-e814631ab1e9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e7ed6c04a46a767ed122e54df0695429cf923b8a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126202"
---
# <a name="icordebugexceptionobjectcallstackenum-interface"></a><span data-ttu-id="1f92c-102">ICorDebugExceptionObjectCallStackEnum, interface</span><span class="sxs-lookup"><span data-stu-id="1f92c-102">ICorDebugExceptionObjectCallStackEnum Interface</span></span>
<span data-ttu-id="1f92c-103">Fournit un énumérateur pour les informations de la pile des appels qui sont incorporées dans un objet exception.</span><span class="sxs-lookup"><span data-stu-id="1f92c-103">Provides an enumerator for call stack information that is embedded in an exception object.</span></span> <span data-ttu-id="1f92c-104">Cette interface est une sous-classe de l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="1f92c-104">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1f92c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1f92c-105">Methods</span></span>  
  
|<span data-ttu-id="1f92c-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="1f92c-106">Method</span></span>|<span data-ttu-id="1f92c-107">Description</span><span class="sxs-lookup"><span data-stu-id="1f92c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1f92c-108">ICorDebugExceptionObjectCallStackEnum::Next</span><span class="sxs-lookup"><span data-stu-id="1f92c-108">ICorDebugExceptionObjectCallStackEnum::Next</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md)|<span data-ttu-id="1f92c-109">Obtient un nombre spécifié de [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) les objets qui contiennent des informations sur la pile des appels d’un objet exception.</span><span class="sxs-lookup"><span data-stu-id="1f92c-109">Gets a specified number of [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) objects that contain information about an exception object's call stack.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1f92c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1f92c-110">Remarks</span></span>  
 <span data-ttu-id="1f92c-111">Le `ICorDebugExceptionObjectCallStackEnum` interface implémente l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="1f92c-111">The `ICorDebugExceptionObjectCallStackEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="1f92c-112">Un `ICorDebugExceptionObjectCallStackEnum` instance est remplie avec [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) objets en appelant le [ICorDebugExceptionObjectValue::EnumerateExceptionCallStack](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1f92c-112">An `ICorDebugExceptionObjectCallStackEnum` instance is populated with [CorDebugExceptionObjectStackFrame](../../../../docs/framework/unmanaged-api/debugging/cordebugexceptionobjectstackframe-structure.md) objects by calling the [ICorDebugExceptionObjectValue::EnumerateExceptionCallStack](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md) method.</span></span> <span data-ttu-id="1f92c-113">Les éléments de pile d’appel dans la collection peuvent être énumérés en appelant le [ICorDebugExceptionObjectCallStackEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md) (méthode)</span><span class="sxs-lookup"><span data-stu-id="1f92c-113">The call stack items in the collection can be enumerated by calling the [ICorDebugExceptionObjectCallStackEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-next-method.md) method</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1f92c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f92c-114">Requirements</span></span>  
 <span data-ttu-id="1f92c-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1f92c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1f92c-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1f92c-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1f92c-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1f92c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1f92c-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1f92c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f92c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f92c-119">See also</span></span>

- [<span data-ttu-id="1f92c-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1f92c-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="1f92c-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="1f92c-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
