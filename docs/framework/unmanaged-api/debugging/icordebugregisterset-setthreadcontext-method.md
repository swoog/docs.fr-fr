---
title: ICorDebugRegisterSet::SetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::SetThreadContext
helpviewer_keywords:
- ICorDebugRegisterSet::SetThreadContext method [.NET Framework debugging]
- SetThreadContext method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 73afa930-32cb-4c40-81f8-83e8e6fbe213
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7283266857d81b7d97bcacb56862b50f01cd3f0f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419941"
---
# <a name="icordebugregistersetsetthreadcontext-method"></a><span data-ttu-id="41284-102">ICorDebugRegisterSet::SetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="41284-102">ICorDebugRegisterSet::SetThreadContext Method</span></span>
<span data-ttu-id="41284-103">`SetThreadContext` n’est pas implémentée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="41284-103">`SetThreadContext` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="41284-104">N’appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="41284-104">Do not call this method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="41284-105">Utilisez le niveau supérieur de l’opération [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) pour définir le contexte d’un thread.</span><span class="sxs-lookup"><span data-stu-id="41284-105">Use the higher-level operation [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) to set the context of a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41284-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41284-106">Syntax</span></span>  
  
```  
HRESULT SetThreadContext (  
    [in] ULONG32 contextSize,  
    [in, length_is(contextSize),  
         size_is(contextSize)] BYTE context[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="41284-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41284-107">Requirements</span></span>  
 <span data-ttu-id="41284-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41284-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41284-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="41284-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="41284-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="41284-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="41284-111">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="41284-111">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41284-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41284-112">See Also</span></span>  
 [<span data-ttu-id="41284-113">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="41284-113">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)  
 [<span data-ttu-id="41284-114">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="41284-114">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
