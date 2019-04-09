---
title: IAssemblyCache::CreateAssemblyCacheItem, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCache.CreateAssemblyCacheItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::CreateAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCache::CreateAssemblyCacheItem method [.NET Framework fusion]
- CreateAssemblyCacheItem method [.NET Framework fusion]
ms.assetid: 017a7ba5-aaaf-44e2-9cbe-ceebef259df0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 648b641cbd2ec97305674451df06ce5be6a93a49
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59183688"
---
# <a name="iassemblycachecreateassemblycacheitem-method"></a><span data-ttu-id="0380c-102">IAssemblyCache::CreateAssemblyCacheItem, méthode</span><span class="sxs-lookup"><span data-stu-id="0380c-102">IAssemblyCache::CreateAssemblyCacheItem Method</span></span>
<span data-ttu-id="0380c-103">Obtient une référence à un nouveau [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="0380c-103">Gets a reference to a new [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0380c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0380c-104">Syntax</span></span>  
  
```  
HRESULT CreateAssemblyCacheItem (  
    [in]  DWORD dwFlags,  
    [in]  PVOID pvReserved,  
    [out] IAssemblyCacheItem **ppAsmItem,  
    [in, optional] LPCWSTR pszAssemblyName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0380c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0380c-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="0380c-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="0380c-106">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="0380c-107">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="0380c-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="0380c-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0380c-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span></span>  
  
-   <span data-ttu-id="0380c-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="0380c-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="0380c-110">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="0380c-110">[in] Reserved for future extensibility.</span></span> `pvReserved` <span data-ttu-id="0380c-111">doit être une référence null.</span><span class="sxs-lookup"><span data-stu-id="0380c-111">must be a null reference.</span></span>  
  
 `ppAsmItem`  
 <span data-ttu-id="0380c-112">[out] Retourné `IAssemblyCacheItem` pointeur.</span><span class="sxs-lookup"><span data-stu-id="0380c-112">[out] The returned `IAssemblyCacheItem` pointer.</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="0380c-113">[in, optional] Rendu non canonique, séparés par des virgules `name=value` paires.</span><span class="sxs-lookup"><span data-stu-id="0380c-113">[in, optional] Uncanonicalized, comma-separated `name=value` pairs.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0380c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0380c-114">Requirements</span></span>  
 <span data-ttu-id="0380c-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0380c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0380c-116">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="0380c-116">**Header:** Fusion.h</span></span>  
  
 **<span data-ttu-id="0380c-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0380c-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0380c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0380c-118">See also</span></span>

- [<span data-ttu-id="0380c-119">IAssemblyCache, interface</span><span class="sxs-lookup"><span data-stu-id="0380c-119">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
- [<span data-ttu-id="0380c-120">IAssemblyCacheItem, interface</span><span class="sxs-lookup"><span data-stu-id="0380c-120">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
