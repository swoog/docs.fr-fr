---
title: ICorDebugAppDomain::GetId, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetId
helpviewer_keywords:
- GetId method, ICorDebugAppDomain interface [.NET Framework debugging]
- ICorDebugAppDomain::GetId method [.NET Framework debugging]
ms.assetid: 32c27576-71fa-42ee-8230-67b92913ea08
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8122f1b5017faac3425d59d12d77f84180134d65
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401627"
---
# <a name="icordebugappdomaingetid-method"></a><span data-ttu-id="10ce2-102">ICorDebugAppDomain::GetId, méthode</span><span class="sxs-lookup"><span data-stu-id="10ce2-102">ICorDebugAppDomain::GetId Method</span></span>
<span data-ttu-id="10ce2-103">Obtient l’identificateur unique du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="10ce2-103">Gets the unique identifier of the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10ce2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10ce2-104">Syntax</span></span>  
  
```  
HRESULT GetID (  
    [out] ULONG32   *pId  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="10ce2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10ce2-105">Parameters</span></span>  
 `pId`  
 <span data-ttu-id="10ce2-106">[out] Identificateur unique du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="10ce2-106">[out] The unique identifier of the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="10ce2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="10ce2-107">Remarks</span></span>  
 <span data-ttu-id="10ce2-108">L’identificateur du domaine d’application est unique au sein du processus de conteneur.</span><span class="sxs-lookup"><span data-stu-id="10ce2-108">The identifier for the application domain is unique within the containing process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10ce2-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="10ce2-109">Requirements</span></span>  
 <span data-ttu-id="10ce2-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="10ce2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10ce2-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="10ce2-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="10ce2-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="10ce2-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="10ce2-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10ce2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
