---
title: IMetaDataImport::EnumMemberRefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMemberRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMemberRefs
helpviewer_keywords:
- EnumMemberRefs method [.NET Framework metadata]
- IMetaDataImport::EnumMemberRefs method [.NET Framework metadata]
ms.assetid: e97c97a6-6e4f-41f5-9af1-9b3cf3bdbd6b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a08577f15a6fab0e630d40032a23c273ee935faa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992327"
---
# <a name="imetadataimportenummemberrefs-method"></a><span data-ttu-id="6fe8b-102">IMetaDataImport::EnumMemberRefs, méthode</span><span class="sxs-lookup"><span data-stu-id="6fe8b-102">IMetaDataImport::EnumMemberRefs Method</span></span>
<span data-ttu-id="6fe8b-103">Énumère les jetons MemberRef représentant les membres du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-103">Enumerates MemberRef tokens representing members of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6fe8b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe8b-104">Syntax</span></span>  
  
```  
HRESULT EnumMemberRefs (  
   [in, out] HCORENUM    *phEnum,   
   [in]   mdToken        tkParent,   
   [out]  mdMemberRef    rMemberRefs[],   
   [in]   ULONG          cMax,   
   [out]  ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6fe8b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe8b-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="6fe8b-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="6fe8b-107">[in] Un jeton TypeDef, TypeRef, MethodDef ou ModuleRef pour le type dont les membres doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-107">[in] A TypeDef, TypeRef, MethodDef, or ModuleRef token for the type whose members are to be enumerated.</span></span>  
  
 `rMemberRefs`  
 <span data-ttu-id="6fe8b-108">[out] Tableau utilisé pour stocker les jetons MemberRef.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-108">[out] The array used to store MemberRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="6fe8b-109">[in] Taille maximale du tableau `rMemberRefs`.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-109">[in] The maximum size of the `rMemberRefs` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="6fe8b-110">[out] Le nombre réel de jetons MemberRef retournés dans `rMemberRefs`.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-110">[out] The actual number of MemberRef tokens returned in `rMemberRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6fe8b-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6fe8b-111">Return Value</span></span>  
  
|<span data-ttu-id="6fe8b-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6fe8b-112">HRESULT</span></span>|<span data-ttu-id="6fe8b-113">Description</span><span class="sxs-lookup"><span data-stu-id="6fe8b-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="6fe8b-114">`EnumMemberRefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-114">`EnumMemberRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="6fe8b-115">Il n’y a aucune jetons MemberRef à énumérer.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-115">There are no MemberRef tokens to enumerate.</span></span> <span data-ttu-id="6fe8b-116">Dans ce cas, `pcTokens` est à zéro.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-116">In that case, `pcTokens` is to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6fe8b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe8b-117">Requirements</span></span>  
 <span data-ttu-id="6fe8b-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6fe8b-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6fe8b-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6fe8b-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6fe8b-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6fe8b-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6fe8b-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6fe8b-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6fe8b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe8b-122">See also</span></span>

- [<span data-ttu-id="6fe8b-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="6fe8b-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="6fe8b-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="6fe8b-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
