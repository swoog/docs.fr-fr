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
ms.openlocfilehash: 91acfa5545f3115c9e95207f05708ff32530994f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437279"
---
# <a name="idebuggerinfoisdebuggerattached-method"></a><span data-ttu-id="a86ac-102">IDebuggerInfo::IsDebuggerAttached, méthode</span><span class="sxs-lookup"><span data-stu-id="a86ac-102">IDebuggerInfo::IsDebuggerAttached Method</span></span>
<span data-ttu-id="a86ac-103">Obtient une valeur qui indique si un débogueur managé est attaché à ce processus.</span><span class="sxs-lookup"><span data-stu-id="a86ac-103">Gets a value that indicates whether a managed debugger is attached to this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a86ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a86ac-104">Syntax</span></span>  
  
```  
HRESULT IsDebuggerAttached (  
    [out] BOOL *pbAttached  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a86ac-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a86ac-105">Parameters</span></span>  
 `pbAttached`  
 <span data-ttu-id="a86ac-106">[out] Un pointeur vers une valeur qui est `true` si un débogueur managé est attaché au processus ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="a86ac-106">[out] A pointer to a value that is `true` if a managed debugger is attached to the process; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a86ac-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a86ac-107">Requirements</span></span>  
 <span data-ttu-id="a86ac-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a86ac-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a86ac-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a86ac-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a86ac-110">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a86ac-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a86ac-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a86ac-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a86ac-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a86ac-112">See Also</span></span>  
 [<span data-ttu-id="a86ac-113">IDebuggerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="a86ac-113">IDebuggerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)
