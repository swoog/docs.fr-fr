---
title: ICorDebugLoadedModule::GetSize (méthode)
ms.date: 03/30/2017
ms.assetid: aaa0e5c0-be9d-4fe1-8418-5295b9b184d6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9768fb91749158bf3193919b2106bde1c618468a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413229"
---
# <a name="icordebugloadedmodulegetsize-method"></a><span data-ttu-id="0dadf-102">ICorDebugLoadedModule::GetSize (méthode)</span><span class="sxs-lookup"><span data-stu-id="0dadf-102">ICorDebugLoadedModule::GetSize Method</span></span>
<span data-ttu-id="0dadf-103">Obtient la taille en octets du module chargé.</span><span class="sxs-lookup"><span data-stu-id="0dadf-103">Gets the size in bytes of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0dadf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dadf-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcBytes  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0dadf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dadf-105">Parameters</span></span>  
 `pcBytes`  
 <span data-ttu-id="0dadf-106">[out] Pointeur vers le nombre d'octets dans le module chargé.</span><span class="sxs-lookup"><span data-stu-id="0dadf-106">[out] A pointer to the number of bytes in the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0dadf-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0dadf-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0dadf-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="0dadf-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0dadf-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0dadf-109">Requirements</span></span>  
 <span data-ttu-id="0dadf-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0dadf-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0dadf-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0dadf-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0dadf-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0dadf-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0dadf-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0dadf-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0dadf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dadf-114">See Also</span></span>  
 [<span data-ttu-id="0dadf-115">ICorDebugLoadedModule, interface</span><span class="sxs-lookup"><span data-stu-id="0dadf-115">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)  
 [<span data-ttu-id="0dadf-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0dadf-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
