---
title: Icordebugvirtualunwinder::Next, méthode
ms.date: 03/30/2017
ms.assetid: 790e0426-e5cd-49fd-a792-f8c8635d72fe
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 74be827dc97213507b96da9e025923f859011acd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076885"
---
# <a name="icordebugvirtualunwindernext-method"></a><span data-ttu-id="63a16-102">Icordebugvirtualunwinder::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="63a16-102">ICorDebugVirtualUnwinder::Next Method</span></span>
<span data-ttu-id="63a16-103">Avance jusqu'au contexte de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="63a16-103">Advances to the caller's context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63a16-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63a16-104">Syntax</span></span>  
  
```  
HRESULT Next();  
```  
  
## <a name="parameters"></a><span data-ttu-id="63a16-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63a16-105">Parameters</span></span>  
 <span data-ttu-id="63a16-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="63a16-106">None.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="63a16-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="63a16-107">Return Value</span></span>  
 <span data-ttu-id="63a16-108">`S_OK` en cas de réussite du déroulement ou `CORDBG_S_AT_END_OF_STACK` si le déroulement ne peut pas être effectué étant donné qu'il ne reste plus de frames.</span><span class="sxs-lookup"><span data-stu-id="63a16-108">`S_OK` if the unwind occurred successfully, or `CORDBG_S_AT_END_OF_STACK` if the unwind cannot be completed because there are no more frames.</span></span>  
  
 <span data-ttu-id="63a16-109">Si un HRESULT indiquant un échec est retourné, les API ICorDebug retournent `CORDBG_E_DATA_TARGET_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="63a16-109">If a failing HRESULT is returned, ICorDebug APIs will return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="63a16-110">Notes</span><span class="sxs-lookup"><span data-stu-id="63a16-110">Remarks</span></span>  
 <span data-ttu-id="63a16-111">L'explorateur de pile doit vérifier sa progression vers l'avant. Ainsi, un appel à `Next` doit retourner un HRESULT indiquant un échec ou `CORDBG_S_AT_END_OF_STACK`.</span><span class="sxs-lookup"><span data-stu-id="63a16-111">The stack walker should ensure that it makes forward progress, so that eventually a call to `Next` will return a failing HRESULT or `CORDBG_S_AT_END_OF_STACK`.</span></span> <span data-ttu-id="63a16-112">Retour `S_OK` indéfiniment peut provoquer une boucle infinie.</span><span class="sxs-lookup"><span data-stu-id="63a16-112">Returning `S_OK` indefinitely may cause an infinite loop.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="63a16-113">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="63a16-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63a16-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63a16-114">Requirements</span></span>  
 <span data-ttu-id="63a16-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63a16-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63a16-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="63a16-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="63a16-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="63a16-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="63a16-118">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63a16-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63a16-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63a16-119">See also</span></span>

- [<span data-ttu-id="63a16-120">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="63a16-120">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="63a16-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="63a16-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
