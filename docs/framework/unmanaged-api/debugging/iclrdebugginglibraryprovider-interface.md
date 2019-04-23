---
title: ICLRDebuggingLibraryProvider, interface
ms.date: 03/30/2017
api_name:
- ICLRDebuggingLibraryProvider
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebuggingLibraryProvider
helpviewer_keywords:
- ICLRDebuggingLibraryProvider interface [.NET Framework debugging]
ms.assetid: 67739617-6add-41a9-9de5-a3200c3109ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c62079a87c09bcbe09167a137fd39530652ae3e5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59106338"
---
# <a name="iclrdebugginglibraryprovider-interface"></a><span data-ttu-id="4be4f-102">ICLRDebuggingLibraryProvider, interface</span><span class="sxs-lookup"><span data-stu-id="4be4f-102">ICLRDebuggingLibraryProvider Interface</span></span>
<span data-ttu-id="4be4f-103">Inclut le [ProvideLibrary, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md) (méthode), qui obtient un fournisseur de bibliothèque interface de rappel qui permet de common language runtime des bibliothèques de débogage spécifiques à la version être à la demande et le chargement.</span><span class="sxs-lookup"><span data-stu-id="4be4f-103">Includes the [ProvideLibrary Method](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md) method, which gets a library provider callback interface that allows common language runtime version-specific debugging libraries to be located and loaded on demand.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4be4f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4be4f-104">Methods</span></span>  
  
|<span data-ttu-id="4be4f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4be4f-105">Method</span></span>|<span data-ttu-id="4be4f-106">Description</span><span class="sxs-lookup"><span data-stu-id="4be4f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4be4f-107">ProvideLibrary, méthode</span><span class="sxs-lookup"><span data-stu-id="4be4f-107">ProvideLibrary Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md)|<span data-ttu-id="4be4f-108">Permet au débogueur de fournir un handle à un module qui peut être utilisé pour charger une bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="4be4f-108">Allows the debugger to provide a handle to a module which can be used to load a debug library.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4be4f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4be4f-109">Requirements</span></span>  
 <span data-ttu-id="4be4f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4be4f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4be4f-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4be4f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4be4f-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4be4f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4be4f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4be4f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4be4f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4be4f-114">See also</span></span>

- [<span data-ttu-id="4be4f-115">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4be4f-115">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="4be4f-116">Débogage</span><span class="sxs-lookup"><span data-stu-id="4be4f-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
