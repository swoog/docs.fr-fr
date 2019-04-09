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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59169791"
---
# <a name="icordebuggetprocess-method"></a><span data-ttu-id="b9409-102">ICorDebug::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="b9409-102">ICorDebug::GetProcess Method</span></span>
<span data-ttu-id="b9409-103">Obtient un pointeur vers l’instance « ICorDebugProcess » pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9409-103">Gets a pointer to the "ICorDebugProcess" instance for the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9409-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9409-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [in] DWORD               dwProcessId,  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b9409-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9409-105">Parameters</span></span>  
 `dwProcessId`  
 <span data-ttu-id="b9409-106">[in] ID du processus.</span><span class="sxs-lookup"><span data-stu-id="b9409-106">[in] The ID of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="b9409-107">[out] Un pointeur vers l’adresse d’un `ICorDebugProcess` instance pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="b9409-107">[out] A pointer to the address of a `ICorDebugProcess` instance for the specified process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b9409-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9409-108">Requirements</span></span>  
 <span data-ttu-id="b9409-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9409-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9409-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b9409-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b9409-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b9409-111">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="b9409-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b9409-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b9409-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9409-113">See also</span></span>

- [<span data-ttu-id="b9409-114">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="b9409-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
