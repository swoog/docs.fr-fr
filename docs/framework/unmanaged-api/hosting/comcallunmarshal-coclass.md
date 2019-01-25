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
ms.openlocfilehash: 5a404448c45a37d50794ceae9a9bf8ff6af08eeb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574571"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="4ff8f-102">Coclasse ComCallUnmarshal</span><span class="sxs-lookup"><span data-stu-id="4ff8f-102">ComCallUnmarshal Coclass</span></span>
<span data-ttu-id="4ff8f-103">Fournit des interfaces pour gérer le marshaling de pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="4ff8f-103">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ff8f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ff8f-104">Syntax</span></span>  
  
```  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="4ff8f-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4ff8f-105">Interfaces</span></span>  
  
|<span data-ttu-id="4ff8f-106">Interface</span><span class="sxs-lookup"><span data-stu-id="4ff8f-106">Interface</span></span>|<span data-ttu-id="4ff8f-107">Description</span><span class="sxs-lookup"><span data-stu-id="4ff8f-107">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="4ff8f-108">Fournit des méthodes pour créer, de l’initialisation et de gérer un proxy dans un processus client.</span><span class="sxs-lookup"><span data-stu-id="4ff8f-108">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4ff8f-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4ff8f-109">Requirements</span></span>  
 <span data-ttu-id="4ff8f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ff8f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ff8f-111">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="4ff8f-111">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="4ff8f-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4ff8f-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4ff8f-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ff8f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ff8f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ff8f-114">See also</span></span>
- [<span data-ttu-id="4ff8f-115">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="4ff8f-115">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
