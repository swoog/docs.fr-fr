---
title: IMetaDataDispenserEx::GetCORSystemDirectory, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetCORSystemDirectory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory
helpviewer_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory method [.NET Framework metadata]
- GetCORSystemDirectory method [.NET Framework metadata]
ms.assetid: d9e0f3b6-e106-4820-bada-5bfba34ce360
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3dbfca942d61cd5667293d11f358f06bd000fa2e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59117999"
---
# <a name="imetadatadispenserexgetcorsystemdirectory-method"></a><span data-ttu-id="afca1-102">IMetaDataDispenserEx::GetCORSystemDirectory, méthode</span><span class="sxs-lookup"><span data-stu-id="afca1-102">IMetaDataDispenserEx::GetCORSystemDirectory Method</span></span>
<span data-ttu-id="afca1-103">Obtient le répertoire qui contient le common language runtime (CLR) actuel.</span><span class="sxs-lookup"><span data-stu-id="afca1-103">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="afca1-104">Cette méthode est prise en charge uniquement pour une utilisation par les débogueurs out-of-process.</span><span class="sxs-lookup"><span data-stu-id="afca1-104">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="afca1-105">Si elle est appelée à partir d’un autre composant, elle retournera E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="afca1-105">If called from another component, it will return E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="afca1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afca1-106">Syntax</span></span>  
  
```  
HRESULT GetCORSystemDirectory (  
    [out] LPWSTR      szBuffer,   
    [in]  DWORD       cchBuffer,   
    [out] DWORD*      pchBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="afca1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="afca1-107">Parameters</span></span>  
 `szBuffer`  
 <span data-ttu-id="afca1-108">[out] La mémoire tampon pour recevoir le nom du répertoire.</span><span class="sxs-lookup"><span data-stu-id="afca1-108">[out] The buffer to receive the directory name.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="afca1-109">[in] La taille, en octets, de `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="afca1-109">[in] The size, in bytes, of `szBuffer`.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="afca1-110">[out] Le nombre d’octets réellement retournés dans `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="afca1-110">[out] The number of bytes actually returned in `szBuffer`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="afca1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afca1-111">Requirements</span></span>  
 <span data-ttu-id="afca1-112">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="afca1-112">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="afca1-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="afca1-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="afca1-114">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="afca1-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="afca1-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="afca1-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="afca1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afca1-116">See also</span></span>

- [<span data-ttu-id="afca1-117">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="afca1-117">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="afca1-118">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="afca1-118">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
