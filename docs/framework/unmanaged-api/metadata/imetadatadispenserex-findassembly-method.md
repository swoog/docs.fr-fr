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
ms.openlocfilehash: 0b4caf27fe45ce0a85b7e1800827a1e5cd0893ca
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445236"
---
# <a name="imetadatadispenserexfindassembly-method"></a><span data-ttu-id="b057d-102">IMetaDataDispenserEx::FindAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="b057d-102">IMetaDataDispenserEx::FindAssembly Method</span></span>
<span data-ttu-id="b057d-103">Cette méthode n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="b057d-103">This method is not implemented.</span></span> <span data-ttu-id="b057d-104">Si elle est appelée, elle retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b057d-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b057d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b057d-105">Syntax</span></span>  
  
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
  
#### <a name="parameters"></a><span data-ttu-id="b057d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b057d-106">Parameters</span></span>  
 `szAppBase`  
 <span data-ttu-id="b057d-107">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b057d-107">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="b057d-108">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b057d-108">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="b057d-109">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b057d-109">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="b057d-110">[in] L’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="b057d-110">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="b057d-111">[out] Le nom simple de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="b057d-111">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="b057d-112">[in] La taille, en octets, de `szName`.</span><span class="sxs-lookup"><span data-stu-id="b057d-112">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="b057d-113">[out] Le nombre de caractères réellement retournés dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="b057d-113">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b057d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b057d-114">Requirements</span></span>  
 <span data-ttu-id="b057d-115">**Plateforme :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b057d-115">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b057d-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b057d-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b057d-117">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b057d-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b057d-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b057d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b057d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b057d-119">See Also</span></span>  
 [<span data-ttu-id="b057d-120">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="b057d-120">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)  
 [<span data-ttu-id="b057d-121">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="b057d-121">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
