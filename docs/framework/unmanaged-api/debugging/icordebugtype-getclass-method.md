---
title: ICorDebugType::GetClass, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetClass
helpviewer_keywords:
- ICorDebugType::GetClass method [.NET Framework debugging]
- GetClass method, ICorDebugType interface [.NET Framework debugging]
ms.assetid: 2644f48b-db3c-429f-ae62-76f1c98a1af5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0915027ce6a3768ff854eafc5496c5057081cc4d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499535"
---
# <a name="icordebugtypegetclass-method"></a><span data-ttu-id="fba99-102">ICorDebugType::GetClass, méthode</span><span class="sxs-lookup"><span data-stu-id="fba99-102">ICorDebugType::GetClass Method</span></span>
<span data-ttu-id="fba99-103">Obtient un pointeur d’interface ICorDebugClass qui représente le type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="fba99-103">Gets an interface pointer to an ICorDebugClass that represents the uninstantiated generic type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fba99-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba99-104">Syntax</span></span>  
  
```  
HRESULT GetClass (  
    [out] ICorDebugClass   **ppClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fba99-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fba99-105">Parameters</span></span>  
 `ppClass`  
 <span data-ttu-id="fba99-106">[out] Un pointeur vers l’adresse d’un `ICorDebugClass` interface qui représente le type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="fba99-106">[out] A pointer to the address of an `ICorDebugClass` interface that represents the uninstantiated generic type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fba99-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fba99-107">Remarks</span></span>  
 <span data-ttu-id="fba99-108">`GetClass` peut être appelée uniquement sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="fba99-108">`GetClass` can be called only under certain conditions.</span></span> <span data-ttu-id="fba99-109">Appelez [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) avant d’appeler `GetClass`.</span><span class="sxs-lookup"><span data-stu-id="fba99-109">Call [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) before calling `GetClass`.</span></span> <span data-ttu-id="fba99-110">Si `ICorDebugType::GetType` retourne une valeur CorElementType ELEMENT_TYPE_CLASS ou ELEMENT_TYPE_VALUETYPE, `GetClass` peut être appelée pour obtenir le type non instancié pour un type générique.</span><span class="sxs-lookup"><span data-stu-id="fba99-110">If `ICorDebugType::GetType` returns a CorElementType value that is ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE, `GetClass` can be called to get the uninstantiated type for a generic type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fba99-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fba99-111">Requirements</span></span>  
 <span data-ttu-id="fba99-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fba99-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fba99-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fba99-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fba99-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fba99-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fba99-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fba99-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
