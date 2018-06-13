---
title: IMetaDataEmit::SaveToStream, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SaveToStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToStream
helpviewer_keywords:
- IMetaDataEmit::SaveToStream method [.NET Framework metadata]
- SaveToStream method [.NET Framework metadata]
ms.assetid: e0290a49-3818-4a43-ad46-3014faa34f97
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 656f5ee20e50ea9ac5c03711adfd0b8264fbcca0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444956"
---
# <a name="imetadataemitsavetostream-method"></a><span data-ttu-id="98b94-102">IMetaDataEmit::SaveToStream, méthode</span><span class="sxs-lookup"><span data-stu-id="98b94-102">IMetaDataEmit::SaveToStream Method</span></span>
<span data-ttu-id="98b94-103">Enregistre toutes les métadonnées dans la portée actuelle spécifié `IStream`.</span><span class="sxs-lookup"><span data-stu-id="98b94-103">Saves all metadata in the current scope to the specified `IStream`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98b94-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98b94-104">Syntax</span></span>  
  
```  
HRESULT SaveToStream (   
    [in]  IStream     *pIStream,  
    [in]  DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="98b94-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98b94-105">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="98b94-106">[in] Flux de données accessible en écriture pour enregistrer dans.</span><span class="sxs-lookup"><span data-stu-id="98b94-106">[in] The writable stream to save to.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="98b94-107">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="98b94-107">[in] Reserved.</span></span> <span data-ttu-id="98b94-108">Doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="98b94-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="98b94-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98b94-109">Requirements</span></span>  
 <span data-ttu-id="98b94-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="98b94-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="98b94-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="98b94-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="98b94-112">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="98b94-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="98b94-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="98b94-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98b94-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b94-114">See Also</span></span>  
 [<span data-ttu-id="98b94-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="98b94-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="98b94-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="98b94-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
