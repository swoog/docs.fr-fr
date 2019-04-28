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
ms.openlocfilehash: c1af0f8f792c856c0b27b4d3d9ff557bcc5fce82
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994862"
---
# <a name="icordebugmodulegetfunctionfromtoken-method"></a><span data-ttu-id="0e6e1-102">ICorDebugModule::GetFunctionFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="0e6e1-102">ICorDebugModule::GetFunctionFromToken Method</span></span>
<span data-ttu-id="0e6e1-103">Obtient la fonction qui est spécifiée par le jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="0e6e1-103">Gets the function that is specified by the metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e6e1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e6e1-104">Syntax</span></span>  
  
```  
HRESULT GetFunctionFromToken(  
    [in] mdMethodDef methodDef,  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e6e1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e6e1-105">Parameters</span></span>  
 `methodDef`  
 <span data-ttu-id="0e6e1-106">[in] Un `mdMethodDef` jeton de métadonnées qui référence les métadonnées de la fonction.</span><span class="sxs-lookup"><span data-stu-id="0e6e1-106">[in] A `mdMethodDef` metadata token that references the function's metadata.</span></span>  
  
 `ppFunction`  
 <span data-ttu-id="0e6e1-107">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugFunction qui représente la fonction.</span><span class="sxs-lookup"><span data-stu-id="0e6e1-107">[out] A pointer to the address of a ICorDebugFunction interface object that represents the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0e6e1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0e6e1-108">Remarks</span></span>  
 <span data-ttu-id="0e6e1-109">Le `GetFunctionFromToken` méthode retourne une valeur HRESULT CORDBG_E_FUNCTION_NOT_IL si la valeur passée dans `methodDef` ne fait pas référence à une méthode MSIL (intermediate language).</span><span class="sxs-lookup"><span data-stu-id="0e6e1-109">The `GetFunctionFromToken` method returns a CORDBG_E_FUNCTION_NOT_IL HRESULT if the value passed in `methodDef` does not refer to a Microsoft intermediate language (MSIL) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e6e1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e6e1-110">Requirements</span></span>  
 <span data-ttu-id="0e6e1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0e6e1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0e6e1-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0e6e1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0e6e1-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0e6e1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0e6e1-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0e6e1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
