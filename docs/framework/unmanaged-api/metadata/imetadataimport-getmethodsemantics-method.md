---
title: IMetaDataImport::GetMethodSemantics, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMethodSemantics
helpviewer_keywords:
- GetMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::GetMethodSemantics method [.NET Framework metadata]
ms.assetid: 5e018eaa-d60e-4a0b-a2c5-8c36bd09d905
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4f4908f5d03687fb415c91325941aaab148832dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447736"
---
# <a name="imetadataimportgetmethodsemantics-method"></a><span data-ttu-id="27f28-102">IMetaDataImport::GetMethodSemantics, méthode</span><span class="sxs-lookup"><span data-stu-id="27f28-102">IMetaDataImport::GetMethodSemantics Method</span></span>
<span data-ttu-id="27f28-103">Obtient les indicateurs qui indique la relation entre la méthode référencée par le jeton MethodDef spécifié et la paire propriété et événement référencée par la EventProp spécifié jeton.</span><span class="sxs-lookup"><span data-stu-id="27f28-103">Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27f28-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27f28-104">Syntax</span></span>  
  
```  
HRESULT GetMethodSemantics (  
   [in]  mdMethodDef   mb,  
   [in]  mdToken       tkEventProp,  
   [out] DWORD         *pdwSemanticsFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="27f28-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27f28-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="27f28-106">[in] Jeton MethodDef représentant la méthode à obtenir les informations de rôle sémantique.</span><span class="sxs-lookup"><span data-stu-id="27f28-106">[in] A MethodDef token representing the method to get the semantic role information for.</span></span>  
  
 `tkEventProp`  
 <span data-ttu-id="27f28-107">[in] Un jeton représentant la paire propriété et un événement pour lequel obtenir le rôle de la méthode.</span><span class="sxs-lookup"><span data-stu-id="27f28-107">[in] A token representing the paired property and event for which to get the method's role.</span></span>  
  
 `pdwSemanticsFlags`  
 <span data-ttu-id="27f28-108">[out] Pointeur vers les indicateurs de sémantique associés.</span><span class="sxs-lookup"><span data-stu-id="27f28-108">[out] A pointer to the associated semantics flags.</span></span> <span data-ttu-id="27f28-109">Cette valeur est un masque de bits de le [CorMethodSemanticsAttr](../../../../docs/framework/unmanaged-api/metadata/cormethodsemanticsattr-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="27f28-109">This value is a bitmask from the [CorMethodSemanticsAttr](../../../../docs/framework/unmanaged-api/metadata/cormethodsemanticsattr-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="27f28-110">Notes</span><span class="sxs-lookup"><span data-stu-id="27f28-110">Remarks</span></span>  
 <span data-ttu-id="27f28-111">Le [IMetaDataEmit::DefineProperty](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md) méthode définit les indicateurs de sémantique d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="27f28-111">The [IMetaDataEmit::DefineProperty](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md) method sets a method's semantics flags.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="27f28-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="27f28-112">Requirements</span></span>  
 <span data-ttu-id="27f28-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="27f28-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="27f28-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="27f28-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="27f28-115">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="27f28-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="27f28-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="27f28-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27f28-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27f28-117">See Also</span></span>  
 [<span data-ttu-id="27f28-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="27f28-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="27f28-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="27f28-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
