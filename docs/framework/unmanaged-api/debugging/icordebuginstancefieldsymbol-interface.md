---
title: ICorDebugInstanceFieldSymbol, interface
ms.date: 03/30/2017
ms.assetid: a4a8f259-b83a-4425-ae8b-72b067dbc0d9
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 82f6ccd43059f33a69b8b052f9efa34c4e4f2c1e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417714"
---
# <a name="icordebuginstancefieldsymbol-interface"></a><span data-ttu-id="bf081-102">ICorDebugInstanceFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="bf081-102">ICorDebugInstanceFieldSymbol Interface</span></span>
<span data-ttu-id="bf081-103">Représente les informations sur les symboles de débogage pour un champ d’instance.</span><span class="sxs-lookup"><span data-stu-id="bf081-103">Represents the debug symbol information for an instance field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bf081-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bf081-104">Methods</span></span>  
  
|<span data-ttu-id="bf081-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bf081-105">Method</span></span>|<span data-ttu-id="bf081-106">Description</span><span class="sxs-lookup"><span data-stu-id="bf081-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bf081-107">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="bf081-107">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-getname-method.md)|<span data-ttu-id="bf081-108">Obtient le nom du champ d'instance.</span><span class="sxs-lookup"><span data-stu-id="bf081-108">Gets the name of the instance field.</span></span>|  
|[<span data-ttu-id="bf081-109">GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="bf081-109">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-getoffset-method.md)|<span data-ttu-id="bf081-110">Obtient l'offset en octets de ce champ d'instance dans sa classe parente.</span><span class="sxs-lookup"><span data-stu-id="bf081-110">Gets the offset in bytes of this instance field in its parent class.</span></span>|  
|[<span data-ttu-id="bf081-111">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="bf081-111">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginstancefieldsymbol-getsize-method.md)|<span data-ttu-id="bf081-112">Obtient la taille en octets du champ d'instance.</span><span class="sxs-lookup"><span data-stu-id="bf081-112">Gets the size in bytes of the instance field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bf081-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf081-113">Remarks</span></span>  
 <span data-ttu-id="bf081-114">L'interface `ICorDebugInstanceFieldSymbol` est utilisée pour récupérer les informations sur les symboles de débogage pour un champ d'instance.</span><span class="sxs-lookup"><span data-stu-id="bf081-114">The `ICorDebugInstanceFieldSymbol` interface is used to retrieve the debug symbol information for an instance field.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bf081-115">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="bf081-115">This interface is available with .NET Native only.</span></span> <span data-ttu-id="bf081-116">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="bf081-116">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf081-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf081-117">Requirements</span></span>  
 <span data-ttu-id="bf081-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf081-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf081-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bf081-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bf081-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bf081-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bf081-121">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bf081-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf081-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf081-122">See Also</span></span>  
 [<span data-ttu-id="bf081-123">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="bf081-123">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)  
 [<span data-ttu-id="bf081-124">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="bf081-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="bf081-125">Débogage</span><span class="sxs-lookup"><span data-stu-id="bf081-125">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
