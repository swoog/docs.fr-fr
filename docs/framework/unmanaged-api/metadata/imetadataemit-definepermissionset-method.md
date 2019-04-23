---
title: IMetaDataEmit::DefinePermissionSet, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefinePermissionSet
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefinePermissionSet
helpviewer_keywords:
- DefinePermissionSet method [.NET Framework metadata]
- IMetaDataEmit::DefinePermissionSet method [.NET Framework metadata]
ms.assetid: 36cffbf7-82ca-4cf9-bf60-50ab491ac2d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 33eadccf691b14289a46ff460f3cef8ae636b129
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074844"
---
# <a name="imetadataemitdefinepermissionset-method"></a><span data-ttu-id="bd3be-102">IMetaDataEmit::DefinePermissionSet, méthode</span><span class="sxs-lookup"><span data-stu-id="bd3be-102">IMetaDataEmit::DefinePermissionSet Method</span></span>
<span data-ttu-id="bd3be-103">Crée une définition pour un jeu d’autorisations avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de jeu d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="bd3be-103">Creates a definition for a permission set with the specified metadata signature, and gets a token to that permission set definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd3be-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd3be-104">Syntax</span></span>  
  
```  
HRESULT DefinePermissionSet (  
    [in]  mdToken        tk,   
    [in]  DWORD          dwAction,   
    [in]  void const     *pvPermission,   
    [in]  ULONG          cbPermission,   
    [out] mdPermission   *ppm   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bd3be-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd3be-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="bd3be-106">[in] Objet à être décorés.</span><span class="sxs-lookup"><span data-stu-id="bd3be-106">[in] The object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="bd3be-107">[in] Un [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md) valeur qui spécifie le type de sécurité déclarative à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bd3be-107">[in] A [CorDeclSecurity](../../../../docs/framework/unmanaged-api/metadata/cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="bd3be-108">[in] L’objet BLOB d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="bd3be-108">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="bd3be-109">[in] La taille, en octets, de `pvPermission`.</span><span class="sxs-lookup"><span data-stu-id="bd3be-109">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="bd3be-110">[out] Le jeton d’autorisation retournée.</span><span class="sxs-lookup"><span data-stu-id="bd3be-110">[out] The returned permission token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd3be-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd3be-111">Requirements</span></span>  
 <span data-ttu-id="bd3be-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bd3be-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd3be-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bd3be-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bd3be-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bd3be-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bd3be-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd3be-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd3be-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd3be-116">See also</span></span>

- [<span data-ttu-id="bd3be-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="bd3be-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="bd3be-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="bd3be-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
