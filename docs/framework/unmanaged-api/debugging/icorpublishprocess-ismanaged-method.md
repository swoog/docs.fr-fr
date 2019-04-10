---
title: ICorPublishProcess::IsManaged, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 29c5f96bab374d6e2d43424370bff2a4a2ab6df3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218288"
---
# <a name="icorpublishprocessismanaged-method"></a><span data-ttu-id="0bd15-102">ICorPublishProcess::IsManaged, méthode</span><span class="sxs-lookup"><span data-stu-id="0bd15-102">ICorPublishProcess::IsManaged Method</span></span>
<span data-ttu-id="0bd15-103">Obtient une valeur qui indique si le processus référencé par ce [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) ne connaît ont du code managé.</span><span class="sxs-lookup"><span data-stu-id="0bd15-103">Gets a value that indicates whether the process referenced by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) is known to have managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bd15-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd15-104">Syntax</span></span>  
  
```  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0bd15-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bd15-105">Parameters</span></span>  
 `pbManaged`  
 <span data-ttu-id="0bd15-106">[out] Pointeur vers une valeur booléenne qui indique si le processus a du code managé.</span><span class="sxs-lookup"><span data-stu-id="0bd15-106">[out] A pointer to a Boolean value that indicates whether the process has managed code.</span></span> <span data-ttu-id="0bd15-107">La valeur est `true` si le processus a du code managé ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="0bd15-107">The value is `true` if the process has managed code; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0bd15-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0bd15-108">Remarks</span></span>  
 <span data-ttu-id="0bd15-109">Depuis la version actuelle de `ICorPublishProcess` autorise l’accès uniquement aux processus qui ont du code managé, `IsManaged` retourne toujours `true`.</span><span class="sxs-lookup"><span data-stu-id="0bd15-109">Since the current version of `ICorPublishProcess` allows access only to processes that have managed code, `IsManaged` always returns `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0bd15-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bd15-110">Requirements</span></span>  
 <span data-ttu-id="0bd15-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0bd15-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0bd15-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="0bd15-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="0bd15-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0bd15-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0bd15-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0bd15-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0bd15-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bd15-115">See also</span></span>

- [<span data-ttu-id="0bd15-116">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="0bd15-116">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
