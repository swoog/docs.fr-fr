---
title: IMetaDataEmit::DefineUserString, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineUserString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineUserString
helpviewer_keywords:
- DefineUserString method [.NET Framework metadata]
- IMetaDataEmit::DefineUserString method [.NET Framework metadata]
ms.assetid: 88fb7ef3-bbdf-429c-b678-c9c153456461
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 820b0c464f591ca71072d35886a910f5409f654e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57478295"
---
# <a name="imetadataemitdefineuserstring-method"></a><span data-ttu-id="deb2b-102">IMetaDataEmit::DefineUserString, méthode</span><span class="sxs-lookup"><span data-stu-id="deb2b-102">IMetaDataEmit::DefineUserString Method</span></span>
<span data-ttu-id="deb2b-103">Obtient les métadonnées jeton pour la chaîne littérale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="deb2b-103">Gets a metadata token for the specified literal string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="deb2b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deb2b-104">Syntax</span></span>  
  
```  
HRESULT DefineUserString (   
    [in]  LPCWSTR     szString,   
    [in]  ULONG       cchString,   
    [out] mdString    *pstk   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="deb2b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="deb2b-105">Parameters</span></span>  
 `szString`  
 <span data-ttu-id="deb2b-106">[in] La chaîne de l’utilisateur à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="deb2b-106">[in] The user string to store.</span></span>  
  
 `cchString`  
 <span data-ttu-id="deb2b-107">[in] Le nombre de caractères larges dans `szString`.</span><span class="sxs-lookup"><span data-stu-id="deb2b-107">[in] The count of wide characters in `szString`.</span></span>  
  
 `pstk`  
 <span data-ttu-id="deb2b-108">[out] Le jeton de chaîne assigné.</span><span class="sxs-lookup"><span data-stu-id="deb2b-108">[out] The string token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="deb2b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="deb2b-109">Requirements</span></span>  
 <span data-ttu-id="deb2b-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="deb2b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="deb2b-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="deb2b-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="deb2b-112">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="deb2b-112">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="deb2b-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="deb2b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="deb2b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deb2b-114">See also</span></span>
- [<span data-ttu-id="deb2b-115">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="deb2b-115">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="deb2b-116">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="deb2b-116">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
