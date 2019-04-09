---
title: ICorDebugStaticFieldSymbol, interface
ms.date: 03/30/2017
ms.assetid: c0b93609-631e-4b15-878a-189ede922631
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 382f3fc9377c25379809badac0bc580c3593cbde
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59103894"
---
# <a name="icordebugstaticfieldsymbol-interface"></a><span data-ttu-id="66077-102">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="66077-102">ICorDebugStaticFieldSymbol Interface</span></span>
<span data-ttu-id="66077-103">Représente les informations sur les symboles de débogage pour un champ static.</span><span class="sxs-lookup"><span data-stu-id="66077-103">Represents the debug symbol information for a static field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="66077-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="66077-104">Methods</span></span>  
  
|<span data-ttu-id="66077-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="66077-105">Method</span></span>|<span data-ttu-id="66077-106">Description</span><span class="sxs-lookup"><span data-stu-id="66077-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="66077-107">GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="66077-107">GetAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-getaddress-method.md)|<span data-ttu-id="66077-108">Obtient l'adresse du champ statique.</span><span class="sxs-lookup"><span data-stu-id="66077-108">Gets the address of the static field.</span></span>|  
|[<span data-ttu-id="66077-109">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="66077-109">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-getname-method.md)|<span data-ttu-id="66077-110">Obtient le nom du champ static.</span><span class="sxs-lookup"><span data-stu-id="66077-110">Gets the name of the static field.</span></span>|  
|[<span data-ttu-id="66077-111">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="66077-111">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-getsize-method.md)|<span data-ttu-id="66077-112">Obtient la taille en octets du champ static.</span><span class="sxs-lookup"><span data-stu-id="66077-112">Gets the size in bytes of the static field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="66077-113">Notes</span><span class="sxs-lookup"><span data-stu-id="66077-113">Remarks</span></span>  
 <span data-ttu-id="66077-114">L’interface `ICorDebugStaticFieldSymbol` est utilisée pour récupérer les informations sur les symboles de débogage pour un champ statique.</span><span class="sxs-lookup"><span data-stu-id="66077-114">The `ICorDebugStaticFieldSymbol` interface is used to retrieve the debug symbol information for a static field.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="66077-115">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="66077-115">This interface is available with .NET Native only.</span></span> <span data-ttu-id="66077-116">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="66077-116">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66077-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66077-117">Requirements</span></span>  
 <span data-ttu-id="66077-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="66077-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66077-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="66077-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66077-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="66077-120">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="66077-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="66077-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="66077-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66077-122">See also</span></span>

- [<span data-ttu-id="66077-123">ICorDebugInstanceFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="66077-123">ICorDebugInstanceFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="66077-124">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="66077-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="66077-125">Débogage</span><span class="sxs-lookup"><span data-stu-id="66077-125">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
