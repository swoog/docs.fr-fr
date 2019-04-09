---
title: IMetaDataEmit2::SaveDelta, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.SaveDelta
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::SaveDelta
helpviewer_keywords:
- IMetaDataEmit2::SaveDelta method [.NET Framework metadata]
- SaveDelta method [.NET Framework metadata]
ms.assetid: b95739fe-d2fa-4776-ae0d-31d9707ef799
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d97f536d54ac1cb77c5d0413d2437508374ac7f4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59168998"
---
# <a name="imetadataemit2savedelta-method"></a><span data-ttu-id="c5924-102">IMetaDataEmit2::SaveDelta, méthode</span><span class="sxs-lookup"><span data-stu-id="c5924-102">IMetaDataEmit2::SaveDelta Method</span></span>
<span data-ttu-id="c5924-103">Enregistre les modifications de la session active modifier et continuer dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c5924-103">Saves changes from the current edit-and-continue session to the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5924-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5924-104">Syntax</span></span>  
  
```  
HRESULT SaveDelta (  
    [in] LPCWSTR     szFile,   
    [in] DWORD       dwSaveFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c5924-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5924-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="c5924-106">[in] Le nom de fichier sous lequel enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="c5924-106">[in] The file name under which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="c5924-107">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="c5924-107">[in] Reserved.</span></span> <span data-ttu-id="c5924-108">Doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5924-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5924-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5924-109">Requirements</span></span>  
 <span data-ttu-id="c5924-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c5924-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c5924-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c5924-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c5924-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c5924-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="c5924-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c5924-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c5924-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5924-114">See also</span></span>

- [<span data-ttu-id="c5924-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="c5924-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [<span data-ttu-id="c5924-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="c5924-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
