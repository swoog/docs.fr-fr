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
ms.openlocfilehash: 242618fb2a5ab748132baf68e24240d1ffaf2301
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59139839"
---
# <a name="imetadataemitgettokenfromsig-method"></a><span data-ttu-id="051ce-102">IMetaDataEmit::GetTokenFromSig, méthode</span><span class="sxs-lookup"><span data-stu-id="051ce-102">IMetaDataEmit::GetTokenFromSig Method</span></span>
<span data-ttu-id="051ce-103">Obtient un jeton pour la signature de métadonnées spécifié.</span><span class="sxs-lookup"><span data-stu-id="051ce-103">Gets a token for the specified metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="051ce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="051ce-104">Syntax</span></span>  
  
```  
HRESULT GetTokenFromSig (   
    [in]  PCCOR_SIGNATURE pvSig,   
    [in]  ULONG       cbSig,   
    [out] mdSignature *pmsig   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="051ce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="051ce-105">Parameters</span></span>  
 `pvSig`  
 <span data-ttu-id="051ce-106">[in] La signature à rendre persistante et stockées.</span><span class="sxs-lookup"><span data-stu-id="051ce-106">[in] The signature to be persisted and stored.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="051ce-107">[in] Le nombre d’octets dans `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="051ce-107">[in] The count of bytes in `pvSig`.</span></span>  
  
 `pmsig`  
 <span data-ttu-id="051ce-108">[out] Le `mdSignature` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="051ce-108">[out] The `mdSignature` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="051ce-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="051ce-109">Requirements</span></span>  
 <span data-ttu-id="051ce-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="051ce-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="051ce-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="051ce-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="051ce-112">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="051ce-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="051ce-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="051ce-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="051ce-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="051ce-114">See also</span></span>

- [<span data-ttu-id="051ce-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="051ce-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="051ce-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="051ce-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
