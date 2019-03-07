---
title: IMetaDataEmit::SetModuleProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetModuleProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetModuleProps
helpviewer_keywords:
- SetModuleProps method [.NET Framework metadata]
- IMetaDataEmit::SetModuleProps method [.NET Framework metadata]
ms.assetid: b74d7629-5f46-458f-8d67-2456a1e7030c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5219a414c5961128d4eaa27c1f18d635938dc5ba
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57497403"
---
# <a name="imetadataemitsetmoduleprops-method"></a><span data-ttu-id="a669b-102">IMetaDataEmit::SetModuleProps, méthode</span><span class="sxs-lookup"><span data-stu-id="a669b-102">IMetaDataEmit::SetModuleProps Method</span></span>
<span data-ttu-id="a669b-103">Met à jour les références à un module défini par un appel antérieur à [IMetaDataEmit::DefineModuleRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemoduleref-method.md).</span><span class="sxs-lookup"><span data-stu-id="a669b-103">Updates references to a module defined by a prior call to [IMetaDataEmit::DefineModuleRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemoduleref-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a669b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a669b-104">Syntax</span></span>  
  
```  
HRESULT SetModuleProps (   
    [in]  LPCWSTR     szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a669b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a669b-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="a669b-106">[in] Le nom du module au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="a669b-106">[in] The module name in Unicode.</span></span> <span data-ttu-id="a669b-107">C’est le nom de fichier uniquement et pas le nom de chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="a669b-107">This is the file name only and not the full path name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a669b-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a669b-108">Requirements</span></span>  
 <span data-ttu-id="a669b-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a669b-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a669b-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a669b-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a669b-111">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a669b-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a669b-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a669b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a669b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a669b-113">See also</span></span>
- [<span data-ttu-id="a669b-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a669b-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="a669b-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="a669b-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
