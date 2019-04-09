---
title: ICLRDataTarget2, interface
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2
helpviewer_keywords:
- ICLRDataTarget2 interface [.NET Framework debugging]
ms.assetid: 94249397-861b-4294-a538-cf01466a66d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d21bced214242866c47f40f392593f3f51cda02f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104713"
---
# <a name="iclrdatatarget2-interface"></a><span data-ttu-id="a8a88-102">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="a8a88-102">ICLRDataTarget2 Interface</span></span>
<span data-ttu-id="a8a88-103">Une sous-classe de [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) qui est utilisée par la couche de services d’accès aux données pour manipuler les régions de mémoire virtuelle dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="a8a88-103">A subclass of [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) that is used by the data access services layer to manipulate virtual memory regions in the target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a8a88-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8a88-104">Methods</span></span>  
  
|<span data-ttu-id="a8a88-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a8a88-105">Method</span></span>|<span data-ttu-id="a8a88-106">Description</span><span class="sxs-lookup"><span data-stu-id="a8a88-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a8a88-107">AllocVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="a8a88-107">AllocVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-allocvirtual-method.md)|<span data-ttu-id="a8a88-108">Alloue de la mémoire dans l’espace d’adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="a8a88-108">Allocates memory in the address space of the target process.</span></span>|  
|[<span data-ttu-id="a8a88-109">FreeVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="a8a88-109">FreeVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-freevirtual-method.md)|<span data-ttu-id="a8a88-110">Libère la mémoire précédemment alloué dans l’espace d’adressage du processus cible.</span><span class="sxs-lookup"><span data-stu-id="a8a88-110">Frees memory that was previously allocated in the address space of the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8a88-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a8a88-111">Remarks</span></span>  
 <span data-ttu-id="a8a88-112">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="a8a88-112">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="a8a88-113">Par exemple, un processus actif aurait une implémentation différente de celle d'un vidage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8a88-113">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="a8a88-114">La cible ne prend peut-être pas en charge la modification de ses régions de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8a88-114">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8a88-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8a88-115">Requirements</span></span>  
 <span data-ttu-id="a8a88-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8a88-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8a88-117">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="a8a88-117">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a8a88-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8a88-118">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="a8a88-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a8a88-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a8a88-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a88-120">See also</span></span>

- [<span data-ttu-id="a8a88-121">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="a8a88-121">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
- [<span data-ttu-id="a8a88-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a8a88-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
