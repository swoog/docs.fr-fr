---
title: ICorDebugHeapValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue
helpviewer_keywords:
- ICorDebugHeapValue interface [.NET Framework debugging]
ms.assetid: 1bca66db-0359-4ae8-846e-e35f7e547e8b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d5fcd8c17c4006714fa9d11aece5cccc57c97087
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59075494"
---
# <a name="icordebugheapvalue-interface"></a><span data-ttu-id="5ad6a-102">ICorDebugHeapValue, interface</span><span class="sxs-lookup"><span data-stu-id="5ad6a-102">ICorDebugHeapValue Interface</span></span>

<span data-ttu-id="5ad6a-103">Une sous-classe de « ICorDebugValue » qui représente un objet qui a été collecté par le garbage collector du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="5ad6a-103">A subclass of "ICorDebugValue" that represents an object that has been collected by the common language runtime (CLR) garbage collector.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5ad6a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5ad6a-104">Methods</span></span>  
  
|<span data-ttu-id="5ad6a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="5ad6a-105">Method</span></span>|<span data-ttu-id="5ad6a-106">Description</span><span class="sxs-lookup"><span data-stu-id="5ad6a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5ad6a-107">CreateRelocBreakpoint, méthode</span><span class="sxs-lookup"><span data-stu-id="5ad6a-107">CreateRelocBreakpoint Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-createrelocbreakpoint-method.md)|<span data-ttu-id="5ad6a-108">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="5ad6a-108">Not implemented.</span></span>|  
|[<span data-ttu-id="5ad6a-109">IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="5ad6a-109">IsValid Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue-isvalid-method.md)|<span data-ttu-id="5ad6a-110">Obtient une valeur qui indique si l’objet représenté par cet `ICorDebugHeapValue` est valide, ou a été récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="5ad6a-110">Gets a value that indicates whether the object represented by this `ICorDebugHeapValue` is valid, or has been reclaimed by the garbage collector.</span></span> <span data-ttu-id="5ad6a-111">Cette méthode a été déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="5ad6a-111">This method has been deprecated in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5ad6a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5ad6a-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5ad6a-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="5ad6a-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ad6a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ad6a-114">Requirements</span></span>  
 <span data-ttu-id="5ad6a-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ad6a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ad6a-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5ad6a-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5ad6a-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5ad6a-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="5ad6a-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5ad6a-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5ad6a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad6a-119">See also</span></span>

- [<span data-ttu-id="5ad6a-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5ad6a-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
