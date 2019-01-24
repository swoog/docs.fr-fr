---
title: ICLRDataTarget2::AllocVirtual, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.AllocVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::AllocVirtual
helpviewer_keywords:
- ICLRDataTarget2::AllocVirtual method [.NET Framework debugging]
- AllocVirtual method [.NET Framework debugging]
ms.assetid: e3226230-964b-47fb-9f53-d6fdbeda1e9e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d9fc894cdd12e58689fb6b010820bb24d14a9541
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543745"
---
# <a name="iclrdatatarget2allocvirtual-method"></a><span data-ttu-id="d2e06-102">ICLRDataTarget2::AllocVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="d2e06-102">ICLRDataTarget2::AllocVirtual Method</span></span>
<span data-ttu-id="d2e06-103">Appelé par les services d’accès aux données du common language runtime (CLR) d’allocation de mémoire dans l’espace d’adressage de ce processus cible.</span><span class="sxs-lookup"><span data-stu-id="d2e06-103">Called by the common language runtime (CLR) data access services to allocate memory in the address space of this target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2e06-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2e06-104">Syntax</span></span>  
  
```  
HRESULT AllocVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags,  
    [in] ULONG32 protectFlags,  
    [out] CLRDATA_ADDRESS* virt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d2e06-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2e06-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="d2e06-106">[in] Un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ demandée de la mémoire à allouer.</span><span class="sxs-lookup"><span data-stu-id="d2e06-106">[in] A `CLRDATA_ADDRESS` value that specifies the requested starting address of the memory to be allocated.</span></span>  
  
 `size`  
 <span data-ttu-id="d2e06-107">[in] La taille, en octets, de la mémoire à allouer.</span><span class="sxs-lookup"><span data-stu-id="d2e06-107">[in] The size, in bytes, of the memory to be allocated.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="d2e06-108">[in] Indicateurs qui contrôlent l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d2e06-108">[in] Flags that control the allocation of memory.</span></span> <span data-ttu-id="d2e06-109">Consultez Win32 `VirtualAlloc` (fonction).</span><span class="sxs-lookup"><span data-stu-id="d2e06-109">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `protectFlags`  
 <span data-ttu-id="d2e06-110">[in] Attributs de protection de la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="d2e06-110">[in] The protection attributes for the allocated memory.</span></span> <span data-ttu-id="d2e06-111">Consultez Win32 `VirtualAlloc` (fonction).</span><span class="sxs-lookup"><span data-stu-id="d2e06-111">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `virt`  
 <span data-ttu-id="d2e06-112">[out] Un pointeur vers un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ réelle de la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="d2e06-112">[out] A pointer to a `CLRDATA_ADDRESS` value that specifies the actual starting address of the allocated memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d2e06-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d2e06-113">Remarks</span></span>  
 <span data-ttu-id="d2e06-114">Le `AllocVirtual` méthode sert de wrapper logique pour Win32 `VirtualAlloc` (fonction).</span><span class="sxs-lookup"><span data-stu-id="d2e06-114">The `AllocVirtual` method serves as a logical wrapper for the Win32 `VirtualAlloc` function.</span></span>  
  
 <span data-ttu-id="d2e06-115">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="d2e06-115">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2e06-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d2e06-116">Requirements</span></span>  
 <span data-ttu-id="d2e06-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d2e06-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2e06-118">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="d2e06-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="d2e06-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2e06-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2e06-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2e06-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2e06-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e06-121">See also</span></span>
- [<span data-ttu-id="d2e06-122">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="d2e06-122">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="d2e06-123">FreeVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="d2e06-123">FreeVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-freevirtual-method.md)
