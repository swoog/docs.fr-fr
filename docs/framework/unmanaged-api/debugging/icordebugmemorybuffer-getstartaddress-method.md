---
title: ICorDebugMemoryBuffer::GetStartAddress, méthode
ms.date: 03/30/2017
ms.assetid: f804d9ab-8c88-44f0-b278-5fcca7f87726
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 29149ceb155cdfdf7b735d6939809e80f2ba4dc0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695541"
---
# <a name="icordebugmemorybuffergetstartaddress-method"></a><span data-ttu-id="fe3f5-102">ICorDebugMemoryBuffer::GetStartAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="fe3f5-102">ICorDebugMemoryBuffer::GetStartAddress Method</span></span>
<span data-ttu-id="fe3f5-103">Obtient l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe3f5-103">Gets the starting address of the memory buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe3f5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe3f5-104">Syntax</span></span>  
  
```  
HRESULT GetStartAddress(  
   [out] LPCVOID *address  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe3f5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe3f5-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="fe3f5-106">[out] Pointeur vers l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe3f5-106">[out] A pointer to the starting address of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe3f5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fe3f5-107">Remarks</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="fe3f5-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="fe3f5-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe3f5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe3f5-109">Requirements</span></span>  
 <span data-ttu-id="fe3f5-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe3f5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe3f5-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fe3f5-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fe3f5-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe3f5-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe3f5-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe3f5-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe3f5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe3f5-114">See also</span></span>
- [<span data-ttu-id="fe3f5-115">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="fe3f5-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="fe3f5-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="fe3f5-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
