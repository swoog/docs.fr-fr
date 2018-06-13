---
title: IMetaDataImport::FindField, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindField
helpviewer_keywords:
- IMetaDataImport::FindField method [.NET Framework metadata]
- FindField method [.NET Framework metadata]
ms.assetid: 38cd4e16-fbb2-471c-aa73-ac51a1931ad2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ac69bab45ccd39b6a055fe4d2f74950ab47da779
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447030"
---
# <a name="imetadataimportfindfield-method"></a><span data-ttu-id="59733-102">IMetaDataImport::FindField, méthode</span><span class="sxs-lookup"><span data-stu-id="59733-102">IMetaDataImport::FindField Method</span></span>
<span data-ttu-id="59733-103">Obtient un pointeur vers le FieldDef jeton pour le champ est placé entre la <xref:System.Type> et qui possède la signature de nom et de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="59733-103">Gets a pointer to the FieldDef token for the field that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59733-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59733-104">Syntax</span></span>  
  
```  
HRESULT FindField (  
   [in]  mdTypeDef         td,  
   [in]  LPCWSTR           szName,  
   [in]  PCCOR_SIGNATURE   pvSigBlob,  
   [in]  ULONG             cbSigBlob,  
   [out] mdFieldDef        *pmb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="59733-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59733-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="59733-106">[in] Le jeton TypeDef pour la classe ou interface qui définit le champ à rechercher.</span><span class="sxs-lookup"><span data-stu-id="59733-106">[in] The TypeDef token for the class or interface that encloses the field to search for.</span></span> <span data-ttu-id="59733-107">Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale.</span><span class="sxs-lookup"><span data-stu-id="59733-107">If this value is `mdTokenNil`, the lookup is done for a global variable.</span></span>  
  
 `szName`  
 <span data-ttu-id="59733-108">[in] Le nom du champ à rechercher.</span><span class="sxs-lookup"><span data-stu-id="59733-108">[in] The name of the field to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="59733-109">[in] Pointeur vers la signature de métadonnées binaires du champ.</span><span class="sxs-lookup"><span data-stu-id="59733-109">[in] A pointer to the binary metadata signature of the field.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="59733-110">[in] La taille en octets de `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="59733-110">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmb`  
 <span data-ttu-id="59733-111">[out] Pointeur vers le jeton FieldDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="59733-111">[out] A pointer to the matching FieldDef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="59733-112">Notes</span><span class="sxs-lookup"><span data-stu-id="59733-112">Remarks</span></span>  
 <span data-ttu-id="59733-113">Vous spécifiez le champ à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement de sa signature (`pvSigBlob`).</span><span class="sxs-lookup"><span data-stu-id="59733-113">You specify the field using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span>  
  
 <span data-ttu-id="59733-114">La signature passée à `FindField` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="59733-114">The signature passed to `FindField` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="59733-115">Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant.</span><span class="sxs-lookup"><span data-stu-id="59733-115">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="59733-116">(Le jeton est un index dans la table TypeDef locale).</span><span class="sxs-lookup"><span data-stu-id="59733-116">(The token is an index into the local TypeDef table).</span></span> <span data-ttu-id="59733-117">Vous ne peut pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée pour `FindField`.</span><span class="sxs-lookup"><span data-stu-id="59733-117">You cannot build a run-time signature outside the context of the current scope and use that signature as input to `FindField`.</span></span>  
  
 <span data-ttu-id="59733-118">`FindField` recherche uniquement les champs qui ont été définis directement dans la classe ou interface ; Il ne trouve pas les champs hérités.</span><span class="sxs-lookup"><span data-stu-id="59733-118">`FindField` finds only fields that were defined directly in the class or interface; it does not find inherited fields.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59733-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59733-119">Requirements</span></span>  
 <span data-ttu-id="59733-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59733-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59733-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="59733-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="59733-122">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="59733-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="59733-123">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59733-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59733-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59733-124">See Also</span></span>  
 [<span data-ttu-id="59733-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="59733-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="59733-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="59733-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
