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
ms.openlocfilehash: bab625b8415183b9cf90c35cba140c4d28095805
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076872"
---
# <a name="imetadataimportenummethods-method"></a><span data-ttu-id="3314f-102">IMetaDataImport::EnumMethods, méthode</span><span class="sxs-lookup"><span data-stu-id="3314f-102">IMetaDataImport::EnumMethods Method</span></span>
<span data-ttu-id="3314f-103">Énumère les jetons MethodDef représentant les méthodes du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="3314f-103">Enumerates MethodDef tokens representing methods of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3314f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3314f-104">Syntax</span></span>  
  
```  
HRESULT EnumMethods (  
   [in, out] HCORENUM   *phEnum,   
   [in]  mdTypeDef      cl,   
   [out] mdMethodDef    rMethods[],   
   [in]  ULONG          cMax,   
   [out] ULONG          *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3314f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3314f-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="3314f-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="3314f-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="3314f-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3314f-107">This must be NULL for the first call of this method.</span></span>  
  
 `cl`  
 <span data-ttu-id="3314f-108">[in] Jeton TypeDef représentant le type dont les méthodes à énumérer.</span><span class="sxs-lookup"><span data-stu-id="3314f-108">[in] A TypeDef token representing the type with the methods to enumerate.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="3314f-109">[out] Le tableau pour stocker les jetons MethodDef.</span><span class="sxs-lookup"><span data-stu-id="3314f-109">[out] The array to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3314f-110">[in] La taille maximale de le MethodDef `rMethods` tableau.</span><span class="sxs-lookup"><span data-stu-id="3314f-110">[in] The maximum size of the MethodDef `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="3314f-111">[out] Le nombre de jetons MethodDef retournés dans `rMethods`.</span><span class="sxs-lookup"><span data-stu-id="3314f-111">[out] The number of MethodDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3314f-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3314f-112">Return Value</span></span>  
  
|<span data-ttu-id="3314f-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3314f-113">HRESULT</span></span>|<span data-ttu-id="3314f-114">Description</span><span class="sxs-lookup"><span data-stu-id="3314f-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="3314f-115">`EnumMethods` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3314f-115">`EnumMethods` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3314f-116">Il n’y a aucune jetons MethodDef à énumérer.</span><span class="sxs-lookup"><span data-stu-id="3314f-116">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="3314f-117">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3314f-117">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3314f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3314f-118">Requirements</span></span>  
 <span data-ttu-id="3314f-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3314f-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3314f-120">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3314f-120">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3314f-121">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3314f-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3314f-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3314f-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3314f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3314f-123">See also</span></span>

- [<span data-ttu-id="3314f-124">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3314f-124">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="3314f-125">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="3314f-125">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
