---
title: ICorDebugVariableSymbol, interface
ms.date: 03/30/2017
ms.assetid: 0e58b85e-69bd-41ff-bedb-8cdc8be6a7a2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c7cdababd1e4b5fae4f5e48a654f861b708a6e3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59226558"
---
# <a name="icordebugvariablesymbol-interface"></a><span data-ttu-id="ea30f-102">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="ea30f-102">ICorDebugVariableSymbol Interface</span></span>
<span data-ttu-id="ea30f-103">Récupère les informations sur les symboles de débogage pour une variable.</span><span class="sxs-lookup"><span data-stu-id="ea30f-103">Retrieves the debug symbol information for a variable.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ea30f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea30f-104">Methods</span></span>  
  
|<span data-ttu-id="ea30f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-105">Method</span></span>|<span data-ttu-id="ea30f-106">Description</span><span class="sxs-lookup"><span data-stu-id="ea30f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ea30f-107">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-107">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getname-method.md)|<span data-ttu-id="ea30f-108">Obtient le nom d'une variable.</span><span class="sxs-lookup"><span data-stu-id="ea30f-108">Gets the name of a variable.</span></span>|  
|[<span data-ttu-id="ea30f-109">GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-109">GetSize Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getsize-method.md)|<span data-ttu-id="ea30f-110">Obtient la taille d'une variable en octets.</span><span class="sxs-lookup"><span data-stu-id="ea30f-110">Gets the size of a variable in bytes.</span></span>|  
|[<span data-ttu-id="ea30f-111">GetSlotIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-111">GetSlotIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getslotindex-method.md)|<span data-ttu-id="ea30f-112">Obtient l'index d'emplacement géré d'une variable locale.</span><span class="sxs-lookup"><span data-stu-id="ea30f-112">Gets the managed slot index of a local variable.</span></span>|  
|[<span data-ttu-id="ea30f-113">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-113">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-getvalue-method.md)|<span data-ttu-id="ea30f-114">Obtient la valeur d'une variable sous forme d'un tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="ea30f-114">Gets the value of a variable as a byte array.</span></span>|  
|[<span data-ttu-id="ea30f-115">SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="ea30f-115">SetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-setvalue-method.md)|<span data-ttu-id="ea30f-116">Affecte la valeur d'un tableau d'octets à une variable.</span><span class="sxs-lookup"><span data-stu-id="ea30f-116">Assigns the value of a byte array to a variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ea30f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ea30f-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ea30f-118">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ea30f-118">This interface is available with .NET Native only.</span></span> <span data-ttu-id="ea30f-119">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="ea30f-119">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea30f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea30f-120">Requirements</span></span>  
 <span data-ttu-id="ea30f-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ea30f-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea30f-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ea30f-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ea30f-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ea30f-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ea30f-124">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea30f-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea30f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea30f-125">See also</span></span>

- [<span data-ttu-id="ea30f-126">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ea30f-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="ea30f-127">Débogage</span><span class="sxs-lookup"><span data-stu-id="ea30f-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
