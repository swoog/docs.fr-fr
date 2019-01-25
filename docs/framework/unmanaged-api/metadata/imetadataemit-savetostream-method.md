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
ms.openlocfilehash: 515e925c9b086823450b73cfbb558d0409b4948a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575997"
---
# <a name="imetadataemitsavetostream-method"></a><span data-ttu-id="a52de-102">IMetaDataEmit::SaveToStream, méthode</span><span class="sxs-lookup"><span data-stu-id="a52de-102">IMetaDataEmit::SaveToStream Method</span></span>
<span data-ttu-id="a52de-103">Enregistre toutes les métadonnées dans la portée actuelle spécifié `IStream`.</span><span class="sxs-lookup"><span data-stu-id="a52de-103">Saves all metadata in the current scope to the specified `IStream`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a52de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a52de-104">Syntax</span></span>  
  
```  
HRESULT SaveToStream (   
    [in]  IStream     *pIStream,  
    [in]  DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a52de-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a52de-105">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="a52de-106">[in] Flux accessible en écriture pour enregistrer dans.</span><span class="sxs-lookup"><span data-stu-id="a52de-106">[in] The writable stream to save to.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="a52de-107">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="a52de-107">[in] Reserved.</span></span> <span data-ttu-id="a52de-108">Doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="a52de-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a52de-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a52de-109">Requirements</span></span>  
 <span data-ttu-id="a52de-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a52de-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a52de-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a52de-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a52de-112">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a52de-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a52de-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a52de-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a52de-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a52de-114">See also</span></span>
- [<span data-ttu-id="a52de-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a52de-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="a52de-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="a52de-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
