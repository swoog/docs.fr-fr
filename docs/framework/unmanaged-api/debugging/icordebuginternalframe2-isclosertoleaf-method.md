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
ms.openlocfilehash: 30a9d26283d4f544bdd865e40cfc1c1c625ae462
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61995499"
---
# <a name="icordebuginternalframe2isclosertoleaf-method"></a><span data-ttu-id="7e995-102">ICorDebugInternalFrame2::IsCloserToLeaf, méthode</span><span class="sxs-lookup"><span data-stu-id="7e995-102">ICorDebugInternalFrame2::IsCloserToLeaf Method</span></span>
<span data-ttu-id="7e995-103">Vérifie si le `this` frame interne est la plus proche de la feuille que l’objet ICorDebugFrame spécifié.</span><span class="sxs-lookup"><span data-stu-id="7e995-103">Checks whether the `this` internal frame is closer to the leaf than the specified ICorDebugFrame object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e995-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e995-104">Syntax</span></span>  
  
```  
HRESULT IsCloserToLeaf([in] ICorDebugFrame * pFrameToCompare,  
                       [out] BOOL * pIsCloser);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7e995-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e995-105">Parameters</span></span>  
 `pFrameToCompare`  
 <span data-ttu-id="7e995-106">[in] Un pointeur vers la comparaison `ICorDebugFrame` objet.</span><span class="sxs-lookup"><span data-stu-id="7e995-106">[in] A pointer to the comparison `ICorDebugFrame` object.</span></span>  
  
 `pIsCloser`  
 <span data-ttu-id="7e995-107">[out] `true` si le `this` frame interne est la plus proche de la feuille que le frame spécifié par `pFrameToCompare`; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7e995-107">[out] `true` if the `this` internal frame is closer to the leaf than the frame specified by `pFrameToCompare`; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7e995-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7e995-108">Return Value</span></span>  
 <span data-ttu-id="7e995-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7e995-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="7e995-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7e995-110">HRESULT</span></span>|<span data-ttu-id="7e995-111">Description</span><span class="sxs-lookup"><span data-stu-id="7e995-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="7e995-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e995-112">S_OK</span></span>|<span data-ttu-id="7e995-113">La comparaison a été effectuée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7e995-113">The comparison was successfully performed.</span></span>|  
|<span data-ttu-id="7e995-114">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="7e995-114">E_FAIL</span></span>|<span data-ttu-id="7e995-115">La comparaison n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="7e995-115">The comparison could not be performed.</span></span>|  
|<span data-ttu-id="7e995-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7e995-116">E_INVALIDARG</span></span>|<span data-ttu-id="7e995-117">`pFrameToCompare` ou `pIsCloser` est null.</span><span class="sxs-lookup"><span data-stu-id="7e995-117">`pFrameToCompare` or `pIsCloser` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7e995-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7e995-118">Remarks</span></span>  
 <span data-ttu-id="7e995-119">`IsCloserToLeaf` peut être utilisé pour implémenter une stratégie pour entrelacer les frames internes avec d’autres images sur la pile.</span><span class="sxs-lookup"><span data-stu-id="7e995-119">`IsCloserToLeaf` can be used to implement a policy for interleaving internal frames with other frames on the stack.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e995-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e995-120">Requirements</span></span>  
 <span data-ttu-id="7e995-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7e995-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e995-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7e995-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7e995-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7e995-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7e995-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e995-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e995-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e995-125">See also</span></span>

- [<span data-ttu-id="7e995-126">ICorDebugInternalFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="7e995-126">ICorDebugInternalFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md)
- [<span data-ttu-id="7e995-127">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7e995-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="7e995-128">Débogage</span><span class="sxs-lookup"><span data-stu-id="7e995-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
