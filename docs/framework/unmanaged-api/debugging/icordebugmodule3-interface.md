---
title: ICorDebugModule3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugModule3
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3
helpviewer_keywords:
- ICorDebugModule3 interface [.NET Framework debugging]
ms.assetid: 0b69f945-263a-4e11-8512-89d27f6ea296
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58bad617eb91b7e529ff3d95edd06a5c73feee64
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46472033"
---
# <a name="icordebugmodule3-interface"></a><span data-ttu-id="083ff-102">ICorDebugModule3, interface</span><span class="sxs-lookup"><span data-stu-id="083ff-102">ICorDebugModule3 Interface</span></span>
<span data-ttu-id="083ff-103">Crée un lecteur de symboles pour un module dynamique.</span><span class="sxs-lookup"><span data-stu-id="083ff-103">Creates a symbol reader for a dynamic module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="083ff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="083ff-104">Syntax</span></span>  
  
```  
interface ICorDebugModule3 : IUnknown  
{  
    HRESULT CreateReaderForInMemorySymbols  
      (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **  ppObj  
      );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="083ff-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="083ff-105">Methods</span></span>  
  
|<span data-ttu-id="083ff-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="083ff-106">Method</span></span>|<span data-ttu-id="083ff-107">Description</span><span class="sxs-lookup"><span data-stu-id="083ff-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="083ff-108">ICorDebugModule3::CreateReaderForInMemorySymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="083ff-108">ICorDebugModule3::CreateReaderForInMemorySymbols Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule3-createreaderforinmemorysymbols-method.md)|<span data-ttu-id="083ff-109">Crée un lecteur de symboles (généralement [ISymUnmanagedReader Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)) pour un module dynamique.</span><span class="sxs-lookup"><span data-stu-id="083ff-109">Creates a symbol reader (typically [ISymUnmanagedReader Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)) for a dynamic module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="083ff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="083ff-110">Remarks</span></span>  
 <span data-ttu-id="083ff-111">Cette interface étend logiquement les interfaces « ICorDebugModule » et « ICorDebugModule2 ».</span><span class="sxs-lookup"><span data-stu-id="083ff-111">This interface logically extends the "ICorDebugModule" and "ICorDebugModule2" interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="083ff-112">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="083ff-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="083ff-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="083ff-113">Requirements</span></span>  
 <span data-ttu-id="083ff-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="083ff-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="083ff-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="083ff-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="083ff-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="083ff-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="083ff-117">**Versions du .NET framework :** 4.5, 4, 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="083ff-117">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>
  
## <a name="see-also"></a><span data-ttu-id="083ff-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="083ff-118">See Also</span></span>  
 [<span data-ttu-id="083ff-119">ICorDebugRemoteTarget, interface</span><span class="sxs-lookup"><span data-stu-id="083ff-119">ICorDebugRemoteTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md)  
 [<span data-ttu-id="083ff-120">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="083ff-120">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
    
 [<span data-ttu-id="083ff-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="083ff-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
