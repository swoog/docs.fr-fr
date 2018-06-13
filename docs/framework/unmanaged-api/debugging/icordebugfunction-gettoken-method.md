---
title: ICorDebugFunction::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetToken
helpviewer_keywords:
- ICorDebugFunction::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: c6bbf479-062e-48e9-9c70-0f92e293e36a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acfb8910df6e20bf55ed33fdbb9b1c30d22f4684
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412050"
---
# <a name="icordebugfunctiongettoken-method"></a><span data-ttu-id="c4263-102">ICorDebugFunction::GetToken, méthode</span><span class="sxs-lookup"><span data-stu-id="c4263-102">ICorDebugFunction::GetToken Method</span></span>
<span data-ttu-id="c4263-103">Obtient les métadonnées de jeton pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c4263-103">Gets the metadata token for this function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4263-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4263-104">Syntax</span></span>  
  
```  
HRESULT GetToken (  
    [out] mdMethodDef *pMethodDef  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c4263-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4263-105">Parameters</span></span>  
 `pMethodDef`  
 <span data-ttu-id="c4263-106">[out] Un pointeur vers un `mdMethodDef` jeton qui référence les métadonnées pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c4263-106">[out] A pointer to an `mdMethodDef` token that references the metadata for this function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4263-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4263-107">Requirements</span></span>  
 <span data-ttu-id="c4263-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4263-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4263-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c4263-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c4263-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c4263-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c4263-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4263-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
