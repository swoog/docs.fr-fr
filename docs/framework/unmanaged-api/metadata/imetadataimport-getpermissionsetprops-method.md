---
title: IMetaDataImport::GetPermissionSetProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPermissionSetProps
helpviewer_keywords:
- GetPermissionSetProps method [.NET Framework metadata]
- IMetaDataImport::GetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 9855f0e4-12c0-4d3d-ab5d-d6bc52d25eae
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 806f1ebcacb9e7ad27b7370f9976b3341bf64f8c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466932"
---
# <a name="imetadataimportgetpermissionsetprops-method"></a><span data-ttu-id="94b52-102">IMetaDataImport::GetPermissionSetProps, méthode</span><span class="sxs-lookup"><span data-stu-id="94b52-102">IMetaDataImport::GetPermissionSetProps Method</span></span>
<span data-ttu-id="94b52-103">Obtient les métadonnées associées à la <xref:System.Security.PermissionSet?displayProperty=nameWithType> représenté par le jeton d’autorisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="94b52-103">Gets the metadata associated with the <xref:System.Security.PermissionSet?displayProperty=nameWithType> represented by the specified Permission token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94b52-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94b52-104">Syntax</span></span>  
  
```  
HRESULT GetPermissionSetProps (  
   [in]  mdPermission      pm,  
   [out] DWORD             *pdwAction,   
   [out] void const        **ppvPermission,   
   [out] ULONG             *pcbPermission  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94b52-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94b52-105">Parameters</span></span>  
 `pm`  
 <span data-ttu-id="94b52-106">[in] Le jeton de métadonnées d’autorisation qui représente la jeu d’autorisations à obtenir les propriétés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="94b52-106">[in] The Permission metadata token that represents the permission set to get the metadata properties for.</span></span>  
  
 `pdwAction`  
 <span data-ttu-id="94b52-107">[out] Pointeur vers le jeu d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="94b52-107">[out] A pointer to the permission set.</span></span>  
  
 `ppvPermission`  
 <span data-ttu-id="94b52-108">[out] Pointeur vers la signature de métadonnées binaires du jeu d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="94b52-108">[out] A pointer to the binary metadata signature of the permission set.</span></span>  
  
 `pcbPermission`  
 <span data-ttu-id="94b52-109">[out] La taille en octets de `ppvPermission`.</span><span class="sxs-lookup"><span data-stu-id="94b52-109">[out] The size in bytes of `ppvPermission`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94b52-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="94b52-110">Requirements</span></span>  
 <span data-ttu-id="94b52-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="94b52-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94b52-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="94b52-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="94b52-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="94b52-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="94b52-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94b52-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94b52-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94b52-115">See also</span></span>
- <xref:System.Security.PermissionSet>
- [<span data-ttu-id="94b52-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="94b52-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="94b52-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="94b52-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
