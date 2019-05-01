---
title: IMetaDataImport::EnumModuleRefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumModuleRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumModuleRefs
helpviewer_keywords:
- EnumModuleRefs method [.NET Framework metadata]
- IMetaDataImport::EnumModuleRefs method [.NET Framework metadata]
ms.assetid: 53441f3a-68d2-477c-906e-37c55dfcfb4d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d66d24da05bc3b8f0c3d0a828456d7c61613d219
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049880"
---
# <a name="imetadataimportenummodulerefs-method"></a><span data-ttu-id="7f9f9-102">IMetaDataImport::EnumModuleRefs, méthode</span><span class="sxs-lookup"><span data-stu-id="7f9f9-102">IMetaDataImport::EnumModuleRefs Method</span></span>
<span data-ttu-id="7f9f9-103">Énumère les jetons ModuleRef qui représentent des modules importés.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-103">Enumerates ModuleRef tokens that represent imported modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f9f9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f9f9-104">Syntax</span></span>  
  
```  
HRESULT EnumModuleRefs (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdModuleRef  rModuleRefs[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcModuleRefs  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f9f9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f9f9-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="7f9f9-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="7f9f9-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-107">This must be NULL for the first call of this method.</span></span>  
  
 `rModuleRefs`  
 <span data-ttu-id="7f9f9-108">[out] Tableau utilisé pour stocker les jetons ModuleRef.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-108">[out] The array used to store the ModuleRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="7f9f9-109">[in] Taille maximale du tableau `rModuleRefs`.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-109">[in] The maximum size of the `rModuleRefs` array.</span></span>  
  
 `pcModuleRefs`  
 <span data-ttu-id="7f9f9-110">[out] Le nombre de jetons ModuleRef retournés dans `rModuleRefs`.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-110">[out] The number of ModuleRef tokens returned in `rModuleRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f9f9-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7f9f9-111">Return Value</span></span>  
  
|<span data-ttu-id="7f9f9-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7f9f9-112">HRESULT</span></span>|<span data-ttu-id="7f9f9-113">Description</span><span class="sxs-lookup"><span data-stu-id="7f9f9-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="7f9f9-114">`EnumModuleRefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-114">`EnumModuleRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="7f9f9-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="7f9f9-116">Dans ce cas, `pcModuleRefs` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7f9f9-116">In that case, `pcModuleRefs` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7f9f9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f9f9-117">Requirements</span></span>  
 <span data-ttu-id="7f9f9-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7f9f9-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f9f9-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7f9f9-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7f9f9-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f9f9-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7f9f9-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f9f9-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f9f9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f9f9-122">See also</span></span>

- [<span data-ttu-id="7f9f9-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="7f9f9-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="7f9f9-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="7f9f9-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
