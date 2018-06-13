---
title: IMetaDataEmit::DefineMethodImpl, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMethodImpl
helpviewer_keywords:
- DefineMethodImpl method [.NET Framework metadata]
- IMetaDataEmit::DefineMethodImpl method [.NET Framework metadata]
ms.assetid: 9dcc8b3d-33ee-4c7c-8d6f-322c57b94a0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2ab66fecfaa66b5c56690950f6b19ecfd7e85e33
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443987"
---
# <a name="imetadataemitdefinemethodimpl-method"></a><span data-ttu-id="b7894-102">IMetaDataEmit::DefineMethodImpl, méthode</span><span class="sxs-lookup"><span data-stu-id="b7894-102">IMetaDataEmit::DefineMethodImpl Method</span></span>
<span data-ttu-id="b7894-103">Crée une définition pour l’implémentation d’une méthode héritée d’une interface et retourne un jeton pour cette définition d’implémentation de méthode.</span><span class="sxs-lookup"><span data-stu-id="b7894-103">Creates a definition for implementation of a method inherited from an interface, and returns a token to that method-implementation definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7894-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7894-104">Syntax</span></span>  
  
```  
HRESULT DefineMethodImpl (   
    [in]  mdTypeDef         td,   
    [in]  mdToken           tkBody,   
    [in]  mdToken           tkDecl  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b7894-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7894-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="b7894-106">[in] Le `mdTypedef` jeton de la classe d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="b7894-106">[in] The `mdTypedef` token of the implementing class.</span></span>  
  
 `tkBody`  
 <span data-ttu-id="b7894-107">[in] Le `mdMethodDef` ou `mdMethodRef` jeton du corps du code.</span><span class="sxs-lookup"><span data-stu-id="b7894-107">[in] The `mdMethodDef` or `mdMethodRef` token of the code body.</span></span>  
  
 `tkDecl`  
 <span data-ttu-id="b7894-108">[in] Le `mdMethodDef` ou `mdMethodRef` jeton de la méthode d’interface implémentée.</span><span class="sxs-lookup"><span data-stu-id="b7894-108">[in] The `mdMethodDef` or `mdMethodRef` token of the interface method being implemented.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7894-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7894-109">Requirements</span></span>  
 <span data-ttu-id="b7894-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7894-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7894-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b7894-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b7894-112">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b7894-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b7894-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7894-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7894-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7894-114">See Also</span></span>  
 [<span data-ttu-id="b7894-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="b7894-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="b7894-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="b7894-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
