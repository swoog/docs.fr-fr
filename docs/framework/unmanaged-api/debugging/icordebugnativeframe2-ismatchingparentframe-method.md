---
title: ICorDebugNativeFrame2::IsMatchingParentFrame, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.IsMatchingParentFrame Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::IsMatchingParentFrame
helpviewer_keywords:
- IsMatchingParentFrame method [.NET Framework debugging]
- ICorDebugNativeFrame2::IsMatchingParentFrame method [.NET Framework debugging]
ms.assetid: d2ca20db-df22-4528-a0dd-a09ea62c8998
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 39c0ea69a0922f5e0d25c98c21ec17a872b2f421
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418868"
---
# <a name="icordebugnativeframe2ismatchingparentframe-method"></a><span data-ttu-id="e63af-102">ICorDebugNativeFrame2::IsMatchingParentFrame, méthode</span><span class="sxs-lookup"><span data-stu-id="e63af-102">ICorDebugNativeFrame2::IsMatchingParentFrame Method</span></span>
<span data-ttu-id="e63af-103">Détermine si le frame spécifié est le parent de l’image actuelle.</span><span class="sxs-lookup"><span data-stu-id="e63af-103">Determines whether the specified frame is the parent of the current frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e63af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e63af-104">Syntax</span></span>  
  
```  
HRESULT IsMatchingParentFrame([in] ICorDebugNativeFrame2  
                                      *pPotentialParentFrame,  
                              [out] BOOL *pIsParent);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e63af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e63af-105">Parameters</span></span>  
 `pPotentialParentFrame`  
 <span data-ttu-id="e63af-106">[in] Pointeur vers l’objet frame que vous souhaitez évaluer l’état de parent.</span><span class="sxs-lookup"><span data-stu-id="e63af-106">[in] A pointer to the frame object that you want to evaluate for parent status.</span></span>  
  
 `pIsParent`  
 <span data-ttu-id="e63af-107">[out] `true` si `pPotentialParentFrame` est le parent du frame actuel ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e63af-107">[out] `true` if `pPotentialParentFrame` is the current frame’s parent; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e63af-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e63af-108">Return Value</span></span>  
 <span data-ttu-id="e63af-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e63af-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="e63af-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e63af-110">HRESULT</span></span>|<span data-ttu-id="e63af-111">Description</span><span class="sxs-lookup"><span data-stu-id="e63af-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e63af-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e63af-112">S_OK</span></span>|<span data-ttu-id="e63af-113">L’état parent a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e63af-113">The parent status was successfully returned.</span></span>|  
|<span data-ttu-id="e63af-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e63af-114">E_FAIL</span></span>|<span data-ttu-id="e63af-115">L’état de parent n’a pas pu être retourné.</span><span class="sxs-lookup"><span data-stu-id="e63af-115">The parent status could not be returned.</span></span>|  
|<span data-ttu-id="e63af-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e63af-116">E_INVALIDARG</span></span>|<span data-ttu-id="e63af-117">`pPotentialParentFrame` ou `pIsParent` est null.</span><span class="sxs-lookup"><span data-stu-id="e63af-117">`pPotentialParentFrame` or `pIsParent` is null.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="e63af-118">Exceptions</span><span class="sxs-lookup"><span data-stu-id="e63af-118">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e63af-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e63af-119">Remarks</span></span>  
 <span data-ttu-id="e63af-120">`IsMatchingParentFrame` Retourne `true` si l’objet frame que vous passez à la méthode est le parent de l’objet frame sur lequel la méthode a été appelée.</span><span class="sxs-lookup"><span data-stu-id="e63af-120">`IsMatchingParentFrame` returns `true` if the frame object you pass to the method is the parent of the frame object on which the method was called.</span></span> <span data-ttu-id="e63af-121">Si vous appelez la méthode sur un frame qui n’est pas un enfant du frame spécifié, elle retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e63af-121">If you call the method on a frame that is not a child of the specified frame, it returns an error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e63af-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e63af-122">Requirements</span></span>  
 <span data-ttu-id="e63af-123">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e63af-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e63af-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e63af-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e63af-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e63af-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e63af-126">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e63af-126">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e63af-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e63af-127">See Also</span></span>  
 [<span data-ttu-id="e63af-128">ICorDebugNativeFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="e63af-128">ICorDebugNativeFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)  
 [<span data-ttu-id="e63af-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e63af-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="e63af-130">Débogage</span><span class="sxs-lookup"><span data-stu-id="e63af-130">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
