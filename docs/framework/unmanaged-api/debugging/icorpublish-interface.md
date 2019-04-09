---
title: ICorPublish, interface
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7581d68f5c2b575403ddc84d06147f012e7ab39e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076339"
---
# <a name="icorpublish-interface"></a><span data-ttu-id="92532-102">ICorPublish, interface</span><span class="sxs-lookup"><span data-stu-id="92532-102">ICorPublish Interface</span></span>
<span data-ttu-id="92532-103">Sert d’interface générale pour la publication d’informations sur les processus et des informations sur les domaines d’application dans ces processus.</span><span class="sxs-lookup"><span data-stu-id="92532-103">Serves as the general interface for publishing information about processes and information about the application domains in those processes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="92532-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92532-104">Methods</span></span>  
  
|<span data-ttu-id="92532-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="92532-105">Method</span></span>|<span data-ttu-id="92532-106">Description</span><span class="sxs-lookup"><span data-stu-id="92532-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="92532-107">EnumProcesses, méthode</span><span class="sxs-lookup"><span data-stu-id="92532-107">EnumProcesses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)|<span data-ttu-id="92532-108">Obtient un [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance qui contient les processus gérés en cours d’exécution sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92532-108">Gets an [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance that contains the managed processes running on this computer.</span></span>|  
|[<span data-ttu-id="92532-109">GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="92532-109">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-getprocess-method.md)|<span data-ttu-id="92532-110">Obtient un [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance qui représente le processus avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="92532-110">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="92532-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92532-111">Requirements</span></span>  
 <span data-ttu-id="92532-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="92532-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="92532-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="92532-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="92532-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="92532-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="92532-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="92532-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="92532-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92532-116">See also</span></span>

- [<span data-ttu-id="92532-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="92532-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="92532-118">CorpubPublish (coclasse)</span><span class="sxs-lookup"><span data-stu-id="92532-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
