---
title: ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypesForIIDs
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs method, [.NET Framework debugging]
- GetCachedWinRTTypesForIIDs method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 23682ca0-1bcf-48e6-996e-69f7ba337682
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ed1d7ad95b7c8474121994d0f54557c1c36cb531
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095124"
---
# <a name="icordebugappdomain3getcachedwinrttypesforiids-method"></a><span data-ttu-id="3e914-102">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs, méthode</span><span class="sxs-lookup"><span data-stu-id="3e914-102">ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs Method</span></span>
<span data-ttu-id="3e914-103">Obtient un énumérateur pour la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types dans un domaine d’application basés sur leurs identificateurs de l’interface.</span><span class="sxs-lookup"><span data-stu-id="3e914-103">Gets an enumerator for cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types in an application domain based on their interface identifiers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e914-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e914-104">Syntax</span></span>  
  
```  
HRESULT GetCachedWinRTTypesForIIDs (   
    [in]  ULONG32            cReqTypes,  
    [in]  GUID                *iidsToResolve,  
    [out] ICorDebugTypeEnum   **ppTypesEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e914-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e914-105">Parameters</span></span>  
 `cReqTypes`  
 <span data-ttu-id="3e914-106">[in] Le nombre de types requis.</span><span class="sxs-lookup"><span data-stu-id="3e914-106">[in] The number of required types.</span></span>  
  
 `iidsToResolve`  
 <span data-ttu-id="3e914-107">[in] Un pointeur vers un tableau qui contient les identificateurs d’interface correspondant à des représentations managées de le [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types à récupérer.</span><span class="sxs-lookup"><span data-stu-id="3e914-107">[in] A pointer to an array that contains the interface identifiers corresponding to the managed representations of the [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types to be retrieved.</span></span>  
  
 `ppTypesEnum`  
 <span data-ttu-id="3e914-108">[out] Un pointeur vers l’adresse d’un objet d’interface « ICorDebugTypeEnum » qui permet l’énumération de la mise en cache géré les représentations sous forme de la [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types récupérés, basé sur les identificateurs d’interface dans `iidsToResolve`.</span><span class="sxs-lookup"><span data-stu-id="3e914-108">[out] A pointer to the address of an "ICorDebugTypeEnum" interface object that allows enumeration of the cached managed representations of the [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types retrieved, based on the interface identifiers in `iidsToResolve`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3e914-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3e914-109">Remarks</span></span>  
 <span data-ttu-id="3e914-110">Si la méthode ne parvient pas à récupérer des informations pour un identificateur d’interface spécifique, l’entrée correspondante dans la collection « ICorDebugTypeEnum » est d’un type de `ELEMENT_TYPE_END` pour les erreurs en raison de problèmes de récupération des données, ou `ELEMENT_TYPE_VOID` pour interface inconnue identificateurs.</span><span class="sxs-lookup"><span data-stu-id="3e914-110">If the method fails to retrieve information for a specific interface identifier, the corresponding entry in the "ICorDebugTypeEnum" collection will have a type of `ELEMENT_TYPE_END` for errors due to data retrieval issues, or `ELEMENT_TYPE_VOID` for unknown interface identifiers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e914-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e914-111">Requirements</span></span>  
 <span data-ttu-id="3e914-112">**Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e914-112">**Platforms:** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]</span></span>  
  
 <span data-ttu-id="3e914-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3e914-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3e914-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3e914-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3e914-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e914-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e914-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e914-116">See also</span></span>

- [<span data-ttu-id="3e914-117">ICorDebugAppDomain3, interface</span><span class="sxs-lookup"><span data-stu-id="3e914-117">ICorDebugAppDomain3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-interface.md)
