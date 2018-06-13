---
title: ICorDebugModule::GetFunctionFromToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetFunctionFromToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetFunctionFromToken
helpviewer_keywords:
- GetFunctionFromToken method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetFunctionFromToken method [.NET Framework debugging]
ms.assetid: 6fe12194-4ef7-43c1-9570-ade35ccf127a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acffd24ae9d5aad5f48058eec036f912ee016289
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415982"
---
# <a name="icordebugmodulegetfunctionfromtoken-method"></a><span data-ttu-id="ae186-102">ICorDebugModule::GetFunctionFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="ae186-102">ICorDebugModule::GetFunctionFromToken Method</span></span>
<span data-ttu-id="ae186-103">Obtient la fonction qui est spécifiée par le jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ae186-103">Gets the function that is specified by the metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae186-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae186-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromToken(  
    [in] mdMethodDef methodDef,  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae186-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae186-105">Parameters</span></span>  
 `methodDef`  
 <span data-ttu-id="ae186-106">[in] A `mdMethodDef` jeton de métadonnées qui référence les métadonnées de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ae186-106">[in] A `mdMethodDef` metadata token that references the function's metadata.</span></span>  
  
 `ppFunction`  
 <span data-ttu-id="ae186-107">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugFunction qui représente la fonction.</span><span class="sxs-lookup"><span data-stu-id="ae186-107">[out] A pointer to the address of a ICorDebugFunction interface object that represents the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae186-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ae186-108">Remarks</span></span>  
 <span data-ttu-id="ae186-109">Le `GetFunctionFromToken` méthode retourne un CORDBG_E_FUNCTION_NOT_IL HRESULT si la valeur passée dans `methodDef` ne fait pas référence à une méthode MSIL (intermediate language).</span><span class="sxs-lookup"><span data-stu-id="ae186-109">The `GetFunctionFromToken` method returns a CORDBG_E_FUNCTION_NOT_IL HRESULT if the value passed in `methodDef` does not refer to a Microsoft intermediate language (MSIL) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae186-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae186-110">Requirements</span></span>  
 <span data-ttu-id="ae186-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae186-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae186-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ae186-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ae186-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae186-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae186-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae186-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
