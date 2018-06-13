---
title: ICorDebugVirtualUnwinder::Next, méthode
ms.date: 03/30/2017
ms.assetid: 790e0426-e5cd-49fd-a792-f8c8635d72fe
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a4bacbd9ef11f6f6cb6d9952290c00f1b8ce50aa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423427"
---
# <a name="icordebugvirtualunwindernext-method"></a><span data-ttu-id="1c92f-102">ICorDebugVirtualUnwinder::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="1c92f-102">ICorDebugVirtualUnwinder::Next Method</span></span>
<span data-ttu-id="1c92f-103">Avance jusqu'au contexte de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="1c92f-103">Advances to the caller's context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c92f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c92f-104">Syntax</span></span>  
  
```  
HRESULT Next();  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1c92f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c92f-105">Parameters</span></span>  
 <span data-ttu-id="1c92f-106">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1c92f-106">None.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1c92f-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1c92f-107">Return Value</span></span>  
 <span data-ttu-id="1c92f-108">`S_OK` en cas de réussite du déroulement ou `CORDBG_S_AT_END_OF_STACK` si le déroulement ne peut pas être effectué étant donné qu'il ne reste plus de frames.</span><span class="sxs-lookup"><span data-stu-id="1c92f-108">`S_OK` if the unwind occurred successfully, or `CORDBG_S_AT_END_OF_STACK` if the unwind cannot be completed because there are no more frames.</span></span>  
  
 <span data-ttu-id="1c92f-109">Si un HRESULT indiquant un échec est retourné, les API ICorDebug retournent `CORDBG_E_DATA_TARGET_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="1c92f-109">If a failing HRESULT is returned, ICorDebug APIs will return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1c92f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1c92f-110">Remarks</span></span>  
 <span data-ttu-id="1c92f-111">L'explorateur de pile doit vérifier sa progression vers l'avant. Ainsi, un appel à `Next` doit retourner un HRESULT indiquant un échec ou `CORDBG_S_AT_END_OF_STACK`.</span><span class="sxs-lookup"><span data-stu-id="1c92f-111">The stack walker should ensure that it makes forward progress, so that eventually a call to `Next` will return a failing HRESULT or `CORDBG_S_AT_END_OF_STACK`.</span></span> <span data-ttu-id="1c92f-112">Retour de `S_OK` indéfiniment peut provoquer une boucle infinie.</span><span class="sxs-lookup"><span data-stu-id="1c92f-112">Returning `S_OK` indefinitely may cause an infinite loop.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1c92f-113">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="1c92f-113">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c92f-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c92f-114">Requirements</span></span>  
 <span data-ttu-id="1c92f-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c92f-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c92f-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1c92f-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1c92f-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1c92f-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1c92f-118">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c92f-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c92f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c92f-119">See Also</span></span>  
 [<span data-ttu-id="1c92f-120">ICorDebugMemoryBuffer, interface</span><span class="sxs-lookup"><span data-stu-id="1c92f-120">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)  
 [<span data-ttu-id="1c92f-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1c92f-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
