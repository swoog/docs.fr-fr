---
title: ICorDebugNativeFrame2::GetStackParameterSize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame2.GetStackParameterSize Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame2::GetStackParameterSize
helpviewer_keywords:
- ICorDebugNativeFrame2::GetStackParameterSize method [.NET Framework debugging]
- GetStackParameterSize method [.NET Framework debugging]
ms.assetid: f6a449c8-a941-43ba-9a90-c98b29ae3c36
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 47968d7550c3d16d201680caab705c0d7c85c784
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200140"
---
# <a name="icordebugnativeframe2getstackparametersize-method"></a><span data-ttu-id="d5d1a-102">ICorDebugNativeFrame2::GetStackParameterSize, méthode</span><span class="sxs-lookup"><span data-stu-id="d5d1a-102">ICorDebugNativeFrame2::GetStackParameterSize Method</span></span>
<span data-ttu-id="d5d1a-103">Retourne la taille cumulée des paramètres sur la pile sur x86 systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-103">Returns the cumulative size of the parameters on the stack on x86 operating systems.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5d1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d1a-104">Syntax</span></span>  
  
```  
HRESULT GetStackParameterSize([out] ULONG32 * pSize)  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5d1a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5d1a-105">Parameters</span></span>  
 `pSize`  
 <span data-ttu-id="d5d1a-106">[out] Pointeur vers la taille cumulée des paramètres sur la pile.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-106">[out] A pointer to the cumulative size of the parameters on the stack.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d5d1a-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d5d1a-107">Return Value</span></span>  
 <span data-ttu-id="d5d1a-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="d5d1a-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d5d1a-109">HRESULT</span></span>|<span data-ttu-id="d5d1a-110">Description</span><span class="sxs-lookup"><span data-stu-id="d5d1a-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d5d1a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5d1a-111">S_OK</span></span>|<span data-ttu-id="d5d1a-112">La taille de pile a été retournée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-112">The stack size was successfully returned.</span></span>|  
|<span data-ttu-id="d5d1a-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d5d1a-113">S_FALSE</span></span>|`GetStackParameterSize` <span data-ttu-id="d5d1a-114">a été appelé sur une plateforme non x86.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-114">was called on a non-x86 platform.</span></span>|  
|<span data-ttu-id="d5d1a-115">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d5d1a-115">E_FAIL</span></span>|`The size of the parameters could not be returned`<span data-ttu-id="d5d1a-116">.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-116">.</span></span>|  
|<span data-ttu-id="d5d1a-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d5d1a-117">E_INVALIDARG</span></span>|`pSize` <span data-ttu-id="d5d1a-118">Is `null`.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-118">Is `null`.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="d5d1a-119">Exceptions</span><span class="sxs-lookup"><span data-stu-id="d5d1a-119">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d5d1a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="d5d1a-120">Remarks</span></span>  
 <span data-ttu-id="d5d1a-121">Le [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) méthodes ne s’ajustent pas le pointeur de pile pour les paramètres qui sont envoyées sur la pile.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-121">The [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) methods do not adjust the stack pointer for parameters that are pushed on the stack.</span></span> <span data-ttu-id="d5d1a-122">Au lieu de cela, vous pouvez utiliser la valeur retournée par `GetStackParameterSize` pour ajuster le pointeur de pile pour amorcer un dérouleur natif, qui effectue l’ajustement pour les paramètres.</span><span class="sxs-lookup"><span data-stu-id="d5d1a-122">Instead, you can use the value returned by `GetStackParameterSize` to adjust the stack pointer to seed a native unwinder, which does adjust for the parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5d1a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d1a-123">Requirements</span></span>  
 <span data-ttu-id="d5d1a-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d5d1a-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5d1a-125">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d5d1a-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d5d1a-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5d1a-126">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d5d1a-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d5d1a-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d5d1a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d1a-128">See also</span></span>

- [<span data-ttu-id="d5d1a-129">ICorDebugNativeFrame2, interface</span><span class="sxs-lookup"><span data-stu-id="d5d1a-129">ICorDebugNativeFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe2-interface.md)
- [<span data-ttu-id="d5d1a-130">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d5d1a-130">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="d5d1a-131">Débogage</span><span class="sxs-lookup"><span data-stu-id="d5d1a-131">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
