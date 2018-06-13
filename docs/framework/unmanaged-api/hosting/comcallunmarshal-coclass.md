---
title: Coclasse ComCallUnmarshal
ms.date: 03/30/2017
api_name:
- ComCallUnmarshal Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ComCallUnmarshal
helpviewer_keywords:
- ComCallUnmarshal coclass [.NET Framework hosting]
ms.assetid: 2adb5827-2268-4914-a1c6-f62b61880a45
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7884d53630ca13a30d7b4efd55d46684a9dd7d30
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427640"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="42ccb-102">Coclasse ComCallUnmarshal</span><span class="sxs-lookup"><span data-stu-id="42ccb-102">ComCallUnmarshal Coclass</span></span>
<span data-ttu-id="42ccb-103">Fournit des interfaces pour gérer le marshaling de pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="42ccb-103">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42ccb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42ccb-104">Syntax</span></span>  
  
```  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="42ccb-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="42ccb-105">Interfaces</span></span>  
  
|<span data-ttu-id="42ccb-106">Interface</span><span class="sxs-lookup"><span data-stu-id="42ccb-106">Interface</span></span>|<span data-ttu-id="42ccb-107">Description</span><span class="sxs-lookup"><span data-stu-id="42ccb-107">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="42ccb-108">Fournit des méthodes de création, de l’initialisation et de gérer un proxy dans un processus client.</span><span class="sxs-lookup"><span data-stu-id="42ccb-108">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="42ccb-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42ccb-109">Requirements</span></span>  
 <span data-ttu-id="42ccb-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="42ccb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42ccb-111">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="42ccb-111">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="42ccb-112">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="42ccb-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="42ccb-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42ccb-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42ccb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42ccb-114">See Also</span></span>  
 [<span data-ttu-id="42ccb-115">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="42ccb-115">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
