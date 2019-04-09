---
title: ICorPublishAppDomainEnum, interface
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum
helpviewer_keywords:
- ICorPublishAppDomainEnum interface [.NET Framework debugging]
ms.assetid: bb798c56-042e-475d-a245-b6fac36d0c07
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f6d4af7c01f91dff77d6ba715ef845f523c7fb6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090028"
---
# <a name="icorpublishappdomainenum-interface"></a><span data-ttu-id="b8a9d-102">ICorPublishAppDomainEnum, interface</span><span class="sxs-lookup"><span data-stu-id="b8a9d-102">ICorPublishAppDomainEnum Interface</span></span>
<span data-ttu-id="b8a9d-103">Une sous-classe de la [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface qui fournit des méthodes pour parcourir une collection de [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) les objets qui existent actuellement dans un processus.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-103">A subclass of the [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md) interface that provides methods to traverse a collection of [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objects that currently exist within a process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b8a9d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8a9d-104">Methods</span></span>  
  
|<span data-ttu-id="b8a9d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8a9d-105">Method</span></span>|<span data-ttu-id="b8a9d-106">Description</span><span class="sxs-lookup"><span data-stu-id="b8a9d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b8a9d-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="b8a9d-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-next-method.md)|<span data-ttu-id="b8a9d-108">Obtient le nombre spécifié de `ICorPublishAppDomain` instances à partir de la collection, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-108">Gets the specified number of `ICorPublishAppDomain` instances from the collection, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8a9d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b8a9d-109">Remarks</span></span>  
 <span data-ttu-id="b8a9d-110">Le `ICorPublishAppDomainEnum` interface implémente les méthodes de l’interface abstraite, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b8a9d-110">The `ICorPublishAppDomainEnum` interface implements the methods of the abstract interface, [ICorPublishEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-interface.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8a9d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8a9d-111">Requirements</span></span>  
 <span data-ttu-id="b8a9d-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b8a9d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8a9d-113">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="b8a9d-113">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="b8a9d-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8a9d-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="b8a9d-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b8a9d-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b8a9d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8a9d-116">See also</span></span>

- [<span data-ttu-id="b8a9d-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b8a9d-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="b8a9d-118">CorpubPublish (coclasse)</span><span class="sxs-lookup"><span data-stu-id="b8a9d-118">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
