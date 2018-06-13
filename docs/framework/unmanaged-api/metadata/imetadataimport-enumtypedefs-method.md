---
title: IMetaDataImport::EnumTypeDefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeDefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeDefs
helpviewer_keywords:
- EnumTypeDefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeDefs method [.NET Framework metadata]
ms.assetid: 4e508711-da92-4381-aaf8-6803075cdaa2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 53ed486a885514d02bf2be9c473e102c2c5f0e15
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446841"
---
# <a name="imetadataimportenumtypedefs-method"></a><span data-ttu-id="402c7-102">IMetaDataImport::EnumTypeDefs, méthode</span><span class="sxs-lookup"><span data-stu-id="402c7-102">IMetaDataImport::EnumTypeDefs Method</span></span>
<span data-ttu-id="402c7-103">Énumère les jetons TypeDef représentant tous les types au sein la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="402c7-103">Enumerates TypeDef tokens representing all types within the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="402c7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="402c7-104">Syntax</span></span>  
  
```  
HRESULT EnumTypeDefs (  
   [out] HCORENUM   *phEnum,   
   [in]  mdTypeDef  rTypeDefs[],  
   [in]  ULONG      cMax,   
   [out] ULONG      *pcTypeDefs  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="402c7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="402c7-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="402c7-106">[out] Pointeur vers le nouvel énumérateur.</span><span class="sxs-lookup"><span data-stu-id="402c7-106">[out] A pointer to the new enumerator.</span></span> <span data-ttu-id="402c7-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="402c7-107">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeDefs`  
 <span data-ttu-id="402c7-108">[in] Tableau utilisé pour stocker les jetons TypeDef.</span><span class="sxs-lookup"><span data-stu-id="402c7-108">[in] The array used to store the TypeDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="402c7-109">[in] Taille maximale du tableau `rTypeDefs`.</span><span class="sxs-lookup"><span data-stu-id="402c7-109">[in] The maximum size of the `rTypeDefs` array.</span></span>  
  
 `pcTypeDefs`  
 <span data-ttu-id="402c7-110">[out] Le nombre de jetons TypeDef retournés dans `rTypeDefs`.</span><span class="sxs-lookup"><span data-stu-id="402c7-110">[out] The number of TypeDef tokens returned in `rTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="402c7-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="402c7-111">Return Value</span></span>  
  
|<span data-ttu-id="402c7-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="402c7-112">HRESULT</span></span>|<span data-ttu-id="402c7-113">Description</span><span class="sxs-lookup"><span data-stu-id="402c7-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="402c7-114">`EnumTypeDefs` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="402c7-114">`EnumTypeDefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="402c7-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="402c7-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="402c7-116">Dans ce cas, `pcTypeDefs` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="402c7-116">In that case, `pcTypeDefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="402c7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="402c7-117">Remarks</span></span>  
 <span data-ttu-id="402c7-118">Le jeton TypeDef représente un type tel qu’une classe ou une interface, ainsi que tout type ajouté via un mécanisme d’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="402c7-118">The TypeDef token represents a type such as a class or an interface, as well as any type added via an extensibility mechanism.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="402c7-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="402c7-119">Requirements</span></span>  
 <span data-ttu-id="402c7-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="402c7-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="402c7-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="402c7-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="402c7-122">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="402c7-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="402c7-123">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="402c7-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="402c7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="402c7-124">See Also</span></span>  
 [<span data-ttu-id="402c7-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="402c7-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="402c7-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="402c7-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
