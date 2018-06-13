---
title: CorDebugCodeInvokeKind, énumération
ms.date: 03/30/2017
api_name:
- CorDebugCodeInvokeKind
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: e795e6a2-1008-4a81-af88-d777888e942e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf777214c015f0bbc434e3123d3ec7ef7f723549
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405650"
---
# <a name="cordebugcodeinvokekind-enumeration"></a><span data-ttu-id="d033e-102">CorDebugCodeInvokeKind, énumération</span><span class="sxs-lookup"><span data-stu-id="d033e-102">CorDebugCodeInvokeKind Enumeration</span></span>
<span data-ttu-id="d033e-103">Indique de quelle manière une fonction exportée appelle du code managé.</span><span class="sxs-lookup"><span data-stu-id="d033e-103">Describes how an exported function invokes managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d033e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d033e-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCodeInvokeKind  
{  
    CODE_INVOKE_KIND_NONE,       
    CODE_INVOKE_KIND_RETURN,     
    CODE_INVOKE_KIND_TAILCALL,   
} CorDebugCodeInvokeKind;  
```  
  
## <a name="members"></a><span data-ttu-id="d033e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d033e-105">Members</span></span>  
  
|<span data-ttu-id="d033e-106">Membre</span><span class="sxs-lookup"><span data-stu-id="d033e-106">Member</span></span>|<span data-ttu-id="d033e-107">Description</span><span class="sxs-lookup"><span data-stu-id="d033e-107">Description</span></span>|  
|------------|-----------------|  
|`CODE_INVOKE_KIND_NONE`|<span data-ttu-id="d033e-108">Si du code managé est appelé par cette méthode, il devra ensuite être localisé par des événements ou des points d'arrêt explicites.</span><span class="sxs-lookup"><span data-stu-id="d033e-108">If any managed code is invoked by this method, it will have to be located by explicit events or breakpoints later.</span></span><br /><br /> <span data-ttu-id="d033e-109">– ou –</span><span class="sxs-lookup"><span data-stu-id="d033e-109">--or--</span></span><br /><br /> <span data-ttu-id="d033e-110">Une partie du code managé appelé par cette méthode risque d'être oubliée, car il n'existe pas de moyen simple d'arrêter son exécution.</span><span class="sxs-lookup"><span data-stu-id="d033e-110">We may just miss some of the managed code this method calls because there is no easy way to stop on it.</span></span><br /><br /> <span data-ttu-id="d033e-111">– ou –</span><span class="sxs-lookup"><span data-stu-id="d033e-111">--or--</span></span><br /><br /> <span data-ttu-id="d033e-112">La méthode risque de ne jamais appeler le code managé.</span><span class="sxs-lookup"><span data-stu-id="d033e-112">The method may never invoke managed code.</span></span>|  
|`CODE_INVOKE_KIND_RETURN`|<span data-ttu-id="d033e-113">Cette méthode appelle le code managé via une instruction de retour.</span><span class="sxs-lookup"><span data-stu-id="d033e-113">This method will invoke managed code via a return instruction.</span></span> <span data-ttu-id="d033e-114">Le pas à pas sortant doit normalement se produire dans le code managé suivant.</span><span class="sxs-lookup"><span data-stu-id="d033e-114">Stepping out should arrive at the next managed code.</span></span>|  
|`CODE_INVOKE_KIND_TAILCALL`|<span data-ttu-id="d033e-115">Cette méthode appelle le code managé via un appel tail.</span><span class="sxs-lookup"><span data-stu-id="d033e-115">This method will invoke managed code via a tail-call.</span></span> <span data-ttu-id="d033e-116">Le pas à pas détaillé et le pas à pas principal sur des instructions d'appel doivent normalement se produire dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="d033e-116">Single-stepping and stepping over any call instructions should arrive at managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d033e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d033e-117">Remarks</span></span>  
 <span data-ttu-id="d033e-118">Cette énumération est utilisée par le [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) méthode pour fournir des informations sur l’exécution pas à pas du code managé.</span><span class="sxs-lookup"><span data-stu-id="d033e-118">This enumeration is used by the [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) method to provide information about stepping through managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d033e-119">Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.</span><span class="sxs-lookup"><span data-stu-id="d033e-119">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d033e-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d033e-120">Requirements</span></span>  
 <span data-ttu-id="d033e-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d033e-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d033e-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d033e-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d033e-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d033e-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d033e-124">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d033e-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d033e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d033e-125">See Also</span></span>  
 [<span data-ttu-id="d033e-126">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="d033e-126">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [<span data-ttu-id="d033e-127">Débogage</span><span class="sxs-lookup"><span data-stu-id="d033e-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
