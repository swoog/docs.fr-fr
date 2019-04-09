---
title: IGCHost::Collect, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.Collect
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- Collect
helpviewer_keywords:
- Collect method, IGCHost interface [.NET Framework hosting]
- IGCHost::Collect method [.NET Framework hosting]
ms.assetid: fc7d9448-3186-494d-9f0d-ea39717e9a82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fdacb454783cfb8f90ea5a73807f0a199e16475d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154776"
---
# <a name="igchostcollect-method"></a><span data-ttu-id="80b32-102">IGCHost::Collect, méthode</span><span class="sxs-lookup"><span data-stu-id="80b32-102">IGCHost::Collect Method</span></span>
<span data-ttu-id="80b32-103">Force une collection pour la génération donnée, quel que soit l’état du garbage collection en cours.</span><span class="sxs-lookup"><span data-stu-id="80b32-103">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80b32-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b32-104">Syntax</span></span>  
  
```  
HRESULT Collect (  
    [in] LONG Generation  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="80b32-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b32-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="80b32-106">[in] La génération sur laquelle effectuer le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="80b32-106">[in] The generation on which to perform the garbage collection.</span></span> <span data-ttu-id="80b32-107">La valeur -1 indique que toutes les générations subiront un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="80b32-107">A value of -1 indicates that all generations will undergo a garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="80b32-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b32-108">Requirements</span></span>  
 <span data-ttu-id="80b32-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="80b32-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="80b32-110">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="80b32-110">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="80b32-111">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="80b32-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="80b32-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="80b32-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="80b32-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b32-113">See also</span></span>

- [<span data-ttu-id="80b32-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="80b32-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
