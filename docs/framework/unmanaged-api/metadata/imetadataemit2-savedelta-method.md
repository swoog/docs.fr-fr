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
ms.openlocfilehash: 7098bceee6bf60cd7781606ffc889b6af9c3e3cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445333"
---
# <a name="imetadataemit2savedelta-method"></a><span data-ttu-id="ebbff-102">IMetaDataEmit2::SaveDelta, méthode</span><span class="sxs-lookup"><span data-stu-id="ebbff-102">IMetaDataEmit2::SaveDelta Method</span></span>
<span data-ttu-id="ebbff-103">Enregistre les modifications de la session modifier et continuer actuelle dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ebbff-103">Saves changes from the current edit-and-continue session to the specified file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebbff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebbff-104">Syntax</span></span>  
  
```  
HRESULT SaveDelta (  
    [in] LPCWSTR     szFile,   
    [in] DWORD       dwSaveFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ebbff-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebbff-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="ebbff-106">[in] Le nom de fichier sous lequel enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="ebbff-106">[in] The file name under which to save changes.</span></span>  
  
 `dwSaveFlags`  
 <span data-ttu-id="ebbff-107">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="ebbff-107">[in] Reserved.</span></span> <span data-ttu-id="ebbff-108">Doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ebbff-108">Must be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebbff-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ebbff-109">Requirements</span></span>  
 <span data-ttu-id="ebbff-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ebbff-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebbff-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ebbff-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ebbff-112">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ebbff-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ebbff-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ebbff-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebbff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebbff-114">See Also</span></span>  
 [<span data-ttu-id="ebbff-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="ebbff-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)  
 [<span data-ttu-id="ebbff-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="ebbff-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
