---
title: ICorPublishAppDomainEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomainEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomainEnum::Next
helpviewer_keywords:
- Next method, ICorPublishAppDomainEnum interface [.NET Framework debugging]
- ICorPublishAppDomainEnum::Next method [.NET Framework debugging]
ms.assetid: ad37cd10-0339-4d08-9b0e-4b3428bb4dc3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c14d364320c82f061ef606a402563dacfce28139
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986646"
---
# <a name="icorpublishappdomainenumnext-method"></a><span data-ttu-id="45ad2-102">ICorPublishAppDomainEnum::Next, méthode</span><span class="sxs-lookup"><span data-stu-id="45ad2-102">ICorPublishAppDomainEnum::Next Method</span></span>
<span data-ttu-id="45ad2-103">Obtient le nombre spécifié de domaines d’application qui existent actuellement dans le processus, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="45ad2-103">Gets the specified number of application domains that currently exist in the process, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45ad2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45ad2-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]   
        ICorPublishAppDomain **objects,  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="45ad2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45ad2-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="45ad2-106">[in] Le nombre d’éléments à récupérer.</span><span class="sxs-lookup"><span data-stu-id="45ad2-106">[in] The number of elements to be retrieved.</span></span>  
  
 `objects`  
 <span data-ttu-id="45ad2-107">[out] Extrait un pointeur vers le tableau de [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objets, chacun d’eux représente un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="45ad2-107">[out] A pointer to the array of retrieved [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md) objects, each of which represents an application domain.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="45ad2-108">[out] Pointeur vers le nombre de domaines d’application réellement retournés.</span><span class="sxs-lookup"><span data-stu-id="45ad2-108">[out] Pointer to the number of application domains actually returned.</span></span> <span data-ttu-id="45ad2-109">Cette valeur peut être null si `celt` fait partie.</span><span class="sxs-lookup"><span data-stu-id="45ad2-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45ad2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45ad2-110">Requirements</span></span>  
 <span data-ttu-id="45ad2-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="45ad2-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45ad2-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="45ad2-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="45ad2-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45ad2-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45ad2-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45ad2-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45ad2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45ad2-115">See also</span></span>

- [<span data-ttu-id="45ad2-116">ICorPublishAppDomainEnum, interface</span><span class="sxs-lookup"><span data-stu-id="45ad2-116">ICorPublishAppDomainEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md)
