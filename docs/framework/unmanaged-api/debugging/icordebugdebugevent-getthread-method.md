---
title: ICorDebugDebugEvent::GetThread, méthode
ms.date: 03/30/2017
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c5b4a15f637526cd2faadd2d9d3da143c40140f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414903"
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="5649d-102">ICorDebugDebugEvent::GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="5649d-102">ICorDebugDebugEvent::GetThread Method</span></span>
<span data-ttu-id="5649d-103">Obtient le thread sur lequel l'événement s'est produit.</span><span class="sxs-lookup"><span data-stu-id="5649d-103">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5649d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5649d-104">Syntax</span></span>  
  
```  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5649d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5649d-105">Parameters</span></span>  
 <span data-ttu-id="5649d-106">ppThread</span><span class="sxs-lookup"><span data-stu-id="5649d-106">ppThread</span></span>  
 <span data-ttu-id="5649d-107">[out] Pointeur vers l’adresse d’un objet ICorDebugThread qui représente le thread sur lequel l’événement s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5649d-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5649d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5649d-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5649d-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="5649d-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5649d-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5649d-110">Requirements</span></span>  
 <span data-ttu-id="5649d-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5649d-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5649d-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5649d-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5649d-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5649d-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5649d-114">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5649d-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5649d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5649d-115">See Also</span></span>  
 [<span data-ttu-id="5649d-116">ICorDebugDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="5649d-116">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)  
 [<span data-ttu-id="5649d-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5649d-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
