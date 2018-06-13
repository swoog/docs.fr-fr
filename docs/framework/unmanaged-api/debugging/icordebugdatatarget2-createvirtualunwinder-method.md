---
title: ICorDebugDataTarget2::CreateVirtualUnwinder, méthode
ms.date: 03/30/2017
ms.assetid: 354c8b4c-7d23-45c6-a7d7-3be4c2a5b772
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 92dd0a4ad8128f7ce300ca5da1e5022b944d91e8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417639"
---
# <a name="icordebugdatatarget2createvirtualunwinder-method"></a><span data-ttu-id="c4e83-102">ICorDebugDataTarget2::CreateVirtualUnwinder, méthode</span><span class="sxs-lookup"><span data-stu-id="c4e83-102">ICorDebugDataTarget2::CreateVirtualUnwinder Method</span></span>
<span data-ttu-id="c4e83-103">Crée un dérouleur de pile qui commence le déroulement à partir d'un contexte initial (qui n'est pas forcément la feuille d'un thread).</span><span class="sxs-lookup"><span data-stu-id="c4e83-103">Creates a new stack unwinder that starts unwinding from an initial context (which isn't necessarily the leaf of a thread).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4e83-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4e83-104">Syntax</span></span>  
  
```  
HRESULT CreateVirtualUnwinder(  
    [in] DWORD nativeThreadID,  
    [in] ULONG32 contextFlags,  
    [in] ULONG32 cbContext,  
    [in, size_is(cbContext)] BYTE initialContext[],  
    [out] ICorDebugVirtualUnwinder ** ppUnwinder);  
};  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c4e83-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4e83-105">Parameters</span></span>  
 <span data-ttu-id="c4e83-106">nativeThreadID</span><span class="sxs-lookup"><span data-stu-id="c4e83-106">nativeThreadID</span></span>  
 <span data-ttu-id="c4e83-107">[in] L'ID de thread natif du thread à partir duquel dérouler la pile.</span><span class="sxs-lookup"><span data-stu-id="c4e83-107">[in] The native thread ID of the thread whose stack is to be unwound.</span></span>  
  
 <span data-ttu-id="c4e83-108">contextFlags</span><span class="sxs-lookup"><span data-stu-id="c4e83-108">contextFlags</span></span>  
 <span data-ttu-id="c4e83-109">[in] Indicateurs qui spécifient les parties du contexte définies dans `initialContext`.</span><span class="sxs-lookup"><span data-stu-id="c4e83-109">[in] Flags that specify which parts of the context are defined in `initialContext`.</span></span>  
  
 <span data-ttu-id="c4e83-110">cbContext</span><span class="sxs-lookup"><span data-stu-id="c4e83-110">cbContext</span></span>  
 <span data-ttu-id="c4e83-111">[in] Taille de `initialContext`.</span><span class="sxs-lookup"><span data-stu-id="c4e83-111">[in] The size of `initialContext`.</span></span>  
  
 <span data-ttu-id="c4e83-112">initialContext</span><span class="sxs-lookup"><span data-stu-id="c4e83-112">initialContext</span></span>  
 <span data-ttu-id="c4e83-113">[in] Données dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="c4e83-113">[in] The data in the context.</span></span>  
  
 <span data-ttu-id="c4e83-114">ppUnwinder</span><span class="sxs-lookup"><span data-stu-id="c4e83-114">ppUnwinder</span></span>  
 <span data-ttu-id="c4e83-115">[out] Pointeur vers l'adresse d'un objet d'interface ICorDebugVirtualUnwinder.</span><span class="sxs-lookup"><span data-stu-id="c4e83-115">[out] A pointer to the address of an ICorDebugVirtualUnwinder interface object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c4e83-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c4e83-116">Return Value</span></span>  
 <span data-ttu-id="c4e83-117">`S_OK` si l'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c4e83-117">`S_OK` if successful.</span></span> <span data-ttu-id="c4e83-118">Toute autre valeur `HRESULT` indique l'échec de l'opération.</span><span class="sxs-lookup"><span data-stu-id="c4e83-118">Any other `HRESULT` indicates failure.</span></span> <span data-ttu-id="c4e83-119">Toute erreur `HRESULT` reçue par mscordbi est considérée comme irrécupérable [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) méthodes pour retourner `CORDBG_E_DATA_TARGET_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="c4e83-119">Any failing `HRESULT` received by mscordbi is considered fatal and causes [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) methods to return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c4e83-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c4e83-120">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c4e83-121">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="c4e83-121">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4e83-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4e83-122">Requirements</span></span>  
 <span data-ttu-id="c4e83-123">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4e83-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4e83-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c4e83-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c4e83-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c4e83-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c4e83-126">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4e83-126">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4e83-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e83-127">See Also</span></span>  
 [<span data-ttu-id="c4e83-128">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="c4e83-128">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)  
 [<span data-ttu-id="c4e83-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c4e83-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
