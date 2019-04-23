---
title: ICorDebugModuleBreakpoint::GetModule, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint.GetModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint::GetModule
helpviewer_keywords:
- ICorDebugModuleBreakpoint::GetModule method [.NET Framework debugging]
- GetModule method, ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: ffd5d9ec-4564-4200-b625-b306eec0ebd7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51403c52d7f8a216e83b817f157979f4af1c433a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162866"
---
# <a name="icordebugmodulebreakpointgetmodule-method"></a><span data-ttu-id="bb962-102">ICorDebugModuleBreakpoint::GetModule, méthode</span><span class="sxs-lookup"><span data-stu-id="bb962-102">ICorDebugModuleBreakpoint::GetModule Method</span></span>
<span data-ttu-id="bb962-103">Obtient un pointeur d’interface vers un « ICorDebugModule » qui fait référence au module dans lequel ce point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="bb962-103">Gets an interface pointer to an "ICorDebugModule" that references the module in which this breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb962-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb962-104">Syntax</span></span>  
  
```  
HRESULT GetModule (  
    [out] ICorDebugModule   **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb962-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb962-105">Parameters</span></span>  
 `ppModule`  
 <span data-ttu-id="bb962-106">[out] Un pointeur vers l’adresse d’un `ICorDebugModule` interface qui fait référence au module dans lequel le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="bb962-106">[out] A pointer to the address of an `ICorDebugModule` interface that references the module in which the breakpoint is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb962-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb962-107">Requirements</span></span>  
 <span data-ttu-id="bb962-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bb962-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb962-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bb962-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bb962-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb962-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb962-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb962-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb962-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb962-112">See also</span></span>
