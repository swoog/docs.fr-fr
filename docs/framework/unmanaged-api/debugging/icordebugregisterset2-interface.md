---
title: ICorDebugRegisterSet2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet2
helpviewer_keywords:
- ICorDebugRegisterSet2 interface [.NET Framework debugging]
ms.assetid: d7fbccbf-3b6b-4db8-a96d-768e1cb6b1a6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 30cecaa1832ba9d45782b164ee65a2f39f28a8f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605404"
---
# <a name="icordebugregisterset2-interface"></a><span data-ttu-id="ba1d1-102">ICorDebugRegisterSet2, interface</span><span class="sxs-lookup"><span data-stu-id="ba1d1-102">ICorDebugRegisterSet2 Interface</span></span>
<span data-ttu-id="ba1d1-103">Étend les fonctionnalités de la [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) interface pour les plateformes matérielles qui possèdent plus de 64 registres.</span><span class="sxs-lookup"><span data-stu-id="ba1d1-103">Extends the capabilities of the [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) interface for hardware platforms that have more than 64 registers.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ba1d1-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba1d1-104">Methods</span></span>  
  
|<span data-ttu-id="ba1d1-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ba1d1-105">Method</span></span>|<span data-ttu-id="ba1d1-106">Description</span><span class="sxs-lookup"><span data-stu-id="ba1d1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ba1d1-107">GetRegisters, méthode</span><span class="sxs-lookup"><span data-stu-id="ba1d1-107">GetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-getregisters-method.md)|<span data-ttu-id="ba1d1-108">Obtient la valeur de chaque registre (sur l’ordinateur qui exécute actuellement le code) qui est spécifié par le masque de bits.</span><span class="sxs-lookup"><span data-stu-id="ba1d1-108">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>|  
|[<span data-ttu-id="ba1d1-109">GetRegistersAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="ba1d1-109">GetRegistersAvailable Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-getregistersavailable-method.md)|<span data-ttu-id="ba1d1-110">Obtient un tableau d’octets qui fournit une image bitmap des registres disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba1d1-110">Gets an array of bytes that provides a bitmap of the available registers.</span></span>|  
|[<span data-ttu-id="ba1d1-111">SetRegisters, méthode</span><span class="sxs-lookup"><span data-stu-id="ba1d1-111">SetRegisters Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-setregisters-method.md)|<span data-ttu-id="ba1d1-112">Pas implémentées dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ba1d1-112">Not implemented in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ba1d1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ba1d1-113">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ba1d1-114">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="ba1d1-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ba1d1-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ba1d1-115">Requirements</span></span>  
 <span data-ttu-id="ba1d1-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ba1d1-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ba1d1-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ba1d1-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ba1d1-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ba1d1-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ba1d1-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ba1d1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba1d1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba1d1-120">See also</span></span>
- [<span data-ttu-id="ba1d1-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ba1d1-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="ba1d1-122">ICorDebugRegisterSet, interface</span><span class="sxs-lookup"><span data-stu-id="ba1d1-122">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
