---
title: ICorDebugProcess2::ClearUnmanagedBreakpoint, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.ClearUnmanagedBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::ClearUnmanagedBreakpoint
helpviewer_keywords:
- ClearUnmanagedBreakpoint method [.NET Framework debugging]
- ICorDebugProcess2::ClearUnmanagedBreakpoint method [.NET Framework debugging]
ms.assetid: 12ed0fff-7f0e-4d7a-bb70-b3376371f36c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f4dcfb977f5ca87f2219fd3ed8ef87d16c2defd2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948965"
---
# <a name="icordebugprocess2clearunmanagedbreakpoint-method"></a><span data-ttu-id="438f2-102">ICorDebugProcess2::ClearUnmanagedBreakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="438f2-102">ICorDebugProcess2::ClearUnmanagedBreakpoint Method</span></span>
<span data-ttu-id="438f2-103">Supprime un précédemment défini point d’arrêt à l’adresse indiquée.</span><span class="sxs-lookup"><span data-stu-id="438f2-103">Removes a previously set breakpoint at the given address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="438f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="438f2-104">Syntax</span></span>  
  
```  
HRESULT ClearUnmanagedBreakpoint (  
    [in] CORDB_ADDRESS   address  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="438f2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="438f2-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="438f2-106">[in] Un `CORDB_ADDRESS` valeur qui spécifie l’adresse à laquelle le point d’arrêt a été défini.</span><span class="sxs-lookup"><span data-stu-id="438f2-106">[in] A `CORDB_ADDRESS` value that specifies the address at which the breakpoint was set.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="438f2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="438f2-107">Remarks</span></span>  
 <span data-ttu-id="438f2-108">Le point d’arrêt spécifié aurait été précédemment défini par un appel antérieur à [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md).</span><span class="sxs-lookup"><span data-stu-id="438f2-108">The specified breakpoint would have been previously set by an earlier call to [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md).</span></span>  
  
 <span data-ttu-id="438f2-109">Le `ClearUnmanagedBreakpoint` méthode peut être appelée pendant le processus en cours de débogage s’exécute.</span><span class="sxs-lookup"><span data-stu-id="438f2-109">The `ClearUnmanagedBreakpoint` method can be called while the process being debugged is running.</span></span>  
  
 <span data-ttu-id="438f2-110">Le `ClearUnmanagedBreakpoint` méthode retourne un code d’erreur si le débogueur est attaché en mode managé uniquement ou si aucun point d’arrêt n’existe à l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="438f2-110">The `ClearUnmanagedBreakpoint` method returns a failure code if the debugger is attached in managed-only mode or if no breakpoint exists at the specified address.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="438f2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="438f2-111">Requirements</span></span>  
 <span data-ttu-id="438f2-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="438f2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="438f2-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="438f2-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="438f2-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="438f2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="438f2-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="438f2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
