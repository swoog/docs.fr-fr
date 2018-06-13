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
ms.openlocfilehash: 52375486eb9d7780a51808dedc5f876587efb115
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444562"
---
# <a name="ihostfiltermarktoken-method"></a><span data-ttu-id="9d32a-102">IHostFilter::MarkToken, méthode</span><span class="sxs-lookup"><span data-stu-id="9d32a-102">IHostFilter::MarkToken Method</span></span>
<span data-ttu-id="9d32a-103">Indique que le jeton de métadonnées spécifié sera traité.</span><span class="sxs-lookup"><span data-stu-id="9d32a-103">Indicates that the specified metadata token will be processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d32a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d32a-104">Syntax</span></span>  
  
```  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9d32a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d32a-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="9d32a-106">[in] Le jeton de métadonnées à traiter.</span><span class="sxs-lookup"><span data-stu-id="9d32a-106">[in] The metadata token to be processed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9d32a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9d32a-107">Remarks</span></span>  
 <span data-ttu-id="9d32a-108">En règle générale, vous souhaitez un jeton de traitement s’il est dans la portée de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9d32a-108">Typically, you want a token to be processed if it is in the metadata scope.</span></span> <span data-ttu-id="9d32a-109">Le `MarkToken` méthode est passée au moteur de métadonnées via la [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="9d32a-109">The `MarkToken` method is passed to the metadata engine via the [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d32a-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d32a-110">Requirements</span></span>  
 <span data-ttu-id="9d32a-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d32a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d32a-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9d32a-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9d32a-113">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d32a-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9d32a-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d32a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d32a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d32a-115">See Also</span></span>  
 [<span data-ttu-id="9d32a-116">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9d32a-116">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)  
 [<span data-ttu-id="9d32a-117">IHostFilter, interface</span><span class="sxs-lookup"><span data-stu-id="9d32a-117">IHostFilter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/ihostfilter-interface.md)
