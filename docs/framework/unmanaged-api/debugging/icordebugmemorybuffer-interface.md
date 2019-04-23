---
title: ICorDebugMemoryBuffer, interface
ms.date: 03/30/2017
ms.assetid: 85dc2d65-3657-4b93-9f23-9feaa95d37ff
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e12b50e964ec470b843ae35c960f20c5675fd572
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59072907"
---
# <a name="icordebugmemorybuffer-interface"></a><span data-ttu-id="1e7e2-102">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="1e7e2-102">ICorDebugMemoryBuffer Interface</span></span>
<span data-ttu-id="1e7e2-103">Représente une mémoire tampon en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-103">Represents an in-memory buffer.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1e7e2-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1e7e2-104">Methods</span></span>  
  
|<span data-ttu-id="1e7e2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1e7e2-105">Method</span></span>|<span data-ttu-id="1e7e2-106">Description</span><span class="sxs-lookup"><span data-stu-id="1e7e2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1e7e2-107">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="1e7e2-107">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-getsize-method.md)|<span data-ttu-id="1e7e2-108">Obtient la taille de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-108">Gets the size of the memory buffer in bytes.</span></span>|  
|[<span data-ttu-id="1e7e2-109">GetStartAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="1e7e2-109">GetStartAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-getstartaddress-method.md)|<span data-ttu-id="1e7e2-110">Obtient l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-110">Gets the starting address of the memory buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1e7e2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1e7e2-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1e7e2-112">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="1e7e2-113">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="1e7e2-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e7e2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e7e2-114">Requirements</span></span>  
 <span data-ttu-id="1e7e2-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1e7e2-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e7e2-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1e7e2-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1e7e2-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1e7e2-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1e7e2-118">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e7e2-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e7e2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7e2-119">See also</span></span>

- [<span data-ttu-id="1e7e2-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1e7e2-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="1e7e2-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="1e7e2-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
