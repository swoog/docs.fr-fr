---
title: IMetaDataEmit::DeleteToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteToken
helpviewer_keywords:
- DeleteToken method [.NET Framework metadata]
- IMetaDataEmit::DeleteToken method [.NET Framework metadata]
ms.assetid: a4926d0a-261b-46b1-9994-82633661a64b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d85fb62936678f830ca7eaf26a97c36be5f23ac8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138240"
---
# <a name="imetadataemitdeletetoken-method"></a><span data-ttu-id="7d0c4-102">IMetaDataEmit::DeleteToken, méthode</span><span class="sxs-lookup"><span data-stu-id="7d0c4-102">IMetaDataEmit::DeleteToken Method</span></span>
<span data-ttu-id="7d0c4-103">Supprime le jeton spécifié à partir de la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="7d0c4-103">Deletes the specified token from the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d0c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d0c4-104">Syntax</span></span>  
  
```  
HRESULT DeleteToken (   
    [in]  mdToken     tkObj   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7d0c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d0c4-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="7d0c4-106">[in] Le jeton doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="7d0c4-106">[in] The token to be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7d0c4-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d0c4-107">Requirements</span></span>  
 <span data-ttu-id="7d0c4-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7d0c4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7d0c4-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7d0c4-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7d0c4-110">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7d0c4-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7d0c4-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7d0c4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d0c4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d0c4-112">See also</span></span>

- [<span data-ttu-id="7d0c4-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="7d0c4-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="7d0c4-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="7d0c4-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
