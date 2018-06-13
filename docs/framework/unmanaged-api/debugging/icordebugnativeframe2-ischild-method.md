---
title: ICorDebugNativeFrame2::IsChild, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.IsChild Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::IsChild
helpviewer_keywords:
- IsChild method [.NET Framework debugging]
- ICorDebugNativeFrame2::IsChild method [.NET Framework debugging]
ms.assetid: 9e2aae09-49cb-4fbd-81e5-e29cd864a88b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d9d613e810724b8e133b490c17a37ecc6565f09a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419385"
---
# <a name="icordebugnativeframe2ischild-method"></a><span data-ttu-id="81bb1-102">ICorDebugNativeFrame2::IsChild, méthode</span><span class="sxs-lookup"><span data-stu-id="81bb1-102">ICorDebugNativeFrame2::IsChild Method</span></span>
<span data-ttu-id="81bb1-103">Détermine si le frame actuel est un frame enfant.</span><span class="sxs-lookup"><span data-stu-id="81bb1-103">Determines whether the current frame is a child frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81bb1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81bb1-104">Syntax</span></span>  
  
```  
HRESULT IsChild([out] BOOL * pIsChild);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="81bb1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81bb1-105">Parameters</span></span>  
 `pIsChild`  
 <span data-ttu-id="81bb1-106">[out] Valeur booléenne qui spécifie si le frame actuel est un frame enfant.</span><span class="sxs-lookup"><span data-stu-id="81bb1-106">[out] A Boolean value that specifies whether the current frame is a child frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="81bb1-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="81bb1-107">Return Value</span></span>  
 <span data-ttu-id="81bb1-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="81bb1-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="81bb1-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="81bb1-109">HRESULT</span></span>|<span data-ttu-id="81bb1-110">Description</span><span class="sxs-lookup"><span data-stu-id="81bb1-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="81bb1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="81bb1-111">S_OK</span></span>|<span data-ttu-id="81bb1-112">L’état enfant a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="81bb1-112">The child status was successfully returned.</span></span>|  
|<span data-ttu-id="81bb1-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="81bb1-113">E_FAIL</span></span>|<span data-ttu-id="81bb1-114">L’état de l’enfant n’a pas pu être retourné.</span><span class="sxs-lookup"><span data-stu-id="81bb1-114">The child status could not be returned.</span></span>|  
|<span data-ttu-id="81bb1-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="81bb1-115">E_INVALIDARG</span></span>|<span data-ttu-id="81bb1-116">`pIsChild` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="81bb1-116">`pIsChild` is null.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="81bb1-117">Exceptions</span><span class="sxs-lookup"><span data-stu-id="81bb1-117">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="81bb1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="81bb1-118">Remarks</span></span>  
 <span data-ttu-id="81bb1-119">Le `IsChild` retourne de la méthode `true` si l’objet frame sur lequel vous appelez la méthode est un enfant d’un autre frame.</span><span class="sxs-lookup"><span data-stu-id="81bb1-119">The `IsChild` method returns `true` if the frame object on which you call the method is a child of another frame.</span></span> <span data-ttu-id="81bb1-120">Si c’est le cas, utilisez le [IsMatchingParentFrame](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-ismatchingparentframe-method.md) méthode permettant de vérifier si un frame est son parent.</span><span class="sxs-lookup"><span data-stu-id="81bb1-120">If this is the case, use the [IsMatchingParentFrame](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-ismatchingparentframe-method.md) method to check whether a frame is its parent.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81bb1-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="81bb1-121">Requirements</span></span>  
 <span data-ttu-id="81bb1-122">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="81bb1-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81bb1-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="81bb1-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="81bb1-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="81bb1-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="81bb1-125">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81bb1-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81bb1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81bb1-126">See Also</span></span>  
 [<span data-ttu-id="81bb1-127">ICorDebugNativeFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="81bb1-127">ICorDebugNativeFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)  
 [<span data-ttu-id="81bb1-128">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="81bb1-128">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="81bb1-129">Débogage</span><span class="sxs-lookup"><span data-stu-id="81bb1-129">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
