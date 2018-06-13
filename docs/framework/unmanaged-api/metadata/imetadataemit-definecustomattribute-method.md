---
title: IMetaDataEmit::DefineCustomAttribute, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineCustomAttribute
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineCustomAttribute
helpviewer_keywords:
- DefineCustomAttribute method [.NET Framework metadata]
- IMetaDataEmit::DefineCustomAttribute method [.NET Framework metadata]
ms.assetid: 7dd14854-b756-4401-b167-88ca576dc8f0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a11e9919dc1338c4b67c3c4b0f082e330c29d9eb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445080"
---
# <a name="imetadataemitdefinecustomattribute-method"></a><span data-ttu-id="3f3c7-102">IMetaDataEmit::DefineCustomAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="3f3c7-102">IMetaDataEmit::DefineCustomAttribute Method</span></span>
<span data-ttu-id="3f3c7-103">Crée une définition pour un attribut personnalisé avec la signature de métadonnées spécifiée, à joindre à l’objet spécifié et obtient un jeton pour cette définition d’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-103">Creates a definition for a custom attribute with the specified metadata signature, to be attached to the specified object, and gets a token to that custom attribute definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f3c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f3c7-104">Syntax</span></span>  
  
```  
HRESULT DefineCustomAttribute (   
    [in]  mdToken     tkObj,   
    [in]  mdToken     tkType,   
    [in]  void const  *pCustomAttribute,   
    [in]  ULONG       cbCustomAttribute,   
    [out] mdCustomAttribute *pcv   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3f3c7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f3c7-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="3f3c7-106">[in] Le jeton pour l’élément propriétaire.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-106">[in] The token for the owner item.</span></span>  
  
 `tkType`  
 <span data-ttu-id="3f3c7-107">[in] Jeton qui identifie l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-107">[in] The token that identifies the custom attribute.</span></span>  
  
 `pCustomAttribute`  
 <span data-ttu-id="3f3c7-108">[in] Pointeur vers l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-108">[in] A pointer to the custom attribute.</span></span>  
  
 `cbCustomAttribute`  
 <span data-ttu-id="3f3c7-109">[in] Le nombre d’octets dans `pCustomAttribute`.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-109">[in] The count of bytes in `pCustomAttribute`.</span></span>  
  
 `pcv`  
 <span data-ttu-id="3f3c7-110">[out] Le `mdCustomAttribute` jeton assigné.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-110">[out] The `mdCustomAttribute` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f3c7-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f3c7-111">Requirements</span></span>  
 <span data-ttu-id="3f3c7-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3f3c7-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f3c7-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3f3c7-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3f3c7-114">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3f3c7-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3f3c7-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f3c7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f3c7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f3c7-116">See Also</span></span>  
 [<span data-ttu-id="3f3c7-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="3f3c7-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="3f3c7-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="3f3c7-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
