---
title: ICorDebugArrayValue::GetDimensions, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetDimensions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetDimensions
helpviewer_keywords:
- ICorDebugArrayValue::GetDimensions method [.NET Framework debugging]
- GetDimensions method [.NET Framework debugging]
ms.assetid: 6c116592-134b-4ef2-a319-680e92d013aa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a52075f33d594787c516f84b65b3319991380907
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645693"
---
# <a name="icordebugarrayvaluegetdimensions-method"></a><span data-ttu-id="3bc6f-102">ICorDebugArrayValue::GetDimensions, méthode</span><span class="sxs-lookup"><span data-stu-id="3bc6f-102">ICorDebugArrayValue::GetDimensions Method</span></span>
<span data-ttu-id="3bc6f-103">Obtient le nombre d’éléments dans chaque dimension de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-103">Gets the number of elements in each dimension of this array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3bc6f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bc6f-104">Syntax</span></span>  
  
```  
HRESULT GetDimensions (  
    [in] ULONG32         cdim,  
    [out, size_is(cdim), length_is(cdim)]   
        ULONG32          dims[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3bc6f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bc6f-105">Parameters</span></span>  
 `cdim`  
 <span data-ttu-id="3bc6f-106">[in] Le nombre de dimensions de cet objet ICorDebugArrayValue.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-106">[in] The number of dimensions of this ICorDebugArrayValue object.</span></span>  
  
 <span data-ttu-id="3bc6f-107">Cette valeur est également la taille de la `dims` tableau car sa taille est égale au nombre de dimensions de la `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-107">This value is also the size of the `dims` array because its size is equal to the number of dimensions of the `ICorDebugArrayValue` object.</span></span>  
  
 `dims`  
 <span data-ttu-id="3bc6f-108">[out] Tableau d’entiers, chacun d’eux spécifie le nombre d’éléments dans une dimension dans ce `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-108">[out] An array of integers, each of which specifies the number of elements in a dimension in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3bc6f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bc6f-109">Requirements</span></span>  
 <span data-ttu-id="3bc6f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3bc6f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3bc6f-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3bc6f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3bc6f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3bc6f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3bc6f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3bc6f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
