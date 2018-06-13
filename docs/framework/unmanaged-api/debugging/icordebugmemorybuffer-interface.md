---
title: ICorDebugMemoryBuffer, interface
ms.date: 03/30/2017
ms.assetid: 85dc2d65-3657-4b93-9f23-9feaa95d37ff
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4a1bc8e1206b8a82127645362cfe0a124074271c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414401"
---
# <a name="icordebugmemorybuffer-interface"></a><span data-ttu-id="2ab12-102">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="2ab12-102">ICorDebugMemoryBuffer Interface</span></span>
<span data-ttu-id="2ab12-103">Représente une mémoire tampon en mémoire.</span><span class="sxs-lookup"><span data-stu-id="2ab12-103">Represents an in-memory buffer.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2ab12-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2ab12-104">Methods</span></span>  
  
|<span data-ttu-id="2ab12-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ab12-105">Method</span></span>|<span data-ttu-id="2ab12-106">Description</span><span class="sxs-lookup"><span data-stu-id="2ab12-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2ab12-107">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="2ab12-107">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-getsize-method.md)|<span data-ttu-id="2ab12-108">Obtient la taille de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="2ab12-108">Gets the size of the memory buffer in bytes.</span></span>|  
|[<span data-ttu-id="2ab12-109">GetStartAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="2ab12-109">GetStartAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-getstartaddress-method.md)|<span data-ttu-id="2ab12-110">Obtient l'adresse de départ de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2ab12-110">Gets the starting address of the memory buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2ab12-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2ab12-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2ab12-112">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="2ab12-112">This interface is available with .NET Native only.</span></span> <span data-ttu-id="2ab12-113">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="2ab12-113">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2ab12-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2ab12-114">Requirements</span></span>  
 <span data-ttu-id="2ab12-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2ab12-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2ab12-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2ab12-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2ab12-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2ab12-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2ab12-118">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2ab12-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ab12-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ab12-119">See Also</span></span>  
 [<span data-ttu-id="2ab12-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="2ab12-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="2ab12-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="2ab12-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
