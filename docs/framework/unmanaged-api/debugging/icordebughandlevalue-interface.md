---
title: ICorDebugHandleValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue
helpviewer_keywords:
- ICorDebugHandleValue interface [.NET Framework debugging]
ms.assetid: 66fcd2b8-ac66-414b-83a8-75a925e17772
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a9eb63e681b47f058901b0ff002015baffe6048
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59117441"
---
# <a name="icordebughandlevalue-interface"></a><span data-ttu-id="7389a-102">ICorDebugHandleValue, interface</span><span class="sxs-lookup"><span data-stu-id="7389a-102">ICorDebugHandleValue Interface</span></span>

<span data-ttu-id="7389a-103">Sous-classe de ICorDebugReferenceValue qui représente une valeur de référence auquel le débogueur a créé un handle pour le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="7389a-103">A subclass of ICorDebugReferenceValue that represents a reference value to which the debugger has created a handle for garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7389a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7389a-104">Methods</span></span>  
  
|<span data-ttu-id="7389a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7389a-105">Method</span></span>|<span data-ttu-id="7389a-106">Description</span><span class="sxs-lookup"><span data-stu-id="7389a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7389a-107">Dispose, méthode</span><span class="sxs-lookup"><span data-stu-id="7389a-107">Dispose Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebughandlevalue-dispose-method.md)|<span data-ttu-id="7389a-108">Libère le handle référencé par ce `ICorDebugHandleValue` objet sans libérer explicitement le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="7389a-108">Releases the handle referenced by this `ICorDebugHandleValue` object without explicitly releasing the interface pointer.</span></span>|  
|[<span data-ttu-id="7389a-109">GetHandleType, méthode</span><span class="sxs-lookup"><span data-stu-id="7389a-109">GetHandleType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebughandlevalue-gethandletype-method.md)|<span data-ttu-id="7389a-110">Obtient une valeur CorDebugHandleType qui décrit le type de handle référencé par cet `ICorDebugHandleValue`.</span><span class="sxs-lookup"><span data-stu-id="7389a-110">Gets a CorDebugHandleType value that describes the kind of handle referenced by this `ICorDebugHandleValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7389a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7389a-111">Remarks</span></span>  
 <span data-ttu-id="7389a-112">Un `ICorDebugReferenceValue` objet est invalidé par un arrêt dans l’exécution du code débogué.</span><span class="sxs-lookup"><span data-stu-id="7389a-112">An `ICorDebugReferenceValue` object is invalidated by a break in the execution of debugged code.</span></span> <span data-ttu-id="7389a-113">Un `ICorDebugHandleValue` conserve sa référence via les arrêts et reprises, jusqu'à ce qu’il est explicitement libéré.</span><span class="sxs-lookup"><span data-stu-id="7389a-113">An `ICorDebugHandleValue` maintains its reference through breaks and continuations, until it is explicitly released.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7389a-114">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="7389a-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7389a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7389a-115">Requirements</span></span>  
 <span data-ttu-id="7389a-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7389a-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7389a-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7389a-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7389a-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7389a-118">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="7389a-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7389a-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7389a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7389a-120">See also</span></span>

- [<span data-ttu-id="7389a-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7389a-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
