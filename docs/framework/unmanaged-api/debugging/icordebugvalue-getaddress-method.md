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
ms.openlocfilehash: 8c0fa19841580c7cfe8902577c3f756712a35893
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420653"
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="cc6a6-102">ICorDebugValue::GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="cc6a6-102">ICorDebugValue::GetAddress Method</span></span>
<span data-ttu-id="cc6a6-103">Obtient l’adresse de cet objet « ICorDebugValue », qui est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="cc6a6-103">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc6a6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc6a6-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cc6a6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc6a6-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="cc6a6-106">[out] Pointeur vers un `CORDB_ADDRESS` objet qui spécifie l’adresse de cet objet de valeur.</span><span class="sxs-lookup"><span data-stu-id="cc6a6-106">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc6a6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cc6a6-107">Remarks</span></span>  
 <span data-ttu-id="cc6a6-108">Si la valeur n’est pas disponible, 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="cc6a6-108">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="cc6a6-109">Cela peut se produire si la valeur est au moins en partie dans les registres ou stockées dans un handle de garbage collector (`GCHandle`).</span><span class="sxs-lookup"><span data-stu-id="cc6a6-109">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc6a6-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cc6a6-110">Requirements</span></span>  
 <span data-ttu-id="cc6a6-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc6a6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc6a6-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cc6a6-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cc6a6-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc6a6-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cc6a6-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc6a6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc6a6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc6a6-115">See Also</span></span>  
 
