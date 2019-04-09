---
title: ICorDebugStaticFieldSymbol::GetSize, méthode
ms.date: 03/30/2017
ms.assetid: 72389860-7e37-4656-ba46-b6aeee1860f8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9baa3632b6ede9ce45f34302611710344ed33761
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154321"
---
# <a name="icordebugstaticfieldsymbolgetsize-method"></a><span data-ttu-id="c0b16-102">ICorDebugStaticFieldSymbol::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="c0b16-102">ICorDebugStaticFieldSymbol::GetSize Method</span></span>
<span data-ttu-id="c0b16-103">Obtient la taille en octets du champ static.</span><span class="sxs-lookup"><span data-stu-id="c0b16-103">Gets the size in bytes of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0b16-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b16-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0b16-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0b16-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="c0b16-106">[out] Pointeur vers la longueur du champ.</span><span class="sxs-lookup"><span data-stu-id="c0b16-106">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0b16-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c0b16-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c0b16-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="c0b16-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0b16-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b16-109">Requirements</span></span>  
 <span data-ttu-id="c0b16-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0b16-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0b16-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c0b16-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c0b16-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0b16-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c0b16-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c0b16-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c0b16-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0b16-114">See also</span></span>

- [<span data-ttu-id="c0b16-115">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="c0b16-115">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="c0b16-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c0b16-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
