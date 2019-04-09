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
ms.openlocfilehash: 3ff91a24dec7f8507989b701ea24b569c1670c89
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59109705"
---
# <a name="imetadataimportgetpermissionsetprops-method"></a><span data-ttu-id="721b6-102">IMetaDataImport::GetPermissionSetProps, méthode</span><span class="sxs-lookup"><span data-stu-id="721b6-102">IMetaDataImport::GetPermissionSetProps Method</span></span>
<span data-ttu-id="721b6-103">Obtient les métadonnées associées à la <xref:System.Security.PermissionSet?displayProperty=nameWithType> représenté par le jeton d’autorisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="721b6-103">Gets the metadata associated with the <xref:System.Security.PermissionSet?displayProperty=nameWithType> represented by the specified Permission token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="721b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="721b6-104">Syntax</span></span>  
  
```  
HRESULT GetPermissionSetProps (  
   [in]  mdPermission      pm,  
   [out] DWORD             *pdwAction,   
   [out] void const        **ppvPermission,   
   [out] ULONG             *pcbPermission  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="721b6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="721b6-105">Parameters</span></span>  
 `pm`  
 <span data-ttu-id="721b6-106">[in] Le jeton de métadonnées d’autorisation qui représente la jeu d’autorisations à obtenir les propriétés de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="721b6-106">[in] The Permission metadata token that represents the permission set to get the metadata properties for.</span></span>  
  
 `pdwAction`  
 <span data-ttu-id="721b6-107">[out] Pointeur vers le jeu d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="721b6-107">[out] A pointer to the permission set.</span></span>  
  
 `ppvPermission`  
 <span data-ttu-id="721b6-108">[out] Pointeur vers la signature de métadonnées binaires du jeu d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="721b6-108">[out] A pointer to the binary metadata signature of the permission set.</span></span>  
  
 `pcbPermission`  
 <span data-ttu-id="721b6-109">[out] La taille en octets de `ppvPermission`.</span><span class="sxs-lookup"><span data-stu-id="721b6-109">[out] The size in bytes of `ppvPermission`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="721b6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="721b6-110">Requirements</span></span>  
 <span data-ttu-id="721b6-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="721b6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="721b6-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="721b6-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="721b6-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="721b6-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="721b6-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="721b6-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="721b6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="721b6-115">See also</span></span>

- <xref:System.Security.PermissionSet>
- [<span data-ttu-id="721b6-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="721b6-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="721b6-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="721b6-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
