---
title: ICorDebugAppDomainEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomainEnum::Next method
helpviewer_keywords:
- ICorDebugAppDomainEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugAppDomainEnum interface [.NET Framework debugging]
ms.assetid: b8d1def7-0ebc-4314-a3a2-fd36a75973e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5fefc933cc84fede1f3dea16d4b13e09801a96e0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996149"
---
# <a name="icordebugappdomainenumnext-method"></a><span data-ttu-id="0a54b-102">ICorDebugAppDomainEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="0a54b-102">ICorDebugAppDomainEnum::Next Method</span></span>
<span data-ttu-id="0a54b-103">Obtient le nombre spécifié de domaines d’application à partir de la collection, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="0a54b-103">Gets the specified number of application domains from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a54b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a54b-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
                           ICorDebugAppDomain *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a54b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a54b-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="0a54b-106">[in] Le nombre de domaines d’application à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0a54b-106">[in] The number of application domains to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="0a54b-107">[out] Tableau de pointeurs, chacun pointant vers un objet ICorDebugAppDomain qui représente un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="0a54b-107">[out] An array of pointers, each of which points to an ICorDebugAppDomain object that represents an application domain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="0a54b-108">[out] Pointeur vers le nombre de domaines d’application réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="0a54b-108">[out] A pointer to the number of application domains actually returned.</span></span> <span data-ttu-id="0a54b-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="0a54b-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a54b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a54b-110">Requirements</span></span>  
 <span data-ttu-id="0a54b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a54b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a54b-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a54b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a54b-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a54b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a54b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a54b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
