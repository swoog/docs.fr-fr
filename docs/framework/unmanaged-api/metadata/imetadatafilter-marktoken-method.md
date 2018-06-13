---
title: IMetaDataFilter::MarkToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter::MarkToken
helpviewer_keywords:
- IMetaDataFilter::MarkToken method [.NET Framework metadata]
- MarkToken method, IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: bd492834-6529-4d39-b93d-f8cdbd3e297f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 97f184bae4628f2aa357644188594396468671ee
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444150"
---
# <a name="imetadatafiltermarktoken-method"></a><span data-ttu-id="263b4-102">IMetaDataFilter::MarkToken, méthode</span><span class="sxs-lookup"><span data-stu-id="263b4-102">IMetaDataFilter::MarkToken Method</span></span>
<span data-ttu-id="263b4-103">Définit une valeur qui indique que le jeton de métadonnées spécifié a été traité.</span><span class="sxs-lookup"><span data-stu-id="263b4-103">Sets a value indicating that the specified metadata token has been processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="263b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="263b4-104">Syntax</span></span>  
  
```  
HRESULT MarkToken (  
    [in] mdToken   tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="263b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="263b4-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="263b4-106">[in] Le jeton à marquer comme traité.</span><span class="sxs-lookup"><span data-stu-id="263b4-106">[in] The token to mark as processed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="263b4-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="263b4-107">Requirements</span></span>  
 <span data-ttu-id="263b4-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="263b4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="263b4-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="263b4-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="263b4-110">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="263b4-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="263b4-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="263b4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="263b4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="263b4-112">See Also</span></span>  
 [<span data-ttu-id="263b4-113">IMetaDataFilter, interface</span><span class="sxs-lookup"><span data-stu-id="263b4-113">IMetaDataFilter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-interface.md)
