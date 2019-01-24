---
title: ICorProfilerFunctionControl, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl
helpviewer_keywords:
- ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: 4e3d3141-4662-4166-8f05-bc857c1b4216
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 37e0c9dcbd8975338e7c64dbd9c44dd54508b4d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649711"
---
# <a name="icorprofilerfunctioncontrol-interface"></a><span data-ttu-id="620b8-102">ICorProfilerFunctionControl, interface</span><span class="sxs-lookup"><span data-stu-id="620b8-102">ICorProfilerFunctionControl Interface</span></span>
<span data-ttu-id="620b8-103">Fournit des méthodes qui permettent à un profileur de code de communiquer avec le CLR (Common Language Runtime) pour contrôler comment le compilateur juste-à-temps doit générer du code lors de la recompilation d'une méthode spécifique.</span><span class="sxs-lookup"><span data-stu-id="620b8-103">Provides methods that allow a code profiler to communicate with the common language runtime (CLR) to control how the JIT compiler should generate code when recompiling a specific method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="620b8-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="620b8-104">Methods</span></span>  
  
|<span data-ttu-id="620b8-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="620b8-105">Method</span></span>|<span data-ttu-id="620b8-106">Description</span><span class="sxs-lookup"><span data-stu-id="620b8-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="620b8-107">SetCodegenFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="620b8-107">SetCodegenFlags Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md)|<span data-ttu-id="620b8-108">Définit un ou plusieurs indicateurs à partir de la [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) fonction recompilée de l’énumération à la génération de code de contrôle pour un juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="620b8-108">Sets one or more flags from the [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) enumeration to control code generation for a just-in-time (JIT) recompiled function.</span></span>|  
|[<span data-ttu-id="620b8-109">SetILFunctionBody, méthode</span><span class="sxs-lookup"><span data-stu-id="620b8-109">SetILFunctionBody Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilfunctionbody-method.md)|<span data-ttu-id="620b8-110">Remplace le corps Common Intermediate Language (CIL) de la méthode.</span><span class="sxs-lookup"><span data-stu-id="620b8-110">Replaces the Common Intermediate Language (CIL) body of the method.</span></span>|  
|[<span data-ttu-id="620b8-111">SetILInstrumentedCodeMap, méthode</span><span class="sxs-lookup"><span data-stu-id="620b8-111">SetILInstrumentedCodeMap Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilinstrumentedcodemap-method.md)|<span data-ttu-id="620b8-112">Définit une carte de code pour la fonction spécifiée à l’aide des entrées de mappage CIL (Common Intermediate Language) spécifiées.</span><span class="sxs-lookup"><span data-stu-id="620b8-112">Sets a code map for the specified function by using the specified Common Intermediate Language (CIL) map entries.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="620b8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="620b8-113">Remarks</span></span>  
 <span data-ttu-id="620b8-114">L'interface `ICorProfilerFunctionControl` fournit des méthodes pour le contrôle de la génération de code pour une seule fonction recompilée.</span><span class="sxs-lookup"><span data-stu-id="620b8-114">The `ICorProfilerFunctionControl` interface provides methods for controlling code generation for a single recompiled function.</span></span> <span data-ttu-id="620b8-115">Le profileur obtient une instance de cette interface via la [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="620b8-115">The profiler obtains an instance of this interface through the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) callback.</span></span> <span data-ttu-id="620b8-116">Chaque instance de `ICorProfilerFunctionControl` contrôle toutes les instances d'une seule fonction.</span><span class="sxs-lookup"><span data-stu-id="620b8-116">Each instance of `ICorProfilerFunctionControl` controls all instances of one function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="620b8-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="620b8-117">Requirements</span></span>  
 <span data-ttu-id="620b8-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="620b8-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="620b8-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="620b8-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="620b8-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="620b8-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="620b8-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="620b8-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="620b8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="620b8-122">See also</span></span>
- [<span data-ttu-id="620b8-123">ICorProfilerInfo4, interface</span><span class="sxs-lookup"><span data-stu-id="620b8-123">ICorProfilerInfo4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [<span data-ttu-id="620b8-124">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="620b8-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="620b8-125">EnumJITedFunctions2, méthode</span><span class="sxs-lookup"><span data-stu-id="620b8-125">EnumJITedFunctions2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-enumjitedfunctions2-method.md)
