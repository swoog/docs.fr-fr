---
title: IMetaDataEmit2::SaveDeltaToStream, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDeltaToStream
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDeltaToStream
helpviewer_keywords:
- IMetaDataEmit2::SaveDeltaToStream method [.NET Framework metadata]
- SaveDeltaToStream method [.NET Framework metadata]
ms.assetid: ecd786e8-f9a4-4190-a6ef-af18e8c6d654
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e9dfd97ce5b9b192b9a2e88e3d7e4f963d929f47
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449258"
---
# <a name="imetadataemit2savedeltatostream-method"></a><span data-ttu-id="b77ff-102">IMetaDataEmit2::SaveDeltaToStream, méthode</span><span class="sxs-lookup"><span data-stu-id="b77ff-102">IMetaDataEmit2::SaveDeltaToStream Method</span></span>
<span data-ttu-id="b77ff-103">Enregistre les modifications de la session modifier et continuer actuelle dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="b77ff-103">Saves changes from the current edit-and-continue session to the specified stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b77ff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b77ff-104">Syntax</span></span>  
  
```  
HRESULT SaveDeltaToStream (  
    [in] IStream     *pIStream,   
    [in] DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b77ff-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b77ff-105">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="b77ff-106">[in] Un pointeur d’interface dans le flux accessible en écriture dans lequel enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="b77ff-106">[in] An interface pointer to the writable stream to which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="b77ff-107">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="b77ff-107">[in] Reserved.</span></span> <span data-ttu-id="b77ff-108">Cette valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b77ff-108">This value must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b77ff-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b77ff-109">Requirements</span></span>  
 <span data-ttu-id="b77ff-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b77ff-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b77ff-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b77ff-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b77ff-112">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b77ff-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b77ff-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b77ff-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b77ff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b77ff-114">See Also</span></span>  
 [<span data-ttu-id="b77ff-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="b77ff-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)  
 [<span data-ttu-id="b77ff-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="b77ff-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
