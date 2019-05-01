---
title: ICorDebugManagedCallback::ControlCTrap, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.ControlCTrap
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::ControlCTrap
helpviewer_keywords:
- ICorDebugManagedCallback::ControlCTrap method [.NET Framework debugging]
- ControlCTrap method [.NET Framework debugging]
ms.assetid: 0500854e-2121-43d9-a028-64312da35258
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7f4794fb0383435f828626497036ad3458df2173
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61995330"
---
# <a name="icordebugmanagedcallbackcontrolctrap-method"></a><span data-ttu-id="bfe5b-102">ICorDebugManagedCallback::ControlCTrap, méthode</span><span class="sxs-lookup"><span data-stu-id="bfe5b-102">ICorDebugManagedCallback::ControlCTrap Method</span></span>
<span data-ttu-id="bfe5b-103">Notifie le débogueur que CTRL + C est intercepté dans le processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="bfe5b-103">Notifies the debugger that a CTRL+C is trapped in the process that is being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bfe5b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfe5b-104">Syntax</span></span>  
  
```  
HRESULT ControlCTrap (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bfe5b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfe5b-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="bfe5b-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus dans lequel CTRL + C est intercepté.</span><span class="sxs-lookup"><span data-stu-id="bfe5b-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the CTRL+C is trapped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bfe5b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bfe5b-107">Return Value</span></span>  
  
|<span data-ttu-id="bfe5b-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bfe5b-108">HRESULT</span></span>|<span data-ttu-id="bfe5b-109">Description</span><span class="sxs-lookup"><span data-stu-id="bfe5b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bfe5b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="bfe5b-110">S_OK</span></span>|<span data-ttu-id="bfe5b-111">Le débogueur gère l’interruption CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="bfe5b-111">The debugger will handle the CTRL+C trap.</span></span>|  
|<span data-ttu-id="bfe5b-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="bfe5b-112">S_FALSE</span></span>|<span data-ttu-id="bfe5b-113">Le débogueur ne gère pas l’interruption CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="bfe5b-113">The debugger will not handle the CTRL+C trap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bfe5b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bfe5b-114">Remarks</span></span>  
 <span data-ttu-id="bfe5b-115">Tous les domaines d’application au sein du processus sont arrêtés pour ce rappel.</span><span class="sxs-lookup"><span data-stu-id="bfe5b-115">All application domains within the process are stopped for this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bfe5b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfe5b-116">Requirements</span></span>  
 <span data-ttu-id="bfe5b-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bfe5b-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bfe5b-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bfe5b-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bfe5b-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bfe5b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bfe5b-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bfe5b-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfe5b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfe5b-121">See also</span></span>

- [<span data-ttu-id="bfe5b-122">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="bfe5b-122">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
