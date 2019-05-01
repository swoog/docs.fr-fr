---
title: IMetaDataEmit::SetMethodProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetMethodProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetMethodProps
helpviewer_keywords:
- SetMethodProps method [.NET Framework metadata]
- IMetaDataEmit::SetMethodProps method [.NET Framework metadata]
ms.assetid: e0c6ac12-22ea-43f5-b799-8cda0faf3336
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 534afdd5990435c6b4db5ef8ea27a8065b199496
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62050010"
---
# <a name="imetadataemitsetmethodprops-method"></a><span data-ttu-id="ef563-102">IMetaDataEmit::SetMethodProps, méthode</span><span class="sxs-lookup"><span data-stu-id="ef563-102">IMetaDataEmit::SetMethodProps Method</span></span>
<span data-ttu-id="ef563-103">Définit ou met à jour de la fonctionnalité, stockée à l’adresse virtuelle relative spécifiée, d’une méthode définie par un appel antérieur à [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="ef563-103">Sets or updates the feature, stored at the specified relative virtual address, of a method defined by a prior call to [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef563-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef563-104">Syntax</span></span>  
  
```  
HRESULT SetMethodProps (   
    [in]  mdMethodDef md,   
    [in]  DWORD       dwMethodFlags,  
    [in]  ULONG       ulCodeRVA,   
    [in]  DWORD       dwImplFlags   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ef563-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef563-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="ef563-106">[in] Le jeton pour la méthode à modifier.</span><span class="sxs-lookup"><span data-stu-id="ef563-106">[in] The token for the method to be changed.</span></span>  
  
 `dwMethodFlags`  
 <span data-ttu-id="ef563-107">[in] Les attributs de membre.</span><span class="sxs-lookup"><span data-stu-id="ef563-107">[in] The member attributes.</span></span>  
  
 `ulCodeRVA`  
 <span data-ttu-id="ef563-108">[in] L’adresse du code.</span><span class="sxs-lookup"><span data-stu-id="ef563-108">[in] The address of the code.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="ef563-109">[in] Les indicateurs d’implémentation pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="ef563-109">[in] The implementation flags for the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef563-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef563-110">Requirements</span></span>  
 <span data-ttu-id="ef563-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef563-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef563-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ef563-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ef563-113">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ef563-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ef563-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef563-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef563-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef563-115">See also</span></span>

- [<span data-ttu-id="ef563-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="ef563-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="ef563-117">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="ef563-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
