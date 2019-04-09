---
title: IMetaDataEmit::DeleteClassLayout, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteClassLayout
helpviewer_keywords:
- DeleteClassLayout method [.NET Framework metadata]
- IMetaDataEmit::DeleteClassLayout method [.NET Framework metadata]
ms.assetid: 65a4ad49-fa49-4b36-8ed1-76dd6a185ab4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a195daf2aa1b1c5a8f9c4335f7c4185f30093360
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178527"
---
# <a name="imetadataemitdeleteclasslayout-method"></a><span data-ttu-id="4f5cb-102">IMetaDataEmit::DeleteClassLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="4f5cb-102">IMetaDataEmit::DeleteClassLayout Method</span></span>
<span data-ttu-id="4f5cb-103">Détruit la signature de métadonnées de disposition de classe pour le type représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f5cb-103">Destroys the class layout metadata signature for the type represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f5cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f5cb-104">Syntax</span></span>  
  
```  
HRESULT DeleteClassLayout (  
    [in]  mdTypeDef   td  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4f5cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f5cb-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="4f5cb-106">[in] Un `mdTypeDef` jeton de métadonnées qui représente le type pour lequel la disposition de classe sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="4f5cb-106">[in] An `mdTypeDef` metadata token that represents the type for which the class layout will be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f5cb-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f5cb-107">Requirements</span></span>  
 <span data-ttu-id="4f5cb-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4f5cb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4f5cb-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4f5cb-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4f5cb-110">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4f5cb-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="4f5cb-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="4f5cb-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4f5cb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f5cb-112">See also</span></span>

- [<span data-ttu-id="4f5cb-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="4f5cb-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="4f5cb-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="4f5cb-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
