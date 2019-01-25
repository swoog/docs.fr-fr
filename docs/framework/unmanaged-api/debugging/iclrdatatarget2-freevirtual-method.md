---
title: ICLRDataTarget2::FreeVirtual, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.FreeVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::FreeVirtual
helpviewer_keywords:
- ICLRDataTarget::FreeVirtual method [.NET Framework debugging]
- FreeVirtual method [.NET Framework debugging]
ms.assetid: 26fb69f8-1467-4711-bd24-cb117c63938f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 02bba59a1c4445b3e432d5e44f2bccc4b72ce1da
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711653"
---
# <a name="iclrdatatarget2freevirtual-method"></a><span data-ttu-id="1bca7-102">ICLRDataTarget2::FreeVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="1bca7-102">ICLRDataTarget2::FreeVirtual Method</span></span>
<span data-ttu-id="1bca7-103">Appelé par les services d’accès aux données du common language runtime (CLR) à la mémoire précédemment allouée dans l’espace d’adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="1bca7-103">Called by the common language runtime (CLR) data access services to free memory that was previously allocated in the address space of the target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1bca7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bca7-104">Syntax</span></span>  
  
```  
HRESULT FreeVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1bca7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bca7-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="1bca7-106">[in] Un `CLRDATA_ADDRESS` valeur qui spécifie l’adresse de départ de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="1bca7-106">[in] A `CLRDATA_ADDRESS` value that specifies the starting address of the memory to be freed.</span></span>  
  
 `size`  
 <span data-ttu-id="1bca7-107">[in] La taille, en octets, de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="1bca7-107">[in] The size, in bytes, of the memory to be freed.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="1bca7-108">[in] Indicateurs qui contrôlent la libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="1bca7-108">[in] Flags that control the freeing of memory.</span></span> <span data-ttu-id="1bca7-109">Consultez Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="1bca7-109">See the Win32 `VirtualFree` function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1bca7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1bca7-110">Remarks</span></span>  
 <span data-ttu-id="1bca7-111">Le `FreeVirtual` méthode sert de wrapper logique pour Win32 `VirtualFree` (fonction).</span><span class="sxs-lookup"><span data-stu-id="1bca7-111">The `FreeVirtual` method serves as a logical wrapper for the Win32 `VirtualFree` function.</span></span>  
  
 <span data-ttu-id="1bca7-112">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="1bca7-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1bca7-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1bca7-113">Requirements</span></span>  
 <span data-ttu-id="1bca7-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1bca7-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1bca7-115">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="1bca7-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="1bca7-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1bca7-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1bca7-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1bca7-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1bca7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bca7-118">See also</span></span>
- [<span data-ttu-id="1bca7-119">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="1bca7-119">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="1bca7-120">AllocVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="1bca7-120">AllocVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-allocvirtual-method.md)
