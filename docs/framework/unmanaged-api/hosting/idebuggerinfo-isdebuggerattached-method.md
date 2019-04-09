---
title: IDebuggerInfo::IsDebuggerAttached, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerInfo.IsDebuggerAttached
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IsDebuggerAttached
helpviewer_keywords:
- IDebuggerInfo::IsDebuggerAttached method [.NET Framework hosting]
- IsDebuggerAttached method, IDebuggerInfo interface [.NET Framework hosting]
ms.assetid: 6e21872f-602f-411a-a423-bff5cdf27000
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0708a3b501a99b5f71be5ba4c6cc4ea2b754d12a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191339"
---
# <a name="idebuggerinfoisdebuggerattached-method"></a><span data-ttu-id="625a4-102">IDebuggerInfo::IsDebuggerAttached, méthode</span><span class="sxs-lookup"><span data-stu-id="625a4-102">IDebuggerInfo::IsDebuggerAttached Method</span></span>
<span data-ttu-id="625a4-103">Obtient une valeur qui indique si un débogueur managé est attaché à ce processus.</span><span class="sxs-lookup"><span data-stu-id="625a4-103">Gets a value that indicates whether a managed debugger is attached to this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="625a4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="625a4-104">Syntax</span></span>  
  
```  
HRESULT IsDebuggerAttached (  
    [out] BOOL *pbAttached  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="625a4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="625a4-105">Parameters</span></span>  
 `pbAttached`  
 <span data-ttu-id="625a4-106">[out] Un pointeur vers une valeur qui est `true` si un débogueur managé est attaché au processus ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="625a4-106">[out] A pointer to a value that is `true` if a managed debugger is attached to the process; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="625a4-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="625a4-107">Requirements</span></span>  
 <span data-ttu-id="625a4-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="625a4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="625a4-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="625a4-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="625a4-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="625a4-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="625a4-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="625a4-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="625a4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="625a4-112">See also</span></span>

- [<span data-ttu-id="625a4-113">IDebuggerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="625a4-113">IDebuggerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)
