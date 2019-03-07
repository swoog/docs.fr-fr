---
title: ICorDebugFrame::GetFunction, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetFunction method [.NET Framework debugging]
ms.assetid: 879d2311-0ff1-4616-a8b3-959ea5868b2e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a48396f8ef668cfe7755b2718180317b465793b6
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57475280"
---
# <a name="icordebugframegetfunction-method"></a><span data-ttu-id="d904f-102">ICorDebugFrame::GetFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="d904f-102">ICorDebugFrame::GetFunction Method</span></span>
<span data-ttu-id="d904f-103">Obtient la fonction qui contient le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="d904f-103">Gets the function that contains the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d904f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d904f-104">Syntax</span></span>  
  
```  
HRESULT GetFunction (  
    [out] ICorDebugFunction  **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d904f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d904f-105">Parameters</span></span>  
 `ppFunction`  
 <span data-ttu-id="d904f-106">[out] Pointeur vers l’adresse d’un objet ICorDebugFunction qui représente la fonction contenant le code associé à ce frame de pile.</span><span class="sxs-lookup"><span data-stu-id="d904f-106">[out] A pointer to the address of an ICorDebugFunction object that represents the function containing the code associated with this stack frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d904f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d904f-107">Remarks</span></span>  
 <span data-ttu-id="d904f-108">Le `GetFunction` méthode peut échouer si le frame n’est pas associé à une fonction particulière.</span><span class="sxs-lookup"><span data-stu-id="d904f-108">The `GetFunction` method may fail if the frame is not associated with any particular function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d904f-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d904f-109">Requirements</span></span>  
 <span data-ttu-id="d904f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d904f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d904f-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d904f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d904f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d904f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d904f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d904f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
