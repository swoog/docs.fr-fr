---
title: IMetaDataImport::FindMember, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindMember
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindMember
helpviewer_keywords:
- IMetaDataImport::FindMember method [.NET Framework metadata]
- FindMember method [.NET Framework metadata]
ms.assetid: ad32fb84-c2b6-41cd-888d-787ff3a90449
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 79c9a54a44ae1751cb8b1b57379ccfd6485f6e6b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448189"
---
# <a name="imetadataimportfindmember-method"></a><span data-ttu-id="7ba13-102">IMetaDataImport::FindMember, méthode</span><span class="sxs-lookup"><span data-stu-id="7ba13-102">IMetaDataImport::FindMember Method</span></span>
<span data-ttu-id="7ba13-103">Obtient un pointeur vers le MemberDef jeton pour le champ ou la méthode est placée entre la <xref:System.Type> et qui possède la signature de nom et de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7ba13-103">Gets a pointer to the MemberDef token for field or method that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ba13-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ba13-104">Syntax</span></span>  
  
```  
HRESULT FindMember (  
   [in]  mdTypeDef         td,  
   [in]  LPCWSTR           szName,   
   [in]  PCCOR_SIGNATURE   pvSigBlob,   
   [in]  ULONG             cbSigBlob,   
   [out] mdToken           *pmb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7ba13-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ba13-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="7ba13-106">[in] Le jeton TypeDef pour la classe ou interface qui encadre le membre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="7ba13-106">[in] The TypeDef token for the class or interface that encloses the member to search for.</span></span> <span data-ttu-id="7ba13-107">Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale ou une fonction globale.</span><span class="sxs-lookup"><span data-stu-id="7ba13-107">If this value is `mdTokenNil`, the lookup is done for a global-variable or global-function.</span></span>  
  
 `szName`  
 <span data-ttu-id="7ba13-108">[in] Le nom du membre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="7ba13-108">[in] The name of the member to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="7ba13-109">[in] Pointeur vers la signature de métadonnées binaires du membre.</span><span class="sxs-lookup"><span data-stu-id="7ba13-109">[in] A pointer to the binary metadata signature of the member.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="7ba13-110">[in] La taille en octets de `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="7ba13-110">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmb`  
 <span data-ttu-id="7ba13-111">[out] Pointeur vers le jeton MemberDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="7ba13-111">[out] A pointer to the matching MemberDef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7ba13-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7ba13-112">Remarks</span></span>  
 <span data-ttu-id="7ba13-113">Vous spécifiez le membre à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement de sa signature (`pvSigBlob`).</span><span class="sxs-lookup"><span data-stu-id="7ba13-113">You specify the member using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span> <span data-ttu-id="7ba13-114">Il peut exister plusieurs membres avec le même nom dans une classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="7ba13-114">There might be multiple members with the same name in a class or interface.</span></span> <span data-ttu-id="7ba13-115">Dans ce cas, passez la signature du membre pour rechercher la correspondance unique.</span><span class="sxs-lookup"><span data-stu-id="7ba13-115">In that case, pass the member's signature to find the unique match.</span></span>  
  
 <span data-ttu-id="7ba13-116">La signature passée à `FindMember` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="7ba13-116">The signature passed to `FindMember` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="7ba13-117">Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant.</span><span class="sxs-lookup"><span data-stu-id="7ba13-117">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="7ba13-118">Le jeton est un index dans la table TypeDef locale.</span><span class="sxs-lookup"><span data-stu-id="7ba13-118">The token is an index into the local TypeDef table.</span></span> <span data-ttu-id="7ba13-119">Vous ne peut pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée à `FindMember`.</span><span class="sxs-lookup"><span data-stu-id="7ba13-119">You cannot build a run-time signature outside the context of the current scope and use that signature as input to input to `FindMember`.</span></span>  
  
 <span data-ttu-id="7ba13-120">`FindMember` recherche uniquement les membres qui ont été définis directement dans la classe ou interface ; Il ne trouve pas les membres hérités.</span><span class="sxs-lookup"><span data-stu-id="7ba13-120">`FindMember` finds only members that were defined directly in the class or interface; it does not find inherited members.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7ba13-121">`FindMember` est une méthode d’assistance.</span><span class="sxs-lookup"><span data-stu-id="7ba13-121">`FindMember` is a helper method.</span></span> <span data-ttu-id="7ba13-122">Il appelle [IMetaDataImport::FindMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-findmethod-method.md); si cet appel ne trouve pas de correspondance, `FindMember` appelle ensuite [IMetaDataImport::FindField](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-findfield-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-122">It calls [IMetaDataImport::FindMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-findmethod-method.md); if that call does not find a match, `FindMember` then calls [IMetaDataImport::FindField](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-findfield-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7ba13-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ba13-123">Requirements</span></span>  
 <span data-ttu-id="7ba13-124">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7ba13-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7ba13-125">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7ba13-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7ba13-126">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7ba13-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7ba13-127">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7ba13-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ba13-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ba13-128">See Also</span></span>  
 [<span data-ttu-id="7ba13-129">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="7ba13-129">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="7ba13-130">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="7ba13-130">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
