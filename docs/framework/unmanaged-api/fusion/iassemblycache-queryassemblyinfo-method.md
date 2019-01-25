---
title: IAssemblyCache::QueryAssemblyInfo, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCache.QueryAssemblyInfo
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache::QueryAssemblyInfo
helpviewer_keywords:
- IAssemblyCache::QueryAssemblyInfo method [.NET Framework fusion]
- QueryAssemblyInfo method [.NET Framework fusion]
ms.assetid: 09313cb5-06f6-43bd-94f4-1055c6b0c99a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1c3d20b1b9470c744f6dca9ef638555b9322c1c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658115"
---
# <a name="iassemblycachequeryassemblyinfo-method"></a><span data-ttu-id="a40b4-102">IAssemblyCache::QueryAssemblyInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="a40b4-102">IAssemblyCache::QueryAssemblyInfo Method</span></span>
<span data-ttu-id="a40b4-103">Obtient les données demandées sur l’assembly spécifié.</span><span class="sxs-lookup"><span data-stu-id="a40b4-103">Gets the requested data about the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a40b4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a40b4-104">Syntax</span></span>  
  
```  
HRESULT QueryAssemblyInfo (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszAssemblyName,  
    [in, out] ASSEMBLY_INFO *pAsmInfo  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a40b4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a40b4-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="a40b4-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="a40b4-106">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="a40b4-107">Les valeurs suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="a40b4-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="a40b4-108">QUERYASMINFO_FLAG_VALIDATE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a40b4-108">QUERYASMINFO_FLAG_VALIDATE (0x00000001)</span></span>  
  
-   <span data-ttu-id="a40b4-109">QUERYASMINFO_FLAG_GETSIZE (0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="a40b4-109">QUERYASMINFO_FLAG_GETSIZE (0x00000002)</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="a40b4-110">[in] Le nom de l’assembly pour lequel les données seront récupérées.</span><span class="sxs-lookup"><span data-stu-id="a40b4-110">[in] The name of the assembly for which data will be retrieved.</span></span>  
  
 `pAsmInfo`  
 <span data-ttu-id="a40b4-111">[in, out] Un [ASSEMBLY_INFO](../../../../docs/framework/unmanaged-api/fusion/assembly-info-structure.md) structure qui contient les données relatives à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a40b4-111">[in, out] An [ASSEMBLY_INFO](../../../../docs/framework/unmanaged-api/fusion/assembly-info-structure.md) structure that contains data about the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a40b4-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a40b4-112">Requirements</span></span>  
 <span data-ttu-id="a40b4-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a40b4-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a40b4-114">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="a40b4-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a40b4-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a40b4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a40b4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a40b4-116">See also</span></span>
- [<span data-ttu-id="a40b4-117">IAssemblyCache, interface</span><span class="sxs-lookup"><span data-stu-id="a40b4-117">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
