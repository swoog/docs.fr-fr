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
ms.openlocfilehash: 5ea100ff86286cb98db5aa9fa6f3c12f5d318a90
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217742"
---
# <a name="imetadataemitdeletepinvokemap-method"></a><span data-ttu-id="f9e23-102">IMetaDataEmit::DeletePinvokeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="f9e23-102">IMetaDataEmit::DeletePinvokeMap Method</span></span>
<span data-ttu-id="f9e23-103">Détruit les métadonnées de mappage PInvoke pour l’objet référencé par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9e23-103">Destroys the PInvoke mapping metadata for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9e23-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9e23-104">Syntax</span></span>  
  
```  
HRESULT DeletePinvokeMap (   
    [in]  mdToken     tk   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f9e23-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9e23-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="f9e23-106">[in] Un `mdFieldDef` ou `mdMethodDef` jeton qui représente l’objet pour lequel supprimer les métadonnées de mappage PInvoke.</span><span class="sxs-lookup"><span data-stu-id="f9e23-106">[in] An `mdFieldDef` or `mdMethodDef` token that represents the object for which to delete the PInvoke mapping metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f9e23-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9e23-107">Requirements</span></span>  
 <span data-ttu-id="f9e23-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f9e23-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9e23-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f9e23-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f9e23-110">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f9e23-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f9e23-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9e23-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9e23-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9e23-112">See also</span></span>

- [<span data-ttu-id="f9e23-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="f9e23-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="f9e23-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="f9e23-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
