---
title: ICLRDebugging, interface
ms.date: 03/30/2017
api_name:
- ICLRDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebugging
helpviewer_keywords:
- ICLRDebugging interface [.NET Framework debugging]
ms.assetid: 429d8fce-b1b1-49d7-895c-28c1c1aa2dbd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a0357b5b072216173546a1aafc03e1a347c48c57
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730047"
---
# <a name="iclrdebugging-interface"></a><span data-ttu-id="65e28-102">ICLRDebugging, interface</span><span class="sxs-lookup"><span data-stu-id="65e28-102">ICLRDebugging Interface</span></span>
<span data-ttu-id="65e28-103">Fournit des méthodes qui gèrent le chargement et le déchargement des modules pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="65e28-103">Provides methods that handle loading and unloading modules for debugging.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="65e28-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65e28-104">Methods</span></span>  
  
|<span data-ttu-id="65e28-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="65e28-105">Method</span></span>|<span data-ttu-id="65e28-106">Description</span><span class="sxs-lookup"><span data-stu-id="65e28-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="65e28-107">OpenVirtualProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="65e28-107">OpenVirtualProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md)|<span data-ttu-id="65e28-108">Obtient l’interface « ICorDebugProcess » qui correspond à un module common language runtime (CLR) chargé dans le processus.</span><span class="sxs-lookup"><span data-stu-id="65e28-108">Gets the "ICorDebugProcess" interface that corresponds to a common language runtime (CLR) module loaded in the process.</span></span>|  
|[<span data-ttu-id="65e28-109">CanUnloadNow, méthode</span><span class="sxs-lookup"><span data-stu-id="65e28-109">CanUnloadNow Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-canunloadnow-method.md)|<span data-ttu-id="65e28-110">Détermine si une bibliothèque qui a été fournie par un [ICLRDebuggingLibraryProvider](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-interface.md) interface est en cours d’utilisation ou peut être déchargée.</span><span class="sxs-lookup"><span data-stu-id="65e28-110">Determines whether a library that was provided by an [ICLRDebuggingLibraryProvider](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-interface.md) interface is still in use or can be unloaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="65e28-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65e28-111">Remarks</span></span>  
 <span data-ttu-id="65e28-112">Vous pouvez obtenir une instance de la `ICLRDebugging` interface à l’aide de la [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="65e28-112">You can obtain an instance of the `ICLRDebugging` interface by using the [CLRCreateInstance](../../../../docs/framework/unmanaged-api/hosting/clrcreateinstance-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65e28-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65e28-113">Requirements</span></span>  
 <span data-ttu-id="65e28-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="65e28-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65e28-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="65e28-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="65e28-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="65e28-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="65e28-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65e28-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65e28-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65e28-118">See also</span></span>
- [<span data-ttu-id="65e28-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="65e28-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="65e28-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="65e28-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
