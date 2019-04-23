---
title: ICorDebugDebugEvent::GetThread, méthode
ms.date: 03/30/2017
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 103768918f67ca695a47c52b9cd97f24fb8d46ce
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59081571"
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="3b1af-102">ICorDebugDebugEvent::GetThread, méthode</span><span class="sxs-lookup"><span data-stu-id="3b1af-102">ICorDebugDebugEvent::GetThread Method</span></span>
<span data-ttu-id="3b1af-103">Obtient le thread sur lequel l'événement s'est produit.</span><span class="sxs-lookup"><span data-stu-id="3b1af-103">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b1af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b1af-104">Syntax</span></span>  
  
```  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3b1af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b1af-105">Parameters</span></span>  
 <span data-ttu-id="3b1af-106">ppThread</span><span class="sxs-lookup"><span data-stu-id="3b1af-106">ppThread</span></span>  
 <span data-ttu-id="3b1af-107">[out] Pointeur vers l’adresse d’un objet ICorDebugThread qui représente le thread sur lequel l’événement s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3b1af-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b1af-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3b1af-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3b1af-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="3b1af-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b1af-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b1af-110">Requirements</span></span>  
 <span data-ttu-id="3b1af-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b1af-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b1af-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b1af-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b1af-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b1af-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b1af-114">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b1af-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b1af-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b1af-115">See also</span></span>

- [<span data-ttu-id="3b1af-116">ICorDebugDebugEvent, interface</span><span class="sxs-lookup"><span data-stu-id="3b1af-116">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)
- [<span data-ttu-id="3b1af-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3b1af-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
