---
title: IMetaDataEmit::SetFieldMarshal, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldMarshal
helpviewer_keywords:
- SetFieldMarshal method [.NET Framework metadata]
- IMetaDataEmit::SetFieldMarshal method [.NET Framework metadata]
ms.assetid: be232314-7f69-4855-bfab-63361bd22307
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82675af85f049aeb288b3dcc18f222c0387a37b3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150395"
---
# <a name="imetadataemitsetfieldmarshal-method"></a><span data-ttu-id="a4266-102">IMetaDataEmit::SetFieldMarshal, méthode</span><span class="sxs-lookup"><span data-stu-id="a4266-102">IMetaDataEmit::SetFieldMarshal Method</span></span>
<span data-ttu-id="a4266-103">Définit l’informations de marshaling pour le paramètre de retour de la méthode, champ ou la méthode référencée par le jeton spécifié de PInvoke.</span><span class="sxs-lookup"><span data-stu-id="a4266-103">Sets the PInvoke marshaling information for the field, method return, or method parameter referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4266-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4266-104">Syntax</span></span>  
  
```  
HRESULT SetFieldMarshal (  
    [in]  mdToken          tk,   
    [in]  PCCOR_SIGNATURE  pvNativeType,   
    [in]  ULONG            cbNativeType   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4266-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4266-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="a4266-106">[in] Le jeton pour l’élément de données cible.</span><span class="sxs-lookup"><span data-stu-id="a4266-106">[in] The token for target data item.</span></span> <span data-ttu-id="a4266-107">Il s’agit soit un `mdFieldDef` ou un `mdParamDef` jeton.</span><span class="sxs-lookup"><span data-stu-id="a4266-107">This is either a `mdFieldDef` or a `mdParamDef` token.</span></span>  
  
 `pvNativeType`  
 <span data-ttu-id="a4266-108">[in] Signature de type non managé.</span><span class="sxs-lookup"><span data-stu-id="a4266-108">[in] The signature for unmanaged type.</span></span>  
  
 `cbNativeType`  
 <span data-ttu-id="a4266-109">[in] Le nombre d’octets dans `pvNativeType`.</span><span class="sxs-lookup"><span data-stu-id="a4266-109">[in] The count of bytes in `pvNativeType`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4266-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4266-110">Requirements</span></span>  
 <span data-ttu-id="a4266-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4266-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4266-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a4266-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a4266-113">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a4266-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="a4266-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a4266-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a4266-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4266-115">See also</span></span>

- [<span data-ttu-id="a4266-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a4266-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="a4266-117">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="a4266-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
