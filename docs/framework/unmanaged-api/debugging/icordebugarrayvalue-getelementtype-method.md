---
title: ICorDebugArrayValue::GetElementType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElementType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElementType
helpviewer_keywords:
- ICorDebugArrayValue::GetElementType method [.NET Framework debugging]
- GetElementType method [.NET Framework debugging]
ms.assetid: ed71961e-ae9b-4dfc-9554-06637696d697
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e6f5f1da94e1ae07a604a616c631a38d02caea9d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645628"
---
# <a name="icordebugarrayvaluegetelementtype-method"></a><span data-ttu-id="f1ae8-102">ICorDebugArrayValue::GetElementType, méthode</span><span class="sxs-lookup"><span data-stu-id="f1ae8-102">ICorDebugArrayValue::GetElementType Method</span></span>
<span data-ttu-id="f1ae8-103">Obtient une valeur qui indique le type simple des éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f1ae8-103">Gets a value that indicates the simple type of the elements in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1ae8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1ae8-104">Syntax</span></span>  
  
```  
HRESULT GetElementType (  
    [out] CorElementType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f1ae8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1ae8-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="f1ae8-106">[out] Pointeur vers une valeur de l’énumération CorElementType qui indique le type.</span><span class="sxs-lookup"><span data-stu-id="f1ae8-106">[out] A pointer to a value of the CorElementType enumeration that indicates the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1ae8-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1ae8-107">Requirements</span></span>  
 <span data-ttu-id="f1ae8-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f1ae8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1ae8-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f1ae8-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f1ae8-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f1ae8-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f1ae8-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1ae8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
