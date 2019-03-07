---
title: ICorDebugFunction::GetILCode, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetILCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetILCode
helpviewer_keywords:
- ICorDebugFunction::GetILCode method [.NET Framework debugging]
- GetILCode method [.NET Framework debugging]
ms.assetid: f794dd47-a7cd-47f6-96e9-a41a4dae8e72
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f34a2fe2bb1f92e75f77c086b03776ec59495600
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482098"
---
# <a name="icordebugfunctiongetilcode-method"></a><span data-ttu-id="3b1d2-102">ICorDebugFunction::GetILCode, méthode</span><span class="sxs-lookup"><span data-stu-id="3b1d2-102">ICorDebugFunction::GetILCode Method</span></span>
<span data-ttu-id="3b1d2-103">Obtient l’instance ICorDebugCode qui représente le code de Microsoft intermediate language (MSIL) associé à cet objet ICorDebugFunction.</span><span class="sxs-lookup"><span data-stu-id="3b1d2-103">Gets the ICorDebugCode instance that represents the Microsoft intermediate language (MSIL) code associated with this ICorDebugFunction object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b1d2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b1d2-104">Syntax</span></span>  
  
```  
HRESULT GetILCode (  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3b1d2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b1d2-105">Parameters</span></span>  
 `ppCode`  
 <span data-ttu-id="3b1d2-106">[out] Un pointeur vers le `ICorDebugCode` de l’instance, ou null si la fonction n’a pas été compilée dans du code MSIL.</span><span class="sxs-lookup"><span data-stu-id="3b1d2-106">[out] A pointer to the `ICorDebugCode` instance, or null, if the function was not compiled into MSIL.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b1d2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3b1d2-107">Remarks</span></span>  
 <span data-ttu-id="3b1d2-108">Si Modifier & Continuer a été autorisée pour cette fonction, le `GetILCode` méthode obtiendra le code MSIL correspondant à cette version modifiée fonction du code dans le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="3b1d2-108">If Edit and Continue has been allowed on this function, the `GetILCode` method will get the MSIL code corresponding to this function's edited version of the code in the common language runtime (CLR).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b1d2-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b1d2-109">Requirements</span></span>  
 <span data-ttu-id="3b1d2-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b1d2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b1d2-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b1d2-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b1d2-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b1d2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b1d2-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b1d2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
