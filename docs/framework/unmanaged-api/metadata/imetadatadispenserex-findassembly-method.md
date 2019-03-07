---
title: IMetaDataDispenserEx::FindAssembly, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssembly
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssembly
helpviewer_keywords:
- FindAssembly method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssembly method [.NET Framework metadata]
ms.assetid: 3afe7252-5f28-48d9-a74d-1927566c404c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a3fc0d59bfb8a5b5c41955b52ae3f2ea99fbc46e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502434"
---
# <a name="imetadatadispenserexfindassembly-method"></a><span data-ttu-id="5bb4d-102">IMetaDataDispenserEx::FindAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="5bb4d-102">IMetaDataDispenserEx::FindAssembly Method</span></span>
<span data-ttu-id="5bb4d-103">Cette méthode n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-103">This method is not implemented.</span></span> <span data-ttu-id="5bb4d-104">Si elle est appelée, elle retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bb4d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bb4d-105">Syntax</span></span>  
  
```  
HRESULT FindAssembly(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5bb4d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bb4d-106">Parameters</span></span>  
 `szAppBase`  
 <span data-ttu-id="5bb4d-107">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-107">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="5bb4d-108">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-108">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="5bb4d-109">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-109">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="5bb4d-110">[in] L’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-110">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="5bb4d-111">[out] Le nom simple de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-111">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="5bb4d-112">[in] La taille, en octets, de `szName`.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-112">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="5bb4d-113">[out] Le nombre de caractères réellement retournés dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="5bb4d-113">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bb4d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5bb4d-114">Requirements</span></span>  
 <span data-ttu-id="5bb4d-115">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5bb4d-115">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bb4d-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5bb4d-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5bb4d-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5bb4d-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5bb4d-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bb4d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bb4d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bb4d-119">See also</span></span>
- [<span data-ttu-id="5bb4d-120">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="5bb4d-120">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="5bb4d-121">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="5bb4d-121">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
