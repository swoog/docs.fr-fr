---
title: ICorDebugMetaDataLocator, interface
ms.date: 03/30/2017
api_name:
- ICorDebugMetaDataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMetaDataLocator
helpviewer_keywords:
- ICorDebugMetaDataLocator interface [.NET Framework debugging]
ms.assetid: 287f5ecd-863f-4090-a615-077859f0257b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c1ee52e993859963984f7468e41a5daf3a77ba26
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621667"
---
# <a name="icordebugmetadatalocator-interface"></a><span data-ttu-id="cda42-102">ICorDebugMetaDataLocator, interface</span><span class="sxs-lookup"><span data-stu-id="cda42-102">ICorDebugMetaDataLocator Interface</span></span>
<span data-ttu-id="cda42-103">Fournit des informations de métadonnées au débogueur.</span><span class="sxs-lookup"><span data-stu-id="cda42-103">Provides metadata information to the debugger.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cda42-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cda42-104">Methods</span></span>  
  
|<span data-ttu-id="cda42-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="cda42-105">Method</span></span>|<span data-ttu-id="cda42-106">Description</span><span class="sxs-lookup"><span data-stu-id="cda42-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cda42-107">GetMetaData, méthode</span><span class="sxs-lookup"><span data-stu-id="cda42-107">GetMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmetadatalocator-getmetadata-method.md)|<span data-ttu-id="cda42-108">Indique au débogueur de retourner le chemin d’accès complet à un module dont les métadonnées sont nécessaires pour effectuer une opération demandée par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="cda42-108">Asks the debugger to return the full path to a module whose metadata is needed to complete an operation the debugger requested.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cda42-109">Notes</span><span class="sxs-lookup"><span data-stu-id="cda42-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cda42-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="cda42-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cda42-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cda42-111">Requirements</span></span>  
 <span data-ttu-id="cda42-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cda42-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cda42-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cda42-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cda42-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cda42-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cda42-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cda42-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cda42-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cda42-116">See also</span></span>
- [<span data-ttu-id="cda42-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="cda42-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="cda42-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="cda42-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
