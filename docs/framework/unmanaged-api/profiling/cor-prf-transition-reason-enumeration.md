---
title: COR_PRF_TRANSITION_REASON, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_TRANSITION_REASON
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_TRANSITION_REASON
helpviewer_keywords:
- COR_PRF_TRANSITION_REASON enumeration [.NET Framework profiling]
ms.assetid: da941118-01b7-4197-ae5b-9f2f8adcd623
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2556196b7c8f81709e6880962e8ff36e126dd8b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450061"
---
# <a name="corprftransitionreason-enumeration"></a><span data-ttu-id="bdd26-102">COR_PRF_TRANSITION_REASON, énumération</span><span class="sxs-lookup"><span data-stu-id="bdd26-102">COR_PRF_TRANSITION_REASON Enumeration</span></span>
<span data-ttu-id="bdd26-103">Indique la raison d'une transition de code managé en code non managé, ou l'inverse.</span><span class="sxs-lookup"><span data-stu-id="bdd26-103">Indicates the reason for a transition from managed to unmanaged code, or vice versa.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdd26-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdd26-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_TRANSITION_CALL,  
    COR_PRF_TRANSITION_RETURN  
} COR_PRF_TRANSITION_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="bdd26-105">Membres</span><span class="sxs-lookup"><span data-stu-id="bdd26-105">Members</span></span>  
  
|<span data-ttu-id="bdd26-106">Membre</span><span class="sxs-lookup"><span data-stu-id="bdd26-106">Member</span></span>|<span data-ttu-id="bdd26-107">Description</span><span class="sxs-lookup"><span data-stu-id="bdd26-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_TRANSITION_CALL`|<span data-ttu-id="bdd26-108">La transition est en raison d’un appel dans une fonction.</span><span class="sxs-lookup"><span data-stu-id="bdd26-108">The transition is due to a call into a function.</span></span>|  
|`COR_PRF_TRANSITION_RETURN`|<span data-ttu-id="bdd26-109">La transition est dû à un retour d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="bdd26-109">The transition is due to a return from a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bdd26-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bdd26-110">Remarks</span></span>  
 <span data-ttu-id="bdd26-111">Lorsqu’une transition se produit, le profileur reçoit un [ICorProfilerCallback::ManagedToUnmanagedTransition](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-managedtounmanagedtransition-method.md) ou [ICorProfilerCallback::UnmanagedToManagedTransition](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-unmanagedtomanagedtransition-method.md) rappel, qui Fournit une valeur de la `COR_PRF_TRANSITION_REASON` énumération pour indiquer la raison de la transition.</span><span class="sxs-lookup"><span data-stu-id="bdd26-111">When a transition occurs, the profiler receives an [ICorProfilerCallback::ManagedToUnmanagedTransition](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-managedtounmanagedtransition-method.md) or [ICorProfilerCallback::UnmanagedToManagedTransition](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-unmanagedtomanagedtransition-method.md) callback, either of which provides a value of the `COR_PRF_TRANSITION_REASON` enumeration to indicate the reason for the transition.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdd26-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bdd26-112">Requirements</span></span>  
 <span data-ttu-id="bdd26-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bdd26-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdd26-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="bdd26-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="bdd26-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bdd26-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bdd26-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdd26-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
