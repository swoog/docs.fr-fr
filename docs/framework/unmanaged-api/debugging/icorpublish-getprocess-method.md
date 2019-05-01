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
ms.openlocfilehash: 021068caa8f1ad2c64e5ca3d18ea25dc827563a4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986698"
---
# <a name="icorpublishgetprocess-method"></a><span data-ttu-id="28f17-102">ICorPublish::GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="28f17-102">ICorPublish::GetProcess Method</span></span>
<span data-ttu-id="28f17-103">Obtient un [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance qui représente le processus avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="28f17-103">Gets an [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) instance that represents the process with the specified identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28f17-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28f17-104">Syntax</span></span>  
  
```  
HRESULT GetProcess(  
    [in] unsigned              pid,   
    [out] ICorPublishProcess   **ppProcess  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="28f17-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28f17-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="28f17-106">[in] L’identificateur du processus.</span><span class="sxs-lookup"><span data-stu-id="28f17-106">[in] The identifier of the process.</span></span>  
  
 `ppProcess`  
 <span data-ttu-id="28f17-107">[out] Un pointeur vers l’adresse d’un `ICorPublishProcess` instance qui représente le processus.</span><span class="sxs-lookup"><span data-stu-id="28f17-107">[out] A pointer to the address of an `ICorPublishProcess` instance that represents the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="28f17-108">Notes</span><span class="sxs-lookup"><span data-stu-id="28f17-108">Remarks</span></span>  
 <span data-ttu-id="28f17-109">`GetProcess` échoue si le processus n’existe pas ou n’est pas un processus géré qui peuvent être débogué à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="28f17-109">`GetProcess` fails if the process doesn't exist, or isn't a managed process that can be debugged by the current user.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28f17-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28f17-110">Requirements</span></span>  
 <span data-ttu-id="28f17-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="28f17-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28f17-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="28f17-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="28f17-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28f17-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="28f17-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28f17-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28f17-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28f17-115">See also</span></span>

- [<span data-ttu-id="28f17-116">ICorPublish, interface</span><span class="sxs-lookup"><span data-stu-id="28f17-116">ICorPublish Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublish-interface.md)
