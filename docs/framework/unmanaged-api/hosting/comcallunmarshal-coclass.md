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
ms.openlocfilehash: 2f17a88a90905006432ae8c5dc040277124c947b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59166879"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="a16af-102">Coclasse ComCallUnmarshal</span><span class="sxs-lookup"><span data-stu-id="a16af-102">ComCallUnmarshal Coclass</span></span>
<span data-ttu-id="a16af-103">Fournit des interfaces pour gérer le marshaling de pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="a16af-103">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a16af-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a16af-104">Syntax</span></span>  
  
```  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="a16af-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="a16af-105">Interfaces</span></span>  
  
|<span data-ttu-id="a16af-106">Interface</span><span class="sxs-lookup"><span data-stu-id="a16af-106">Interface</span></span>|<span data-ttu-id="a16af-107">Description</span><span class="sxs-lookup"><span data-stu-id="a16af-107">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="a16af-108">Fournit des méthodes pour créer, de l’initialisation et de gérer un proxy dans un processus client.</span><span class="sxs-lookup"><span data-stu-id="a16af-108">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a16af-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a16af-109">Requirements</span></span>  
 <span data-ttu-id="a16af-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a16af-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a16af-111">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="a16af-111">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="a16af-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a16af-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a16af-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a16af-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a16af-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a16af-114">See also</span></span>

- [<span data-ttu-id="a16af-115">Coclasses d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a16af-115">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
