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
ms.openlocfilehash: ac550ee7b1d66612557b30d15c275c90cf09b8af
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59187329"
---
# <a name="icordebugvaluegetaddress-method"></a><span data-ttu-id="1b188-102">ICorDebugValue::GetAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="1b188-102">ICorDebugValue::GetAddress Method</span></span>
<span data-ttu-id="1b188-103">Obtient l’adresse de cet objet « ICorDebugValue », qui est en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="1b188-103">Gets the address of this "ICorDebugValue" object, which is in the process of being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b188-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b188-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1b188-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b188-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="1b188-106">[out] Pointeur vers un `CORDB_ADDRESS` objet qui spécifie l’adresse de cet objet de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b188-106">[out] Pointer to a `CORDB_ADDRESS` object that specifies the address of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1b188-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1b188-107">Remarks</span></span>  
 <span data-ttu-id="1b188-108">Si la valeur n’est pas disponible, 0 (zéro) est retournée.</span><span class="sxs-lookup"><span data-stu-id="1b188-108">If the value is unavailable, 0 (zero) is returned.</span></span> <span data-ttu-id="1b188-109">Cela peut se produire si la valeur est au moins en partie dans les registres ou stockées dans un handle du RÉCUPÉRATEUR de mémoire (`GCHandle`).</span><span class="sxs-lookup"><span data-stu-id="1b188-109">This could happen if the value is at least partly in registers or stored in a garbage collector handle (`GCHandle`).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b188-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b188-110">Requirements</span></span>  
 <span data-ttu-id="1b188-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b188-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b188-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1b188-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1b188-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1b188-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="1b188-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1b188-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1b188-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b188-115">See also</span></span>
