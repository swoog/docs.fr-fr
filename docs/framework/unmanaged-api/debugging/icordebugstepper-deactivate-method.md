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
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417399"
---
# <a name="icordebugstepperdeactivate-method"></a><span data-ttu-id="1022c-102">ICorDebugStepper::Deactivate, méthode</span><span class="sxs-lookup"><span data-stu-id="1022c-102">ICorDebugStepper::Deactivate Method</span></span>
<span data-ttu-id="1022c-103">Provoque un ICorDebugStepper annuler la dernière commande reçue.</span><span class="sxs-lookup"><span data-stu-id="1022c-103">Causes this ICorDebugStepper to cancel the last step command that it received.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1022c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1022c-104">Syntax</span></span>  
  
```  
HRESULT Deactivate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="1022c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1022c-105">Remarks</span></span>  
 <span data-ttu-id="1022c-106">Une nouvelle commande de pas à pas peut être émise après que la commande d’étape la plus récemment reçue a été annulée.</span><span class="sxs-lookup"><span data-stu-id="1022c-106">A new stepping command may be issued after the most recently received step command has been canceled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1022c-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1022c-107">Requirements</span></span>  
 <span data-ttu-id="1022c-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1022c-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1022c-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1022c-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1022c-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1022c-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1022c-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1022c-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
