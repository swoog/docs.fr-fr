---
title: ICLRDataTarget3, interface
ms.date: 03/30/2017
api_name:
- ICLRDataTarget3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d2711bdf-64b3-404c-a0c3-01ba4907f703
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: df113a2839b0f2651e15f4029d86cc5efc171c63
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59111811"
---
# <a name="iclrdatatarget3-interface"></a><span data-ttu-id="8d97f-102">ICLRDataTarget3, interface</span><span class="sxs-lookup"><span data-stu-id="8d97f-102">ICLRDataTarget3 Interface</span></span>
<span data-ttu-id="8d97f-103">Une sous-classe de [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) qui fournit l’accès aux informations sur les exceptions.</span><span class="sxs-lookup"><span data-stu-id="8d97f-103">A subclass of [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) that provides access to exception information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8d97f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d97f-104">Methods</span></span>  
  
|<span data-ttu-id="8d97f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d97f-105">Method</span></span>|<span data-ttu-id="8d97f-106">Description</span><span class="sxs-lookup"><span data-stu-id="8d97f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8d97f-107">GetExceptionRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="8d97f-107">GetExceptionRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)|<span data-ttu-id="8d97f-108">Appelé par les services d'accès aux données du Common Langage Runtime (CLR) pour récupérer l'enregistrement d'exception associé au processus cible.</span><span class="sxs-lookup"><span data-stu-id="8d97f-108">Called by the common language runtime (CLR) data access services to retrieve the exception record associated with the target process.</span></span>|  
|[<span data-ttu-id="8d97f-109">GetExceptionContextRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="8d97f-109">GetExceptionContextRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)|<span data-ttu-id="8d97f-110">Appelé par les services d'accès aux données CLR pour récupérer l'enregistrement de contexte associé au processus cible.</span><span class="sxs-lookup"><span data-stu-id="8d97f-110">Called by the CLR data access services to retrieve the context record associated with the target process.</span></span>|  
|[<span data-ttu-id="8d97f-111">GetExceptionThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="8d97f-111">GetExceptionThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionthreadid-method.md)|<span data-ttu-id="8d97f-112">Appelée par les services d'accès aux données de CLR (Common Language Runtime) pour obtenir l'ID du thread qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="8d97f-112">Called by the CLR data access services to get the ID of the thread that threw the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8d97f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8d97f-113">Remarks</span></span>  
 <span data-ttu-id="8d97f-114">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="8d97f-114">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="8d97f-115">Par exemple, un processus actif aurait une implémentation différente de celle d'un vidage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8d97f-115">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="8d97f-116">La cible ne prend peut-être pas en charge la modification de ses régions de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8d97f-116">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d97f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d97f-117">Requirements</span></span>  
 <span data-ttu-id="8d97f-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8d97f-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d97f-119">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="8d97f-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="8d97f-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d97f-120">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8d97f-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8d97f-121">.NET Framework Versions:</span></span>** [!INCLUDE[v451_update](../../../../includes/net-current-v451-nov-plus.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8d97f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d97f-122">See also</span></span>

- [<span data-ttu-id="8d97f-123">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="8d97f-123">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
- [<span data-ttu-id="8d97f-124">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="8d97f-124">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)
- [<span data-ttu-id="8d97f-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8d97f-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
