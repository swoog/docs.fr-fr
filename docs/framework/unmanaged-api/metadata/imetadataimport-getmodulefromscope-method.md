---
title: IMetaDataImport::GetModuleFromScope, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetModuleFromScope
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetModuleFromScope
helpviewer_keywords:
- GetModuleFromScope method [.NET Framework metadata]
- IMetaDataImport::GetModuleFromScope method [.NET Framework metadata]
ms.assetid: add68d3f-45fd-4bef-af94-eb5273f26b11
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1118c29acd926821e3b5db31694df9935bdefb9e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468804"
---
# <a name="imetadataimportgetmodulefromscope-method"></a><span data-ttu-id="d75a9-102">IMetaDataImport::GetModuleFromScope, méthode</span><span class="sxs-lookup"><span data-stu-id="d75a9-102">IMetaDataImport::GetModuleFromScope Method</span></span>
<span data-ttu-id="d75a9-103">Obtient les métadonnées jeton pour le module référencé dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="d75a9-103">Gets a metadata token for the module referenced in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d75a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d75a9-104">Syntax</span></span>  
  
```  
HRESULT GetModuleFromScope (  
   [out] mdModule    *pmd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d75a9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d75a9-105">Parameters</span></span>  
 `pmd`  
 <span data-ttu-id="d75a9-106">[out] Pointeur vers le jeton représentant le module référencé dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="d75a9-106">[out] A pointer to the token representing the module referenced in the current metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d75a9-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d75a9-107">Requirements</span></span>  
 <span data-ttu-id="d75a9-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d75a9-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d75a9-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d75a9-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d75a9-110">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d75a9-110">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d75a9-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d75a9-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d75a9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d75a9-112">See also</span></span>
- [<span data-ttu-id="d75a9-113">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="d75a9-113">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="d75a9-114">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="d75a9-114">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
