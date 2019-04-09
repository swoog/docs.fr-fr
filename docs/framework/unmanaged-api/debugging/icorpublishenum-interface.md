---
title: ICorPublishEnum, interface
ms.date: 03/30/2017
api_name:
- ICorPublishEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishEnum
helpviewer_keywords:
- ICorPublishEnum interface [.NET Framework debugging]
ms.assetid: 76a136b5-e444-417a-8ade-f1596d597dc7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1eac0b9fe252e476f8ff781f2181a203886d3beb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59160132"
---
# <a name="icorpublishenum-interface"></a><span data-ttu-id="e7c23-102">ICorPublishEnum, interface</span><span class="sxs-lookup"><span data-stu-id="e7c23-102">ICorPublishEnum Interface</span></span>
<span data-ttu-id="e7c23-103">Sert de l’interface de base abstraite pour les énumérateurs qui sont utilisés dans la publication d’informations sur les processus et domaines d’application.</span><span class="sxs-lookup"><span data-stu-id="e7c23-103">Serves as the abstract base interface for the enumerators that are used in the publishing of information about processes and application domains.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e7c23-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e7c23-104">Methods</span></span>  
  
|<span data-ttu-id="e7c23-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e7c23-105">Method</span></span>|<span data-ttu-id="e7c23-106">Description</span><span class="sxs-lookup"><span data-stu-id="e7c23-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e7c23-107">Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="e7c23-107">Clone Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-clone-method.md)|<span data-ttu-id="e7c23-108">Crée une copie de cet `ICorPublishEnum` objet.</span><span class="sxs-lookup"><span data-stu-id="e7c23-108">Creates a copy of this `ICorPublishEnum` object.</span></span>|  
|[<span data-ttu-id="e7c23-109">GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="e7c23-109">GetCount Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-getcount-method.md)|<span data-ttu-id="e7c23-110">Obtient le nombre d’éléments dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e7c23-110">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="e7c23-111">Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="e7c23-111">Reset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-reset-method.md)|<span data-ttu-id="e7c23-112">Place le curseur au début de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e7c23-112">Moves the cursor of to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="e7c23-113">Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="e7c23-113">Skip Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishenum-skip-method.md)|<span data-ttu-id="e7c23-114">Déplace le curseur vers l’avant dans l’énumération par le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="e7c23-114">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7c23-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e7c23-115">Remarks</span></span>  
 <span data-ttu-id="e7c23-116">Les énumérateurs suivants dérivent `ICorPublishEnum`:</span><span class="sxs-lookup"><span data-stu-id="e7c23-116">The following enumerators derive from `ICorPublishEnum`:</span></span>  
  
-   [<span data-ttu-id="e7c23-117">ICorPublishAppDomainEnum</span><span class="sxs-lookup"><span data-stu-id="e7c23-117">ICorPublishAppDomainEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md)  
  
-   [<span data-ttu-id="e7c23-118">ICorPublishProcessEnum</span><span class="sxs-lookup"><span data-stu-id="e7c23-118">ICorPublishProcessEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocessenum-interface.md)  
  
## <a name="requirements"></a><span data-ttu-id="e7c23-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7c23-119">Requirements</span></span>  
 <span data-ttu-id="e7c23-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7c23-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7c23-121">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="e7c23-121">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="e7c23-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e7c23-122">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e7c23-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e7c23-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e7c23-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7c23-124">See also</span></span>

- [<span data-ttu-id="e7c23-125">CorpubPublish (coclasse)</span><span class="sxs-lookup"><span data-stu-id="e7c23-125">CorpubPublish Coclass</span></span>](../../../../docs/framework/unmanaged-api/debugging/corpubpublish-coclass.md)
- [<span data-ttu-id="e7c23-126">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e7c23-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
