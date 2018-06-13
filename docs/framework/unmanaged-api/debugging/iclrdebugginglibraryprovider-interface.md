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
ms.openlocfilehash: 7537d3d6f741f36ab81d73751963a8539de0a36c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404467"
---
# <a name="iclrdebugginglibraryprovider-interface"></a><span data-ttu-id="d2285-102">ICLRDebuggingLibraryProvider, interface</span><span class="sxs-lookup"><span data-stu-id="d2285-102">ICLRDebuggingLibraryProvider Interface</span></span>
<span data-ttu-id="d2285-103">Inclut le [ProvideLibrary, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md) méthode, qui obtient un fournisseur de bibliothèque interface de rappel qui permet de common language runtime des bibliothèques de débogage spécifiques à la version à la demande et le chargement.</span><span class="sxs-lookup"><span data-stu-id="d2285-103">Includes the [ProvideLibrary Method](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md) method, which gets a library provider callback interface that allows common language runtime version-specific debugging libraries to be located and loaded on demand.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d2285-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2285-104">Methods</span></span>  
  
|<span data-ttu-id="d2285-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d2285-105">Method</span></span>|<span data-ttu-id="d2285-106">Description</span><span class="sxs-lookup"><span data-stu-id="d2285-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d2285-107">ProvideLibrary, méthode</span><span class="sxs-lookup"><span data-stu-id="d2285-107">ProvideLibrary Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdebugginglibraryprovider-providelibrary-method.md)|<span data-ttu-id="d2285-108">Permet au débogueur de fournir un handle à un module qui peut être utilisé pour charger une bibliothèque de débogage.</span><span class="sxs-lookup"><span data-stu-id="d2285-108">Allows the debugger to provide a handle to a module which can be used to load a debug library.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d2285-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2285-109">Requirements</span></span>  
 <span data-ttu-id="d2285-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d2285-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2285-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d2285-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d2285-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2285-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2285-113">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2285-113">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2285-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2285-114">See Also</span></span>  
 [<span data-ttu-id="d2285-115">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d2285-115">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="d2285-116">Débogage</span><span class="sxs-lookup"><span data-stu-id="d2285-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
