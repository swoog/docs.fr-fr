---
title: ICorDebugReferenceValue::IsNull, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.IsNull
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::IsNull
helpviewer_keywords:
- IsNull method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::IsNull method [.NET Framework debugging]
ms.assetid: 99e8c8d7-a1c0-47c8-9dbd-03e0b2bcb4d5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 972df4613255dc1b71801e02d387a735dfc632c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782933"
---
# <a name="icordebugreferencevalueisnull-method"></a><span data-ttu-id="597de-102">ICorDebugReferenceValue::IsNull, méthode</span><span class="sxs-lookup"><span data-stu-id="597de-102">ICorDebugReferenceValue::IsNull Method</span></span>
<span data-ttu-id="597de-103">Obtient une valeur qui indique si cette ICorDebugReferenceValue est une valeur null, auquel cas le `ICorDebugReferenceValue` ne pointe pas vers un objet.</span><span class="sxs-lookup"><span data-stu-id="597de-103">Gets a value that indicates whether this ICorDebugReferenceValue is a null value, in which case the `ICorDebugReferenceValue` does not point to an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="597de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="597de-104">Syntax</span></span>  
  
```  
HRESULT IsNull (  
    [out] BOOL   *pbNull  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="597de-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="597de-105">Parameters</span></span>  
 `pbNull`  
 <span data-ttu-id="597de-106">[out] Un pointeur vers une valeur booléenne qui est `true` si ce `ICorDebugReferenceValue` objet est null ; sinon, `pbNull` est `false`.</span><span class="sxs-lookup"><span data-stu-id="597de-106">[out] A pointer to a Boolean value that is `true` if this `ICorDebugReferenceValue` object is null; otherwise, `pbNull` is `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="597de-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="597de-107">Requirements</span></span>  
 <span data-ttu-id="597de-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="597de-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="597de-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="597de-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="597de-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="597de-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="597de-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="597de-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
