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
ms.openlocfilehash: 4a6f2e428366d2fe96313879ef1256d7b86ddd29
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57490409"
---
# <a name="imetadataimportfindfield-method"></a><span data-ttu-id="95d3e-102">IMetaDataImport::FindField, méthode</span><span class="sxs-lookup"><span data-stu-id="95d3e-102">IMetaDataImport::FindField Method</span></span>
<span data-ttu-id="95d3e-103">Obtient un pointeur vers le FieldDef jeton pour le champ est placé par spécifié <xref:System.Type> et qui a la signature de nom et de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95d3e-103">Gets a pointer to the FieldDef token for the field that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95d3e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95d3e-104">Syntax</span></span>  
  
```  
HRESULT FindField (  
   [in]  mdTypeDef         td,  
   [in]  LPCWSTR           szName,  
   [in]  PCCOR_SIGNATURE   pvSigBlob,  
   [in]  ULONG             cbSigBlob,  
   [out] mdFieldDef        *pmb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95d3e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95d3e-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="95d3e-106">[in] Le jeton TypeDef pour la classe ou interface qui encadre le champ à rechercher.</span><span class="sxs-lookup"><span data-stu-id="95d3e-106">[in] The TypeDef token for the class or interface that encloses the field to search for.</span></span> <span data-ttu-id="95d3e-107">Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale.</span><span class="sxs-lookup"><span data-stu-id="95d3e-107">If this value is `mdTokenNil`, the lookup is done for a global variable.</span></span>  
  
 `szName`  
 <span data-ttu-id="95d3e-108">[in] Le nom du champ à rechercher.</span><span class="sxs-lookup"><span data-stu-id="95d3e-108">[in] The name of the field to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="95d3e-109">[in] Pointeur vers la signature de métadonnées binaires du champ.</span><span class="sxs-lookup"><span data-stu-id="95d3e-109">[in] A pointer to the binary metadata signature of the field.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="95d3e-110">[in] La taille en octets de `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="95d3e-110">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmb`  
 <span data-ttu-id="95d3e-111">[out] Pointeur vers le jeton FieldDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="95d3e-111">[out] A pointer to the matching FieldDef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="95d3e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="95d3e-112">Remarks</span></span>  
 <span data-ttu-id="95d3e-113">Vous spécifiez le champ à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement sa signature (`pvSigBlob`).</span><span class="sxs-lookup"><span data-stu-id="95d3e-113">You specify the field using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span>  
  
 <span data-ttu-id="95d3e-114">La signature est passé à `FindField` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="95d3e-114">The signature passed to `FindField` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="95d3e-115">Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant.</span><span class="sxs-lookup"><span data-stu-id="95d3e-115">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="95d3e-116">(Le jeton est un index dans la table TypeDef local).</span><span class="sxs-lookup"><span data-stu-id="95d3e-116">(The token is an index into the local TypeDef table).</span></span> <span data-ttu-id="95d3e-117">Vous ne pouvez pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée dans `FindField`.</span><span class="sxs-lookup"><span data-stu-id="95d3e-117">You cannot build a run-time signature outside the context of the current scope and use that signature as input to `FindField`.</span></span>  
  
 <span data-ttu-id="95d3e-118">`FindField` recherche uniquement les champs qui ont été définis directement dans la classe ou interface ; Il ne trouve pas les champs hérités.</span><span class="sxs-lookup"><span data-stu-id="95d3e-118">`FindField` finds only fields that were defined directly in the class or interface; it does not find inherited fields.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95d3e-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95d3e-119">Requirements</span></span>  
 <span data-ttu-id="95d3e-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="95d3e-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95d3e-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="95d3e-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="95d3e-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="95d3e-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="95d3e-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95d3e-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95d3e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95d3e-124">See also</span></span>
- [<span data-ttu-id="95d3e-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="95d3e-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="95d3e-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="95d3e-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
