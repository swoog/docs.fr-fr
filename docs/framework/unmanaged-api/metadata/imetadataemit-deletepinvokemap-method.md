---
title: IMetaDataEmit::DeletePinvokeMap, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeletePinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeletePinvokeMap
helpviewer_keywords:
- IMetaDataEmit::DeletePinvokeMap method [.NET Framework metadata]
- DeletePinvokeMap method [.NET Framework metadata]
ms.assetid: 3c4f6b54-5ce7-4a2a-83e1-6dec16441f50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c3b7c116410ce3309d970929580f4ec7f65bd657
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558280"
---
# <a name="imetadataemitdeletepinvokemap-method"></a><span data-ttu-id="c1b1e-102">IMetaDataEmit::DeletePinvokeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="c1b1e-102">IMetaDataEmit::DeletePinvokeMap Method</span></span>
<span data-ttu-id="c1b1e-103">Détruit les métadonnées de mappage PInvoke pour l’objet référencé par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-103">Destroys the PInvoke mapping metadata for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1b1e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1b1e-104">Syntax</span></span>  
  
```  
HRESULT DeletePinvokeMap (   
    [in]  mdToken     tk   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c1b1e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1b1e-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="c1b1e-106">[in] Un `mdFieldDef` ou `mdMethodDef` jeton qui représente l’objet pour lequel supprimer les métadonnées de mappage PInvoke.</span><span class="sxs-lookup"><span data-stu-id="c1b1e-106">[in] An `mdFieldDef` or `mdMethodDef` token that represents the object for which to delete the PInvoke mapping metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c1b1e-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c1b1e-107">Requirements</span></span>  
 <span data-ttu-id="c1b1e-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c1b1e-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c1b1e-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c1b1e-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c1b1e-110">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c1b1e-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c1b1e-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1b1e-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1b1e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b1e-112">See also</span></span>
- [<span data-ttu-id="c1b1e-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="c1b1e-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="c1b1e-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="c1b1e-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
