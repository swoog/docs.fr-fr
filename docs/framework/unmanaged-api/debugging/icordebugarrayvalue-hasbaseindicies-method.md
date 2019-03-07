---
title: ICorDebugArrayValue::HasBaseIndicies, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.HasBaseIndicies
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::HasBaseIndicies
helpviewer_keywords:
- HasBaseIndicies method [.NET Framework debugging]
- ICorDebugArrayValue::HasBaseIndicies method [.NET Framework debugging]
ms.assetid: aa26df07-e0a6-4608-bdef-d4afafec89aa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 49f5ed8b24d81ba8f32a9fe0ad7488693718bde9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468557"
---
# <a name="icordebugarrayvaluehasbaseindicies-method"></a><span data-ttu-id="caf5b-102">ICorDebugArrayValue::HasBaseIndicies, méthode</span><span class="sxs-lookup"><span data-stu-id="caf5b-102">ICorDebugArrayValue::HasBaseIndicies Method</span></span>
<span data-ttu-id="caf5b-103">Obtient une valeur qui indique si toutes les dimensions de ce tableau ont un index de base de zéro.</span><span class="sxs-lookup"><span data-stu-id="caf5b-103">Gets a value that indicates whether any dimensions of this array have a base index of non-zero.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="caf5b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caf5b-104">Syntax</span></span>  
  
```  
HRESULT HasBaseIndicies (  
    [out] BOOL    *pbHasBaseIndicies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="caf5b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caf5b-105">Parameters</span></span>  
 `pbHasBaseIndicies`  
 <span data-ttu-id="caf5b-106">[out] Un pointeur vers une valeur booléenne qui est `true` si une ou plusieurs dimensions de ce `ICorDebugArrayValue` objet a un index de base de zéro ; sinon, la valeur booléenne est `false`.</span><span class="sxs-lookup"><span data-stu-id="caf5b-106">[out] A pointer to a Boolean value that is `true` if one or more dimensions of this `ICorDebugArrayValue` object have a base index of non-zero; otherwise, the Boolean value is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="caf5b-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="caf5b-107">Requirements</span></span>  
 <span data-ttu-id="caf5b-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="caf5b-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="caf5b-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="caf5b-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="caf5b-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="caf5b-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="caf5b-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="caf5b-111">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>
