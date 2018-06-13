---
title: ICorDebugValue2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue2
helpviewer_keywords:
- ICorDebugValue2 interface [.NET Framework debugging]
ms.assetid: 3ff2ad2a-da5a-461b-8627-1a8eba49df9c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a2462d1de9f1b5f94f2581c1a06ca2987712fd7b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421172"
---
# <a name="icordebugvalue2-interface"></a><span data-ttu-id="de195-102">ICorDebugValue2, interface</span><span class="sxs-lookup"><span data-stu-id="de195-102">ICorDebugValue2 Interface</span></span>
<span data-ttu-id="de195-103">Étend l’interface « ICorDebugValue » pour prendre en charge des objets « ICorDebugType ».</span><span class="sxs-lookup"><span data-stu-id="de195-103">Extends the "ICorDebugValue" interface to provide support for "ICorDebugType" objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="de195-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="de195-104">Methods</span></span>  
  
|<span data-ttu-id="de195-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="de195-105">Method</span></span>|<span data-ttu-id="de195-106">Description</span><span class="sxs-lookup"><span data-stu-id="de195-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="de195-107">GetExactType, méthode</span><span class="sxs-lookup"><span data-stu-id="de195-107">GetExactType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md)|<span data-ttu-id="de195-108">Obtient un pointeur d’interface vers un `ICorDebugType` objet qui représente le <xref:System.Type> de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="de195-108">Gets an interface pointer to an `ICorDebugType` object that represents the <xref:System.Type> of this value.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="de195-109">Notes</span><span class="sxs-lookup"><span data-stu-id="de195-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="de195-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="de195-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="de195-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="de195-111">Requirements</span></span>  
 <span data-ttu-id="de195-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="de195-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="de195-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="de195-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="de195-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="de195-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="de195-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="de195-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de195-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de195-116">See Also</span></span>  
 [<span data-ttu-id="de195-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="de195-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
    
 [<span data-ttu-id="de195-118">ICorDebugValue3, interface</span><span class="sxs-lookup"><span data-stu-id="de195-118">ICorDebugValue3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
