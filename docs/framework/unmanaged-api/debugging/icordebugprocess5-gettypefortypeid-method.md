---
title: ICorDebugProcess5::GetTypeForTypeID, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetTypeForTypeID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeForTypeID
helpviewer_keywords:
- GetTypeForTypeID method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetTypeForTypeID method [.NET Framework debugging]
ms.assetid: e0eed5a8-fa6d-4818-bd00-7babcea30325
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3b5800890a5dfaef40225616f1d661a8e37ed4d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54661098"
---
# <a name="icordebugprocess5gettypefortypeid-method"></a><span data-ttu-id="fe287-102">ICorDebugProcess5::GetTypeForTypeID, méthode</span><span class="sxs-lookup"><span data-stu-id="fe287-102">ICorDebugProcess5::GetTypeForTypeID Method</span></span>
<span data-ttu-id="fe287-103">Convertit un identificateur de type valeur ICorDebugType.</span><span class="sxs-lookup"><span data-stu-id="fe287-103">Converts a type identifier to an ICorDebugType value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe287-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe287-104">Syntax</span></span>  
  
```  
HRESULT GetTypeForTypeID(  
    [in] COR_TYPEID id, [  
    out] ICorDebugType **ppType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe287-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe287-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="fe287-106">[in] L’identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="fe287-106">[in] The type identifier.</span></span>  
  
 `ppType`  
 <span data-ttu-id="fe287-107">[out] Pointeur vers l’adresse d’un objet de ICorDebugType.</span><span class="sxs-lookup"><span data-stu-id="fe287-107">[out] A pointer to the address of an ICorDebugType object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fe287-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fe287-108">Remarks</span></span>  
 <span data-ttu-id="fe287-109">Dans certains cas, les méthodes qui retournent un identificateur de type peuvent retourner une valeur null `COR_TYPEID` valeur.</span><span class="sxs-lookup"><span data-stu-id="fe287-109">In some cases, methods that return a type identifier may return a null `COR_TYPEID` value.</span></span> <span data-ttu-id="fe287-110">Si cette valeur est passée en tant que le `id` argument, le `GetTypeForTypeID` méthode échouent et retournent `E_FAIL`.</span><span class="sxs-lookup"><span data-stu-id="fe287-110">If this value is passed as the `id` argument, the `GetTypeForTypeID` method will fail and return `E_FAIL`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe287-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe287-111">Requirements</span></span>  
 <span data-ttu-id="fe287-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe287-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe287-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fe287-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fe287-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fe287-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fe287-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe287-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe287-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe287-116">See also</span></span>
- [<span data-ttu-id="fe287-117">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="fe287-117">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="fe287-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="fe287-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
