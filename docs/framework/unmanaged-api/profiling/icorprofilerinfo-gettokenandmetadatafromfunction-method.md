---
title: ICorProfilerInfo::GetTokenAndMetadataFromFunction, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetTokenAndMetadataFromFunction
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction
helpviewer_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction method [.NET Framework profiling]
- GetTokenAndMetadataFromFunction method [.NET Framework profiling]
ms.assetid: e525aa16-c923-4b16-833b-36f1f0dd70fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0561f76c70da603d50b96ce5b5162efac4eff2de
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54492975"
---
# <a name="icorprofilerinfogettokenandmetadatafromfunction-method"></a><span data-ttu-id="77ff4-102">ICorProfilerInfo::GetTokenAndMetadataFromFunction, méthode</span><span class="sxs-lookup"><span data-stu-id="77ff4-102">ICorProfilerInfo::GetTokenAndMetadataFromFunction Method</span></span>
<span data-ttu-id="77ff4-103">Obtient le jeton de métadonnées et une instance d’interface de métadonnées qui permettre être utilisée avec le jeton pour la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77ff4-103">Gets the metadata token and a metadata interface instance that can be used against the token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77ff4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77ff4-104">Syntax</span></span>  
  
```  
HRESULT GetTokenAndMetaDataFromFunction(  
    [in]  FunctionID functionId,  
    [in]  REFIID     riid,  
    [out] IUnknown   **ppImport,  
    [out] mdToken    *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="77ff4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77ff4-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="77ff4-106">[in] L’ID de la fonction pour laquelle obtenir le jeton de métadonnées et l’interface de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="77ff4-106">[in] The ID of the function for which to get the metadata token and metadata interface.</span></span>  
  
 `riid`  
 <span data-ttu-id="77ff4-107">[in] L’ID de référence de l’interface de métadonnées pour obtenir l’instance de.</span><span class="sxs-lookup"><span data-stu-id="77ff4-107">[in] The reference ID of the metadata interface to get the instance of.</span></span>  
  
 `ppImport`  
 <span data-ttu-id="77ff4-108">[out] Pointeur vers l’adresse de l’instance d’interface de métadonnées qui permettre être utilisé avec le jeton pour la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77ff4-108">[out] A pointer to the address of the metadata interface instance that can be used against the token for the specified function.</span></span>  
  
 `pToken`  
 <span data-ttu-id="77ff4-109">[out] Pointeur vers le jeton de métadonnées pour la fonction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77ff4-109">[out] A pointer to the metadata token for the specified function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77ff4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77ff4-110">Requirements</span></span>  
 <span data-ttu-id="77ff4-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77ff4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77ff4-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="77ff4-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="77ff4-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="77ff4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="77ff4-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77ff4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77ff4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77ff4-115">See also</span></span>
- [<span data-ttu-id="77ff4-116">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="77ff4-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
