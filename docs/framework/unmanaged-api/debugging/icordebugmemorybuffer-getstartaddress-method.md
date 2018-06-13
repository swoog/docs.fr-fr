---
title: ICorDebugMemoryBuffer::GetStartAddress, méthode
ms.date: 03/30/2017
ms.assetid: f804d9ab-8c88-44f0-b278-5fcca7f87726
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1aa816ea9e6185791e09bcdb0e47c50761a5ebc6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422931"
---
# <a name="icordebugmemorybuffergetstartaddress-method"></a><span data-ttu-id="56a02-102">ICorDebugMemoryBuffer::GetStartAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="56a02-102">ICorDebugMemoryBuffer::GetStartAddress Method</span></span>
<span data-ttu-id="56a02-103">Obtient l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="56a02-103">Gets the starting address of the memory buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56a02-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56a02-104">Syntax</span></span>  
  
```  
HRESULT GetStartAddress(  
   [out] LPCVOID *address  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="56a02-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56a02-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="56a02-106">[out] Pointeur vers l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="56a02-106">[out] A pointer to the starting address of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="56a02-107">Notes</span><span class="sxs-lookup"><span data-stu-id="56a02-107">Remarks</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="56a02-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="56a02-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56a02-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="56a02-109">Requirements</span></span>  
 <span data-ttu-id="56a02-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="56a02-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56a02-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="56a02-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="56a02-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="56a02-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="56a02-113">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56a02-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56a02-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56a02-114">See Also</span></span>  
 [<span data-ttu-id="56a02-115">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="56a02-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)  
 [<span data-ttu-id="56a02-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="56a02-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
