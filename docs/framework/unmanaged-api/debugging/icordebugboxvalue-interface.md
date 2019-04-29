---
title: ICorDebugBoxValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugBoxValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBoxValue
helpviewer_keywords:
- ICorDebugBoxValue interface [.NET Framework debugging]
ms.assetid: 3d3ae7e2-97d4-46de-a2c3-cb78f3490f9d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1a9a647a9c77a3c1f82ae3691e2a5e5b2f544cad
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645407"
---
# <a name="icordebugboxvalue-interface"></a><span data-ttu-id="da5d5-102">ICorDebugBoxValue, interface</span><span class="sxs-lookup"><span data-stu-id="da5d5-102">ICorDebugBoxValue Interface</span></span>

<span data-ttu-id="da5d5-103">Une sous-classe de « ICorDebugHeapValue » qui représente un objet de classe de valeur boxed.</span><span class="sxs-lookup"><span data-stu-id="da5d5-103">A subclass of "ICorDebugHeapValue" that represents a boxed value class object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="da5d5-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="da5d5-104">Methods</span></span>  
  
|<span data-ttu-id="da5d5-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="da5d5-105">Method</span></span>|<span data-ttu-id="da5d5-106">Description</span><span class="sxs-lookup"><span data-stu-id="da5d5-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="da5d5-107">GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="da5d5-107">GetObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugboxvalue-getobject-method.md)|<span data-ttu-id="da5d5-108">Obtient un pointeur d’interface vers l’instance boxed « ICorDebugObjectValue ».</span><span class="sxs-lookup"><span data-stu-id="da5d5-108">Gets an interface pointer to the boxed "ICorDebugObjectValue" instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="da5d5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="da5d5-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="da5d5-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="da5d5-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da5d5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da5d5-111">Requirements</span></span>  
 <span data-ttu-id="da5d5-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="da5d5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da5d5-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="da5d5-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="da5d5-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="da5d5-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="da5d5-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da5d5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da5d5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da5d5-116">See also</span></span>

- [<span data-ttu-id="da5d5-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="da5d5-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
