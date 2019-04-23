---
title: IMetaDataImport::FindMemberRef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindMemberRef
helpviewer_keywords:
- IMetaDataImport::FindMemberRef method [.NET Framework metadata]
- FindMemberRef method [.NET Framework metadata]
ms.assetid: 1ccda329-d752-4d89-abe8-511af3c3f4c9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: abbd35fe390cc09951b762a5fd671d2d34a57c6c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177890"
---
# <a name="imetadataimportfindmemberref-method"></a><span data-ttu-id="748c9-102">IMetaDataImport::FindMemberRef, méthode</span><span class="sxs-lookup"><span data-stu-id="748c9-102">IMetaDataImport::FindMemberRef Method</span></span>
<span data-ttu-id="748c9-103">Obtient un pointeur vers le jeton MemberRef pour le membre de référence qui est délimitée par spécifié <xref:System.Type> et qui a la signature de nom et de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="748c9-103">Gets a pointer to the MemberRef token for the member reference that is enclosed by the specified <xref:System.Type> and that has the specified name and metadata signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="748c9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="748c9-104">Syntax</span></span>  
  
```  
HRESULT FindMemberRef (  
   [in]  mdTypeRef          td,  
   [in]  LPCWSTR            szName,   
   [in]  PCCOR_SIGNATURE    pvSigBlob,   
   [in]  ULONG              cbSigBlob,   
   [out] mdMemberRef        *pmr  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="748c9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="748c9-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="748c9-106">[in] Le jeton TypeRef pour la classe ou interface qui englobe la référence de membre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="748c9-106">[in] The TypeRef token for the class or interface that encloses the member reference to search for.</span></span> <span data-ttu-id="748c9-107">Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale ou une référence de fonction globale.</span><span class="sxs-lookup"><span data-stu-id="748c9-107">If this value is `mdTokenNil`, the lookup is done for a global variable or a global-function reference.</span></span>  
  
 `szName`  
 <span data-ttu-id="748c9-108">[in] Le nom de la référence de membre à rechercher.</span><span class="sxs-lookup"><span data-stu-id="748c9-108">[in] The name of the member reference to search for.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="748c9-109">[in] Pointeur vers la signature de métadonnées binaires de la référence de membre.</span><span class="sxs-lookup"><span data-stu-id="748c9-109">[in] A pointer to the binary metadata signature of the member reference.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="748c9-110">[in] La taille en octets de `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="748c9-110">[in] The size in bytes of `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="748c9-111">[out] Pointeur vers le jeton MemberRef correspondant.</span><span class="sxs-lookup"><span data-stu-id="748c9-111">[out] A pointer to the matching MemberRef token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="748c9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="748c9-112">Remarks</span></span>  
 <span data-ttu-id="748c9-113">Vous spécifiez le membre à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement sa signature (`pvSigBlob`).</span><span class="sxs-lookup"><span data-stu-id="748c9-113">You specify the member using its enclosing class or interface (`td`), its name (`szName`), and optionally its signature (`pvSigBlob`).</span></span>  
  
 <span data-ttu-id="748c9-114">La signature est passé à `FindMemberRef` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique.</span><span class="sxs-lookup"><span data-stu-id="748c9-114">The signature passed to `FindMemberRef` must have been generated in the current scope, because signatures are bound to a particular scope.</span></span> <span data-ttu-id="748c9-115">Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant.</span><span class="sxs-lookup"><span data-stu-id="748c9-115">A signature can embed a token that identifies the enclosing class or value type.</span></span> <span data-ttu-id="748c9-116">Le jeton est un index dans la table TypeDef local.</span><span class="sxs-lookup"><span data-stu-id="748c9-116">The token is an index into the local TypeDef table.</span></span> <span data-ttu-id="748c9-117">Vous ne pouvez pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée dans `FindMemberRef`.</span><span class="sxs-lookup"><span data-stu-id="748c9-117">You cannot build a run-time signature outside the context of the current scope and use that signature as input to `FindMemberRef`.</span></span>  
  
 <span data-ttu-id="748c9-118">`FindMemberRef` recherche uniquement les références de membre ont été définis directement dans la classe ou interface ; Il ne trouve pas de références de membre hérité.</span><span class="sxs-lookup"><span data-stu-id="748c9-118">`FindMemberRef` finds only member references that were defined directly in the class or interface; it does not find inherited member references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="748c9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="748c9-119">Requirements</span></span>  
 <span data-ttu-id="748c9-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="748c9-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="748c9-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="748c9-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="748c9-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="748c9-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="748c9-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="748c9-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="748c9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="748c9-124">See also</span></span>

- [<span data-ttu-id="748c9-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="748c9-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="748c9-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="748c9-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
