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
ms.openlocfilehash: fc095b2c9f546e8b75d4330024c8c593f7ada8b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404769"
---
# <a name="icordebuggetprocess-method"></a><span data-ttu-id="e3517-102">ICorDebug::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="e3517-102">ICorDebug::GetProcess Method</span></span>
<span data-ttu-id="e3517-103">Obtient un pointeur vers l’instance « ICorDebugProcess » pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3517-103">Gets a pointer to the "ICorDebugProcess" instance for the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3517-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3517-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [in] DWORD               dwProcessId,  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e3517-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3517-105">Parameters</span></span>  
 `dwProcessId`  
 <span data-ttu-id="e3517-106">[in] L’ID du processus.</span><span class="sxs-lookup"><span data-stu-id="e3517-106">[in] The ID of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="e3517-107">[out] Un pointeur vers l’adresse d’un `ICorDebugProcess` instance pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="e3517-107">[out] A pointer to the address of a `ICorDebugProcess` instance for the specified process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3517-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3517-108">Requirements</span></span>  
 <span data-ttu-id="e3517-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3517-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3517-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e3517-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e3517-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e3517-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e3517-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3517-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3517-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3517-113">See Also</span></span>  
 [<span data-ttu-id="e3517-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="e3517-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
