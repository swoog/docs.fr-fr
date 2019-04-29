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
ms.openlocfilehash: 8bae2d134c412023d0f126453b5285662d994c78
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61789595"
---
# <a name="clrruntimehost-coclass"></a><span data-ttu-id="c85ed-102">Coclasse CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="c85ed-102">CLRRuntimeHost Coclass</span></span>
<span data-ttu-id="c85ed-103">Fournit des interfaces pour la gestion de l’exécution de code par le runtime.</span><span class="sxs-lookup"><span data-stu-id="c85ed-103">Provides interfaces for managing code execution by the runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c85ed-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c85ed-104">Syntax</span></span>  
  
```  
coclass CLRRuntimeHost {  
    [default] interface  ICLRRuntimeHost;  
    interface            ICLRValidator;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="c85ed-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="c85ed-105">Interfaces</span></span>  
  
|<span data-ttu-id="c85ed-106">Interface</span><span class="sxs-lookup"><span data-stu-id="c85ed-106">Interface</span></span>|<span data-ttu-id="c85ed-107">Description</span><span class="sxs-lookup"><span data-stu-id="c85ed-107">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="c85ed-108">ICLRRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="c85ed-108">ICLRRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)|<span data-ttu-id="c85ed-109">Fournit des méthodes pour contrôler l’exécution d’applications par le runtime.</span><span class="sxs-lookup"><span data-stu-id="c85ed-109">Provides methods for controlling the execution of applications by the runtime.</span></span>|  
|[<span data-ttu-id="c85ed-110">ICLRValidator, interface</span><span class="sxs-lookup"><span data-stu-id="c85ed-110">ICLRValidator Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrvalidator-interface.md)|<span data-ttu-id="c85ed-111">Fournit des méthodes pour la validation d’images exécutables portables et pour un rapport détaillé des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="c85ed-111">Provides methods for validation of portable executable images and for detailed reporting of validation errors.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c85ed-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c85ed-112">Requirements</span></span>  
 <span data-ttu-id="c85ed-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c85ed-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c85ed-114">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="c85ed-114">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="c85ed-115">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c85ed-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c85ed-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c85ed-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c85ed-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c85ed-117">See also</span></span>

- [<span data-ttu-id="c85ed-118">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="c85ed-118">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
