---
title: IMetaDataImport::EnumMethods, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethods
helpviewer_keywords:
- IMetaDataImport::EnumMethods method [.NET Framework metadata]
- EnumMethods method [.NET Framework metadata]
ms.assetid: 8cc3b0c3-d97d-4f71-9e7d-ef2a92b4959a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 668c7298a9543cce93cce324672334c9ec1e8cd2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732815"
---
# <a name="imetadataimportenummethods-method"></a><span data-ttu-id="ef5f2-102">IMetaDataImport::EnumMethods, méthode</span><span class="sxs-lookup"><span data-stu-id="ef5f2-102">IMetaDataImport::EnumMethods Method</span></span>
<span data-ttu-id="ef5f2-103">Énumère les jetons MethodDef représentant les méthodes du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-103">Enumerates MethodDef tokens representing methods of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef5f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef5f2-104">Syntax</span></span>  
  
```  
HRESULT EnumMethods (  
   [in, out] HCORENUM   *phEnum,   
   [in]  mdTypeDef      cl,   
   [out] mdMethodDef    rMethods[],   
   [in]  ULONG          cMax,   
   [out] ULONG          *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ef5f2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef5f2-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="ef5f2-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="ef5f2-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-107">This must be NULL for the first call of this method.</span></span>  
  
 `cl`  
 <span data-ttu-id="ef5f2-108">[in] Jeton TypeDef représentant le type dont les méthodes à énumérer.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-108">[in] A TypeDef token representing the type with the methods to enumerate.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="ef5f2-109">[out] Le tableau pour stocker les jetons MethodDef.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-109">[out] The array to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="ef5f2-110">[in] La taille maximale de le MethodDef `rMethods` tableau.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-110">[in] The maximum size of the MethodDef `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="ef5f2-111">[out] Le nombre de jetons MethodDef retournés dans `rMethods`.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-111">[out] The number of MethodDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ef5f2-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ef5f2-112">Return Value</span></span>  
  
|<span data-ttu-id="ef5f2-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ef5f2-113">HRESULT</span></span>|<span data-ttu-id="ef5f2-114">Description</span><span class="sxs-lookup"><span data-stu-id="ef5f2-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="ef5f2-115">`EnumMethods` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-115">`EnumMethods` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="ef5f2-116">Il n’y a aucune jetons MethodDef à énumérer.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-116">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="ef5f2-117">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef5f2-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ef5f2-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ef5f2-118">Requirements</span></span>  
 <span data-ttu-id="ef5f2-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef5f2-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef5f2-120">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ef5f2-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ef5f2-121">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ef5f2-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ef5f2-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef5f2-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef5f2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef5f2-123">See also</span></span>
- [<span data-ttu-id="ef5f2-124">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="ef5f2-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="ef5f2-125">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="ef5f2-125">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
