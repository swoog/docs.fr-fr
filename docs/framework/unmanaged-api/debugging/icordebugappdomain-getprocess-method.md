---
title: ICorDebugAppDomain::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebugAppDomain interface [.NET Framework debugging]
- ICorDebugAppDomain::GetProcess method [.NET Framework debugging]
ms.assetid: 9d0b9628-a91c-40d0-b9bc-00b34a396b8f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b05c35c810630897e4a7bd28e1cbe8cedefefb1f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61996201"
---
# <a name="icordebugappdomaingetprocess-method"></a><span data-ttu-id="a4689-102">ICorDebugAppDomain::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="a4689-102">ICorDebugAppDomain::GetProcess Method</span></span>
<span data-ttu-id="a4689-103">Obtient le processus contenant le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="a4689-103">Gets the process containing the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4689-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4689-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4689-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4689-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="a4689-106">[out] Pointeur vers l’adresse d’un objet ICorDebugProcess qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="a4689-106">[out] A pointer to the address of an ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4689-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4689-107">Requirements</span></span>  
 <span data-ttu-id="a4689-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4689-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4689-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a4689-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a4689-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a4689-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a4689-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4689-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
