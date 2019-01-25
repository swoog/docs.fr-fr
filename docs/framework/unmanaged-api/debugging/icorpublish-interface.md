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
ms.openlocfilehash: e1dea8cc54c68db333c409e3bd7b3e4211bd52ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54713965"
---
# <a name="icorpublish-interface"></a><span data-ttu-id="2e8bc-102">ICorPublish, interface</span><span class="sxs-lookup"><span data-stu-id="2e8bc-102">ICorPublish Interface</span></span>
<span data-ttu-id="2e8bc-103">Sert d’interface générale pour la publication d’informations sur les processus et des informations sur les domaines d’application dans ces processus.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-103">Serves as the general interface for publishing information about processes and information about the application domains in those processes.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2e8bc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e8bc-104">Methods</span></span>  
  
|<span data-ttu-id="2e8bc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="2e8bc-105">Method</span></span>|<span data-ttu-id="2e8bc-106">Description</span><span class="sxs-lookup"><span data-stu-id="2e8bc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2e8bc-107">EnumProcesses, méthode</span><span class="sxs-lookup"><span data-stu-id="2e8bc-107">EnumProcesses Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-enumprocesses-method.md)|<span data-ttu-id="2e8bc-108">Obtient un [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance qui contient les processus gérés en cours d’exécution sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-108">Gets an [ICorPublishProcessEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md) instance that contains the managed processes running on this computer.</span></span>|  
|[<span data-ttu-id="2e8bc-109">GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="2e8bc-109">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-getprocess-method.md)|<span data-ttu-id="2e8bc-110">Obtient un [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance qui représente le processus avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e8bc-110">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2e8bc-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2e8bc-111">Requirements</span></span>  
 <span data-ttu-id="2e8bc-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2e8bc-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2e8bc-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="2e8bc-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="2e8bc-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2e8bc-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2e8bc-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2e8bc-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e8bc-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e8bc-116">See also</span></span>
- [<span data-ttu-id="2e8bc-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="2e8bc-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="2e8bc-118">CorpubPublish, coclasse</span><span class="sxs-lookup"><span data-stu-id="2e8bc-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
