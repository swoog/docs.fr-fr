---
title: ICorDebugModule::GetGlobalVariableValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetGlobalVariableValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetGlobalVariableValue
helpviewer_keywords:
- ICorDebugModule::GetGlobalVariableValue method [.NET Framework debugging]
- GetGlobalVariableValue method [.NET Framework debugging]
ms.assetid: bbc0881c-6a59-41a0-b5ee-2f3d1b71684c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa558bf58f3033cc39a2b52d99e3a5329d9e99bd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413031"
---
# <a name="icordebugmodulegetglobalvariablevalue-method"></a><span data-ttu-id="201a6-102">ICorDebugModule::GetGlobalVariableValue, méthode</span><span class="sxs-lookup"><span data-stu-id="201a6-102">ICorDebugModule::GetGlobalVariableValue Method</span></span>
<span data-ttu-id="201a6-103">Obtient la valeur de la variable globale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="201a6-103">Gets the value of the specified global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="201a6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="201a6-104">Syntax</span></span>  
  
```  
HRESULT GetGlobalVariableValue(  
    [in]  mdFieldDef      fieldDef,  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="201a6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="201a6-105">Parameters</span></span>  
 `fieldDef`  
 <span data-ttu-id="201a6-106">[in] Un `mdFieldDef` jeton qui référence les métadonnées décrivant la variable globale.</span><span class="sxs-lookup"><span data-stu-id="201a6-106">[in] An `mdFieldDef` token that references the metadata describing the global variable.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="201a6-107">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur de la variable globale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="201a6-107">[out] A pointer to the address of an ICorDebugValue object that represents the value of the specified global variable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="201a6-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="201a6-108">Requirements</span></span>  
 <span data-ttu-id="201a6-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="201a6-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="201a6-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="201a6-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="201a6-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="201a6-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="201a6-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="201a6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
