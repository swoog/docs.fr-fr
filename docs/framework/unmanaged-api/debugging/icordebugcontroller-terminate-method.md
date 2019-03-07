---
title: ICorDebugController::Terminate, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Terminate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Terminate
helpviewer_keywords:
- Terminate method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Terminate method [.NET Framework debugging]
ms.assetid: 4275af0c-b5a7-4e4c-97c9-7e41f36b2dd8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 65a374f942697ee670507987c4a97a7977970b69
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481091"
---
# <a name="icordebugcontrollerterminate-method"></a><span data-ttu-id="bfe07-102">ICorDebugController::Terminate, méthode</span><span class="sxs-lookup"><span data-stu-id="bfe07-102">ICorDebugController::Terminate Method</span></span>
<span data-ttu-id="bfe07-103">Met fin au processus avec le code de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="bfe07-103">Terminates the process with the specified exit code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bfe07-104">Cette méthode est un wrapper pour Win32 `TerminateProcess` (fonction).</span><span class="sxs-lookup"><span data-stu-id="bfe07-104">This method is a wrapper for the Win32 `TerminateProcess` function.</span></span> <span data-ttu-id="bfe07-105">Par conséquent, `Terminate` utilise le code de sortie de la même façon que Win32 `TerminateProcess` utilise la fonction.</span><span class="sxs-lookup"><span data-stu-id="bfe07-105">Thus, `Terminate` uses the exit code in the same way that the Win32 `TerminateProcess` function uses it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfe07-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfe07-106">Syntax</span></span>  
  
```  
HRESULT Terminate (  
    [in] UINT exitCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bfe07-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfe07-107">Parameters</span></span>  
 `exitCode`  
 <span data-ttu-id="bfe07-108">[in] Valeur numérique qui est le code de sortie.</span><span class="sxs-lookup"><span data-stu-id="bfe07-108">[in] A numeric value that is the exit code.</span></span> <span data-ttu-id="bfe07-109">Les valeurs numériques valides sont définis dans Winbase.h.</span><span class="sxs-lookup"><span data-stu-id="bfe07-109">The valid numeric values are defined in Winbase.h.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bfe07-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bfe07-110">Remarks</span></span>  
 <span data-ttu-id="bfe07-111">Si le processus est arrêté lorsque `Terminate` est appelée, le processus doit être poursuivi à l’aide de la [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) méthode afin que le débogueur reçoive confirmation de l’arrêt via le [ ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) ou [ICorDebugManagedCallback::ExitAppDomain](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitappdomain-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="bfe07-111">If the process is stopped when `Terminate` is called, the process should be continued by using the [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) method so that the debugger receives confirmation of the termination through the [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) or [ICorDebugManagedCallback::ExitAppDomain](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitappdomain-method.md) callback.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bfe07-112">Cette méthode n’est pas implémentée par un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="bfe07-112">This method is not implemented by an application domain.</span></span> <span data-ttu-id="bfe07-113">Autrement dit, il n’est pas implémentée à le <xref:System.AppDomain> niveau.</span><span class="sxs-lookup"><span data-stu-id="bfe07-113">That is, it is not implemented at the <xref:System.AppDomain> level.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bfe07-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bfe07-114">Requirements</span></span>  
 <span data-ttu-id="bfe07-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bfe07-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bfe07-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bfe07-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bfe07-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bfe07-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bfe07-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bfe07-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfe07-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfe07-119">See also</span></span>

