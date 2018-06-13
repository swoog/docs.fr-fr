---
title: IMetaDataEmit::SetRVA, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetRVA
helpviewer_keywords:
- IMetaDataEmit::SetRVA method [.NET Framework metadata]
- SetRVA method [.NET Framework metadata]
ms.assetid: 4d69fb6d-ee35-4318-8224-5eea2bd16818
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 371eed84883e2816892c0a6a212a4a89a287cc58
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445271"
---
# <a name="imetadataemitsetrva-method"></a><span data-ttu-id="ff538-102">IMetaDataEmit::SetRVA, méthode</span><span class="sxs-lookup"><span data-stu-id="ff538-102">IMetaDataEmit::SetRVA Method</span></span>
<span data-ttu-id="ff538-103">Définit l’adresse virtuelle relative de la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ff538-103">Sets the relative virtual address of the specified method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff538-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff538-104">Syntax</span></span>  
  
```  
HRESULT SetRVA (  
    [in]  mdMethodDef  md,   
    [in]  ULONG        ulRVA   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ff538-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff538-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="ff538-106">[in] Le jeton pour la méthode cible ou l’implémentation de méthode.</span><span class="sxs-lookup"><span data-stu-id="ff538-106">[in] The token for the target method or method implementation.</span></span>  
  
 `ulRVA`  
 <span data-ttu-id="ff538-107">[in] L’adresse de la zone de code ou de données.</span><span class="sxs-lookup"><span data-stu-id="ff538-107">[in] The address of the code or data area.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff538-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ff538-108">Requirements</span></span>  
 <span data-ttu-id="ff538-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff538-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff538-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ff538-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ff538-111">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ff538-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ff538-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff538-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff538-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff538-113">See Also</span></span>  
 [<span data-ttu-id="ff538-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="ff538-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="ff538-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="ff538-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
