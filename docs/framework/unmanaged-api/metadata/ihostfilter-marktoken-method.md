---
title: IHostFilter::MarkToken, méthode
ms.date: 03/30/2017
api_name:
- IHostFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostFilter::MarkToken
helpviewer_keywords:
- MarkToken method, IHostFilter interface [.NET Framework metadata]
- IHostFilter::MarkToken method [.NET Framework metadata]
ms.assetid: d7061343-d0a3-4fd5-b312-61974f98bd62
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f3214a21dda27fda01054e96400997b15d11f71b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59194433"
---
# <a name="ihostfiltermarktoken-method"></a><span data-ttu-id="f50c4-102">IHostFilter::MarkToken, méthode</span><span class="sxs-lookup"><span data-stu-id="f50c4-102">IHostFilter::MarkToken Method</span></span>
<span data-ttu-id="f50c4-103">Indique que le jeton de métadonnées spécifié est traité.</span><span class="sxs-lookup"><span data-stu-id="f50c4-103">Indicates that the specified metadata token will be processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f50c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f50c4-104">Syntax</span></span>  
  
```  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f50c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f50c4-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="f50c4-106">[in] Le jeton de métadonnées à traiter.</span><span class="sxs-lookup"><span data-stu-id="f50c4-106">[in] The metadata token to be processed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f50c4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f50c4-107">Remarks</span></span>  
 <span data-ttu-id="f50c4-108">En règle générale, vous souhaitez un jeton à traiter si elle est dans la portée de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f50c4-108">Typically, you want a token to be processed if it is in the metadata scope.</span></span> <span data-ttu-id="f50c4-109">Le `MarkToken` méthode est passée au moteur de métadonnées via le [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f50c4-109">The `MarkToken` method is passed to the metadata engine via the [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f50c4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f50c4-110">Requirements</span></span>  
 <span data-ttu-id="f50c4-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f50c4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f50c4-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f50c4-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f50c4-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f50c4-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f50c4-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f50c4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f50c4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f50c4-115">See also</span></span>

- [<span data-ttu-id="f50c4-116">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f50c4-116">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="f50c4-117">IHostFilter, interface</span><span class="sxs-lookup"><span data-stu-id="f50c4-117">IHostFilter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/ihostfilter-interface.md)
