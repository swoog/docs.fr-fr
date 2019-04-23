---
title: ICorDebugVariableHomeEnum Interface
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum
helpviewer_keywords:
- ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: c312ae6d-c8dc-48d6-9f1e-ead515c88fdf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4e67e4685320f56a4a6a8be2e3eb2e6c8065ce59
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080382"
---
# <a name="icordebugvariablehomeenum-interface"></a><span data-ttu-id="0c51a-102">ICorDebugVariableHomeEnum Interface</span><span class="sxs-lookup"><span data-stu-id="0c51a-102">ICorDebugVariableHomeEnum Interface</span></span>
<span data-ttu-id="0c51a-103">Fournit un énumérateur pour les variables locales et les arguments dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="0c51a-103">Provides an enumerator to the local variables and arguments in a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0c51a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c51a-104">Methods</span></span>  
  
|<span data-ttu-id="0c51a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c51a-105">Method</span></span>|<span data-ttu-id="0c51a-106">Description</span><span class="sxs-lookup"><span data-stu-id="0c51a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0c51a-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="0c51a-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md)|<span data-ttu-id="0c51a-108">Obtient le nombre spécifié de [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances qui contiennent des informations sur les variables locales et les arguments dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="0c51a-108">Gets the specified number of [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances that contain information about the local variables and arguments in a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c51a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0c51a-109">Remarks</span></span>  
 <span data-ttu-id="0c51a-110">Le `ICorDebugVariableHomeEnum` interface implémente l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="0c51a-110">The `ICorDebugVariableHomeEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="0c51a-111">Un `ICorDebugVariableHomeEnum` instance est remplie avec [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances en appelant le [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0c51a-111">An `ICorDebugVariableHomeEnum` instance is populated with [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances by calling the [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) method.</span></span> <span data-ttu-id="0c51a-112">Chaque [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance dans la collection représente une variable locale ou un argument dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="0c51a-112">Each [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance in the collection represents a local variable or argument in a function.</span></span> <span data-ttu-id="0c51a-113">Le [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objets dans la collection peuvent être énumérés en appelant le [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0c51a-113">The  [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objects in the collection can be enumerated by calling the [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c51a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c51a-114">Requirements</span></span>  
 <span data-ttu-id="0c51a-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c51a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c51a-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0c51a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0c51a-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0c51a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0c51a-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c51a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c51a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c51a-119">See also</span></span>

- [<span data-ttu-id="0c51a-120">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="0c51a-120">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
- [<span data-ttu-id="0c51a-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0c51a-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
