---
title: ICorDebugArrayValue::GetRank, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetRank
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetRank
helpviewer_keywords:
- ICorDebugArrayValue::GetRank method [.NET Framework debugging]
- GetRank method, ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: 5e83c82c-593d-4691-90b0-383d218b415e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 699c65aae205efd5b08f1d163b4ff9a223bbc217
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645654"
---
# <a name="icordebugarrayvaluegetrank-method"></a><span data-ttu-id="57b53-102">ICorDebugArrayValue::GetRank, méthode</span><span class="sxs-lookup"><span data-stu-id="57b53-102">ICorDebugArrayValue::GetRank Method</span></span>
<span data-ttu-id="57b53-103">Obtient le nombre de dimensions dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="57b53-103">Gets the number of dimensions in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57b53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57b53-104">Syntax</span></span>  
  
```  
HRESULT GetRank (  
    [out] ULONG32   *pnRank  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57b53-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57b53-105">Parameters</span></span>  
 `pnRank`  
 <span data-ttu-id="57b53-106">[out] Un pointeur vers le nombre de dimensions dans ce `ICorDebugArrayValue` objet.</span><span class="sxs-lookup"><span data-stu-id="57b53-106">[out] A pointer to the number of dimensions in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57b53-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57b53-107">Requirements</span></span>  
 <span data-ttu-id="57b53-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="57b53-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57b53-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="57b53-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57b53-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57b53-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57b53-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57b53-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
