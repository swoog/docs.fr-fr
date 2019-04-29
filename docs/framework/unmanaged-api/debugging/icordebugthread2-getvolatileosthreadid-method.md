---
title: ICorDebugThread2::GetVolatileOSThreadID, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetVolatileOSThreadID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetVolatileOSThreadID
helpviewer_keywords:
- GetVolatileOSThreadID method [.NET Framework debugging]
- ICorDebugThread2::GetVolatileOSThreadID method [.NET Framework debugging]
ms.assetid: f0922545-c2cf-40c8-9ef6-ca033563e682
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a9bf96371798b38bc392bc6bbd8f6fe8f97c7969
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946304"
---
# <a name="icordebugthread2getvolatileosthreadid-method"></a><span data-ttu-id="d8bde-102">ICorDebugThread2::GetVolatileOSThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bde-102">ICorDebugThread2::GetVolatileOSThreadID Method</span></span>
<span data-ttu-id="d8bde-103">Obtient l’identificateur de thread de système d’exploitation pour ICorDebugThread2.</span><span class="sxs-lookup"><span data-stu-id="d8bde-103">Gets the operating system thread identifier for this ICorDebugThread2.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8bde-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8bde-104">Syntax</span></span>  
  
```  
HRESULT GetVolatileOSThreadID (  
    [out] DWORD    *pdwTid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8bde-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8bde-105">Parameters</span></span>  
 `pdwTid`  
 <span data-ttu-id="d8bde-106">[out] L’identificateur de thread de système d’exploitation pour ce thread.</span><span class="sxs-lookup"><span data-stu-id="d8bde-106">[out] The operating system thread identifier for this thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8bde-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8bde-107">Requirements</span></span>  
 <span data-ttu-id="d8bde-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8bde-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8bde-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8bde-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8bde-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8bde-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8bde-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8bde-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
