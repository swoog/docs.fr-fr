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
ms.openlocfilehash: 9503c12da9e98fbd43f3904aad25c5d10655cec2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994641"
---
# <a name="icordebugnativeframe2ischild-method"></a><span data-ttu-id="1bb3c-102">ICorDebugNativeFrame2::IsChild, méthode</span><span class="sxs-lookup"><span data-stu-id="1bb3c-102">ICorDebugNativeFrame2::IsChild Method</span></span>
<span data-ttu-id="1bb3c-103">Détermine si le frame actuel est un frame enfant.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-103">Determines whether the current frame is a child frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1bb3c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bb3c-104">Syntax</span></span>  
  
```  
HRESULT IsChild([out] BOOL * pIsChild);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1bb3c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bb3c-105">Parameters</span></span>  
 `pIsChild`  
 <span data-ttu-id="1bb3c-106">[out] Valeur booléenne qui spécifie si le frame actuel est un frame enfant.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-106">[out] A Boolean value that specifies whether the current frame is a child frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1bb3c-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1bb3c-107">Return Value</span></span>  
 <span data-ttu-id="1bb3c-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="1bb3c-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1bb3c-109">HRESULT</span></span>|<span data-ttu-id="1bb3c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1bb3c-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1bb3c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bb3c-111">S_OK</span></span>|<span data-ttu-id="1bb3c-112">L’état de l’enfant a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-112">The child status was successfully returned.</span></span>|  
|<span data-ttu-id="1bb3c-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1bb3c-113">E_FAIL</span></span>|<span data-ttu-id="1bb3c-114">L’état de l’enfant n’a pas pu être retourné.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-114">The child status could not be returned.</span></span>|  
|<span data-ttu-id="1bb3c-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1bb3c-115">E_INVALIDARG</span></span>|<span data-ttu-id="1bb3c-116">`pIsChild` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-116">`pIsChild` is null.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="1bb3c-117">Exceptions</span><span class="sxs-lookup"><span data-stu-id="1bb3c-117">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1bb3c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1bb3c-118">Remarks</span></span>  
 <span data-ttu-id="1bb3c-119">Le `IsChild` retourne de la méthode `true` si l’objet de frame sur lequel vous appelez la méthode est un enfant d’un autre frame.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-119">The `IsChild` method returns `true` if the frame object on which you call the method is a child of another frame.</span></span> <span data-ttu-id="1bb3c-120">Si c’est le cas, utilisez le [IsMatchingParentFrame](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-ismatchingparentframe-method.md) méthode pour vérifier si un frame est son parent.</span><span class="sxs-lookup"><span data-stu-id="1bb3c-120">If this is the case, use the [IsMatchingParentFrame](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-ismatchingparentframe-method.md) method to check whether a frame is its parent.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1bb3c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bb3c-121">Requirements</span></span>  
 <span data-ttu-id="1bb3c-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1bb3c-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1bb3c-123">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1bb3c-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1bb3c-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1bb3c-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1bb3c-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1bb3c-125">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bb3c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb3c-126">See also</span></span>

- [<span data-ttu-id="1bb3c-127">ICorDebugNativeFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="1bb3c-127">ICorDebugNativeFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)
- [<span data-ttu-id="1bb3c-128">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1bb3c-128">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="1bb3c-129">Débogage</span><span class="sxs-lookup"><span data-stu-id="1bb3c-129">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
