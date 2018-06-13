---
title: ICorDebugInternalFrame2::IsCloserToLeaf, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2.IsCloserToLeaf Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2::IsCloserToLeaf
helpviewer_keywords:
- ICorDebugInternalFrame2::IsCloserToLeaf method [.NET Framework debugging]
- IsCloserToLeaf method [.NET Framework debugging]
ms.assetid: c1d3d1eb-8370-4f25-8297-3bd262b4740a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6d26d4dc046841a891c8a36530bd579d100b8f5b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416122"
---
# <a name="icordebuginternalframe2isclosertoleaf-method"></a><span data-ttu-id="4b424-102">ICorDebugInternalFrame2::IsCloserToLeaf, méthode</span><span class="sxs-lookup"><span data-stu-id="4b424-102">ICorDebugInternalFrame2::IsCloserToLeaf Method</span></span>
<span data-ttu-id="4b424-103">Vérifie si le `this` frame interne est proche de la feuille de l’objet ICorDebugFrame spécifié.</span><span class="sxs-lookup"><span data-stu-id="4b424-103">Checks whether the `this` internal frame is closer to the leaf than the specified ICorDebugFrame object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b424-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b424-104">Syntax</span></span>  
  
```  
HRESULT IsCloserToLeaf([in] ICorDebugFrame * pFrameToCompare,  
                       [out] BOOL * pIsCloser);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4b424-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b424-105">Parameters</span></span>  
 `pFrameToCompare`  
 <span data-ttu-id="4b424-106">[in] Un pointeur vers la comparaison `ICorDebugFrame` objet.</span><span class="sxs-lookup"><span data-stu-id="4b424-106">[in] A pointer to the comparison `ICorDebugFrame` object.</span></span>  
  
 `pIsCloser`  
 <span data-ttu-id="4b424-107">[out] `true` si le `this` frame interne est proche de la feuille que le frame spécifié par `pFrameToCompare`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="4b424-107">[out] `true` if the `this` internal frame is closer to the leaf than the frame specified by `pFrameToCompare`; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b424-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4b424-108">Return Value</span></span>  
 <span data-ttu-id="4b424-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="4b424-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="4b424-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4b424-110">HRESULT</span></span>|<span data-ttu-id="4b424-111">Description</span><span class="sxs-lookup"><span data-stu-id="4b424-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4b424-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b424-112">S_OK</span></span>|<span data-ttu-id="4b424-113">La comparaison a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4b424-113">The comparison was successfully performed.</span></span>|  
|<span data-ttu-id="4b424-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="4b424-114">E_FAIL</span></span>|<span data-ttu-id="4b424-115">La comparaison n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b424-115">The comparison could not be performed.</span></span>|  
|<span data-ttu-id="4b424-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4b424-116">E_INVALIDARG</span></span>|<span data-ttu-id="4b424-117">`pFrameToCompare` ou `pIsCloser` est null.</span><span class="sxs-lookup"><span data-stu-id="4b424-117">`pFrameToCompare` or `pIsCloser` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4b424-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4b424-118">Remarks</span></span>  
 <span data-ttu-id="4b424-119">`IsCloserToLeaf` peut être utilisé pour implémenter une stratégie pour entrelacer les frames internes avec d’autres frames sur la pile.</span><span class="sxs-lookup"><span data-stu-id="4b424-119">`IsCloserToLeaf` can be used to implement a policy for interleaving internal frames with other frames on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b424-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4b424-120">Requirements</span></span>  
 <span data-ttu-id="4b424-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4b424-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b424-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4b424-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4b424-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4b424-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4b424-124">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b424-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b424-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b424-125">See Also</span></span>  
 [<span data-ttu-id="4b424-126">ICorDebugInternalFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="4b424-126">ICorDebugInternalFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md)  
 [<span data-ttu-id="4b424-127">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4b424-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="4b424-128">Débogage</span><span class="sxs-lookup"><span data-stu-id="4b424-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
