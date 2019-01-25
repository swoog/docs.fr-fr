---
title: IMetaDataEmit2::GetDeltaSaveSize, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.GetDeltaSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::GetDeltaSaveSize
helpviewer_keywords:
- IMetaDataEmit2::GetDeltaSaveSize method [.NET Framework metadata]
- GetDeltaSaveSize method [.NET Framework metadata]
ms.assetid: 036db5e7-8211-4645-9a34-03d1a89be955
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cb59fdb2249d798c70b1990a6bca41c5c14b80c0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610563"
---
# <a name="imetadataemit2getdeltasavesize-method"></a><span data-ttu-id="35e64-102">IMetaDataEmit2::GetDeltaSaveSize, méthode</span><span class="sxs-lookup"><span data-stu-id="35e64-102">IMetaDataEmit2::GetDeltaSaveSize Method</span></span>
<span data-ttu-id="35e64-103">Obtient une valeur indiquant toute modification de la taille des métadonnées qui résulte de la session active modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="35e64-103">Gets a value indicating any change in metadata size that results from the current edit-and-continue session.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35e64-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35e64-104">Syntax</span></span>  
  
```  
HRESULT GetDeltaSaveSize (  
    [in]  CorSaveSize  fSave,  
    [out] DWORD        *pdwSaveSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="35e64-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35e64-105">Parameters</span></span>  
 `fSave`  
 <span data-ttu-id="35e64-106">[in] Parmi les [CorSaveSize](../../../../docs/framework/unmanaged-api/metadata/corsavesize-enumeration.md) valeurs indiquant le niveau de précision que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="35e64-106">[in] One of the [CorSaveSize](../../../../docs/framework/unmanaged-api/metadata/corsavesize-enumeration.md) values, indicating the level of precision desired.</span></span> <span data-ttu-id="35e64-107">Pour le .NET Framework version 2.0, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="35e64-107">For the .NET Framework version 2.0, this parameter is ignored.</span></span>  
  
 `pdwSaveSize`  
 <span data-ttu-id="35e64-108">[out] La modification de la taille des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="35e64-108">[out] The change in the size of the metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35e64-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="35e64-109">Requirements</span></span>  
 <span data-ttu-id="35e64-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35e64-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35e64-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="35e64-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="35e64-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="35e64-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="35e64-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35e64-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="35e64-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35e64-114">See also</span></span>
- [<span data-ttu-id="35e64-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="35e64-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="35e64-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="35e64-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
