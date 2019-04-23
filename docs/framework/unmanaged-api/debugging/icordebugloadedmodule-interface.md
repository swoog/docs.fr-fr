---
title: ICorDebugLoadedModule (interface)
ms.date: 03/30/2017
ms.assetid: 34be6369-2e75-4a95-a538-3b29ac97cf6d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e91dda9cbc5957768e98db2b2a9e1026d94c03e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200751"
---
# <a name="icordebugloadedmodule-interface"></a><span data-ttu-id="15576-102">ICorDebugLoadedModule (interface)</span><span class="sxs-lookup"><span data-stu-id="15576-102">ICorDebugLoadedModule Interface</span></span>
<span data-ttu-id="15576-103">Fournit des informations sur un module chargé.</span><span class="sxs-lookup"><span data-stu-id="15576-103">Provides information about a loaded module.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="15576-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="15576-104">Methods</span></span>  
  
|<span data-ttu-id="15576-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="15576-105">Method</span></span>|<span data-ttu-id="15576-106">Description</span><span class="sxs-lookup"><span data-stu-id="15576-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="15576-107">GetBaseAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="15576-107">GetBaseAddress Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getbaseaddress-method.md)|<span data-ttu-id="15576-108">Obtient l'adresse de base du module chargé.</span><span class="sxs-lookup"><span data-stu-id="15576-108">Gets the base address of the loaded module.</span></span>|  
|[<span data-ttu-id="15576-109">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="15576-109">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getname-method.md)|<span data-ttu-id="15576-110">Obtient le nom du module chargé.</span><span class="sxs-lookup"><span data-stu-id="15576-110">Gets the name of the loaded module.</span></span>|  
|[<span data-ttu-id="15576-111">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="15576-111">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-getsize-method.md)|<span data-ttu-id="15576-112">Obtient la taille en octets du module chargé.</span><span class="sxs-lookup"><span data-stu-id="15576-112">Gets the size in bytes of the loaded module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="15576-113">Notes</span><span class="sxs-lookup"><span data-stu-id="15576-113">Remarks</span></span>  
 <span data-ttu-id="15576-114">L'interface `ICorDebugLoadedModule` est implémentée par un débogueur et est utilisée par les interfaces de débogage du CLR pour obtenir des informations sur le module chargé à partir du débogueur.</span><span class="sxs-lookup"><span data-stu-id="15576-114">The `ICorDebugLoadedModule` interface is implemented by a debugger and is used by the CLR debugging interfaces to get information about the loaded module from the debugger.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="15576-115">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="15576-115">This interface is available with .NET Native only.</span></span> <span data-ttu-id="15576-116">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="15576-116">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="15576-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15576-117">Requirements</span></span>  
 <span data-ttu-id="15576-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="15576-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="15576-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="15576-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="15576-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="15576-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="15576-121">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="15576-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15576-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15576-122">See also</span></span>

- [<span data-ttu-id="15576-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="15576-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="15576-124">Débogage</span><span class="sxs-lookup"><span data-stu-id="15576-124">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
