---
title: IMetaDataEmit::SetPermissionSetProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPermissionSetProps
helpviewer_keywords:
- SetPermissionSetProps method [.NET Framework metadata]
- IMetaDataEmit::SetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 8eaee971-40bf-45e2-a3d8-6e57674213b6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8d80e3206f74c3c50c8436563b0e39d1229a963b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446367"
---
# <a name="imetadataemitsetpermissionsetprops-method"></a><span data-ttu-id="79772-102">IMetaDataEmit::SetPermissionSetProps, méthode</span><span class="sxs-lookup"><span data-stu-id="79772-102">IMetaDataEmit::SetPermissionSetProps Method</span></span>
<span data-ttu-id="79772-103">Définit ou met à jour des fonctionnalités de la signature de métadonnées d’un jeu d’autorisations défini par un appel antérieur à [IMetaDataEmit::DefinePermissionSet](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepermissionset-method.md).</span><span class="sxs-lookup"><span data-stu-id="79772-103">Sets or updates features of the metadata signature of a permission set defined by a prior call to [IMetaDataEmit::DefinePermissionSet](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definepermissionset-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79772-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79772-104">Syntax</span></span>  
  
```  
HRESULT SetPermissionSetProps (   
    [in]  mdToken         tk,   
    [in]  DWORD           dwAction,   
    [in]  void const      *pvPermission,   
    [in]  ULONG           cbPermission,   
    [out] mdPermission    *ppm   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="79772-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79772-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="79772-106">[in] Un jeton de métadonnées qui représente l’objet à être décorée.</span><span class="sxs-lookup"><span data-stu-id="79772-106">[in] A metadata token that represents the object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="79772-107">[in] A [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md) valeur qui spécifie le type de sécurité déclarative à utiliser.</span><span class="sxs-lookup"><span data-stu-id="79772-107">[in] A [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="79772-108">[in] L’objet BLOB d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="79772-108">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="79772-109">[in] La taille, en octets, de `pvPermission`.</span><span class="sxs-lookup"><span data-stu-id="79772-109">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="79772-110">[out] Un `mdPermission` jeton de métadonnées qui représente les autorisations de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="79772-110">[out] An `mdPermission` metadata token that represents the updated permissions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79772-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="79772-111">Requirements</span></span>  
 <span data-ttu-id="79772-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79772-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79772-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="79772-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79772-114">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="79772-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="79772-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79772-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79772-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79772-116">See Also</span></span>  
 [<span data-ttu-id="79772-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="79772-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="79772-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="79772-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
