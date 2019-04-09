---
title: ICorDebugHeapValue3::GetThreadOwningMonitorLock, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3.GetThreadOwningMonitorLock
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3::GetThreadOwningMonitorLock
helpviewer_keywords:
- GetThreadOwningMonitorLock method [.NET Framework debugging]
- ICorDebugHeapValue3::GetThreadOwningMonitorLock method [.NET Framework debugging]
ms.assetid: e06fc19d-2cf4-4cad-81a3-137a68af8969
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1678f1de7c23387f028348dadbc7b61e2cdc035c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201427"
---
# <a name="icordebugheapvalue3getthreadowningmonitorlock-method"></a><span data-ttu-id="c88e8-102">ICorDebugHeapValue3::GetThreadOwningMonitorLock, méthode</span><span class="sxs-lookup"><span data-stu-id="c88e8-102">ICorDebugHeapValue3::GetThreadOwningMonitorLock Method</span></span>
<span data-ttu-id="c88e8-103">Retourne le thread managé qui possède le verrou du moniteur sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="c88e8-103">Returns the managed thread that owns the monitor lock on this object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c88e8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c88e8-104">Syntax</span></span>  
  
```  
HRESULT GetThreadOwningMonitorLock (  
    [out] ICorDebugThread   **ppThread,  
    [out] DWORD              *pAcquisitionCount  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c88e8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c88e8-105">Parameters</span></span>  
 `ppThread`  
 <span data-ttu-id="c88e8-106">[out] Le thread managé qui possède le verrou du moniteur sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="c88e8-106">[out] The managed thread that owns the monitor lock on this object.</span></span>  
  
 `pAcquisitionCount`  
 <span data-ttu-id="c88e8-107">[out] Le nombre de fois où que ce thread aurait pour libérer le verrou avant qu’il redevienne sans propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c88e8-107">[out] The number of times this thread would have to release the lock before it returns to being unowned.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c88e8-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c88e8-108">Return Value</span></span>  
 <span data-ttu-id="c88e8-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="c88e8-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="c88e8-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c88e8-110">HRESULT</span></span>|<span data-ttu-id="c88e8-111">Description</span><span class="sxs-lookup"><span data-stu-id="c88e8-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c88e8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c88e8-112">S_OK</span></span>|<span data-ttu-id="c88e8-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="c88e8-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="c88e8-114">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c88e8-114">S_FALSE</span></span>|<span data-ttu-id="c88e8-115">Aucun thread managé possède le verrou du moniteur sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="c88e8-115">No managed thread owns the monitor lock on this object.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="c88e8-116">Exceptions</span><span class="sxs-lookup"><span data-stu-id="c88e8-116">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c88e8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c88e8-117">Remarks</span></span>  
 <span data-ttu-id="c88e8-118">Si un thread managé possède le verrou du moniteur sur cet objet :</span><span class="sxs-lookup"><span data-stu-id="c88e8-118">If a managed thread owns the monitor lock on this object:</span></span>  
  
-   <span data-ttu-id="c88e8-119">La méthode retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="c88e8-119">The method returns S_OK.</span></span>  
  
-   <span data-ttu-id="c88e8-120">L’objet thread est valide jusqu'à ce que le thread se termine.</span><span class="sxs-lookup"><span data-stu-id="c88e8-120">The thread object is valid until the thread exits.</span></span>  
  
 <span data-ttu-id="c88e8-121">Si aucun thread managé ne possède le verrou du moniteur sur cet objet, `ppThread` et `pAcquisitionCount` sont identiques, et la méthode retourne S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="c88e8-121">If no managed thread owns the monitor lock on this object, `ppThread` and `pAcquisitionCount` are unchanged, and the method returns S_FALSE.</span></span>  
  
 <span data-ttu-id="c88e8-122">Si `ppThread` ou `pAcquisitionCount` n’est pas un pointeur valide, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="c88e8-122">If `ppThread` or `pAcquisitionCount` is not a valid pointer, the result is undefined.</span></span>  
  
 <span data-ttu-id="c88e8-123">Si une erreur se produit et il est impossible de déterminer qui, le cas échéant, le thread possède le verrou du moniteur sur cet objet, la méthode retourne un HRESULT qui indique un échec.</span><span class="sxs-lookup"><span data-stu-id="c88e8-123">If an error occurs such that it cannot be determined which, if any, thread owns the monitor lock on this object, the method returns an HRESULT that indicates failure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c88e8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c88e8-124">Requirements</span></span>  
 <span data-ttu-id="c88e8-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c88e8-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c88e8-126">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c88e8-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c88e8-127">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c88e8-127">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c88e8-128">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c88e8-128">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c88e8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c88e8-129">See also</span></span>

- [<span data-ttu-id="c88e8-130">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="c88e8-130">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="c88e8-131">Débogage</span><span class="sxs-lookup"><span data-stu-id="c88e8-131">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
