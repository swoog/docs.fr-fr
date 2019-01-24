---
title: ICorDebugValueBreakpoint Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint
helpviewer_keywords:
- ICorDebugValueBreakpoint interface [.NET Framework debugging]
ms.assetid: c02338fe-da6c-467f-9567-70ebb387e901
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58e6807b0546eadc4baacc276fa1ba7bda4e3aba
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557758"
---
# <a name="icordebugvaluebreakpoint-interface1"></a><span data-ttu-id="b8749-102">ICorDebugValueBreakpoint Interface1</span><span class="sxs-lookup"><span data-stu-id="b8749-102">ICorDebugValueBreakpoint Interface1</span></span>
<span data-ttu-id="b8749-103">Étend l’interface ICorDebugBreakpoint pour fournir l’accès à des valeurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b8749-103">Extends the ICorDebugBreakpoint interface to provide access to specific values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b8749-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8749-104">Methods</span></span>  
  
|<span data-ttu-id="b8749-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8749-105">Method</span></span>|<span data-ttu-id="b8749-106">Description</span><span class="sxs-lookup"><span data-stu-id="b8749-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b8749-107">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="b8749-107">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvaluebreakpoint-getvalue-method.md)|<span data-ttu-id="b8749-108">Obtient un pointeur d’interface vers un objet ICorDebugValue qui représente la valeur de l’objet sur lequel le point d’arrêt est défini.</span><span class="sxs-lookup"><span data-stu-id="b8749-108">Gets an interface pointer to an ICorDebugValue object that represents the value of the object upon which the breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b8749-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b8749-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b8749-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="b8749-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b8749-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b8749-111">Requirements</span></span>  
 <span data-ttu-id="b8749-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b8749-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b8749-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b8749-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b8749-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b8749-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b8749-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b8749-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8749-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8749-116">See also</span></span>
- [<span data-ttu-id="b8749-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="b8749-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
