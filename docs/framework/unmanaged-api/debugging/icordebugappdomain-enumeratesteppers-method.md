---
title: ICorDebugAppDomain::EnumerateSteppers, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateSteppers
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateSteppers
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateSteppers method [.NET Framework debugging]
- EnumerateSteppers method [.NET Framework debugging]
ms.assetid: 3f3c4503-570e-44c1-ae6a-a3c6b840c732
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d326c801ed17fa6fe79f9e464e64844d0016e572
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785152"
---
# <a name="icordebugappdomainenumeratesteppers-method"></a><span data-ttu-id="f7a4a-102">ICorDebugAppDomain::EnumerateSteppers, méthode</span><span class="sxs-lookup"><span data-stu-id="f7a4a-102">ICorDebugAppDomain::EnumerateSteppers Method</span></span>
<span data-ttu-id="f7a4a-103">Obtient un énumérateur pour toutes les exécutions pas à pas active dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="f7a4a-103">Gets an enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f7a4a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7a4a-104">Syntax</span></span>  
  
```  
HRESULT EnumerateSteppers (  
    [out] ICorDebugStepperEnum   **ppSteppers  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f7a4a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7a4a-105">Parameters</span></span>  
 `ppSteppers`  
 <span data-ttu-id="f7a4a-106">[out] Pointeur vers l’adresse d’un objet ICorDebugStepperEnum qui est l’énumérateur pour toutes les exécutions pas à pas active dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="f7a4a-106">[out] A pointer to the address of an ICorDebugStepperEnum object that is the enumerator for all active steppers in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f7a4a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7a4a-107">Requirements</span></span>  
 <span data-ttu-id="f7a4a-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f7a4a-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f7a4a-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f7a4a-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f7a4a-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f7a4a-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f7a4a-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f7a4a-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
