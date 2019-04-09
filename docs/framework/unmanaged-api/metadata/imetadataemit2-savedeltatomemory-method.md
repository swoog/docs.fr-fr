---
title: IMetaDataEmit2::SaveDeltaToMemory, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToMemory
helpviewer_keywords:
- SaveDeltaToMemory method [.NET Framework metadata]
- IMetaDataEmit2::SaveDeltaToMemory method [.NET Framework metadata]
ms.assetid: e2146726-0084-4c9e-a2d2-e8d461b13b21
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fa95a737747e9153eb844cddd8e0684585b9108b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59081131"
---
# <a name="imetadataemit2savedeltatomemory-method"></a><span data-ttu-id="3778d-102">IMetaDataEmit2::SaveDeltaToMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="3778d-102">IMetaDataEmit2::SaveDeltaToMemory Method</span></span>
<span data-ttu-id="3778d-103">Enregistre les modifications de la session active modifier et continuer à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3778d-103">Saves changes from the current edit-and-continue session to memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3778d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3778d-104">Syntax</span></span>  
  
```  
HRESULT SaveDeltaToMemory (  
    [out] void        *pbData,   
    [in]  ULONG       cbData  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3778d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3778d-105">Parameters</span></span>  
 `pbData`  
 <span data-ttu-id="3778d-106">[out] L’adresse à laquelle commencer l’écriture du delta de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3778d-106">[out] The address at which to begin writing the metadata delta.</span></span>  
  
 `cbData`  
 <span data-ttu-id="3778d-107">[in] La taille des modifications.</span><span class="sxs-lookup"><span data-stu-id="3778d-107">[in] The size of the changes.</span></span> <span data-ttu-id="3778d-108">Utilisez [IMetaDataEmit2::GetDeltaSaveSize](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-getdeltasavesize-method.md) pour déterminer la taille.</span><span class="sxs-lookup"><span data-stu-id="3778d-108">Use [IMetaDataEmit2::GetDeltaSaveSize](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-getdeltasavesize-method.md) to determine the size.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3778d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3778d-109">Requirements</span></span>  
 <span data-ttu-id="3778d-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3778d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3778d-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3778d-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3778d-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3778d-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="3778d-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3778d-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3778d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3778d-114">See also</span></span>

- [<span data-ttu-id="3778d-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="3778d-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="3778d-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="3778d-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
