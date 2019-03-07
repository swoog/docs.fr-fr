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
ms.openlocfilehash: cc4ba4f87cd53e12baa0a7cf8b853db0e948201f
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57500384"
---
# <a name="iclrdatatargetgetcurrentthreadid-method"></a><span data-ttu-id="6586b-102">ICLRDataTarget::GetCurrentThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="6586b-102">ICLRDataTarget::GetCurrentThreadID Method</span></span>
<span data-ttu-id="6586b-103">Obtient l’identificateur de système d’exploitation pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="6586b-103">Gets the operating system identifier for the current thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6586b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6586b-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentThreadID (  
    [out] ULONG32    *threadID  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6586b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6586b-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="6586b-106">[out] Un pointeur vers l’identificateur de système d’exploitation du thread actuel pour le processus cible.</span><span class="sxs-lookup"><span data-stu-id="6586b-106">[out] A pointer to the operating system identifier of the current thread for the target process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6586b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6586b-107">Remarks</span></span>  
 <span data-ttu-id="6586b-108">S’il n’existe aucun thread actuel pour le processus cible, le `GetCurrentThreadID` méthode peut échouer.</span><span class="sxs-lookup"><span data-stu-id="6586b-108">If there is no current thread for the target process, the `GetCurrentThreadID` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6586b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6586b-109">Requirements</span></span>  
 <span data-ttu-id="6586b-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6586b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6586b-111">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="6586b-111">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6586b-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6586b-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6586b-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6586b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6586b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6586b-114">See also</span></span>
- [<span data-ttu-id="6586b-115">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="6586b-115">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
