---
title: IMetaDataImport::GetScopeProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetScopeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetScopeProps
helpviewer_keywords:
- IMetaDataImport::GetScopeProps method [.NET Framework metadata]
- GetScopeProps method [.NET Framework metadata]
ms.assetid: c8ba42d2-d9fa-43cb-bbc0-f33e1e592cb6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 17568a46c8e946989af0e401366d7eaa885886da
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59220966"
---
# <a name="imetadataimportgetscopeprops-method"></a><span data-ttu-id="92e9d-102">IMetaDataImport::GetScopeProps, méthode</span><span class="sxs-lookup"><span data-stu-id="92e9d-102">IMetaDataImport::GetScopeProps Method</span></span>
<span data-ttu-id="92e9d-103">Obtient le nom et éventuellement l'identificateur de version de l'assembly ou du module dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="92e9d-103">Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92e9d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92e9d-104">Syntax</span></span>  
  
```  
HRESULT GetScopeProps (  
   [out] LPWSTR           szName,  
   [in]  ULONG            cchName,  
   [out] ULONG            *pchName,  
   [out, optional] GUID   *pmvid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="92e9d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92e9d-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="92e9d-106">[out] Une mémoire tampon pour le nom de l’assembly ou du module.</span><span class="sxs-lookup"><span data-stu-id="92e9d-106">[out] A buffer for the assembly or module name.</span></span>  
  
 `cchName`  
 <span data-ttu-id="92e9d-107">[in] La taille en caractères larges de `szName`.</span><span class="sxs-lookup"><span data-stu-id="92e9d-107">[in] The size in wide characters of `szName`.</span></span>  
  
 `pchName`  
 <span data-ttu-id="92e9d-108">[out] Le nombre de caractères étendus retournés dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="92e9d-108">[out] The number of wide characters returned in `szName`.</span></span>  
  
 `pmvid`  
 <span data-ttu-id="92e9d-109">[out, optional] Pointeur vers un GUID qui identifie de façon unique la version de l’assembly ou le module.</span><span class="sxs-lookup"><span data-stu-id="92e9d-109">[out, optional] A pointer to a GUID that uniquely identifies the version of the assembly or module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="92e9d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="92e9d-110">Remarks</span></span>  
 <span data-ttu-id="92e9d-111">Le [IMetaDataEmit::SetModuleProps](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmoduleprops-method.md) méthode est utilisée pour définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="92e9d-111">The [IMetaDataEmit::SetModuleProps](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-setmoduleprops-method.md) method is used to set these properties.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="92e9d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92e9d-112">Requirements</span></span>  
 <span data-ttu-id="92e9d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="92e9d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="92e9d-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="92e9d-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="92e9d-115">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="92e9d-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="92e9d-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="92e9d-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="92e9d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92e9d-117">See also</span></span>

- [<span data-ttu-id="92e9d-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="92e9d-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="92e9d-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="92e9d-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
