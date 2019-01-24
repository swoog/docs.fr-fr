---
title: Coclasse CLRRuntimeHost
ms.date: 03/30/2017
api_name:
- CLRRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLRRuntimeHost
helpviewer_keywords:
- CLRRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 2ac9cbf5-8a2d-4e4f-8831-0dad8ef0a897
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e40f08a3dae6f17617e97e07a23b9d7eb611083
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558629"
---
# <a name="clrruntimehost-coclass"></a><span data-ttu-id="a231d-102">Coclasse CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="a231d-102">CLRRuntimeHost Coclass</span></span>
<span data-ttu-id="a231d-103">Fournit des interfaces pour la gestion de l’exécution de code par le runtime.</span><span class="sxs-lookup"><span data-stu-id="a231d-103">Provides interfaces for managing code execution by the runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a231d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a231d-104">Syntax</span></span>  
  
```  
coclass CLRRuntimeHost {  
    [default] interface  ICLRRuntimeHost;  
    interface            ICLRValidator;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="a231d-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a231d-105">Interfaces</span></span>  
  
|<span data-ttu-id="a231d-106">Interface</span><span class="sxs-lookup"><span data-stu-id="a231d-106">Interface</span></span>|<span data-ttu-id="a231d-107">Description</span><span class="sxs-lookup"><span data-stu-id="a231d-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="a231d-108">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="a231d-108">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)|<span data-ttu-id="a231d-109">Fournit des méthodes pour contrôler l’exécution d’applications par le runtime.</span><span class="sxs-lookup"><span data-stu-id="a231d-109">Provides methods for controlling the execution of applications by the runtime.</span></span>|  
|[<span data-ttu-id="a231d-110">ICLRValidator, interface</span><span class="sxs-lookup"><span data-stu-id="a231d-110">ICLRValidator Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrvalidator-interface.md)|<span data-ttu-id="a231d-111">Fournit des méthodes pour la validation d’images exécutables portables et pour un rapport détaillé des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="a231d-111">Provides methods for validation of portable executable images and for detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a231d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a231d-112">Requirements</span></span>  
 <span data-ttu-id="a231d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a231d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a231d-114">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="a231d-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="a231d-115">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a231d-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a231d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a231d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a231d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a231d-117">See also</span></span>
- [<span data-ttu-id="a231d-118">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a231d-118">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
