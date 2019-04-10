---
title: ICorDebugThread3::CreateStackWalk, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread3.CreateStackWalk Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread3::CreateStackWalk
helpviewer_keywords:
- CreateStackWalk method [.NET Framework debugging]
- ICorDebugThread3::CreateStackWalk method [.NET Framework debugging]
ms.assetid: c55e35d9-f9aa-4268-94b5-dce44c61acf2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7969d8482970b13951938203262f6ce8f9bf574a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59229301"
---
# <a name="icordebugthread3createstackwalk-method"></a><span data-ttu-id="0f78b-102">ICorDebugThread3::CreateStackWalk, méthode</span><span class="sxs-lookup"><span data-stu-id="0f78b-102">ICorDebugThread3::CreateStackWalk Method</span></span>
<span data-ttu-id="0f78b-103">Crée un [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) objet pour le thread dont vous souhaitez dérouler la pile.</span><span class="sxs-lookup"><span data-stu-id="0f78b-103">Creates an [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f78b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f78b-104">Syntax</span></span>  
  
```  
HRESULT CreateStackWalk([out] ICorDebugStackWalk **ppStackWalk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0f78b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f78b-105">Parameters</span></span>  
 `ppStackWalk`  
 <span data-ttu-id="0f78b-106">[out] Un pointeur vers l’adresse de la [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) objet pour le thread dont vous souhaitez dérouler la pile.</span><span class="sxs-lookup"><span data-stu-id="0f78b-106">[out] A pointer to address of the [ICorDebugStackWalk](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-interface.md) object for the thread whose stack you want to unwind.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0f78b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0f78b-107">Return Value</span></span>  
 <span data-ttu-id="0f78b-108">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0f78b-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="0f78b-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0f78b-109">HRESULT</span></span>|<span data-ttu-id="0f78b-110">Description</span><span class="sxs-lookup"><span data-stu-id="0f78b-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0f78b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0f78b-111">S_OK</span></span>|<span data-ttu-id="0f78b-112">Le `ICorDebugStackWalk` objet a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="0f78b-112">The `ICorDebugStackWalk` object was successfully created.</span></span>|  
|<span data-ttu-id="0f78b-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0f78b-113">E_FAIL</span></span>|<span data-ttu-id="0f78b-114">Le `ICorDebugStackWalk` objet n’a pas été créé.</span><span class="sxs-lookup"><span data-stu-id="0f78b-114">The `ICorDebugStackWalk` object was not created.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="0f78b-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="0f78b-115">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0f78b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0f78b-116">Remarks</span></span>  
 <span data-ttu-id="0f78b-117">Si le `CreateStackWalk` méthode réussit, retourné `ICorDebugStackWalk` contexte de l’objet est défini sur le contexte du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="0f78b-117">If the `CreateStackWalk` method succeeds, the returned `ICorDebugStackWalk` object's context is set to the thread's current context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f78b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f78b-118">Requirements</span></span>  
 <span data-ttu-id="0f78b-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f78b-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f78b-120">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f78b-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f78b-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f78b-121">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0f78b-122">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0f78b-122">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0f78b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f78b-123">See also</span></span>

- [<span data-ttu-id="0f78b-124">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0f78b-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="0f78b-125">Débogage</span><span class="sxs-lookup"><span data-stu-id="0f78b-125">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
