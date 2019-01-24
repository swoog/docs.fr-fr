---
title: CoInitializeCor, fonction
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 438f2f58a4ce61d1757238fc46674611e4d677dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508533"
---
# <a name="coinitializecor-function"></a><span data-ttu-id="484da-102">CoInitializeCor, fonction</span><span class="sxs-lookup"><span data-stu-id="484da-102">CoInitializeCor Function</span></span>
<span data-ttu-id="484da-103">`CoInitializeCor` est obsolète.</span><span class="sxs-lookup"><span data-stu-id="484da-103">`CoInitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="484da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="484da-104">Syntax</span></span>  
  
```  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="484da-105">Notes</span><span class="sxs-lookup"><span data-stu-id="484da-105">Remarks</span></span>  
 <span data-ttu-id="484da-106">Pour initialiser le common language runtime, utilisez soit [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) ou [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span><span class="sxs-lookup"><span data-stu-id="484da-106">To initialize the common language runtime, use either [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="484da-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="484da-107">Requirements</span></span>  
 <span data-ttu-id="484da-108">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="484da-108">**Header:** Cor.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="484da-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="484da-109">See also</span></span>
- [<span data-ttu-id="484da-110">Fonctions statiques globales des métadonnées</span><span class="sxs-lookup"><span data-stu-id="484da-110">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
