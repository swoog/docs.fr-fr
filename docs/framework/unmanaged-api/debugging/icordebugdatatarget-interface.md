---
title: ICorDebugDataTarget, interface
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget
helpviewer_keywords:
- ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: df5f05be-bed7-4f3c-bc89-dbb435d79a0b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 480fc27bd41f7ca559ceee379b7f6f81c94da0ba
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59188706"
---
# <a name="icordebugdatatarget-interface"></a><span data-ttu-id="7c977-102">ICorDebugDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="7c977-102">ICorDebugDataTarget Interface</span></span>
<span data-ttu-id="7c977-103">Fournit une interface de rappel qui permet d'accéder à un processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="7c977-103">Provides a callback interface that provides access to a particular target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7c977-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7c977-104">Methods</span></span>  
  
|<span data-ttu-id="7c977-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c977-105">Method</span></span>|<span data-ttu-id="7c977-106">Description</span><span class="sxs-lookup"><span data-stu-id="7c977-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7c977-107">GetPlatform, méthode</span><span class="sxs-lookup"><span data-stu-id="7c977-107">GetPlatform Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md)|<span data-ttu-id="7c977-108">Fournit des informations sur la plateforme, notamment l’architecture de processeur et de système d’exploitation, sur lequel s’exécute le processus cible.</span><span class="sxs-lookup"><span data-stu-id="7c977-108">Provides information about the platform, including processor architecture and operating system, on which the target process is running.</span></span>|  
|[<span data-ttu-id="7c977-109">ReadVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="7c977-109">ReadVirtual Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-readvirtual-method.md)|<span data-ttu-id="7c977-110">Obtient un bloc de mémoire contiguë en commençant à l’adresse spécifiée et le retourne dans la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="7c977-110">Gets a block of contiguous memory starting at the specified address, and returns it in the supplied buffer.</span></span>|  
|[<span data-ttu-id="7c977-111">GetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="7c977-111">GetThreadContext Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getthreadcontext-method.md)|<span data-ttu-id="7c977-112">Demande le contexte actuel du thread pour le thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="7c977-112">Requests the current thread context for the specified thread.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7c977-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7c977-113">Remarks</span></span>  
 `ICorDebugDataTarget` <span data-ttu-id="7c977-114">et ses méthodes ont les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7c977-114">and its methods have the following characteristics:</span></span>  
  
-   <span data-ttu-id="7c977-115">Les services de débogage appellent des méthodes sur cette interface pour accéder à la mémoire et autres données dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="7c977-115">The debugging services call methods on this interface to access memory and other data in the target process.</span></span>  
  
-   <span data-ttu-id="7c977-116">Le client de débogueur doit implémenter cette interface comme il convient pour la cible particulière (par exemple, un processus en cours ou une image mémoire).</span><span class="sxs-lookup"><span data-stu-id="7c977-116">The debugger client must implement this interface as appropriate for the particular target (for example, a live process or a memory dump).</span></span>  
  
-   <span data-ttu-id="7c977-117">Le `ICorDebugDataTarget` méthodes peuvent être appelées qu’à partir de méthodes implémentées dans d’autres `ICorDebug*` interfaces.</span><span class="sxs-lookup"><span data-stu-id="7c977-117">The `ICorDebugDataTarget` methods can be invoked only from within methods implemented in other `ICorDebug*` interfaces.</span></span> <span data-ttu-id="7c977-118">Cela garantit que le client de débogueur a contrôler sur quel thread, il est appelé et à quel moment.</span><span class="sxs-lookup"><span data-stu-id="7c977-118">This ensures that the debugger client has control over which thread it is invoked on, and when.</span></span>  
  
-   <span data-ttu-id="7c977-119">Le `ICorDebugDataTarget` implémentation doit toujours retourner des informations récentes sur la cible.</span><span class="sxs-lookup"><span data-stu-id="7c977-119">The `ICorDebugDataTarget` implementation must always return up-to-date information about the target.</span></span>  
  
 <span data-ttu-id="7c977-120">Le processus cible doit être arrêté et pas changé pendant que `ICorDebug*` interfaces (et par conséquent `ICorDebugDataTarget` méthodes) sont appelées.</span><span class="sxs-lookup"><span data-stu-id="7c977-120">The target process should be stopped and not changed in any way while `ICorDebug*` interfaces (and therefore `ICorDebugDataTarget` methods) are being called.</span></span> <span data-ttu-id="7c977-121">Si la cible est un processus en cours et les modifications de son état, le [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) méthode doit être de nouveau appelée pour fournir une instance de ICorDebugProcess de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7c977-121">If the target is a live process and its state changes, the [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) method has to be called again to provide a replacement ICorDebugProcess instance.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7c977-122">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="7c977-122">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7c977-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c977-123">Requirements</span></span>  
 <span data-ttu-id="7c977-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7c977-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7c977-125">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7c977-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7c977-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7c977-126">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="7c977-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7c977-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7c977-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c977-128">See also</span></span>

- [<span data-ttu-id="7c977-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7c977-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="7c977-130">Débogage</span><span class="sxs-lookup"><span data-stu-id="7c977-130">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
