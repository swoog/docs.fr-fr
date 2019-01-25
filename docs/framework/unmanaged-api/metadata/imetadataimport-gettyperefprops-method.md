---
title: IMetaDataImport::GetTypeRefProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetTypeRefProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetTypeRefProps
helpviewer_keywords:
- IMetaDataImport::GetTypeRefProps method [.NET Framework metadata]
- GetTypeRefProps method [.NET Framework metadata]
ms.assetid: 01837955-ce1e-4068-b338-fd473bd77d1d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 191a6e4fcfe340ed43e85a9aa90f8a2ec0931730
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671653"
---
# <a name="imetadataimportgettyperefprops-method"></a><span data-ttu-id="1dd7d-102">IMetaDataImport::GetTypeRefProps, méthode</span><span class="sxs-lookup"><span data-stu-id="1dd7d-102">IMetaDataImport::GetTypeRefProps Method</span></span>
<span data-ttu-id="1dd7d-103">Obtient les métadonnées associées à la <xref:System.Type> référencé par le jeton TypeRef spécifié.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-103">Gets the metadata associated with the <xref:System.Type> referenced by the specified TypeRef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dd7d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1dd7d-104">Syntax</span></span>  
  
```  
HRESULT GetTypeRefProps (  
   [in]  mdTypeRef   tr,  
   [out] mdToken     *ptkResolutionScope,  
   [out] LPWSTR      szName,  
   [in]  ULONG       cchName,  
   [out] ULONG       *pchName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1dd7d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1dd7d-105">Parameters</span></span>  
 `tr`  
 <span data-ttu-id="1dd7d-106">[in] Le jeton TypeRef qui représente le type à retourner les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-106">[in] The TypeRef token that represents the type to return metadata for.</span></span>  
  
 `ptkResolutionScope`  
 <span data-ttu-id="1dd7d-107">[out] Pointeur vers la portée dans laquelle la référence est faite.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-107">[out] A pointer to the scope in which the reference is made.</span></span> <span data-ttu-id="1dd7d-108">Cette valeur est un jeton AssemblyRef ou ModuleRef.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-108">This value is an AssemblyRef or ModuleRef token.</span></span>  
  
 `szName`  
 <span data-ttu-id="1dd7d-109">[out] Une mémoire tampon contenant le nom de type.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-109">[out] A buffer containing the type name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="1dd7d-110">[in] La taille demandée en caractères larges de `szName`.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-110">[in] The requested size in wide characters of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="1dd7d-111">[out] La taille retournée en caractères larges de `szName`.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-111">[out] The returned size in wide characters of `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dd7d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1dd7d-112">Requirements</span></span>  
 <span data-ttu-id="1dd7d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1dd7d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1dd7d-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1dd7d-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1dd7d-115">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1dd7d-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1dd7d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1dd7d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dd7d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dd7d-117">See also</span></span>
- [<span data-ttu-id="1dd7d-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="1dd7d-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="1dd7d-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="1dd7d-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
