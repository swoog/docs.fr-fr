---
title: IMetaDataImport::ResetEnum Method
ms.date: 03/30/2017
api_name:
- IMetaDataImport.ResetEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::ResetEnum
helpviewer_keywords:
- ResetEnum method [.NET Framework metadata]
- IMetaDataImport::ResetEnum method [.NET Framework metadata]
ms.assetid: dda867b5-1050-49ba-b01c-fcc83b7a5617
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 143b11f0a99081b7d49bfbb68b635d92cf1e9ba3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59163876"
---
# <a name="imetadataimportresetenum-method"></a><span data-ttu-id="19e70-102">IMetaDataImport::ResetEnum Method</span><span class="sxs-lookup"><span data-stu-id="19e70-102">IMetaDataImport::ResetEnum Method</span></span>
<span data-ttu-id="19e70-103">Réinitialise l'énumérateur spécifié à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="19e70-103">Resets the specified enumerator to the specified position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19e70-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19e70-104">Syntax</span></span>  
  
```  
HRESULT ResetEnum (  
   [in] HCORENUM    hEnum,   
   [in] ULONG       ulPos  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="19e70-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19e70-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="19e70-106">[in] L’énumérateur à réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="19e70-106">[in] The enumerator to reset.</span></span>  
  
 `ulPos`  
 <span data-ttu-id="19e70-107">[in] La nouvelle position au niveau duquel placer l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="19e70-107">[in] The new position at which to place the enumerator.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19e70-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19e70-108">Requirements</span></span>  
 <span data-ttu-id="19e70-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="19e70-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19e70-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="19e70-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="19e70-111">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="19e70-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="19e70-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="19e70-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="19e70-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19e70-113">See also</span></span>

- [<span data-ttu-id="19e70-114">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="19e70-114">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="19e70-115">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="19e70-115">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
