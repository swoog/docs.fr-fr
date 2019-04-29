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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61944664"
---
# <a name="iclrhostprotectionmanager-interface"></a><span data-ttu-id="8d3bb-102">ICLRHostProtectionManager, interface</span><span class="sxs-lookup"><span data-stu-id="8d3bb-102">ICLRHostProtectionManager Interface</span></span>
<span data-ttu-id="8d3bb-103">Permet à l’hôte bloquer les classes managées spécifiques, méthodes, propriétés et champs de l’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="8d3bb-103">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8d3bb-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d3bb-104">Methods</span></span>  
  
|<span data-ttu-id="8d3bb-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d3bb-105">Method</span></span>|<span data-ttu-id="8d3bb-106">Description</span><span class="sxs-lookup"><span data-stu-id="8d3bb-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8d3bb-107">SetEagerSerializeGrantSets</span><span class="sxs-lookup"><span data-stu-id="8d3bb-107">SetEagerSerializeGrantSets</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-seteagerserializegrantsets-method.md)|<span data-ttu-id="8d3bb-108">Fournit une garantie que certaines conditions de concurrence rare qui risquent de langage commun irrécupérable erreurs de runtime (CLR) ne seront jamais surviennent.</span><span class="sxs-lookup"><span data-stu-id="8d3bb-108">Provides a guarantee that certain rare race conditions that can cause fatal common language runtime (CLR) errors will never arise.</span></span>|  
|[<span data-ttu-id="8d3bb-109">SetProtectedCategories, méthode</span><span class="sxs-lookup"><span data-stu-id="8d3bb-109">SetProtectedCategories Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrhostprotectionmanager-setprotectedcategories-method.md)|<span data-ttu-id="8d3bb-110">Spécifie les catégories de types managés et les membres qui ne doivent pas recevoir en cours d’exécution dans du code partiellement fiable.</span><span class="sxs-lookup"><span data-stu-id="8d3bb-110">Specifies the categories of managed types and members that should be blocked from running in partially trusted code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8d3bb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d3bb-111">Requirements</span></span>  
 <span data-ttu-id="8d3bb-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8d3bb-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d3bb-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8d3bb-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8d3bb-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8d3bb-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8d3bb-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d3bb-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d3bb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d3bb-116">See also</span></span>

- [<span data-ttu-id="8d3bb-117">EApiCategories, énumération</span><span class="sxs-lookup"><span data-stu-id="8d3bb-117">EApiCategories Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eapicategories-enumeration.md)
- [<span data-ttu-id="8d3bb-118">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="8d3bb-118">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
