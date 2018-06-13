---
title: COR_PRF_CODEGEN_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_CODEGEN_FLAGS
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CODEGEN_FLAGS
helpviewer_keywords:
- COR_PRF_CODEGEN_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 3e184022-0247-4824-a23d-6b29593d8d01
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ab5612a2bb48b2cc93e0150f45107e474a4e6217
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452115"
---
# <a name="corprfcodegenflags-enumeration"></a><span data-ttu-id="b3e1a-102">COR_PRF_CODEGEN_FLAGS, énumération</span><span class="sxs-lookup"><span data-stu-id="b3e1a-102">COR_PRF_CODEGEN_FLAGS Enumeration</span></span>
<span data-ttu-id="b3e1a-103">Définit les indicateurs de génération de code qui peuvent être définies avec la [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b3e1a-103">Defines the code generation flags that can be set with the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b3e1a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3e1a-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CODEGEN_DISABLE_INLINING =          0x0001,  
    COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS = 0x0002,  
} COR_PRF_CODEGEN_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="b3e1a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b3e1a-105">Members</span></span>  
  
|<span data-ttu-id="b3e1a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b3e1a-106">Member</span></span>|<span data-ttu-id="b3e1a-107">Description</span><span class="sxs-lookup"><span data-stu-id="b3e1a-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CODEGEN_DISABLE_INLINING`|<span data-ttu-id="b3e1a-108">Aucune fonctions ne seront incorporées dans les corps de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b3e1a-108">No functions will be inlined into this function’s body.</span></span> <span data-ttu-id="b3e1a-109">Toutefois, la fonction elle-même peut être inline dans ses appelants.</span><span class="sxs-lookup"><span data-stu-id="b3e1a-109">However, the function itself may be inlined into its callers.</span></span>|  
|`COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS`|<span data-ttu-id="b3e1a-110">Toutes les optimisations seront désactivées pour le corps de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b3e1a-110">All optimizations will be disabled for this function’s body.</span></span> <span data-ttu-id="b3e1a-111">Toutefois, la fonction elle-même peut toujours être inline dans ses appelants.</span><span class="sxs-lookup"><span data-stu-id="b3e1a-111">However, the function itself may still be inlined into its callers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3e1a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b3e1a-112">Remarks</span></span>  
 <span data-ttu-id="b3e1a-113">Le `COR_PRF_CODEGEN_FLAGS` énumération est utilisée par le [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) méthode pour activer le profileur contrôler la génération de code pour la fonction recompilée juste-.</span><span class="sxs-lookup"><span data-stu-id="b3e1a-113">The `COR_PRF_CODEGEN_FLAGS` enumeration is used by the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method to enable the profiler to control the code generation for the JIT-recompiled function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3e1a-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b3e1a-114">Requirements</span></span>  
 <span data-ttu-id="b3e1a-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b3e1a-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3e1a-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b3e1a-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b3e1a-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b3e1a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b3e1a-118">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3e1a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3e1a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3e1a-119">See Also</span></span>  
 [<span data-ttu-id="b3e1a-120">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="b3e1a-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
