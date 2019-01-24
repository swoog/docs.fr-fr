---
title: ICorDebugLoadedModule::GetSize (méthode)
ms.date: 03/30/2017
ms.assetid: aaa0e5c0-be9d-4fe1-8418-5295b9b184d6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e4c4888419bb13db43a4a15d98965cc8d3cb8e77
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54515577"
---
# <a name="icordebugloadedmodulegetsize-method"></a><span data-ttu-id="bb9a0-102">ICorDebugLoadedModule::GetSize (méthode)</span><span class="sxs-lookup"><span data-stu-id="bb9a0-102">ICorDebugLoadedModule::GetSize Method</span></span>
<span data-ttu-id="bb9a0-103">Obtient la taille en octets du module chargé.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-103">Gets the size in bytes of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb9a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb9a0-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcBytes  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bb9a0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb9a0-105">Parameters</span></span>  
 `pcBytes`  
 <span data-ttu-id="bb9a0-106">[out] Pointeur vers le nombre d'octets dans le module chargé.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-106">[out] A pointer to the number of bytes in the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bb9a0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bb9a0-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bb9a0-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="bb9a0-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb9a0-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bb9a0-109">Requirements</span></span>  
 <span data-ttu-id="bb9a0-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bb9a0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb9a0-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bb9a0-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bb9a0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb9a0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bb9a0-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb9a0-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb9a0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb9a0-114">See also</span></span>
- [<span data-ttu-id="bb9a0-115">ICorDebugLoadedModule, interface</span><span class="sxs-lookup"><span data-stu-id="bb9a0-115">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)
- [<span data-ttu-id="bb9a0-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="bb9a0-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
