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
ms.openlocfilehash: c630fcd4667c8b19c4e21335549674d32508e439
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432834"
---
# <a name="iclrhostprotectionmanager-interface"></a><span data-ttu-id="d304a-102">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="d304a-102">ICLRHostProtectionManager Interface</span></span>
<span data-ttu-id="d304a-103">Permet à l’hôte bloquer les classes managées spécifiques, les méthodes, les propriétés et les champs de l’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="d304a-103">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d304a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d304a-104">Methods</span></span>  
  
|<span data-ttu-id="d304a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d304a-105">Method</span></span>|<span data-ttu-id="d304a-106">Description</span><span class="sxs-lookup"><span data-stu-id="d304a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d304a-107">SetEagerSerializeGrantSets</span><span class="sxs-lookup"><span data-stu-id="d304a-107">SetEagerSerializeGrantSets</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|<span data-ttu-id="d304a-108">Fournit une garantie que certaines conditions de concurrence peuvent erreurs irrécupérable langage common runtime (CLR) ne seront jamais se produire.</span><span class="sxs-lookup"><span data-stu-id="d304a-108">Provides a guarantee that certain rare race conditions that can cause fatal common language runtime (CLR) errors will never arise.</span></span>|  
|[<span data-ttu-id="d304a-109">SetProtectedCategories, méthode</span><span class="sxs-lookup"><span data-stu-id="d304a-109">SetProtectedCategories Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md)|<span data-ttu-id="d304a-110">Spécifie les catégories de types managés et les membres qui ne doivent pas recevoir de s’exécuter dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="d304a-110">Specifies the categories of managed types and members that should be blocked from running in partially trusted code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d304a-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d304a-111">Requirements</span></span>  
 <span data-ttu-id="d304a-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d304a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d304a-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d304a-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d304a-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d304a-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d304a-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d304a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d304a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d304a-116">See Also</span></span>  
 [<span data-ttu-id="d304a-117">EApiCategories, énumération</span><span class="sxs-lookup"><span data-stu-id="d304a-117">EApiCategories Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)  
 [<span data-ttu-id="d304a-118">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="d304a-118">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
