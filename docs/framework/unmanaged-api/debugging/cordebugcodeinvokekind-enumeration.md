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
ms.openlocfilehash: b3b4906f988d09f7b01aee40e8f63b589da5f33d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59086414"
---
# <a name="cordebugcodeinvokekind-enumeration"></a><span data-ttu-id="aa179-102">CorDebugCodeInvokeKind, énumération</span><span class="sxs-lookup"><span data-stu-id="aa179-102">CorDebugCodeInvokeKind Enumeration</span></span>
<span data-ttu-id="aa179-103">Indique de quelle manière une fonction exportée appelle du code managé.</span><span class="sxs-lookup"><span data-stu-id="aa179-103">Describes how an exported function invokes managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa179-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa179-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCodeInvokeKind  
{  
    CODE_INVOKE_KIND_NONE,       
    CODE_INVOKE_KIND_RETURN,     
    CODE_INVOKE_KIND_TAILCALL,   
} CorDebugCodeInvokeKind;  
```  
  
## <a name="members"></a><span data-ttu-id="aa179-105">Membres</span><span class="sxs-lookup"><span data-stu-id="aa179-105">Members</span></span>  
  
|<span data-ttu-id="aa179-106">Membre</span><span class="sxs-lookup"><span data-stu-id="aa179-106">Member</span></span>|<span data-ttu-id="aa179-107">Description</span><span class="sxs-lookup"><span data-stu-id="aa179-107">Description</span></span>|  
|------------|-----------------|  
|`CODE_INVOKE_KIND_NONE`|<span data-ttu-id="aa179-108">Si du code managé est appelé par cette méthode, il devra ensuite être localisé par des événements ou des points d'arrêt explicites.</span><span class="sxs-lookup"><span data-stu-id="aa179-108">If any managed code is invoked by this method, it will have to be located by explicit events or breakpoints later.</span></span><br /><br /> <span data-ttu-id="aa179-109">– ou –</span><span class="sxs-lookup"><span data-stu-id="aa179-109">--or--</span></span><br /><br /> <span data-ttu-id="aa179-110">Une partie du code managé appelé par cette méthode risque d'être oubliée, car il n'existe pas de moyen simple d'arrêter son exécution.</span><span class="sxs-lookup"><span data-stu-id="aa179-110">We may just miss some of the managed code this method calls because there is no easy way to stop on it.</span></span><br /><br /> <span data-ttu-id="aa179-111">– ou –</span><span class="sxs-lookup"><span data-stu-id="aa179-111">--or--</span></span><br /><br /> <span data-ttu-id="aa179-112">La méthode risque de ne jamais appeler le code managé.</span><span class="sxs-lookup"><span data-stu-id="aa179-112">The method may never invoke managed code.</span></span>|  
|`CODE_INVOKE_KIND_RETURN`|<span data-ttu-id="aa179-113">Cette méthode appelle le code managé via une instruction de retour.</span><span class="sxs-lookup"><span data-stu-id="aa179-113">This method will invoke managed code via a return instruction.</span></span> <span data-ttu-id="aa179-114">Le pas à pas sortant doit normalement se produire dans le code managé suivant.</span><span class="sxs-lookup"><span data-stu-id="aa179-114">Stepping out should arrive at the next managed code.</span></span>|  
|`CODE_INVOKE_KIND_TAILCALL`|<span data-ttu-id="aa179-115">Cette méthode appelle le code managé via un appel tail.</span><span class="sxs-lookup"><span data-stu-id="aa179-115">This method will invoke managed code via a tail-call.</span></span> <span data-ttu-id="aa179-116">Le pas à pas détaillé et le pas à pas principal sur des instructions d'appel doivent normalement se produire dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="aa179-116">Single-stepping and stepping over any call instructions should arrive at managed code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="aa179-117">Notes</span><span class="sxs-lookup"><span data-stu-id="aa179-117">Remarks</span></span>  
 <span data-ttu-id="aa179-118">Cette énumération est utilisée par le [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) méthode pour fournir des informations sur l’exécution pas à pas du code managé.</span><span class="sxs-lookup"><span data-stu-id="aa179-118">This enumeration is used by the [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) method to provide information about stepping through managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aa179-119">Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.</span><span class="sxs-lookup"><span data-stu-id="aa179-119">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa179-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa179-120">Requirements</span></span>  
 <span data-ttu-id="aa179-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aa179-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aa179-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aa179-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aa179-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aa179-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aa179-124">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aa179-124">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa179-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa179-125">See also</span></span>

- [<span data-ttu-id="aa179-126">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="aa179-126">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="aa179-127">Débogage</span><span class="sxs-lookup"><span data-stu-id="aa179-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
