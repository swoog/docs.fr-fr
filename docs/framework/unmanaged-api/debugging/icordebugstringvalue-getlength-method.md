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
ms.openlocfilehash: 7b168673e76beddd8ae0479b8daae009c5f057b2
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494660"
---
# <a name="icordebugstringvaluegetlength-method"></a><span data-ttu-id="cd8a8-102">ICorDebugStringValue::GetLength, méthode</span><span class="sxs-lookup"><span data-stu-id="cd8a8-102">ICorDebugStringValue::GetLength Method</span></span>
<span data-ttu-id="cd8a8-103">Obtient le nombre de caractères dans la chaîne référencée par ICorDebugStringValue.</span><span class="sxs-lookup"><span data-stu-id="cd8a8-103">Gets the number of characters in the string referenced by this ICorDebugStringValue.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd8a8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd8a8-104">Syntax</span></span>  
  
```  
HRESULT GetLength (  
    [out] ULONG32   *pcchString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd8a8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd8a8-105">Parameters</span></span>  
 `pcchString`  
 <span data-ttu-id="cd8a8-106">[out] Un pointeur vers une valeur qui spécifie la longueur de la chaîne référencée par ce `ICorDebugStringValue` objet.</span><span class="sxs-lookup"><span data-stu-id="cd8a8-106">[out] A pointer to a value that specifies the length of the string referenced by this `ICorDebugStringValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd8a8-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cd8a8-107">Requirements</span></span>  
 <span data-ttu-id="cd8a8-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd8a8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd8a8-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cd8a8-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cd8a8-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd8a8-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd8a8-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd8a8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
