---
title: ICorDebugExceptionObjectValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugExceptionObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectValue
helpviewer_keywords:
- ICorDebugExceptionObjectValue interface [.NET Framework debugging]
ms.assetid: 43416dd5-8892-4106-9f59-f9143b19ddb4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6805b7b49f76b80161aef5051fe3c284192f582
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413772"
---
# <a name="icordebugexceptionobjectvalue-interface"></a><span data-ttu-id="09b2e-102">ICorDebugExceptionObjectValue, interface</span><span class="sxs-lookup"><span data-stu-id="09b2e-102">ICorDebugExceptionObjectValue Interface</span></span>
<span data-ttu-id="09b2e-103">Étend l’interface « ICorDebugObjectValue » pour fournir des informations à partir d’un objet d’exception managée.</span><span class="sxs-lookup"><span data-stu-id="09b2e-103">Extends the "ICorDebugObjectValue" interface to provide stack trace information from a managed exception object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="09b2e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09b2e-104">Methods</span></span>  
  
|<span data-ttu-id="09b2e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="09b2e-105">Method</span></span>|<span data-ttu-id="09b2e-106">Description</span><span class="sxs-lookup"><span data-stu-id="09b2e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="09b2e-107">EnumerateExceptionCallStack, méthode</span><span class="sxs-lookup"><span data-stu-id="09b2e-107">EnumerateExceptionCallStack Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)|<span data-ttu-id="09b2e-108">Obtient un énumérateur pour la pile des appels incorporée dans un objet d’exception.</span><span class="sxs-lookup"><span data-stu-id="09b2e-108">Gets an enumerator to the call stack embedded in an exception object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="09b2e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="09b2e-109">Remarks</span></span>  
 <span data-ttu-id="09b2e-110">L’appel à `QueryInterface` réussira pour des objets managés qui dérivent de <xref:System.Exception?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="09b2e-110">The call to `QueryInterface` will succeed for managed objects that derive from <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09b2e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="09b2e-111">Requirements</span></span>  
 <span data-ttu-id="09b2e-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="09b2e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09b2e-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="09b2e-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="09b2e-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="09b2e-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="09b2e-115">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09b2e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09b2e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09b2e-116">See Also</span></span>  
 [<span data-ttu-id="09b2e-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="09b2e-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="09b2e-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="09b2e-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)  
 
