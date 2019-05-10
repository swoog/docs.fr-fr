---
title: ICorDebugDebugEvent, interface
ms.date: 03/30/2017
ms.assetid: a226737a-cb99-4e97-bd94-9a37094ded41
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 013cdfbb6a2904e60d6f7b4df6d40e3d65606fcd
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64606817"
---
# <a name="icordebugdebugevent-interface"></a><span data-ttu-id="03912-102">ICorDebugDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="03912-102">ICorDebugDebugEvent Interface</span></span>
<span data-ttu-id="03912-103">Définit l’interface de base de laquelle dérivent tous les événements de débogage `ICorDebug`.</span><span class="sxs-lookup"><span data-stu-id="03912-103">Defines the base interface from which all `ICorDebug` debug events derive.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="03912-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="03912-104">Methods</span></span>  
  
|<span data-ttu-id="03912-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="03912-105">Method</span></span>|<span data-ttu-id="03912-106">Description</span><span class="sxs-lookup"><span data-stu-id="03912-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="03912-107">GetEventKind, méthode</span><span class="sxs-lookup"><span data-stu-id="03912-107">GetEventKind Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md)|<span data-ttu-id="03912-108">Indique le type d'événement représenté par cet objet `ICorDebugDebugEvent`.</span><span class="sxs-lookup"><span data-stu-id="03912-108">Indicates what kind of event this `ICorDebugDebugEvent` object represents.</span></span>|  
|[<span data-ttu-id="03912-109">GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="03912-109">GetThread Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-getthread-method.md)|<span data-ttu-id="03912-110">Obtient le thread sur lequel l'événement s'est produit.</span><span class="sxs-lookup"><span data-stu-id="03912-110">Gets the thread on which the event occurred.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="03912-111">Notes</span><span class="sxs-lookup"><span data-stu-id="03912-111">Remarks</span></span>  
 <span data-ttu-id="03912-112">Les interfaces suivantes sont dérivées de l'interface `ICorDebugDebugEvent` :</span><span class="sxs-lookup"><span data-stu-id="03912-112">The following interfaces are derived from the `ICorDebugDebugEvent` interface:</span></span>  
  
- [<span data-ttu-id="03912-113">ICorDebugExceptionDebugEvent</span><span class="sxs-lookup"><span data-stu-id="03912-113">ICorDebugExceptionDebugEvent</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-interface.md)  
  
- [<span data-ttu-id="03912-114">ICorDebugModuleDebugEvent</span><span class="sxs-lookup"><span data-stu-id="03912-114">ICorDebugModuleDebugEvent</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmoduledebugevent-interface.md)  
  
> [!NOTE]
>  <span data-ttu-id="03912-115">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="03912-115">The interface is available with .NET Native only.</span></span> <span data-ttu-id="03912-116">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="03912-116">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="03912-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03912-117">Requirements</span></span>  
 <span data-ttu-id="03912-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="03912-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="03912-119">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="03912-119">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="03912-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="03912-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="03912-121">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="03912-121">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03912-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03912-122">See also</span></span>

- [<span data-ttu-id="03912-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="03912-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="03912-124">Débogage</span><span class="sxs-lookup"><span data-stu-id="03912-124">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
