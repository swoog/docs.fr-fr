---
title: IMetaDataEmit::SaveToMemory, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SaveToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToMemory
helpviewer_keywords:
- IMetaDataEmit::SaveToMemory method [.NET Framework metadata]
- SaveToMemory method [.NET Framework metadata]
ms.assetid: d5237628-2675-45ed-a39e-65c0731b6a56
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bc840df9dd0793a7347b7f0d8a05296a09d634c8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192106"
---
# <a name="imetadataemitsavetomemory-method"></a><span data-ttu-id="2b440-102">IMetaDataEmit::SaveToMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="2b440-102">IMetaDataEmit::SaveToMemory Method</span></span>
<span data-ttu-id="2b440-103">Enregistre toutes les métadonnées dans la portée actuelle dans la zone de mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2b440-103">Saves all metadata in the current scope to the specified area of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b440-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b440-104">Syntax</span></span>  
  
```  
HRESULT SaveToMemory (   
    [out]  void        *pbData,   
    [in]   ULONG       cbData   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2b440-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b440-105">Parameters</span></span>  
 `pbData`  
 <span data-ttu-id="2b440-106">[out] L’adresse à laquelle commencer l’écriture des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="2b440-106">[out] The address at which to begin writing metadata.</span></span>  
  
 `cbData`  
 <span data-ttu-id="2b440-107">[in] La taille, en octets, de la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="2b440-107">[in] The size, in bytes, of the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2b440-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b440-108">Requirements</span></span>  
 <span data-ttu-id="2b440-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2b440-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2b440-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2b440-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2b440-111">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2b440-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2b440-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2b440-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b440-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b440-113">See also</span></span>

- [<span data-ttu-id="2b440-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="2b440-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="2b440-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="2b440-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
