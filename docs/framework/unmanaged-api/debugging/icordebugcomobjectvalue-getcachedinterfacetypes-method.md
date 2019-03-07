---
title: ICorDebugComObjectValue::GetCachedInterfaceTypes, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
api_location:
- mscordbi.dll
f1_keywords:
- ICorDebugComObjectValue::GetCachedInterfaceTypes
helpviewer_keywords:
- GetCachedInterface method, ICorDebugComObjectValue interface [.NET Framework debugging]
- ICorDebugComObjectValue::GetCachedInterface method [.NET Framework debugging]
ms.assetid: d492284f-d3c5-4614-adb8-d718d5042500
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 60a74b3c90c11f799f5b9738e84d33b603f0ef04
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485471"
---
# <a name="icordebugcomobjectvaluegetcachedinterfacetypes-method"></a><span data-ttu-id="daa97-102">ICorDebugComObjectValue::GetCachedInterfaceTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="daa97-102">ICorDebugComObjectValue::GetCachedInterfaceTypes Method</span></span>
<span data-ttu-id="daa97-103">Fournit un énumérateur pour les types d’interface que l’objet actuel a été converti en ou utilisé en tant que.</span><span class="sxs-lookup"><span data-stu-id="daa97-103">Provides an enumerator for the interface types that the current object has been cast to or used as.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="daa97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daa97-104">Syntax</span></span>  
  
```  
HRESULT GetCachedInterfaceTypes(  
    [in] BOOL bIInspectableOnly,  
    [out] ICorDebugTypeEnum **ppInterfacesEnum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="daa97-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daa97-105">Parameters</span></span>  
 `bIInspectableOnly`  
 <span data-ttu-id="daa97-106">[in] Une valeur qui indique si la méthode retourne uniquement [!INCLUDE[wrt](../../../../includes/wrt-md.md)] interfaces (`IInspectable` interfaces) ou des interfaces COM mis en cache par le runtime callable wrapper RCW ().</span><span class="sxs-lookup"><span data-stu-id="daa97-106">[in] A value that indicates whether the method returns only [!INCLUDE[wrt](../../../../includes/wrt-md.md)] interfaces (`IInspectable` interfaces) or all COM interfaces cached by the runtime callable wrapper (RCW).</span></span>  
  
 `ppInterfacesEnum`  
 <span data-ttu-id="daa97-107">[out] Un pointeur vers l’adresse d’un énumérateur ICorDebugTypeEnum qui fournit l’accès aux objets de ICorDebugType qui représentent des types d’interface mis en cache est filtrée en fonction de `bIInspectableOnly`.</span><span class="sxs-lookup"><span data-stu-id="daa97-107">[out] A pointer to the address of an ICorDebugTypeEnum enumerator that provides access to ICorDebugType objects that represent cached interface types filtered according to `bIInspectableOnly`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="daa97-108">Notes</span><span class="sxs-lookup"><span data-stu-id="daa97-108">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="daa97-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="daa97-109">Requirements</span></span>  
 <span data-ttu-id="daa97-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="daa97-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="daa97-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="daa97-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="daa97-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="daa97-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="daa97-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="daa97-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="daa97-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daa97-114">See also</span></span>
- [<span data-ttu-id="daa97-115">ICorDebugComObjectValue, interface</span><span class="sxs-lookup"><span data-stu-id="daa97-115">ICorDebugComObjectValue Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcomobjectvalue-interface.md)
- [<span data-ttu-id="daa97-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="daa97-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
