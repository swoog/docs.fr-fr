---
title: ICorDebugProcess5, interface
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5
helpviewer_keywords:
- ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 30a39d79-1f10-4328-9c5d-094ed824e2ba
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e3aed85e989313e4778e12a6f6bb789ccef49747
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423369"
---
# <a name="icordebugprocess5-interface"></a><span data-ttu-id="08094-102">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="08094-102">ICorDebugProcess5 Interface</span></span>
<span data-ttu-id="08094-103">Étend l’interface ICorDebugProcess pour prendre en charge l’accès au tas managé, pour fournir des informations sur le garbage collection d’objets gérés, et pour déterminer si un débogueur charge des images à partir du cache d’images natives locales application.</span><span class="sxs-lookup"><span data-stu-id="08094-103">Extends the ICorDebugProcess interface to support access to the managed heap, to provide information about garbage collection of managed objects, and to determine whether a debugger loads images from the application local native image cache.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="08094-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08094-104">Methods</span></span>  
  
|<span data-ttu-id="08094-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="08094-105">Method</span></span>|<span data-ttu-id="08094-106">Description</span><span class="sxs-lookup"><span data-stu-id="08094-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="08094-107">EnableNGenPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-107">EnableNGenPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enablengenpolicy-method.md)|<span data-ttu-id="08094-108">Définit une valeur qui détermine comment une application charge les images natives lors de son exécution sous un débogueur managé.</span><span class="sxs-lookup"><span data-stu-id="08094-108">Sets a value that determines how an application loads native images while running under a managed debugger.</span></span>|  
|[<span data-ttu-id="08094-109">EnumerateGCReferences, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-109">EnumerateGCReferences Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md)|<span data-ttu-id="08094-110">Obtient un énumérateur pour tous les objets qui doivent être par le garbage collector dans un processus.</span><span class="sxs-lookup"><span data-stu-id="08094-110">Gets an enumerator for all objects that are to be garbage-collected in a process.</span></span>|  
|[<span data-ttu-id="08094-111">EnumerateHandles, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-111">EnumerateHandles Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumeratehandles-method.md)|<span data-ttu-id="08094-112">Obtient un énumérateur pour les handles d’objet dans un processus.</span><span class="sxs-lookup"><span data-stu-id="08094-112">Gets an enumerator for object handles in a process.</span></span>|  
|[<span data-ttu-id="08094-113">EnumerateHeap, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-113">EnumerateHeap Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheap-method.md)|<span data-ttu-id="08094-114">Obtient un énumérateur pour les objets sur le tas managé.</span><span class="sxs-lookup"><span data-stu-id="08094-114">Gets an enumerator for objects on the managed heap.</span></span>|  
|[<span data-ttu-id="08094-115">EnumerateHeapRegions, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-115">EnumerateHeapRegions Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md)|<span data-ttu-id="08094-116">Obtient un énumérateur pour les régions du tas managé.</span><span class="sxs-lookup"><span data-stu-id="08094-116">Gets an enumerator for regions of the managed heap.</span></span>|  
|[<span data-ttu-id="08094-117">GetArrayLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-117">GetArrayLayout Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getarraylayout-method.md)|<span data-ttu-id="08094-118">Obtient des informations sur la disposition d’un tableau dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="08094-118">Gets information about the layout of an array in memory.</span></span>|  
|[<span data-ttu-id="08094-119">GetGCHeapInformation, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-119">GetGCHeapInformation Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md)|<span data-ttu-id="08094-120">Obtient un pointeur vers un [COR_HEAPINFO](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md) structure qui contient des informations sur les objets qui doivent être par le garbage collector sur le tas managé.</span><span class="sxs-lookup"><span data-stu-id="08094-120">Gets a pointer to a [COR_HEAPINFO](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md) structure that contains information about objects that are to be garbage-collected on the managed heap.</span></span>|  
|[<span data-ttu-id="08094-121">GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-121">GetObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getobject-method.md)|<span data-ttu-id="08094-122">Obtient un pointeur vers un objet sur le tas managé.</span><span class="sxs-lookup"><span data-stu-id="08094-122">Gets a pointer to an object on the managed heap.</span></span>|  
|[<span data-ttu-id="08094-123">GetTypeFields, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-123">GetTypeFields Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypefields-method.md)|<span data-ttu-id="08094-124">Obtient un pointeur vers un tableau qui contient les informations pour un type en fonction de son identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="08094-124">Gets a pointer to an array that contains field information for a type based on its type identifier.</span></span>|  
|[<span data-ttu-id="08094-125">GetTypeForTypeID, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-125">GetTypeForTypeID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypefortypeid-method.md)|<span data-ttu-id="08094-126">Obtient un objet de type qui fournit des informations sur un objet basé sur les identificateurs de son type.</span><span class="sxs-lookup"><span data-stu-id="08094-126">Gets a type object that provides information about an object based on its type identifiers.</span></span>|  
|[<span data-ttu-id="08094-127">GetTypeID, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-127">GetTypeID Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypeid-method.md)|<span data-ttu-id="08094-128">Obtient l’identificateur de type pour l’objet à une adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08094-128">Gets the type identifier for the object at a specified address.</span></span>|  
|[<span data-ttu-id="08094-129">GetTypeLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="08094-129">GetTypeLayout Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-gettypelayout-method.md)|<span data-ttu-id="08094-130">Obtient des informations sur la disposition d’un objet dans la mémoire en fonction de son identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="08094-130">Gets information about the layout of an object in memory based on its type identifier.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="08094-131">Notes</span><span class="sxs-lookup"><span data-stu-id="08094-131">Remarks</span></span>  
 <span data-ttu-id="08094-132">Cette interface étend logiquement l’ICorDebugProcess, ICorDebugProcess2, et [ICorDebugProcess3](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-interface.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="08094-132">This interface logically extends the ICorDebugProcess, ICorDebugProcess2, and [ICorDebugProcess3](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess3-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="08094-133">Cette interface ne prend pas en charge l’appel à distance, à partir d’un autre ordinateur ou à partir d’un autre processus.</span><span class="sxs-lookup"><span data-stu-id="08094-133">This interface does not support being called remotely, either from another machine or from another process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08094-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="08094-134">Requirements</span></span>  
 <span data-ttu-id="08094-135">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="08094-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08094-136">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="08094-136">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="08094-137">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="08094-137">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="08094-138">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08094-138">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08094-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08094-139">See Also</span></span>  
 [<span data-ttu-id="08094-140">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="08094-140">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="08094-141">Débogage</span><span class="sxs-lookup"><span data-stu-id="08094-141">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
