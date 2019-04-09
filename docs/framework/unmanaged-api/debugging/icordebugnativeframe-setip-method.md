---
title: ICorDebugNativeFrame::SetIP, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.SetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::SetIP
helpviewer_keywords:
- ICorDebugNativeFrame::SetIP method [.NET Framework debugging]
- SetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
ms.assetid: 57784a51-c76d-48f8-9392-584d0e1946d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 604486a074c3dbe3d19b741df28499ee03e1b2e5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193276"
---
# <a name="icordebugnativeframesetip-method"></a><span data-ttu-id="bd3b6-102">ICorDebugNativeFrame::SetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="bd3b6-102">ICorDebugNativeFrame::SetIP Method</span></span>
<span data-ttu-id="bd3b6-103">Définit le pointeur d’instruction à l’emplacement de décalage spécifié dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-103">Sets the instruction pointer to the specified offset location in native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd3b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd3b6-104">Syntax</span></span>  
  
```  
HRESULT SetIP (  
    [in] ULONG32 nOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bd3b6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd3b6-105">Parameters</span></span>  
 `nOffset`  
 <span data-ttu-id="bd3b6-106">[in] Emplacement de décalage dans le code natif.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-106">[in] The offset location in the native code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bd3b6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bd3b6-107">Remarks</span></span>  
 <span data-ttu-id="bd3b6-108">Les appels à `SetIP` invalider immédiatement tous les frames et des chaînes pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-108">Calls to `SetIP` immediately invalidate all frames and chains for the current thread.</span></span> <span data-ttu-id="bd3b6-109">Si le débogueur a besoin des informations de frame après un appel à `SetIP`, il doit effectuer une nouvelle trace de pile.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-109">If the debugger needs frame information after a call to `SetIP`, it must perform a new stack trace.</span></span>  
  
 <span data-ttu-id="bd3b6-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) essaiera de conserver le frame de pile dans un état valide.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) will attempt to keep the stack frame in a valid state.</span></span> <span data-ttu-id="bd3b6-111">Toutefois, même si le frame est dans un état valide, autant que le runtime est concerné, il reste peut-être des problèmes, tels que des variables locales non initialisées et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-111">However, even if the frame is in a valid state, as far as the runtime is concerned, there still may be problems, such as uninitialized local variables, and so on.</span></span> <span data-ttu-id="bd3b6-112">L’appelant est responsable de la cohérence du programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-112">The caller is responsible for insuring coherency of the running program.</span></span>  
  
 <span data-ttu-id="bd3b6-113">Sur les plateformes 64 bits, le pointeur d’instruction ne peut pas être déplacé hors d’un `catch` ou `finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-113">On 64-bit platforms, the instruction pointer cannot be moved out of a `catch` or `finally` block.</span></span> <span data-ttu-id="bd3b6-114">Si `SetIP` est appelée pour effectuer ce déplacement sur une plateforme 64 bits, il retourne un HRESULT indiquant un échec.</span><span class="sxs-lookup"><span data-stu-id="bd3b6-114">If `SetIP` is called to make such a move on a 64-bit platform, it will return an HRESULT indicating failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd3b6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd3b6-115">Requirements</span></span>  
 <span data-ttu-id="bd3b6-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b6-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd3b6-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bd3b6-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bd3b6-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bd3b6-118">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="bd3b6-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bd3b6-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bd3b6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd3b6-120">See also</span></span>
