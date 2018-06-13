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
ms.openlocfilehash: f1f8acc546c0d96aca079223200b43aec933f729
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447907"
---
# <a name="imetadataimportgetmodulefromscope-method"></a><span data-ttu-id="83e5f-102">IMetaDataImport::GetModuleFromScope, méthode</span><span class="sxs-lookup"><span data-stu-id="83e5f-102">IMetaDataImport::GetModuleFromScope Method</span></span>
<span data-ttu-id="83e5f-103">Obtient des jetons de métadonnées pour le module référencé dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="83e5f-103">Gets a metadata token for the module referenced in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83e5f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83e5f-104">Syntax</span></span>  
  
```  
HRESULT GetModuleFromScope (  
   [out] mdModule    *pmd  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="83e5f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83e5f-105">Parameters</span></span>  
 `pmd`  
 <span data-ttu-id="83e5f-106">[out] Pointeur vers le jeton représentant le module référencé dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="83e5f-106">[out] A pointer to the token representing the module referenced in the current metadata scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83e5f-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83e5f-107">Requirements</span></span>  
 <span data-ttu-id="83e5f-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83e5f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83e5f-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="83e5f-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="83e5f-110">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83e5f-110">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="83e5f-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83e5f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83e5f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83e5f-112">See Also</span></span>  
 [<span data-ttu-id="83e5f-113">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="83e5f-113">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="83e5f-114">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="83e5f-114">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
