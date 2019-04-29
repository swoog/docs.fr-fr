---
title: ICorDebugAssembly2::IsFullyTrusted, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly2.IsFullyTrusted
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly2::IsFullyTrusted
helpviewer_keywords:
- ICorDebugAssembly2::IsFullyTrusted method [.NET Framework debugging]
- IsFullyTrusted method [.NET Framework debugging]
ms.assetid: 26cbd27d-12bf-444a-8197-ccd14d37dda3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd3b977a894f8cb1fc9a866f5a43265d917db513
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645563"
---
# <a name="icordebugassembly2isfullytrusted-method"></a><span data-ttu-id="d090c-102">ICorDebugAssembly2::IsFullyTrusted, méthode</span><span class="sxs-lookup"><span data-stu-id="d090c-102">ICorDebugAssembly2::IsFullyTrusted Method</span></span>
<span data-ttu-id="d090c-103">Obtient une valeur qui indique si l’assembly a été accordé une confiance totale par le système de sécurité du runtime.</span><span class="sxs-lookup"><span data-stu-id="d090c-103">Gets a value that indicates whether the assembly has been granted full trust by the runtime security system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d090c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d090c-104">Syntax</span></span>  
  
```  
HRESULT IsFullyTrusted(  
    [out] BOOL *pbFullyTrusted  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d090c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d090c-105">Parameters</span></span>  
 `pbFullyTrusted`  
 <span data-ttu-id="d090c-106">[out] `true` si l’assembly a été accordé une confiance totale par le système de sécurité du runtime ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="d090c-106">[out] `true` if the assembly has been granted full trust by the runtime security system; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d090c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d090c-107">Remarks</span></span>  
 <span data-ttu-id="d090c-108">Cette méthode retourne un HRESULT de CORDBG_E_NOTREADY si la stratégie de sécurité pour l’assembly n'a pas encore été résolue, autrement dit, si aucun code dans l’assembly a encore été exécuté.</span><span class="sxs-lookup"><span data-stu-id="d090c-108">This method returns an HRESULT of CORDBG_E_NOTREADY if the security policy for the assembly has not yet been resolved, that is, if no code in the assembly has been run yet.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d090c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d090c-109">Requirements</span></span>  
 <span data-ttu-id="d090c-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d090c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d090c-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d090c-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d090c-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d090c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d090c-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d090c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
