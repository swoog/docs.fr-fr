---
title: ICorDebugValue::GetAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetAddress
helpviewer_keywords:
- ICorDebugValue::GetAddress method [.NET Framework debugging]
- GetAddress method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: a247c792-45e1-4538-9e1f-b46acca4a463
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6f8a9c62a1be682d3f0259c27f311e2dcbb2f11
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57492723"
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="1b841-102">ICorDebugValue::GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="1b841-102">ICorDebugValue::GetAddress Method</span></span>
<span data-ttu-id="1b841-103">Obtient l’adresse de cet objet « ICorDebugValue », qui est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="1b841-103">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b841-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b841-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1b841-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b841-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="1b841-106">[out] Pointeur vers un `CORDB_ADDRESS` objet qui spécifie l’adresse de cet objet de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b841-106">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1b841-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1b841-107">Remarks</span></span>  
 <span data-ttu-id="1b841-108">Si la valeur n’est pas disponible, 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="1b841-108">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="1b841-109">Cela peut se produire si la valeur est au moins en partie dans les registres ou stockées dans un handle du RÉCUPÉRATEUR de mémoire (`GCHandle`).</span><span class="sxs-lookup"><span data-stu-id="1b841-109">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b841-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1b841-110">Requirements</span></span>  
 <span data-ttu-id="1b841-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b841-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b841-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1b841-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1b841-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1b841-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1b841-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b841-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b841-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b841-115">See also</span></span>

