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
ms.openlocfilehash: a764aef9c485f7eb9d15bbb4fab667a3f254eb07
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473772"
---
# <a name="imetadataemitsetmethodprops-method"></a><span data-ttu-id="1e7ef-102">IMetaDataEmit::SetMethodProps, méthode</span><span class="sxs-lookup"><span data-stu-id="1e7ef-102">IMetaDataEmit::SetMethodProps Method</span></span>
<span data-ttu-id="1e7ef-103">Définit ou met à jour de la fonctionnalité, stockée à l’adresse virtuelle relative spécifiée, d’une méthode définie par un appel antérieur à [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="1e7ef-103">Sets or updates the feature, stored at the specified relative virtual address, of a method defined by a prior call to [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e7ef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e7ef-104">Syntax</span></span>  
  
```  
HRESULT SetMethodProps (   
    [in]  mdMethodDef md,   
    [in]  DWORD       dwMethodFlags,  
    [in]  ULONG       ulCodeRVA,   
    [in]  DWORD       dwImplFlags   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e7ef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e7ef-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="1e7ef-106">[in] Le jeton pour la méthode à modifier.</span><span class="sxs-lookup"><span data-stu-id="1e7ef-106">[in] The token for the method to be changed.</span></span>  
  
 `dwMethodFlags`  
 <span data-ttu-id="1e7ef-107">[in] Les attributs de membre.</span><span class="sxs-lookup"><span data-stu-id="1e7ef-107">[in] The member attributes.</span></span>  
  
 `ulCodeRVA`  
 <span data-ttu-id="1e7ef-108">[in] L’adresse du code.</span><span class="sxs-lookup"><span data-stu-id="1e7ef-108">[in] The address of the code.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="1e7ef-109">[in] Les indicateurs d’implémentation pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="1e7ef-109">[in] The implementation flags for the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e7ef-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e7ef-110">Requirements</span></span>  
 <span data-ttu-id="1e7ef-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1e7ef-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e7ef-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1e7ef-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1e7ef-113">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1e7ef-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1e7ef-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e7ef-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e7ef-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7ef-115">See also</span></span>
- [<span data-ttu-id="1e7ef-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="1e7ef-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="1e7ef-117">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="1e7ef-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
