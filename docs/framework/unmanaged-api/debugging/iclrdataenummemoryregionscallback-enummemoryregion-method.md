---
title: ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegionsCallback.EnumMemoryRegion
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion
helpviewer_keywords:
- EnumMemoryRegion method [.NET Framework debugging]
- ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion method [.NET Framework debugging]
ms.assetid: 9bb93fab-57e8-4f9a-9ef3-1794504fa896
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 85b1c5455cb2008a352461d6b506e43fcef48d17
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698237"
---
# <a name="iclrdataenummemoryregionscallbackenummemoryregion-method"></a><span data-ttu-id="c0652-102">ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="c0652-102">ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion Method</span></span>
<span data-ttu-id="c0652-103">Appelé par [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) pour signaler au débogueur le résultat d’une tentative d’énumération d’une région spécifiée de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c0652-103">Called by [ICLRDataEnumMemoryRegions::EnumMemoryRegions](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-enummemoryregions-method.md) to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c0652-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0652-104">Syntax</span></span>  
  
```  
HRESULT EnumMemoryRegion (  
    [in] CLRDATA_ADDRESS  address,  
    [in] ULONG32          size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c0652-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0652-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="c0652-106">[in] Adresse de départ de la région de mémoire qui était à énumérer.</span><span class="sxs-lookup"><span data-stu-id="c0652-106">[in] The starting address of the memory region that was to be enumerated.</span></span>  
  
 `size`  
 <span data-ttu-id="c0652-107">[in] La taille, en octets, de la région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c0652-107">[in] The size, in bytes, of the memory region.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c0652-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c0652-108">Remarks</span></span>  
 <span data-ttu-id="c0652-109">Le `ICLRDataEnumMemoryRegions::EnumMemoryRegions` méthode appellera cette méthode de rappel après chaque tentative d’énumération d’une région de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c0652-109">The `ICLRDataEnumMemoryRegions::EnumMemoryRegions` method will call this callback method after each attempt to enumerate a memory region.</span></span> <span data-ttu-id="c0652-110">L’énumération continuera même si cette méthode retourne un HRESULT indiquant un échec.</span><span class="sxs-lookup"><span data-stu-id="c0652-110">The enumeration will continue even if this method returns an HRESULT indicating failure.</span></span>  
  
 <span data-ttu-id="c0652-111">Régions signalées par ce rappel peuvent être des doublons ou des régions qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="c0652-111">Regions reported by this callback may be duplicates or overlapping regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c0652-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0652-112">Requirements</span></span>  
 <span data-ttu-id="c0652-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0652-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0652-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="c0652-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="c0652-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c0652-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c0652-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0652-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0652-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0652-117">See also</span></span>

- [<span data-ttu-id="c0652-118">ICLRDataEnumMemoryRegionsCallback, interface</span><span class="sxs-lookup"><span data-stu-id="c0652-118">ICLRDataEnumMemoryRegionsCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md)
