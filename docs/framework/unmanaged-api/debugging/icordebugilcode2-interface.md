---
title: ICorDebugILCode2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugILCode2
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: f9dc2afd-df8a-464d-bdbf-5af0a1d4bf85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3a27dbd8b5013937bb97f37113687405c988c1fe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59142660"
---
# <a name="icordebugilcode2-interface"></a><span data-ttu-id="50f14-102">ICorDebugILCode2, interface</span><span class="sxs-lookup"><span data-stu-id="50f14-102">ICorDebugILCode2 Interface</span></span>
<span data-ttu-id="50f14-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="50f14-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="50f14-104">Étend logiquement le [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) interface pour fournir des méthodes qui retournent le jeton de signature de variable locale d’une fonction, et qui correspondent le langage intermédiaire instrumenté (IL) d’un profileur aux offsets intermédiaire de la méthode d’origine décalages.</span><span class="sxs-lookup"><span data-stu-id="50f14-104">Logically extends the [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) interface to provide methods that return the token for a function's local variable signature, and that map a profiler's instrumented intermediate language (IL) offsets to original method IL offsets.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="50f14-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="50f14-105">Methods</span></span>  
  
|<span data-ttu-id="50f14-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="50f14-106">Method</span></span>|<span data-ttu-id="50f14-107">Description</span><span class="sxs-lookup"><span data-stu-id="50f14-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="50f14-108">GetInstrumentedILMap, méthode</span><span class="sxs-lookup"><span data-stu-id="50f14-108">GetInstrumentedILMap Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getinstrumentedilmap-method.md)|<span data-ttu-id="50f14-109">Retourne un mappage des décalages du langage intermédiaire instrumenté par le profileur avec les décalages du langage intermédiaire de la méthode d'origine pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="50f14-109">Returns a map from profiler instrumented IL offsets to original method IL offsets for this instance.</span></span>|  
|[<span data-ttu-id="50f14-110">GetLocalVarSigToken, méthode</span><span class="sxs-lookup"><span data-stu-id="50f14-110">GetLocalVarSigToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode2-getlocalvarsigtoken-method.md)|<span data-ttu-id="50f14-111">Obtient le jeton de métadonnées de la signature de variable locale pour la fonction représentée par cette instance.</span><span class="sxs-lookup"><span data-stu-id="50f14-111">Gets the metadata token for the local variable signature for the function that is represented by this instance.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="50f14-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f14-112">Requirements</span></span>  
 <span data-ttu-id="50f14-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50f14-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50f14-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="50f14-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="50f14-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50f14-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="50f14-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="50f14-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="50f14-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f14-117">See also</span></span>

- [<span data-ttu-id="50f14-118">ICorDebugILCode, interface</span><span class="sxs-lookup"><span data-stu-id="50f14-118">ICorDebugILCode Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)
- [<span data-ttu-id="50f14-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="50f14-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="50f14-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="50f14-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
