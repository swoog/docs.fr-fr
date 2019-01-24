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
ms.openlocfilehash: c1baae7d7867b0cbb227af72fcc505a5cadfa4df
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511632"
---
# <a name="icordebugexceptionobjectvalue-interface"></a><span data-ttu-id="4a070-102">ICorDebugExceptionObjectValue, interface</span><span class="sxs-lookup"><span data-stu-id="4a070-102">ICorDebugExceptionObjectValue Interface</span></span>
<span data-ttu-id="4a070-103">Étend l’interface « ICorDebugObjectValue » pour fournir des informations de trace de pile à partir d’un objet d’exception géré.</span><span class="sxs-lookup"><span data-stu-id="4a070-103">Extends the "ICorDebugObjectValue" interface to provide stack trace information from a managed exception object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4a070-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a070-104">Methods</span></span>  
  
|<span data-ttu-id="4a070-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a070-105">Method</span></span>|<span data-ttu-id="4a070-106">Description</span><span class="sxs-lookup"><span data-stu-id="4a070-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4a070-107">EnumerateExceptionCallStack, méthode</span><span class="sxs-lookup"><span data-stu-id="4a070-107">EnumerateExceptionCallStack Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)|<span data-ttu-id="4a070-108">Obtient un énumérateur pour la pile des appels incorporée dans un objet d’exception.</span><span class="sxs-lookup"><span data-stu-id="4a070-108">Gets an enumerator to the call stack embedded in an exception object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4a070-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4a070-109">Remarks</span></span>  
 <span data-ttu-id="4a070-110">L’appel à `QueryInterface` réussit pour des objets managés qui dérivent <xref:System.Exception?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="4a070-110">The call to `QueryInterface` will succeed for managed objects that derive from <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a070-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a070-111">Requirements</span></span>  
 <span data-ttu-id="4a070-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4a070-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a070-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4a070-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4a070-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a070-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a070-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a070-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a070-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a070-116">See also</span></span>
- [<span data-ttu-id="4a070-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4a070-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="4a070-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="4a070-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)

