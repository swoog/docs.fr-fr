---
title: IMetaDataEmit::DeleteFieldMarshal, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dc88baea130adbec3dd8e4065ac0eb14ece7b8ba
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444849"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="ca904-102">IMetaDataEmit::DeleteFieldMarshal, méthode</span><span class="sxs-lookup"><span data-stu-id="ca904-102">IMetaDataEmit::DeleteFieldMarshal Method</span></span>
<span data-ttu-id="ca904-103">Détruit la signature de métadonnées pour l’objet référencé par le jeton spécifié de marshaling de PInvoke.</span><span class="sxs-lookup"><span data-stu-id="ca904-103">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca904-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca904-104">Syntax</span></span>  
  
```  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca904-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca904-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="ca904-106">[in] Un `mdFieldDef` ou `mdParamDef` jeton qui représente le champ ou le paramètre pour lequel supprimer la signature de métadonnées de marshaling.</span><span class="sxs-lookup"><span data-stu-id="ca904-106">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca904-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca904-107">Requirements</span></span>  
 <span data-ttu-id="ca904-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca904-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca904-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ca904-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ca904-110">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ca904-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ca904-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca904-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca904-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca904-112">See Also</span></span>  
 [<span data-ttu-id="ca904-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="ca904-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="ca904-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="ca904-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
