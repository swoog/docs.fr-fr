---
title: ICorDebugAppDomain::Attach, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.Attach
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::Attach
helpviewer_keywords:
- ICorDebugAppDomain::Attach method [.NET Framework debugging]
- Attach method [.NET Framework debugging]
ms.assetid: 0358b84a-4236-4c34-945b-4babff7df570
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a290ca162e5ab71b4184d166bcd00f1d0217cb94
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402494"
---
# <a name="icordebugappdomainattach-method"></a><span data-ttu-id="7d2b4-102">ICorDebugAppDomain::Attach, méthode</span><span class="sxs-lookup"><span data-stu-id="7d2b4-102">ICorDebugAppDomain::Attach Method</span></span>
<span data-ttu-id="7d2b4-103">Attache le débogueur au domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="7d2b4-103">Attaches the debugger to the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d2b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d2b4-104">Syntax</span></span>  
  
```  
HRESULT Attach ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="7d2b4-105">Notes</span><span class="sxs-lookup"><span data-stu-id="7d2b4-105">Remarks</span></span>  
 <span data-ttu-id="7d2b4-106">Le débogueur doit être attaché au domaine d’application pour recevoir des événements et activer le débogage du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="7d2b4-106">The debugger must be attached to the application domain to receive events and to enable debugging of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d2b4-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d2b4-107">Requirements</span></span>  
 <span data-ttu-id="7d2b4-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7d2b4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d2b4-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7d2b4-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7d2b4-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7d2b4-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7d2b4-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d2b4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
