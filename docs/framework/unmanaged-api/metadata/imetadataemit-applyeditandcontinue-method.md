---
title: IMetaDataEmit::ApplyEditAndContinue, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.ApplyEditAndContinue
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::ApplyEditAndContinue
helpviewer_keywords:
- ApplyEditAndContinue method [.NET Framework metadata]
- IMetaDataEmit::ApplyEditAndContinue method [.NET Framework metadata]
ms.assetid: 35991289-f389-495d-8caa-a6384fb1d557
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: faa9bc412e67e0e49ee969bd8b246a424fe628a0
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44193274"
---
# <a name="imetadataemitapplyeditandcontinue-method"></a><span data-ttu-id="2d28f-102">IMetaDataEmit::ApplyEditAndContinue, méthode</span><span class="sxs-lookup"><span data-stu-id="2d28f-102">IMetaDataEmit::ApplyEditAndContinue Method</span></span>
<span data-ttu-id="2d28f-103">Met à jour la portée d’assembly actuelle avec les modifications apportées dans les métadonnées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2d28f-103">Updates the current assembly scope with the changes made in the specified metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d28f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d28f-104">Syntax</span></span>  
  
```  
HRESULT ApplyEditAndContinue (   
    [in]  IUnknown    *pImport  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2d28f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d28f-105">Parameters</span></span>  
 `pImport`  
 <span data-ttu-id="2d28f-106">\[dans\] pointeur vers un [IUnknown](/cpp/atl/iunknown) objet qui représente les métadonnées delta à partir du fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="2d28f-106">\[in\] Pointer to an [IUnknown](/cpp/atl/iunknown) object that represents the delta metadata from the portable executable (PE) file.</span></span>
  
 <span data-ttu-id="2d28f-107">Les métadonnées delta sont le bloc de métadonnées qui inclut les modifications qui ont été apportées à la copie des métadonnées réelles du module.</span><span class="sxs-lookup"><span data-stu-id="2d28f-107">The delta metadata is the block of metadata that includes the changes that were made to the copy of the module's actual metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d28f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d28f-108">Requirements</span></span>  
 <span data-ttu-id="2d28f-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2d28f-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d28f-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2d28f-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2d28f-111">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2d28f-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2d28f-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d28f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d28f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d28f-113">See Also</span></span>  
 [<span data-ttu-id="2d28f-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="2d28f-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="2d28f-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="2d28f-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
