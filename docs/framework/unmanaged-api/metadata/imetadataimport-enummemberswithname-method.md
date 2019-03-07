---
title: IMetaDataImport::EnumMembersWithName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembersWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembersWithName
helpviewer_keywords:
- IMetaDataImport::EnumMembersWithName method [.NET Framework metadata]
- EnumMembersWithName method [.NET Framework metadata]
ms.assetid: 7c9e9120-3104-42f0-86ce-19a025f20dcc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 961c1e0468ab99baca387b7d6ada4733629b7ffa
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57492229"
---
# <a name="imetadataimportenummemberswithname-method"></a><span data-ttu-id="e88cb-102">IMetaDataImport::EnumMembersWithName, méthode</span><span class="sxs-lookup"><span data-stu-id="e88cb-102">IMetaDataImport::EnumMembersWithName Method</span></span>
<span data-ttu-id="e88cb-103">Énumère les jetons MemberDef représentant les membres du type spécifié avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="e88cb-103">Enumerates MemberDef tokens representing members of the specified type with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e88cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e88cb-104">Syntax</span></span>  
  
```  
HRESULT EnumMembersWithName (  
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   cl,   
   [in]      LPCWSTR     szName,   
   [out]     mdToken     rMembers[],   
   [in]      ULONG       cMax,   
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e88cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e88cb-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="e88cb-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e88cb-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="e88cb-107">[in] Jeton TypeDef représentant le type de membres à énumérer.</span><span class="sxs-lookup"><span data-stu-id="e88cb-107">[in] A TypeDef token representing the type with members to enumerate.</span></span>  
  
 `szName`  
 <span data-ttu-id="e88cb-108">[in] Nom du membre qui limite l’étendue de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e88cb-108">[in] The member name that limits the scope of the enumerator.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="e88cb-109">[out] Tableau utilisé pour stocker les jetons MemberDef.</span><span class="sxs-lookup"><span data-stu-id="e88cb-109">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="e88cb-110">[in] Taille maximale du tableau `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="e88cb-110">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="e88cb-111">[out] Le nombre réel de jetons MemberDef retournés dans `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="e88cb-111">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e88cb-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e88cb-112">Remarks</span></span>  
 <span data-ttu-id="e88cb-113">Cette méthode énumère les champs et méthodes, mais pas propriétés ou événements.</span><span class="sxs-lookup"><span data-stu-id="e88cb-113">This method enumerates fields and methods, but not properties or events.</span></span> <span data-ttu-id="e88cb-114">Contrairement aux [IMetaDataImport::EnumMembers](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enummembers-method.md), `EnumMembersWithName` ignore tous les jetons de champ et de membre qui n’ont pas le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="e88cb-114">Unlike [IMetaDataImport::EnumMembers](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enummembers-method.md), `EnumMembersWithName` discards all field and member tokens that do not have the specified name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e88cb-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e88cb-115">Return Value</span></span>  
  
|<span data-ttu-id="e88cb-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e88cb-116">HRESULT</span></span>|<span data-ttu-id="e88cb-117">Description</span><span class="sxs-lookup"><span data-stu-id="e88cb-117">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="e88cb-118">`EnumTypeDefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e88cb-118">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="e88cb-119">Il n’y a aucune jetons MemberDef à énumérer.</span><span class="sxs-lookup"><span data-stu-id="e88cb-119">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="e88cb-120">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e88cb-120">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e88cb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e88cb-121">Requirements</span></span>  
 <span data-ttu-id="e88cb-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e88cb-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e88cb-123">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e88cb-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e88cb-124">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e88cb-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e88cb-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e88cb-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e88cb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e88cb-126">See also</span></span>
- [<span data-ttu-id="e88cb-127">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="e88cb-127">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="e88cb-128">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="e88cb-128">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
