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
ms.openlocfilehash: 52190583338f1c1ee9183a98d5f4a6cd7236342d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59075665"
---
# <a name="imetadataemitdefinecustomattribute-method"></a><span data-ttu-id="982ef-102">IMetaDataEmit::DefineCustomAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="982ef-102">IMetaDataEmit::DefineCustomAttribute Method</span></span>
<span data-ttu-id="982ef-103">Crée une définition pour un attribut personnalisé avec la signature de métadonnées spécifié, à joindre à l’objet spécifié et obtient un jeton pour cette définition d’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="982ef-103">Creates a definition for a custom attribute with the specified metadata signature, to be attached to the specified object, and gets a token to that custom attribute definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="982ef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="982ef-104">Syntax</span></span>  
  
```  
HRESULT DefineCustomAttribute (   
    [in]  mdToken     tkObj,   
    [in]  mdToken     tkType,   
    [in]  void const  *pCustomAttribute,   
    [in]  ULONG       cbCustomAttribute,   
    [out] mdCustomAttribute *pcv   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="982ef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="982ef-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="982ef-106">[in] Le jeton pour l’élément propriétaire.</span><span class="sxs-lookup"><span data-stu-id="982ef-106">[in] The token for the owner item.</span></span>  
  
 `tkType`  
 <span data-ttu-id="982ef-107">[in] Le jeton qui identifie l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="982ef-107">[in] The token that identifies the custom attribute.</span></span>  
  
 `pCustomAttribute`  
 <span data-ttu-id="982ef-108">[in] Pointeur vers l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="982ef-108">[in] A pointer to the custom attribute.</span></span>  
  
 `cbCustomAttribute`  
 <span data-ttu-id="982ef-109">[in] Le nombre d’octets dans `pCustomAttribute`.</span><span class="sxs-lookup"><span data-stu-id="982ef-109">[in] The count of bytes in `pCustomAttribute`.</span></span>  
  
 `pcv`  
 <span data-ttu-id="982ef-110">[out] Le `mdCustomAttribute` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="982ef-110">[out] The `mdCustomAttribute` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="982ef-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="982ef-111">Requirements</span></span>  
 <span data-ttu-id="982ef-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="982ef-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="982ef-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="982ef-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="982ef-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="982ef-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="982ef-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="982ef-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="982ef-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="982ef-116">See also</span></span>

- [<span data-ttu-id="982ef-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="982ef-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="982ef-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="982ef-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
