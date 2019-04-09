---
title: ICorDebugFunction3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFunction3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: b22717b9-ead5-4eea-887e-789b52d613dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4c29d631f84ce2dd7532e32951e71d6597218ebb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59088858"
---
# <a name="icordebugfunction3-interface"></a><span data-ttu-id="85312-102">ICorDebugFunction3, interface</span><span class="sxs-lookup"><span data-stu-id="85312-102">ICorDebugFunction3 Interface</span></span>
<span data-ttu-id="85312-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="85312-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="85312-104">Étend logiquement l’interface ICorDebugFunction pour fournir l’accès au code à partir d’une demande ReJIT.</span><span class="sxs-lookup"><span data-stu-id="85312-104">Logically extends the ICorDebugFunction interface to provide access to code from a ReJIT request.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="85312-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="85312-105">Methods</span></span>  
  
|<span data-ttu-id="85312-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="85312-106">Method</span></span>|<span data-ttu-id="85312-107">Description</span><span class="sxs-lookup"><span data-stu-id="85312-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="85312-108">GetActiveReJitRequestILCode, méthode</span><span class="sxs-lookup"><span data-stu-id="85312-108">GetActiveReJitRequestILCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-getactiverejitrequestilcode-method.md)|<span data-ttu-id="85312-109">Obtient un pointeur d’interface vers un [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) qui contient le langage intermédiaire à partir d’une demande ReJIT active.</span><span class="sxs-lookup"><span data-stu-id="85312-109">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="85312-110">Notes</span><span class="sxs-lookup"><span data-stu-id="85312-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85312-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85312-111">Requirements</span></span>  
 <span data-ttu-id="85312-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="85312-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85312-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="85312-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="85312-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="85312-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="85312-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="85312-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="85312-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85312-116">See also</span></span>

- [<span data-ttu-id="85312-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="85312-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="85312-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="85312-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="85312-119">ReJIT : Guide pratique</span><span class="sxs-lookup"><span data-stu-id="85312-119">ReJIT: A How-To Guide</span></span>](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
