---
title: ICorDebugClass2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugClass2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2
helpviewer_keywords:
- ICorDebugClass2 interface [.NET Framework debugging]
ms.assetid: 5416de70-43f2-4cdf-a11f-d570759c9c0c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 015085cff23028814937dfef9aea19af7438b4f5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173808"
---
# <a name="icordebugclass2-interface"></a><span data-ttu-id="4ca5b-102">ICorDebugClass2, interface</span><span class="sxs-lookup"><span data-stu-id="4ca5b-102">ICorDebugClass2 Interface</span></span>

<span data-ttu-id="4ca5b-103">Représente une classe générique ou une classe avec un paramètre de méthode de type <xref:System.Type>.</span><span class="sxs-lookup"><span data-stu-id="4ca5b-103">Represents a generic class or a class with a method parameter of type <xref:System.Type>.</span></span> <span data-ttu-id="4ca5b-104">Cette interface étend [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4ca5b-104">This interface extends [ICorDebugClass](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4ca5b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4ca5b-105">Methods</span></span>  
  
|<span data-ttu-id="4ca5b-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="4ca5b-106">Method</span></span>|<span data-ttu-id="4ca5b-107">Description</span><span class="sxs-lookup"><span data-stu-id="4ca5b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4ca5b-108">GetParameterizedType, méthode</span><span class="sxs-lookup"><span data-stu-id="4ca5b-108">GetParameterizedType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass2-getparameterizedtype-method.md)|<span data-ttu-id="4ca5b-109">Obtient la déclaration de type pour cette classe.</span><span class="sxs-lookup"><span data-stu-id="4ca5b-109">Gets the type declaration for this class.</span></span>|  
|[<span data-ttu-id="4ca5b-110">SetJMCStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="4ca5b-110">SetJMCStatus Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass2-setjmcstatus-method.md)|<span data-ttu-id="4ca5b-111">Pour chaque méthode de cette classe, définit une valeur qui indique si la méthode est un code défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ca5b-111">For each method of this class, sets a value that indicates whether the method is user-defined code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4ca5b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4ca5b-112">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ca5b-113">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="4ca5b-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ca5b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ca5b-114">Requirements</span></span>  
 <span data-ttu-id="4ca5b-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ca5b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ca5b-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4ca5b-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4ca5b-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4ca5b-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4ca5b-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4ca5b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ca5b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ca5b-119">See also</span></span>

- [<span data-ttu-id="4ca5b-120">ICorDebugClass (Interface)</span><span class="sxs-lookup"><span data-stu-id="4ca5b-120">ICorDebugClass Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugclass-interface.md)
- [<span data-ttu-id="4ca5b-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4ca5b-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
