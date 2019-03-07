---
title: ICorDebugProcess::GetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetThreadContext
helpviewer_keywords:
- ICorDebugProcess::GetThreadContext method [.NET Framework debugging]
- GetThreadContext method, ICorDebugProcess interface [.NET Framework debugging]
ms.assetid: 5b132ef1-8d4b-4525-89b3-54123596c194
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 28d54becc2d7cd4359c78415f25f579b968cb3f4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482338"
---
# <a name="icordebugprocessgetthreadcontext-method"></a><span data-ttu-id="b9f01-102">ICorDebugProcess::GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="b9f01-102">ICorDebugProcess::GetThreadContext Method</span></span>
<span data-ttu-id="b9f01-103">Obtient le contexte pour le thread donné dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="b9f01-103">Gets the context for the given thread in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9f01-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9f01-104">Syntax</span></span>  
  
```  
HRESULT GetThreadContext(  
    [in] DWORD threadID,  
    [in] ULONG32 contextSize,  
    [in, out, length_is(contextSize), size_is(contextSize)]  
    BYTE context[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9f01-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9f01-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="b9f01-106">[in] L’ID du thread pour lequel récupérer le contexte.</span><span class="sxs-lookup"><span data-stu-id="b9f01-106">[in] The ID of the thread for which to retrieve the context.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="b9f01-107">[in] Taille du tableau `context`.</span><span class="sxs-lookup"><span data-stu-id="b9f01-107">[in] The size of the `context` array.</span></span>  
  
 `context`  
 <span data-ttu-id="b9f01-108">[in, out] Un tableau d’octets qui décrivent le contexte du thread.</span><span class="sxs-lookup"><span data-stu-id="b9f01-108">[in, out] An array of bytes that describe the thread's context.</span></span>  
  
 <span data-ttu-id="b9f01-109">Le contexte spécifie l’architecture du processeur sur lequel le thread s’exécute.</span><span class="sxs-lookup"><span data-stu-id="b9f01-109">The context specifies the architecture of the processor on which the thread is executing.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b9f01-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b9f01-110">Remarks</span></span>  
 <span data-ttu-id="b9f01-111">Le débogueur doit appeler cette méthode plutôt que Win32 `GetThreadContext` (méthode), car le thread peut être dans un état « infiltré », son contexte dans lequel a été temporairement modifié.</span><span class="sxs-lookup"><span data-stu-id="b9f01-111">The debugger should call this method rather than the Win32 `GetThreadContext` method, because the thread may actually be in a "hijacked" state, in which its context has been temporarily changed.</span></span> <span data-ttu-id="b9f01-112">Cette méthode doit être utilisée uniquement lorsqu’un thread est en code natif.</span><span class="sxs-lookup"><span data-stu-id="b9f01-112">This method should be used only when a thread is in native code.</span></span> <span data-ttu-id="b9f01-113">Utilisez [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) pour les threads en code managé.</span><span class="sxs-lookup"><span data-stu-id="b9f01-113">Use [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) for threads in managed code.</span></span>  
  
 <span data-ttu-id="b9f01-114">Les données retournées sont une structure de contexte pour la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="b9f01-114">The data returned is a context structure for the current platform.</span></span> <span data-ttu-id="b9f01-115">Comme avec Win32 `GetThreadContext` (méthode), l’appelant doit initialiser le `context` paramètre avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b9f01-115">Just as with the Win32 `GetThreadContext` method, the caller should initialize the `context` parameter before calling this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9f01-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b9f01-116">Requirements</span></span>  
 <span data-ttu-id="b9f01-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9f01-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9f01-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9f01-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9f01-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9f01-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b9f01-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9f01-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
