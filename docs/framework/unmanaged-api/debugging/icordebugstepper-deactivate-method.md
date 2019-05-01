---
title: ICorDebugStepper::Deactivate, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugStepper.Deactivate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper::Deactivate
helpviewer_keywords:
- Deactivate method [.NET Framework debugging]
- ICorDebugStepper::Deactivate method [.NET Framework debugging]
ms.assetid: 855f4199-b62d-40ce-998e-1eb4a1772142
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bcd7bfb52cadf740d8fe3cb92a09b071f530b7ee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994329"
---
# <a name="icordebugstepperdeactivate-method"></a><span data-ttu-id="b77a0-102">ICorDebugStepper::Deactivate, méthode</span><span class="sxs-lookup"><span data-stu-id="b77a0-102">ICorDebugStepper::Deactivate Method</span></span>
<span data-ttu-id="b77a0-103">Entraîne ce ICorDebugStepper annuler la dernière commande reçue.</span><span class="sxs-lookup"><span data-stu-id="b77a0-103">Causes this ICorDebugStepper to cancel the last step command that it received.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b77a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b77a0-104">Syntax</span></span>  
  
```  
HRESULT Deactivate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="b77a0-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b77a0-105">Remarks</span></span>  
 <span data-ttu-id="b77a0-106">Une nouvelle commande de pas à pas peut-être être émise après que la commande d’étape la plus récemment reçue a été annulée.</span><span class="sxs-lookup"><span data-stu-id="b77a0-106">A new stepping command may be issued after the most recently received step command has been canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b77a0-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b77a0-107">Requirements</span></span>  
 <span data-ttu-id="b77a0-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b77a0-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b77a0-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b77a0-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b77a0-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b77a0-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b77a0-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b77a0-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
