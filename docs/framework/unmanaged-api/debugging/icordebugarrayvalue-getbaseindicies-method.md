---
title: ICorDebugArrayValue::GetBaseIndicies, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetBaseIndicies
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetBaseIndicies
helpviewer_keywords:
- ICorDebugArrayValue::GetBaseIndicies method [.NET Framework debugging]
- GetBaseIndicies method [.NET Framework debugging]
ms.assetid: 868b339b-acdb-4fe0-91c7-b85f4fba99eb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f24a1434f737e8281a0c68dd09d2e17b34371694
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471652"
---
# <a name="icordebugarrayvaluegetbaseindicies-method"></a><span data-ttu-id="82e4e-102">ICorDebugArrayValue::GetBaseIndicies, méthode</span><span class="sxs-lookup"><span data-stu-id="82e4e-102">ICorDebugArrayValue::GetBaseIndicies Method</span></span>
<span data-ttu-id="82e4e-103">Obtient l’index de base de chaque dimension dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="82e4e-103">Gets the base index of each dimension in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82e4e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82e4e-104">Syntax</span></span>  
  
```  
HRESULT GetBaseIndicies (  
    [in] ULONG32          cdim,  
    [out, size_is(cdim), length_is(cdim)]   
        ULONG32           indicies[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="82e4e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82e4e-105">Parameters</span></span>  
 `cdim`  
 <span data-ttu-id="82e4e-106">[in] Le nombre de dimensions de ce `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="82e4e-106">[in] The number of dimensions of this `ICorDebugArrayValue` object.</span></span> <span data-ttu-id="82e4e-107">Cette valeur est également la taille de la `indicies` tableau car sa taille est égale au nombre de dimensions de la `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="82e4e-107">This value is also the size of the `indicies` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `indicies`  
 <span data-ttu-id="82e4e-108">[out] Tableau d’entiers, chacun d’eux est l’index de base (autrement dit, l’index de départ) d’une dimension de ce `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="82e4e-108">[out] An array of integers, each of which is the base index (that is, the starting index) of a dimension of this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82e4e-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82e4e-109">Requirements</span></span>  
 <span data-ttu-id="82e4e-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82e4e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82e4e-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="82e4e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="82e4e-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="82e4e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="82e4e-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82e4e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
