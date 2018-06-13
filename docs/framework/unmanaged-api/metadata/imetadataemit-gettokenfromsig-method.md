---
title: IMetaDataEmit::GetTokenFromSig, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.GetTokenFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::GetTokenFromSig
helpviewer_keywords:
- IMetaDataEmit::GetTokenFromSig method [.NET Framework metadata]
- GetTokenFromSig method [.NET Framework metadata]
ms.assetid: 50a58a83-6287-40a4-b315-47823cea0a5c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: be42fea034be4fe5d48874b00db86977a3039a34
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448218"
---
# <a name="imetadataemitgettokenfromsig-method"></a><span data-ttu-id="e8def-102">IMetaDataEmit::GetTokenFromSig, méthode</span><span class="sxs-lookup"><span data-stu-id="e8def-102">IMetaDataEmit::GetTokenFromSig Method</span></span>
<span data-ttu-id="e8def-103">Obtient un jeton pour la signature de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8def-103">Gets a token for the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8def-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8def-104">Syntax</span></span>  
  
```  
HRESULT GetTokenFromSig (   
    [in]  PCCOR_SIGNATURE pvSig,   
    [in]  ULONG       cbSig,   
    [out] mdSignature *pmsig   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8def-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8def-105">Parameters</span></span>  
 `pvSig`  
 <span data-ttu-id="e8def-106">[in] La signature à rendre persistante et stockées.</span><span class="sxs-lookup"><span data-stu-id="e8def-106">[in] The signature to be persisted and stored.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="e8def-107">[in] Le nombre d’octets dans `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="e8def-107">[in] The count of bytes in `pvSig`.</span></span>  
  
 `pmsig`  
 <span data-ttu-id="e8def-108">[out] Le `mdSignature` jeton assigné.</span><span class="sxs-lookup"><span data-stu-id="e8def-108">[out] The `mdSignature` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8def-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e8def-109">Requirements</span></span>  
 <span data-ttu-id="e8def-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8def-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8def-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e8def-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e8def-112">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e8def-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e8def-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8def-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8def-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8def-114">See Also</span></span>  
 [<span data-ttu-id="e8def-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="e8def-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="e8def-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="e8def-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
