---
title: ICorPublish::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorPublish.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish::GetProcess
helpviewer_keywords:
- ICorPublish::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorPublish interface [.NET Framework debugging]
ms.assetid: c5143805-2eb7-45b8-85ed-c8fb34df1084
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 414bc1bbd3578d0707e35fa70fe196b504af9942
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418494"
---
# <a name="icorpublishgetprocess-method"></a><span data-ttu-id="701e3-102">ICorPublish::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="701e3-102">ICorPublish::GetProcess Method</span></span>
<span data-ttu-id="701e3-103">Obtient un [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance qui représente le processus avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="701e3-103">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="701e3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="701e3-104">Syntax</span></span>  
  
```  
HRESULT GetProcess(  
    [in] unsigned              pid,   
    [out] ICorPublishProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="701e3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="701e3-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="701e3-106">[in] L’identificateur du processus.</span><span class="sxs-lookup"><span data-stu-id="701e3-106">[in] The identifier of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="701e3-107">[out] Un pointeur vers l’adresse d’un `ICorPublishProcess` instance qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="701e3-107">[out] A pointer to the address of an `ICorPublishProcess` instance that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="701e3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="701e3-108">Remarks</span></span>  
 <span data-ttu-id="701e3-109">`GetProcess` échoue si le processus n’existe pas ou n’est pas un processus managé qui peut être débogué par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="701e3-109">`GetProcess` fails if the process doesn't exist, or isn't a managed process that can be debugged by the current user.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="701e3-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="701e3-110">Requirements</span></span>  
 <span data-ttu-id="701e3-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="701e3-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="701e3-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="701e3-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="701e3-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="701e3-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="701e3-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="701e3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="701e3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="701e3-115">See Also</span></span>  
 [<span data-ttu-id="701e3-116">ICorPublish, interface</span><span class="sxs-lookup"><span data-stu-id="701e3-116">ICorPublish Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-interface.md)
