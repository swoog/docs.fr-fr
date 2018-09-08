---
title: IMetaDataEmit::Merge, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.Merge
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::Merge
helpviewer_keywords:
- IMetaDataEmit::Merge method [.NET Framework metadata]
- Merge method [.NET Framework metadata]
ms.assetid: 7596220c-f699-4b6c-8ae7-c83220610650
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 899f2ca5ef1b987687f5c065ad3e1965e142d103
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216104"
---
# <a name="imetadataemitmerge-method"></a><span data-ttu-id="e5c39-102">IMetaDataEmit::Merge, méthode</span><span class="sxs-lookup"><span data-stu-id="e5c39-102">IMetaDataEmit::Merge Method</span></span>
<span data-ttu-id="e5c39-103">Ajoute la portée importée spécifiée à la liste des étendues à fusionner.</span><span class="sxs-lookup"><span data-stu-id="e5c39-103">Adds the specified imported scope to the list of scopes to be merged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e5c39-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5c39-104">Syntax</span></span>  
  
```  
HRESULT Merge (   
    [in]  IMetaDataImport  *pImport,   
    [in]  IMapToken        *pHostMapToken,   
    [in]  IUnknown         *pHandler   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e5c39-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5c39-105">Parameters</span></span>  
 `pImport`  
 <span data-ttu-id="e5c39-106">[in] Un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) objet qui identifie la portée importée à fusionner.</span><span class="sxs-lookup"><span data-stu-id="e5c39-106">[in] A pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) object that identifies the imported scope to be merged.</span></span>  
  
 `pIMap`  
 <span data-ttu-id="e5c39-107">[in] Un pointeur vers un [IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md) objet qui spécifie le jeton remapper.</span><span class="sxs-lookup"><span data-stu-id="e5c39-107">[in] A pointer to an [IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md) object that specifies the token re-map.</span></span>  
  
 `pHandleer`  
 <span data-ttu-id="e5c39-108">[in] Un pointeur vers un [IUnknown](/cpp/atl/iunknown) objet qui spécifie les erreurs.</span><span class="sxs-lookup"><span data-stu-id="e5c39-108">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) object that specifies the errors.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e5c39-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e5c39-109">Remarks</span></span>  
 <span data-ttu-id="e5c39-110">Appelez [IMetaDataEmit::MergeEnd](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md) pour déclencher la fusion des métadonnées dans une seule portée.</span><span class="sxs-lookup"><span data-stu-id="e5c39-110">Call [IMetaDataEmit::MergeEnd](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md) to trigger the merger of metadata into a single scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e5c39-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c39-111">Requirements</span></span>  
 <span data-ttu-id="e5c39-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5c39-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5c39-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e5c39-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e5c39-114">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e5c39-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e5c39-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e5c39-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5c39-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5c39-116">See Also</span></span>  
 [<span data-ttu-id="e5c39-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="e5c39-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="e5c39-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="e5c39-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
