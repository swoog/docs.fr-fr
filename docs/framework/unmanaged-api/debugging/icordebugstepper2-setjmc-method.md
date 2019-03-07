---
title: ICorDebugStepper2::SetJMC, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2.SetJMC
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2::SetJMC
helpviewer_keywords:
- ICorDebugStepper2::SetJMC method [.NET Framework debugging]
- SetJMC method [.NET Framework debugging]
ms.assetid: f5cdc135-6db4-4b32-9dd1-260ec58b774f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 129bf04a097b2019b080f813bf049d41b501f8fd
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474213"
---
# <a name="icordebugstepper2setjmc-method"></a><span data-ttu-id="ffd6b-102">ICorDebugStepper2::SetJMC, méthode</span><span class="sxs-lookup"><span data-stu-id="ffd6b-102">ICorDebugStepper2::SetJMC Method</span></span>
<span data-ttu-id="ffd6b-103">Définit une valeur qui spécifie si cette ICorDebugStepper exécute pas à pas uniquement le code créé par le développeur d’une application.</span><span class="sxs-lookup"><span data-stu-id="ffd6b-103">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span> <span data-ttu-id="ffd6b-104">Ce processus est également connu comme débogage uniquement mon code (JMC).</span><span class="sxs-lookup"><span data-stu-id="ffd6b-104">This process is also known as just my code (JMC) debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ffd6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffd6b-105">Syntax</span></span>  
  
```  
HRESULT SetJMC (  
    [in] BOOL    fIsJMCStepper  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ffd6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffd6b-106">Parameters</span></span>  
 `fIsJMCStepper`  
 <span data-ttu-id="ffd6b-107">[in] La valeur `true` à l’étape uniquement par le biais de code qui est créé par le développeur de l’application ; sinon, la valeur est `false`.</span><span class="sxs-lookup"><span data-stu-id="ffd6b-107">[in] Set to `true` to step only through code that is authored by an application's developer; otherwise, set to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ffd6b-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ffd6b-108">Requirements</span></span>  
 <span data-ttu-id="ffd6b-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ffd6b-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ffd6b-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ffd6b-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ffd6b-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ffd6b-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ffd6b-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ffd6b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
