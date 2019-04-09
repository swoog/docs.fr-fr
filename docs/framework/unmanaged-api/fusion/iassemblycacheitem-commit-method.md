---
title: IAssemblyCacheItem::Commit, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.Commit
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::Commit
helpviewer_keywords:
- IAssemblyCacheItem::Commit method [.NET Framework fusion]
- Commit method, IAssemblyCacheItem interface [.NET Framework fusion]
ms.assetid: c2321f17-f46f-4815-ae41-b28678753613
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3757eee4c013ccf4f0f6d21ef64a92a5ffd70f19
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59074311"
---
# <a name="iassemblycacheitemcommit-method"></a><span data-ttu-id="efd7d-102">IAssemblyCacheItem::Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="efd7d-102">IAssemblyCacheItem::Commit Method</span></span>
<span data-ttu-id="efd7d-103">Valide la référence d’assembly mis en cache dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="efd7d-103">Commits the cached assembly reference to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efd7d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efd7d-104">Syntax</span></span>  
  
```  
HRESULT Commit (  
    [in] DWORD dwFlags,   
    [out, optional] ULONG *pulDisposition  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="efd7d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efd7d-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="efd7d-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="efd7d-106">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pulDisposition`  
 <span data-ttu-id="efd7d-107">[out, optional] Une valeur qui indique le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="efd7d-107">[out, optional] A value that indicates the result of the operation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efd7d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efd7d-108">Requirements</span></span>  
 <span data-ttu-id="efd7d-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="efd7d-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="efd7d-110">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="efd7d-110">**Header:** Fusion.h</span></span>  
  
 **<span data-ttu-id="efd7d-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="efd7d-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="efd7d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd7d-112">See also</span></span>

- [<span data-ttu-id="efd7d-113">IAssemblyCacheItem, interface</span><span class="sxs-lookup"><span data-stu-id="efd7d-113">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
