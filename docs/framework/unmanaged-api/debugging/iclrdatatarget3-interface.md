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
ms.openlocfilehash: 54d6535e2b2c4761eb3c67a990c62f2c311cf133
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406862"
---
# <a name="iclrdatatarget3-interface"></a><span data-ttu-id="46ef9-102">ICLRDataTarget3, interface</span><span class="sxs-lookup"><span data-stu-id="46ef9-102">ICLRDataTarget3 Interface</span></span>
<span data-ttu-id="46ef9-103">Une sous-classe de [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) qui fournit l’accès aux informations sur l’exception.</span><span class="sxs-lookup"><span data-stu-id="46ef9-103">A subclass of [ICLRDataTarget2](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md) that provides access to exception information.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46ef9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46ef9-104">Methods</span></span>  
  
|<span data-ttu-id="46ef9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="46ef9-105">Method</span></span>|<span data-ttu-id="46ef9-106">Description</span><span class="sxs-lookup"><span data-stu-id="46ef9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46ef9-107">GetExceptionRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="46ef9-107">GetExceptionRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionrecord-method.md)|<span data-ttu-id="46ef9-108">Appelé par les services d'accès aux données du Common Langage Runtime (CLR) pour récupérer l'enregistrement d'exception associé au processus cible.</span><span class="sxs-lookup"><span data-stu-id="46ef9-108">Called by the common language runtime (CLR) data access services to retrieve the exception record associated with the target process.</span></span>|  
|[<span data-ttu-id="46ef9-109">GetExceptionContextRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="46ef9-109">GetExceptionContextRecord Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptioncontextrecord-method.md)|<span data-ttu-id="46ef9-110">Appelé par les services d'accès aux données CLR pour récupérer l'enregistrement de contexte associé au processus cible.</span><span class="sxs-lookup"><span data-stu-id="46ef9-110">Called by the CLR data access services to retrieve the context record associated with the target process.</span></span>|  
|[<span data-ttu-id="46ef9-111">GetExceptionThreadID, méthode</span><span class="sxs-lookup"><span data-stu-id="46ef9-111">GetExceptionThreadID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget3-getexceptionthreadid-method.md)|<span data-ttu-id="46ef9-112">Appelée par les services d'accès aux données de CLR (Common Language Runtime) pour obtenir l'ID du thread qui a levé l'exception.</span><span class="sxs-lookup"><span data-stu-id="46ef9-112">Called by the CLR data access services to get the ID of the thread that threw the exception.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46ef9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="46ef9-113">Remarks</span></span>  
 <span data-ttu-id="46ef9-114">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="46ef9-114">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="46ef9-115">Par exemple, un processus actif aurait une implémentation différente de celle d'un vidage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="46ef9-115">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="46ef9-116">La cible ne prend peut-être pas en charge la modification de ses régions de mémoire.</span><span class="sxs-lookup"><span data-stu-id="46ef9-116">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46ef9-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46ef9-117">Requirements</span></span>  
 <span data-ttu-id="46ef9-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46ef9-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46ef9-119">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="46ef9-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="46ef9-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46ef9-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46ef9-121">**Versions du .NET framework :** [!INCLUDE[v451_update](../../../../includes/v451-update-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46ef9-121">**.NET Framework Versions:** [!INCLUDE[v451_update](../../../../includes/v451-update-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46ef9-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ef9-122">See Also</span></span>  
 [<span data-ttu-id="46ef9-123">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="46ef9-123">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)  
 [<span data-ttu-id="46ef9-124">ICLRDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="46ef9-124">ICLRDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-interface.md)  
 [<span data-ttu-id="46ef9-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="46ef9-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
