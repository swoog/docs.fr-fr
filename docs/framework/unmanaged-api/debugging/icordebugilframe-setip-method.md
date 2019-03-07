---
title: ICorDebugILFrame::SetIP, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.SetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::SetIP
helpviewer_keywords:
- SetIP method, ICorDebugILFrame interface [.NET Framework debugging]
- ICorDebugILFrame::SetIP method [.NET Framework debugging]
ms.assetid: 23f38dc1-85e4-4263-9235-2d05bbb6a833
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a25e52c6b858aaa602ffade0e407b1aaf6e5c67e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471389"
---
# <a name="icordebugilframesetip-method"></a><span data-ttu-id="3def8-102">ICorDebugILFrame::SetIP, méthode</span><span class="sxs-lookup"><span data-stu-id="3def8-102">ICorDebugILFrame::SetIP Method</span></span>
<span data-ttu-id="3def8-103">Définit le pointeur d’instruction à l’emplacement de décalage spécifié dans le code de Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="3def8-103">Sets the instruction pointer to the specified offset location in the Microsoft intermediate language (MSIL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3def8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3def8-104">Syntax</span></span>  
  
```  
HRESULT SetIP (  
    [in] ULONG32 nOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3def8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3def8-105">Parameters</span></span>  
 `nOffset`  
 <span data-ttu-id="3def8-106">Emplacement de décalage dans le code MSIL.</span><span class="sxs-lookup"><span data-stu-id="3def8-106">The offset location in the MSIL code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3def8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3def8-107">Remarks</span></span>  
 <span data-ttu-id="3def8-108">Les appels à `SetIP` invalider immédiatement tous les frames et des chaînes pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="3def8-108">Calls to `SetIP` immediately invalidate all frames and chains for the current thread.</span></span> <span data-ttu-id="3def8-109">Si le débogueur a besoin des informations de frame après un appel à `SetIP`, il doit effectuer une nouvelle trace de pile.</span><span class="sxs-lookup"><span data-stu-id="3def8-109">If the debugger needs frame information after a call to `SetIP`, it must perform a new stack trace.</span></span>  
  
 <span data-ttu-id="3def8-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) essaiera de conserver le frame de pile dans un état valide.</span><span class="sxs-lookup"><span data-stu-id="3def8-110">[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) will attempt to keep the stack frame in a valid state.</span></span> <span data-ttu-id="3def8-111">Toutefois, même si le frame est dans un état valide, il reste peut-être des problèmes tels que des variables locales non initialisées.</span><span class="sxs-lookup"><span data-stu-id="3def8-111">However, even if the frame is in a valid state, there still may be problems such as uninitialized local variables.</span></span> <span data-ttu-id="3def8-112">L’appelant est responsable de la cohérence du programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3def8-112">The caller is responsible for ensuring the coherency of the running program.</span></span>  
  
 <span data-ttu-id="3def8-113">Sur les plateformes 64 bits, le pointeur d’instruction ne peut pas être déplacé hors d’un `catch` ou `finally` bloc.</span><span class="sxs-lookup"><span data-stu-id="3def8-113">On 64-bit platforms, the instruction pointer cannot be moved out of a `catch` or `finally` block.</span></span> <span data-ttu-id="3def8-114">Si `SetIP` est appelée pour effectuer ce déplacement sur une plateforme 64 bits, il retourne un HRESULT indiquant un échec.</span><span class="sxs-lookup"><span data-stu-id="3def8-114">If `SetIP` is called to make such a move on a 64-bit platform, it will return an HRESULT indicating failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3def8-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3def8-115">Requirements</span></span>  
 <span data-ttu-id="3def8-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3def8-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3def8-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3def8-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3def8-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3def8-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3def8-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3def8-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
