---
title: ICorDebugStackWalk::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk.Next Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk::Next
helpviewer_keywords:
- ICorDebugStackWalk::Next method [.NET Framework debugging]
- Next method, ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 189c36be-028c-4fba-a002-5edfb8fcd07f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 724db50285532c20132fbfd5262df26227db6742
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59130024"
---
# <a name="icordebugstackwalknext-method"></a><span data-ttu-id="93cdf-102">ICorDebugStackWalk::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="93cdf-102">ICorDebugStackWalk::Next Method</span></span>
<span data-ttu-id="93cdf-103">Déplace le [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) objet vers le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="93cdf-103">Moves the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object to the next frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93cdf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93cdf-104">Syntax</span></span>  
  
```  
HRESULT Next();  
```  
  
## <a name="return-value"></a><span data-ttu-id="93cdf-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="93cdf-105">Return Value</span></span>  
 <span data-ttu-id="93cdf-106">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="93cdf-106">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="93cdf-107">HRESULT</span><span class="sxs-lookup"><span data-stu-id="93cdf-107">HRESULT</span></span>|<span data-ttu-id="93cdf-108">Description</span><span class="sxs-lookup"><span data-stu-id="93cdf-108">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="93cdf-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="93cdf-109">S_OK</span></span>|<span data-ttu-id="93cdf-110">Le runtime s’est correctement déroulé le frame suivant (voir Remarques).</span><span class="sxs-lookup"><span data-stu-id="93cdf-110">The runtime successfully unwound to the next frame (see Remarks).</span></span>|  
|<span data-ttu-id="93cdf-111">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="93cdf-111">E_FAIL</span></span>|<span data-ttu-id="93cdf-112">Le `ICorDebugStackWalk` objet n’a pas pu être avancé.</span><span class="sxs-lookup"><span data-stu-id="93cdf-112">The `ICorDebugStackWalk` object could not be advanced.</span></span>|  
|<span data-ttu-id="93cdf-113">CORDBG_S_AT_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="93cdf-113">CORDBG_S_AT_END_OF_STACK</span></span>|<span data-ttu-id="93cdf-114">La fin de la pile a été atteinte à la suite de ce déroulement.</span><span class="sxs-lookup"><span data-stu-id="93cdf-114">The end of the stack was reached as a result of this unwind.</span></span>|  
|<span data-ttu-id="93cdf-115">CORDBG_E_PAST_END_OF_STACK</span><span class="sxs-lookup"><span data-stu-id="93cdf-115">CORDBG_E_PAST_END_OF_STACK</span></span>|<span data-ttu-id="93cdf-116">Le pointeur de frame est déjà à la fin de la pile ; Par conséquent, aucun frame supplémentaires ne sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="93cdf-116">The frame pointer is already at the end of the stack; therefore, no additional frames can be accessed.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="93cdf-117">Exceptions</span><span class="sxs-lookup"><span data-stu-id="93cdf-117">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="93cdf-118">Notes</span><span class="sxs-lookup"><span data-stu-id="93cdf-118">Remarks</span></span>  
 <span data-ttu-id="93cdf-119">Le `Next` méthode avances le `ICorDebugStackWalk` de l’objet vers le frame appelant seulement si le runtime peut dérouler le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="93cdf-119">The `Next` method advances the `ICorDebugStackWalk` object to the calling frame only if the runtime can unwind the current frame.</span></span> <span data-ttu-id="93cdf-120">Sinon, l’objet avance le frame suivant que le runtime est en mesure de déroulement.</span><span class="sxs-lookup"><span data-stu-id="93cdf-120">Otherwise, the object advances to the next frame that the runtime is able to unwind.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="93cdf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93cdf-121">Requirements</span></span>  
 <span data-ttu-id="93cdf-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="93cdf-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93cdf-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="93cdf-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="93cdf-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="93cdf-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="93cdf-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93cdf-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93cdf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93cdf-126">See also</span></span>

- [<span data-ttu-id="93cdf-127">ICorDebugStackWalk, interface</span><span class="sxs-lookup"><span data-stu-id="93cdf-127">ICorDebugStackWalk Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md)
- [<span data-ttu-id="93cdf-128">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="93cdf-128">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="93cdf-129">Débogage</span><span class="sxs-lookup"><span data-stu-id="93cdf-129">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
