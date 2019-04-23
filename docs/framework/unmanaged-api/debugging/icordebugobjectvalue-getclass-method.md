---
title: ICorDebugObjectValue::GetClass, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugObjectValue.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugObjectValue::GetClass
helpviewer_keywords:
- ICorDebugObjectValue::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugObjectValue interface [.NET Framework debugging]
ms.assetid: 5be25292-8357-445f-a09b-f997c0de761c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06e9c7af1c4a769bfb45a8e9f805d97b3bad94aa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174185"
---
# <a name="icordebugobjectvaluegetclass-method"></a><span data-ttu-id="be3af-102">ICorDebugObjectValue::GetClass, méthode</span><span class="sxs-lookup"><span data-stu-id="be3af-102">ICorDebugObjectValue::GetClass Method</span></span>
<span data-ttu-id="be3af-103">Obtient la classe de valeur de cet objet.</span><span class="sxs-lookup"><span data-stu-id="be3af-103">Gets the class of this object value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be3af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be3af-104">Syntax</span></span>  
  
```  
HRESULT GetClass (  
    [out] ICorDebugClass     **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be3af-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be3af-105">Parameters</span></span>  
 `ppClass`  
 <span data-ttu-id="be3af-106">[out] Pointeur vers l’adresse d’un objet « ICorDebugClass » qui représente la classe de la valeur de l’objet représentée par cet objet « ICorDebugObjectValue ».</span><span class="sxs-lookup"><span data-stu-id="be3af-106">[out] A pointer to the address of an "ICorDebugClass" object that represents the class of the object value represented by this "ICorDebugObjectValue" object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="be3af-107">Notes</span><span class="sxs-lookup"><span data-stu-id="be3af-107">Remarks</span></span>  
 <span data-ttu-id="be3af-108">Le `GetClass` et [ICorDebugValue::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) méthodes retournent des informations sur le type d’une valeur ; elles sont remplacées à la fois par le compatible avec les génériques [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md).</span><span class="sxs-lookup"><span data-stu-id="be3af-108">The `GetClass` and [ICorDebugValue::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md) methods each return information about the type of a value; they are both superseded by the generics-aware [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be3af-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be3af-109">Requirements</span></span>  
 <span data-ttu-id="be3af-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="be3af-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be3af-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="be3af-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="be3af-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be3af-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be3af-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be3af-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be3af-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be3af-114">See also</span></span>
