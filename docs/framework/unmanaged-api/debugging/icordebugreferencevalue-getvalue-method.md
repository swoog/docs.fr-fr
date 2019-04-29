---
title: ICorDebugReferenceValue::GetValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::GetValue method [.NET Framework debugging]
ms.assetid: 5da07f99-6c70-46ec-b997-5ab6fb7106cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e52ef20f2b8e3937911dc37e68f8a338ab0d85d9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782965"
---
# <a name="icordebugreferencevaluegetvalue-method"></a><span data-ttu-id="9c163-102">ICorDebugReferenceValue::GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="9c163-102">ICorDebugReferenceValue::GetValue Method</span></span>
<span data-ttu-id="9c163-103">Obtient l’adresse mémoire actuelle de l’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="9c163-103">Gets the current memory address of the referenced object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c163-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c163-104">Syntax</span></span>  
  
```  
HRESULT GetValue (  
    [out] CORDB_ADDRESS   *pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c163-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c163-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="9c163-106">[out] Un pointeur vers un `CORDB_ADDRESS` valeur qui spécifie l’adresse de l’objet vers lequel pointe cet objet ICorDebugReferenceValue.</span><span class="sxs-lookup"><span data-stu-id="9c163-106">[out] A pointer to a `CORDB_ADDRESS` value that specifies the address of the object to which this ICorDebugReferenceValue object points.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c163-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c163-107">Requirements</span></span>  
 <span data-ttu-id="9c163-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9c163-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9c163-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9c163-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9c163-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9c163-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9c163-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9c163-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
