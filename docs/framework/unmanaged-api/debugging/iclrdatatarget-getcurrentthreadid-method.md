---
title: ICLRDataTarget::GetCurrentThreadID, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetCurrentThreadID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetCurrentThreadID
helpviewer_keywords:
- GetCurrentThreadID method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::GetCurrentThreadID method [.NET Framework debugging]
ms.assetid: dc9a0a6c-d592-4fb7-86ed-62684da3b0e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9687f6139d67a2387091367c2c72167e03be4eee
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080655"
---
# <a name="iclrdatatargetgetcurrentthreadid-method"></a><span data-ttu-id="d6df9-102">ICLRDataTarget::GetCurrentThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="d6df9-102">ICLRDataTarget::GetCurrentThreadID Method</span></span>
<span data-ttu-id="d6df9-103">Obtient l’identificateur de système d’exploitation pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="d6df9-103">Gets the operating system identifier for the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6df9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6df9-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentThreadID (  
    [out] ULONG32    *threadID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6df9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6df9-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="d6df9-106">[out] Un pointeur vers l’identificateur de système d’exploitation du thread actuel pour le processus cible.</span><span class="sxs-lookup"><span data-stu-id="d6df9-106">[out] A pointer to the operating system identifier of the current thread for the target process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d6df9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d6df9-107">Remarks</span></span>  
 <span data-ttu-id="d6df9-108">S’il n’existe aucun thread actuel pour le processus cible, le `GetCurrentThreadID` méthode peut échouer.</span><span class="sxs-lookup"><span data-stu-id="d6df9-108">If there is no current thread for the target process, the `GetCurrentThreadID` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d6df9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6df9-109">Requirements</span></span>  
 <span data-ttu-id="d6df9-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d6df9-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6df9-111">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="d6df9-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="d6df9-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d6df9-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d6df9-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6df9-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6df9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6df9-114">See also</span></span>

- [<span data-ttu-id="d6df9-115">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="d6df9-115">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
