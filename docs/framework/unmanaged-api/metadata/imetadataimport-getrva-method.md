---
title: IMetaDataImport::GetRVA, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetRVA
helpviewer_keywords:
- GetRVA method [.NET Framework metadata]
- IMetaDataImport::GetRVA method [.NET Framework metadata]
ms.assetid: ea422217-988b-4acd-b2db-c55357938275
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1232e8c574f263f709a9b66c7b1b3d06cca5e4da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447209"
---
# <a name="imetadataimportgetrva-method"></a><span data-ttu-id="c9eea-102">IMetaDataImport::GetRVA, méthode</span><span class="sxs-lookup"><span data-stu-id="c9eea-102">IMetaDataImport::GetRVA Method</span></span>
<span data-ttu-id="c9eea-103">Obtient l’adresse virtuelle relative (RVA) et les indicateurs d’implémentation de la méthode ou le champ représenté par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9eea-103">Gets the relative virtual address (RVA) and the implementation flags of the method or field represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9eea-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9eea-104">Syntax</span></span>  
  
```  
HRESULT GetRVA (  
   [in]  mdToken     tk,   
   [out] ULONG       *pulCodeRVA,   
   [out]  DWORD      *pdwImplFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c9eea-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9eea-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="c9eea-106">[in] Un jeton de métadonnées MethodDef ou FieldDef qui représente l’objet de code pour renvoyer l’adresse RVA.</span><span class="sxs-lookup"><span data-stu-id="c9eea-106">[in] A MethodDef or FieldDef metadata token that represents the code object to return the RVA for.</span></span> <span data-ttu-id="c9eea-107">Si le jeton est FieldDef, le champ doit être une variable globale.</span><span class="sxs-lookup"><span data-stu-id="c9eea-107">If the token is a FieldDef, the field must be a global variable.</span></span>  
  
 `pulCodeRVA`  
 <span data-ttu-id="c9eea-108">[out] Pointeur vers l’adresse virtuelle relative de l’objet de code représenté par le jeton.</span><span class="sxs-lookup"><span data-stu-id="c9eea-108">[out] A pointer to the relative virtual address of the code object represented by the token.</span></span>  
  
 `pdwImplFlags`  
 <span data-ttu-id="c9eea-109">[out] Pointeur vers les indicateurs d’implémentation pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="c9eea-109">[out] A pointer to the implementation flags for the method.</span></span> <span data-ttu-id="c9eea-110">Cette valeur est un masque de bits de le [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="c9eea-110">This value is a bitmask from the [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) enumeration.</span></span> <span data-ttu-id="c9eea-111">La valeur de `pdwImplFlags` n’est valide uniquement si `tk` est un jeton MethodDef.</span><span class="sxs-lookup"><span data-stu-id="c9eea-111">The value of `pdwImplFlags` is valid only if `tk` is a MethodDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9eea-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9eea-112">Requirements</span></span>  
 <span data-ttu-id="c9eea-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c9eea-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9eea-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c9eea-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c9eea-115">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c9eea-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c9eea-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9eea-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9eea-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9eea-117">See Also</span></span>  
 [<span data-ttu-id="c9eea-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="c9eea-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="c9eea-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="c9eea-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
