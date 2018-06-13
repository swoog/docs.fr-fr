---
title: ICorDebugStaticFieldSymbol::GetSize, méthode
ms.date: 03/30/2017
ms.assetid: 72389860-7e37-4656-ba46-b6aeee1860f8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acb72a7d6c39efa5fa93bfddc314d07ec6cd8348
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419092"
---
# <a name="icordebugstaticfieldsymbolgetsize-method"></a><span data-ttu-id="0680d-102">ICorDebugStaticFieldSymbol::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="0680d-102">ICorDebugStaticFieldSymbol::GetSize Method</span></span>
<span data-ttu-id="0680d-103">Obtient la taille en octets du champ static.</span><span class="sxs-lookup"><span data-stu-id="0680d-103">Gets the size in bytes of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0680d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0680d-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0680d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0680d-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="0680d-106">[out] Pointeur vers la longueur du champ.</span><span class="sxs-lookup"><span data-stu-id="0680d-106">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0680d-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0680d-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0680d-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="0680d-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0680d-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0680d-109">Requirements</span></span>  
 <span data-ttu-id="0680d-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0680d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0680d-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0680d-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0680d-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0680d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0680d-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0680d-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0680d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0680d-114">See Also</span></span>  
 [<span data-ttu-id="0680d-115">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="0680d-115">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)  
 [<span data-ttu-id="0680d-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0680d-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
