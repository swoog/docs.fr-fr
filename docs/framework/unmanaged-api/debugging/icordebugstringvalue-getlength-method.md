---
title: ICorDebugStringValue::GetLength, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue.GetLength
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue::GetLength
helpviewer_keywords:
- ICorDebugStringValue::GetLength method [.NET Framework debugging]
- GetLength method [.NET Framework debugging]
ms.assetid: a1ebfc69-46a6-4225-8788-b7cfb2f15e1d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e62539304817432fcab8f3e0958e5a70b371b83d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416944"
---
# <a name="icordebugstringvaluegetlength-method"></a><span data-ttu-id="5718d-102">ICorDebugStringValue::GetLength, méthode</span><span class="sxs-lookup"><span data-stu-id="5718d-102">ICorDebugStringValue::GetLength Method</span></span>
<span data-ttu-id="5718d-103">Obtient le nombre de caractères dans la chaîne référencée par ICorDebugStringValue.</span><span class="sxs-lookup"><span data-stu-id="5718d-103">Gets the number of characters in the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5718d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5718d-104">Syntax</span></span>  
  
```  
HRESULT GetLength (  
    [out] ULONG32   *pcchString  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5718d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5718d-105">Parameters</span></span>  
 `pcchString`  
 <span data-ttu-id="5718d-106">[out] Un pointeur vers une valeur qui spécifie la longueur de la chaîne référencée par cet `ICorDebugStringValue` objet.</span><span class="sxs-lookup"><span data-stu-id="5718d-106">[out] A pointer to a value that specifies the length of the string referenced by this `ICorDebugStringValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5718d-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5718d-107">Requirements</span></span>  
 <span data-ttu-id="5718d-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5718d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5718d-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5718d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5718d-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5718d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5718d-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5718d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
