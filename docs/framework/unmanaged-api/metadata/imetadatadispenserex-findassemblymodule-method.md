---
title: IMetaDataDispenserEx::FindAssemblyModule, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssemblyModule
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssemblyModule
helpviewer_keywords:
- FindAssemblyModule method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssemblyModule method [.NET Framework metadata]
ms.assetid: d1fb65e1-7e19-4513-85b1-44f87c294d3e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ccb6331399ef3479e43bdb9dc4a72b5fd196672c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57495336"
---
# <a name="imetadatadispenserexfindassemblymodule-method"></a><span data-ttu-id="1a752-102">IMetaDataDispenserEx::FindAssemblyModule, méthode</span><span class="sxs-lookup"><span data-stu-id="1a752-102">IMetaDataDispenserEx::FindAssemblyModule Method</span></span>
<span data-ttu-id="1a752-103">Cette méthode n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="1a752-103">This method is not implemented.</span></span> <span data-ttu-id="1a752-104">Si elle est appelée, elle retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="1a752-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1a752-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a752-105">Syntax</span></span>  
  
```  
HRESULT FindAssemblyModule(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [in]  LPCWSTR  szModuleName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1a752-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a752-106">Parameters</span></span>  
 `szAppBase`  
 <span data-ttu-id="1a752-107">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a752-107">[in] Not used.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="1a752-108">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a752-108">[in] Not used.</span></span>  
  
 `szGlobalBin`  
 <span data-ttu-id="1a752-109">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a752-109">[in] Not used.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="1a752-110">[in] Le nom du module.</span><span class="sxs-lookup"><span data-stu-id="1a752-110">[in] The name of the module.</span></span>  
  
 `szModuleName`  
 <span data-ttu-id="1a752-111">[in] L’assembly à rechercher.</span><span class="sxs-lookup"><span data-stu-id="1a752-111">[in] The assembly to be found.</span></span>  
  
 `szName`  
 <span data-ttu-id="1a752-112">[out] Le nom simple de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="1a752-112">[out] The simple name of the assembly.</span></span>  
  
 `cchName`  
 <span data-ttu-id="1a752-113">[in] La taille, en octets, de `szName`.</span><span class="sxs-lookup"><span data-stu-id="1a752-113">[in] The size, in bytes, of `szName`.</span></span>  
  
 `pcName`  
 <span data-ttu-id="1a752-114">[out] Le nombre de caractères réellement retournés dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="1a752-114">[out] The number of characters actually returned in `szName`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a752-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a752-115">Requirements</span></span>  
 <span data-ttu-id="1a752-116">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a752-116">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a752-117">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1a752-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1a752-118">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1a752-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1a752-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a752-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a752-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a752-120">See also</span></span>
- [<span data-ttu-id="1a752-121">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="1a752-121">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="1a752-122">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="1a752-122">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
