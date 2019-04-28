---
title: ICorDebugHeapValue::IsValid, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue.IsValid
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue::IsValid
helpviewer_keywords:
- IsValid method [.NET Framework debugging]
- ICorDebugHeapValue::IsValid method [.NET Framework debugging]
ms.assetid: 68e20e62-203d-46d8-bb91-8d3c61cfacc3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e1edb1d25a62a9a689c397339740e563d986c8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61700225"
---
# <a name="icordebugheapvalueisvalid-method"></a><span data-ttu-id="50da8-102">ICorDebugHeapValue::IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="50da8-102">ICorDebugHeapValue::IsValid Method</span></span>
<span data-ttu-id="50da8-103">Obtient une valeur qui indique si l’objet représenté par ICorDebugHeapValue est valide.</span><span class="sxs-lookup"><span data-stu-id="50da8-103">Gets a value that indicates whether the object represented by this ICorDebugHeapValue is valid.</span></span>  
  
 <span data-ttu-id="50da8-104">Cette méthode a été déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="50da8-104">This method has been deprecated in the .NET Framework version 2.0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50da8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50da8-105">Syntax</span></span>  
  
```  
HRESULT IsValid (  
    [out] BOOL    *pbValid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="50da8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50da8-106">Parameters</span></span>  
 `pbValid`  
 <span data-ttu-id="50da8-107">[out] Pointeur vers une valeur booléenne qui indique si cette valeur sur le tas est valide.</span><span class="sxs-lookup"><span data-stu-id="50da8-107">[out] A pointer to a Boolean value that indicates whether this value on the heap is valid.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="50da8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="50da8-108">Remarks</span></span>  
 <span data-ttu-id="50da8-109">La valeur n’est pas valide si elle a été récupérée par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="50da8-109">The value is invalid if it has been reclaimed by the garbage collector.</span></span>  
  
 <span data-ttu-id="50da8-110">Cette méthode est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="50da8-110">This method has been deprecated.</span></span> <span data-ttu-id="50da8-111">Dans le .NET Framework 2.0, toutes les valeurs sont valides jusqu'à ce que [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) est appelée, à quel moment les valeurs sont invalidés.</span><span class="sxs-lookup"><span data-stu-id="50da8-111">In the .NET Framework 2.0, all values are valid until [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) is called, at which time the values are invalidated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50da8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50da8-112">Requirements</span></span>  
 <span data-ttu-id="50da8-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50da8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50da8-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="50da8-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="50da8-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50da8-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="50da8-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50da8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
