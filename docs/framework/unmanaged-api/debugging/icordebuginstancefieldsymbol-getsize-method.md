---
title: ICorDebugInstanceFieldSymbol::GetSize, méthode
ms.date: 03/30/2017
ms.assetid: a4af1e3b-6a9f-4855-95ba-5317565c8e2b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8cc09de2120399dcfe309757d554e1de72e55f07
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59081448"
---
# <a name="icordebuginstancefieldsymbolgetsize-method"></a><span data-ttu-id="8fda0-102">ICorDebugInstanceFieldSymbol::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="8fda0-102">ICorDebugInstanceFieldSymbol::GetSize Method</span></span>
<span data-ttu-id="8fda0-103">Obtient la taille en octets du champ d'instance.</span><span class="sxs-lookup"><span data-stu-id="8fda0-103">Gets the size in bytes of the instance field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fda0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fda0-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fda0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fda0-105">Parameters</span></span>  
 `pcbSize`  
 <span data-ttu-id="8fda0-106">[out] Pointeur vers la longueur du champ.</span><span class="sxs-lookup"><span data-stu-id="8fda0-106">[out] A pointer to length of the field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8fda0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8fda0-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8fda0-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="8fda0-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fda0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fda0-109">Requirements</span></span>  
 <span data-ttu-id="8fda0-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8fda0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fda0-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8fda0-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8fda0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8fda0-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8fda0-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8fda0-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8fda0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fda0-114">See also</span></span>

- [<span data-ttu-id="8fda0-115">ICorDebugInstanceFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="8fda0-115">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="8fda0-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8fda0-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
