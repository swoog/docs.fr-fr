---
title: ICLRHostProtectionManager, interface
ms.date: 03/30/2017
api_name:
- ICLRHostProtectionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRHostProtectionManager
helpviewer_keywords:
- ICLRHostProtectionManager interface [.NET Framework hosting]
ms.assetid: ce2770ae-23d0-45d9-8bcf-46504ac5020e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd096344c987d8901f0baab86e370abbb03528e5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177773"
---
# <a name="iclrhostprotectionmanager-interface"></a><span data-ttu-id="42dfd-102">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="42dfd-102">ICLRHostProtectionManager Interface</span></span>
<span data-ttu-id="42dfd-103">Permet à l’hôte bloquer les classes managées spécifiques, méthodes, propriétés et champs de l’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="42dfd-103">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="42dfd-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42dfd-104">Methods</span></span>  
  
|<span data-ttu-id="42dfd-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="42dfd-105">Method</span></span>|<span data-ttu-id="42dfd-106">Description</span><span class="sxs-lookup"><span data-stu-id="42dfd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="42dfd-107">SetEagerSerializeGrantSets</span><span class="sxs-lookup"><span data-stu-id="42dfd-107">SetEagerSerializeGrantSets</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|<span data-ttu-id="42dfd-108">Fournit une garantie que certaines conditions de concurrence rare qui risquent de langage commun irrécupérable erreurs de runtime (CLR) ne seront jamais surviennent.</span><span class="sxs-lookup"><span data-stu-id="42dfd-108">Provides a guarantee that certain rare race conditions that can cause fatal common language runtime (CLR) errors will never arise.</span></span>|  
|[<span data-ttu-id="42dfd-109">SetProtectedCategories, méthode</span><span class="sxs-lookup"><span data-stu-id="42dfd-109">SetProtectedCategories Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md)|<span data-ttu-id="42dfd-110">Spécifie les catégories de types managés et les membres qui ne doivent pas recevoir en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="42dfd-110">Specifies the categories of managed types and members that should be blocked from running in partially trusted code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="42dfd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42dfd-111">Requirements</span></span>  
 <span data-ttu-id="42dfd-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="42dfd-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42dfd-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="42dfd-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="42dfd-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="42dfd-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="42dfd-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="42dfd-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="42dfd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42dfd-116">See also</span></span>

- [<span data-ttu-id="42dfd-117">EApiCategories, énumération</span><span class="sxs-lookup"><span data-stu-id="42dfd-117">EApiCategories Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)
- [<span data-ttu-id="42dfd-118">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="42dfd-118">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
