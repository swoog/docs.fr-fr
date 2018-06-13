---
title: ICorDebugValue::GetType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetType
helpviewer_keywords:
- ICorDebugValue::GetType method [.NET Framework debugging]
- GetType method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: 41e2d503-e1f1-407b-abe0-6a29adb3e0d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0fc0dd03abc1adb8eeea76a1053fb4d58de4ecf8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419830"
---
# <a name="icordebugvaluegettype-method"></a><span data-ttu-id="b0857-102">ICorDebugValue::GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="b0857-102">ICorDebugValue::GetType Method</span></span>
<span data-ttu-id="b0857-103">Obtient le type primitif de cet objet « ICorDebugValue ».</span><span class="sxs-lookup"><span data-stu-id="b0857-103">Gets the primitive type of this "ICorDebugValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0857-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0857-104">Syntax</span></span>  
  
```  
HRESULT GetType (  
    [out] CorElementType   *pType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b0857-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0857-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="b0857-106">[out] Pointeur vers une valeur de l’énumération « CorElementType » qui indique le type de valeur.</span><span class="sxs-lookup"><span data-stu-id="b0857-106">[out] A pointer to a value of the "CorElementType" enumeration that indicates the value's type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b0857-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b0857-107">Remarks</span></span>  
 <span data-ttu-id="b0857-108">Si l’objet est un type d’exécution complexe, ce type peut être examiné via les sous-classes appropriées de le `ICorDebugValue` interface.</span><span class="sxs-lookup"><span data-stu-id="b0857-108">If the object is a complex run-time type, that type may be examined through the appropriate subclasses of the `ICorDebugValue` interface.</span></span> <span data-ttu-id="b0857-109">Par exemple, « ICorDebugObjectValue » qui hérite de `ICorDebugValue`, représente un type complexe.</span><span class="sxs-lookup"><span data-stu-id="b0857-109">For example, "ICorDebugObjectValue", which inherits from `ICorDebugValue`, represents a complex type.</span></span>  
  
 <span data-ttu-id="b0857-110">Le `GetType` et [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) méthodes retournent des informations sur le type d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="b0857-110">The `GetType` and [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) methods each return information about the type of a value.</span></span> <span data-ttu-id="b0857-111">Les deux sont remplacées par les compatible avec les génériques [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b0857-111">They are both superseded by the generics-aware [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0857-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b0857-112">Requirements</span></span>  
 <span data-ttu-id="b0857-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b0857-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0857-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b0857-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b0857-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b0857-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b0857-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0857-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0857-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0857-117">See Also</span></span>  
 
