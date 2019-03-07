---
title: ICorDebugProcess5::EnumerateGCReferences, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateGCReferences
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateGCReferences
helpviewer_keywords:
- EnumerateGCReferences method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateGCReferences method [.NET Framework debugging]
ms.assetid: 86c397c3-81d8-463e-a248-3cbe06c44d9d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 54e2648765d896c189cc2deb5590a0a2a9b3f410
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57476480"
---
# <a name="icordebugprocess5enumerategcreferences-method"></a><span data-ttu-id="40e3f-102">ICorDebugProcess5::EnumerateGCReferences, méthode</span><span class="sxs-lookup"><span data-stu-id="40e3f-102">ICorDebugProcess5::EnumerateGCReferences Method</span></span>
<span data-ttu-id="40e3f-103">Obtient un énumérateur pour tous les objets qui doivent être nettoyées dans un processus.</span><span class="sxs-lookup"><span data-stu-id="40e3f-103">Gets an enumerator for all objects that are to be garbage-collected in a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40e3f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40e3f-104">Syntax</span></span>  
  
```  
HRESULT EnumerateGCReferences(  
    [in] Bool enumerateWeakReferences,   
    [out] ICorDebugGCReferenceEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="40e3f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40e3f-105">Parameters</span></span>  
 `enumerateWeakReferences`  
 <span data-ttu-id="40e3f-106">[in] Une valeur booléenne qui indique si les références faibles doivent également être énumérés.</span><span class="sxs-lookup"><span data-stu-id="40e3f-106">[in] A Boolean value that indicates whether weak references are also to be enumerated.</span></span> <span data-ttu-id="40e3f-107">Si `enumerateWeakReferences` est `true`, le `ppEnum` énumérateur inclut des références fortes et les références faibles.</span><span class="sxs-lookup"><span data-stu-id="40e3f-107">If `enumerateWeakReferences` is `true`, the `ppEnum` enumerator includes both strong references and weak references.</span></span> <span data-ttu-id="40e3f-108">Si `enumerateWeakReferences` est `false`, l’énumérateur inclut uniquement les références fortes.</span><span class="sxs-lookup"><span data-stu-id="40e3f-108">If `enumerateWeakReferences` is `false`, the enumerator includes only strong references.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="40e3f-109">[out] Un pointeur vers l’adresse d’un [ICorDebugGCReferenceEnum](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-interface.md) qui est un énumérateur pour les objets d’être le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="40e3f-109">[out] A pointer to the address of an [ICorDebugGCReferenceEnum](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-interface.md) that is an enumerator for the objects to be garbage-collected.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="40e3f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="40e3f-110">Remarks</span></span>  
 <span data-ttu-id="40e3f-111">Cette méthode fournit un moyen de déterminer la chaîne racine complète pour n’importe quel objet géré dans un processus et peut être utilisée pour déterminer pourquoi un objet est toujours actif.</span><span class="sxs-lookup"><span data-stu-id="40e3f-111">This method provides a way to determine the full rooting chain for any managed object in a process and can be used to determine why an object is still alive.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="40e3f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="40e3f-112">Requirements</span></span>  
 <span data-ttu-id="40e3f-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="40e3f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40e3f-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="40e3f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="40e3f-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="40e3f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="40e3f-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="40e3f-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="40e3f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40e3f-117">See also</span></span>
- [<span data-ttu-id="40e3f-118">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="40e3f-118">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="40e3f-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="40e3f-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
