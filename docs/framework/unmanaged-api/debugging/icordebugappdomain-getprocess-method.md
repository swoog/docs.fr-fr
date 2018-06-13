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
ms.openlocfilehash: d172af14aba418d6e97fe77724bf91b0eaf1c56a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403112"
---
# <a name="icordebugappdomaingetprocess-method"></a><span data-ttu-id="1335a-102">ICorDebugAppDomain::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="1335a-102">ICorDebugAppDomain::GetProcess Method</span></span>
<span data-ttu-id="1335a-103">Obtient le processus qui contient le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="1335a-103">Gets the process containing the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1335a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1335a-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1335a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1335a-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="1335a-106">[out] Pointeur vers l’adresse d’un objet ICorDebugProcess qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="1335a-106">[out] A pointer to the address of an ICorDebugProcess object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1335a-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1335a-107">Requirements</span></span>  
 <span data-ttu-id="1335a-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1335a-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1335a-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1335a-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1335a-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1335a-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1335a-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1335a-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
