---
title: IApartmentCallback, interface
ms.date: 03/30/2017
api_name:
- IApartmentCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IApartmentCallback
helpviewer_keywords:
- IApartmentCallback interface [.NET Framework hosting]
ms.assetid: 57c33c58-bf0b-4533-b569-e6a682d02cba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: db933716cc0602ecda5da8a72726408ae4910179
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129803"
---
# <a name="iapartmentcallback-interface"></a><span data-ttu-id="04188-102">IApartmentCallback, interface</span><span class="sxs-lookup"><span data-stu-id="04188-102">IApartmentCallback Interface</span></span>
<span data-ttu-id="04188-103">Fournit des méthodes pour effectuer des rappels dans un thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="04188-103">Provides methods for making callbacks within an apartment.</span></span> <span data-ttu-id="04188-104">Un *cloisonnement* est un conteneur logique dans un processus pour les objets qui partagent les mêmes exigences d’accès de thread.</span><span class="sxs-lookup"><span data-stu-id="04188-104">An *apartment* is a logical container within a process for objects that share the same thread access requirements.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="04188-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="04188-105">Methods</span></span>  
  
|<span data-ttu-id="04188-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="04188-106">Method</span></span>|<span data-ttu-id="04188-107">Description</span><span class="sxs-lookup"><span data-stu-id="04188-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="04188-108">DoCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="04188-108">DoCallback Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iapartmentcallback-docallback-method.md)|<span data-ttu-id="04188-109">Exécute la fonction spécifiée dans un thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="04188-109">Executes the specified function within an apartment.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="04188-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04188-110">Requirements</span></span>  
 <span data-ttu-id="04188-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04188-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04188-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="04188-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="04188-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="04188-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="04188-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="04188-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="04188-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04188-115">See also</span></span>

- [<span data-ttu-id="04188-116">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="04188-116">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
