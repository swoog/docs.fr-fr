---
title: ICorPublishProcess::EnumAppDomains, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.EnumAppDomains
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::EnumAppDomains
helpviewer_keywords:
- EnumAppDomains method [.NET Framework debugging]
- ICorPublishProcess::EnumAppDomains method [.NET Framework debugging]
ms.assetid: 7da621fc-e7d0-4c00-9439-5c93619d7414
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 173a7d6793bec9262efb661d56e3a371d0bf9b47
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986620"
---
# <a name="icorpublishprocessenumappdomains-method"></a><span data-ttu-id="b6e2a-102">ICorPublishProcess::EnumAppDomains, méthode</span><span class="sxs-lookup"><span data-stu-id="b6e2a-102">ICorPublishProcess::EnumAppDomains Method</span></span>
<span data-ttu-id="b6e2a-103">Obtient un énumérateur pour les domaines d’application dans le processus qui est référencé par ce [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-103">Gets an enumerator for the application domains in the process that is referenced by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6e2a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6e2a-104">Syntax</span></span>  
  
```  
HRESULT EnumAppDomains (  
    [out] ICorPublishAppDomainEnum   **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b6e2a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6e2a-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="b6e2a-106">[out] Un pointeur vers l’adresse d’un [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance qui permet l’itération au sein de la collection de domaines d’application dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-106">[out] A pointer to the address of an [ICorPublishAppDomainEnum](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomainenum-interface.md) instance that allows iteration through the collection of application domains in this process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b6e2a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b6e2a-107">Remarks</span></span>  
 <span data-ttu-id="b6e2a-108">La liste des domaines d’application est basée sur un instantané des domaines d’application qui existe lorsque le `EnumAppDomains` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-108">The list of application domains is based on a snapshot of the application domains that exist when the `EnumAppDomains` method is called.</span></span> <span data-ttu-id="b6e2a-109">Cette méthode peut être appelée plusieurs fois pour créer une nouvelle liste à jour.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-109">This method may be called more than once to create a new up-to-date list.</span></span> <span data-ttu-id="b6e2a-110">Listes existantes ne seront pas affectées par les appels suivants de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-110">Existing lists will not be affected by subsequent calls of this method.</span></span>  
  
 <span data-ttu-id="b6e2a-111">Si le processus a été arrêté, `EnumAppDomains` échoue avec une valeur HRESULT de CORDBG_E_PROCESS_TERMINATED.</span><span class="sxs-lookup"><span data-stu-id="b6e2a-111">If the process has been terminated, `EnumAppDomains` will fail with an HRESULT value of CORDBG_E_PROCESS_TERMINATED.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6e2a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6e2a-112">Requirements</span></span>  
 <span data-ttu-id="b6e2a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b6e2a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6e2a-114">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="b6e2a-114">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="b6e2a-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b6e2a-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b6e2a-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6e2a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6e2a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6e2a-117">See also</span></span>

- [<span data-ttu-id="b6e2a-118">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="b6e2a-118">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
