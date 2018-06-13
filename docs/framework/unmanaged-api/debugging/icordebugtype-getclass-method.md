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
ms.openlocfilehash: ff2258faa8bc766c8c769f4e135f868334516b96
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422557"
---
# <a name="icordebugtypegetclass-method"></a><span data-ttu-id="5e7da-102">ICorDebugType::GetClass, méthode</span><span class="sxs-lookup"><span data-stu-id="5e7da-102">ICorDebugType::GetClass Method</span></span>
<span data-ttu-id="5e7da-103">Obtient un pointeur d’interface ICorDebugClass qui représente le type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="5e7da-103">Gets an interface pointer to an ICorDebugClass that represents the uninstantiated generic type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e7da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e7da-104">Syntax</span></span>  
  
```  
HRESULT GetClass (  
    [out] ICorDebugClass   **ppClass  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5e7da-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e7da-105">Parameters</span></span>  
 `ppClass`  
 <span data-ttu-id="5e7da-106">[out] Un pointeur vers l’adresse d’un `ICorDebugClass` interface qui représente le type générique non instancié.</span><span class="sxs-lookup"><span data-stu-id="5e7da-106">[out] A pointer to the address of an `ICorDebugClass` interface that represents the uninstantiated generic type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5e7da-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5e7da-107">Remarks</span></span>  
 <span data-ttu-id="5e7da-108">`GetClass` peut être appelée uniquement sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="5e7da-108">`GetClass` can be called only under certain conditions.</span></span> <span data-ttu-id="5e7da-109">Appelez [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) avant d’appeler `GetClass`.</span><span class="sxs-lookup"><span data-stu-id="5e7da-109">Call [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) before calling `GetClass`.</span></span> <span data-ttu-id="5e7da-110">Si `ICorDebugType::GetType` retourne une valeur CorElementType ELEMENT_TYPE_CLASS ou ELEMENT_TYPE_VALUETYPE, `GetClass` peut être appelée pour obtenir le type non instancié pour un type générique.</span><span class="sxs-lookup"><span data-stu-id="5e7da-110">If `ICorDebugType::GetType` returns a CorElementType value that is ELEMENT_TYPE_CLASS or ELEMENT_TYPE_VALUETYPE, `GetClass` can be called to get the uninstantiated type for a generic type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e7da-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e7da-111">Requirements</span></span>  
 <span data-ttu-id="5e7da-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5e7da-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5e7da-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5e7da-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5e7da-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5e7da-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5e7da-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5e7da-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
