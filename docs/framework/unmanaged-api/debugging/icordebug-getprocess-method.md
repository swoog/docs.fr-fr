---
title: ICorDebug::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebug.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebug::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::GetProcess method [.NET Framework debugging]
ms.assetid: 10a40ba0-1b65-4721-bd11-cf12d57b280d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dcb869bed71be05e0450580b50dfa9f2a0fca525
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996292"
---
# <a name="icordebuggetprocess-method"></a><span data-ttu-id="d5015-102">ICorDebug::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="d5015-102">ICorDebug::GetProcess Method</span></span>
<span data-ttu-id="d5015-103">Obtient un pointeur vers l’instance « ICorDebugProcess » pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5015-103">Gets a pointer to the "ICorDebugProcess" instance for the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5015-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5015-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [in] DWORD               dwProcessId,  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5015-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5015-105">Parameters</span></span>  
 `dwProcessId`  
 <span data-ttu-id="d5015-106">[in] ID du processus.</span><span class="sxs-lookup"><span data-stu-id="d5015-106">[in] The ID of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="d5015-107">[out] Un pointeur vers l’adresse d’un `ICorDebugProcess` instance pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5015-107">[out] A pointer to the address of a `ICorDebugProcess` instance for the specified process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5015-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5015-108">Requirements</span></span>  
 <span data-ttu-id="d5015-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d5015-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5015-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d5015-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d5015-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5015-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d5015-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5015-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5015-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5015-113">See also</span></span>

- [<span data-ttu-id="d5015-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="d5015-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
