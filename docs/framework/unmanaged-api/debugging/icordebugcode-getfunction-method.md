---
title: ICorDebugCode::GetFunction, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetFunction method [.NET Framework debugging]
ms.assetid: c568b737-fdb2-4816-accd-051f5ab760f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0104a52c3aa206f86daff30d9d16298e6beae324
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099454"
---
# <a name="icordebugcodegetfunction-method"></a><span data-ttu-id="433c4-102">ICorDebugCode::GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="433c4-102">ICorDebugCode::GetFunction Method</span></span>
<span data-ttu-id="433c4-103">Obtient le « ICorDebugFunction « associée « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="433c4-103">Gets the "ICorDebugFunction" associated with this "ICorDebugCode".</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="433c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="433c4-104">Syntax</span></span>  
  
```  
HRESULT GetFunction (  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="433c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="433c4-105">Parameters</span></span>  
 `ppFunction`  
 <span data-ttu-id="433c4-106">[out] Pointeur vers l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="433c4-106">[out] A pointer to the address of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="433c4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="433c4-107">Remarks</span></span>  
 `ICorDebugCode` <span data-ttu-id="433c4-108">et `ICorDebugFunction` maintenir une relation un à un.</span><span class="sxs-lookup"><span data-stu-id="433c4-108">and `ICorDebugFunction` maintain a one-to-one relationship.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="433c4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="433c4-109">Requirements</span></span>  
 <span data-ttu-id="433c4-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="433c4-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="433c4-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="433c4-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="433c4-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="433c4-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="433c4-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="433c4-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="433c4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="433c4-114">See also</span></span>
