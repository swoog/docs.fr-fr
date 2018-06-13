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
ms.openlocfilehash: bce005a677dcb74c176a6dddfb2726f6b1fd0e8a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436905"
---
# <a name="igchostcollect-method"></a><span data-ttu-id="d8b28-102">IGCHost::Collect, méthode</span><span class="sxs-lookup"><span data-stu-id="d8b28-102">IGCHost::Collect Method</span></span>
<span data-ttu-id="d8b28-103">Force une collection pour la génération donnée, quel que soit l’état du garbage collection en cours.</span><span class="sxs-lookup"><span data-stu-id="d8b28-103">Forces a collection to occur for the given generation, regardless of the state of the current garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8b28-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b28-104">Syntax</span></span>  
  
```  
HRESULT Collect (  
    [in] LONG Generation  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d8b28-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b28-105">Parameters</span></span>  
 `Generation`  
 <span data-ttu-id="d8b28-106">[in] La génération sur laquelle effectuer le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d8b28-106">[in] The generation on which to perform the garbage collection.</span></span> <span data-ttu-id="d8b28-107">La valeur -1 indique que toutes les générations subiront un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d8b28-107">A value of -1 indicates that all generations will undergo a garbage collection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8b28-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8b28-108">Requirements</span></span>  
 <span data-ttu-id="d8b28-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8b28-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8b28-110">**En-tête :** GCHost.idl, GCHost.h</span><span class="sxs-lookup"><span data-stu-id="d8b28-110">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="d8b28-111">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d8b28-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d8b28-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8b28-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8b28-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b28-113">See Also</span></span>  
 [<span data-ttu-id="d8b28-114">IGCHost, interface</span><span class="sxs-lookup"><span data-stu-id="d8b28-114">IGCHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
