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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59204989"
---
# <a name="icordebugmanagedcallbackcontrolctrap-method"></a><span data-ttu-id="57319-102">ICorDebugManagedCallback::ControlCTrap, méthode</span><span class="sxs-lookup"><span data-stu-id="57319-102">ICorDebugManagedCallback::ControlCTrap Method</span></span>
<span data-ttu-id="57319-103">Notifie le débogueur que CTRL + C est intercepté dans le processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="57319-103">Notifies the debugger that a CTRL+C is trapped in the process that is being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57319-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57319-104">Syntax</span></span>  
  
```  
HRESULT ControlCTrap (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57319-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57319-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="57319-106">[in] Pointeur vers un objet ICorDebugProcess qui représente le processus dans lequel CTRL + C est intercepté.</span><span class="sxs-lookup"><span data-stu-id="57319-106">[in] A pointer to an ICorDebugProcess object that represents the process in which the CTRL+C is trapped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="57319-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="57319-107">Return Value</span></span>  
  
|<span data-ttu-id="57319-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="57319-108">HRESULT</span></span>|<span data-ttu-id="57319-109">Description</span><span class="sxs-lookup"><span data-stu-id="57319-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="57319-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="57319-110">S_OK</span></span>|<span data-ttu-id="57319-111">Le débogueur gère l’interruption CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="57319-111">The debugger will handle the CTRL+C trap.</span></span>|  
|<span data-ttu-id="57319-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="57319-112">S_FALSE</span></span>|<span data-ttu-id="57319-113">Le débogueur ne gère pas l’interruption CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="57319-113">The debugger will not handle the CTRL+C trap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="57319-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57319-114">Remarks</span></span>  
 <span data-ttu-id="57319-115">Tous les domaines d’application au sein du processus sont arrêtés pour ce rappel.</span><span class="sxs-lookup"><span data-stu-id="57319-115">All application domains within the process are stopped for this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57319-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57319-116">Requirements</span></span>  
 <span data-ttu-id="57319-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="57319-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57319-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="57319-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57319-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57319-119">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="57319-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="57319-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="57319-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57319-121">See also</span></span>

- [<span data-ttu-id="57319-122">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="57319-122">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
