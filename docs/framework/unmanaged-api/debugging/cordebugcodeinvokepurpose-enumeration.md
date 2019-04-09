---
title: CorDebugCodeInvokePurpose, énumération
ms.date: 03/30/2017
api_name:
- CorDebugInvokePurpose
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 31833a2d-a0d6-48a1-b05f-995ca307a08f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 858dfe9b15422680a261fef9e22d8c89d9d7fe45
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59155569"
---
# <a name="cordebugcodeinvokepurpose-enumeration"></a><span data-ttu-id="88f1b-102">CorDebugCodeInvokePurpose, énumération</span><span class="sxs-lookup"><span data-stu-id="88f1b-102">CorDebugCodeInvokePurpose Enumeration</span></span>
<span data-ttu-id="88f1b-103">Indique pourquoi une fonction exportée appelle du code managé.</span><span class="sxs-lookup"><span data-stu-id="88f1b-103">Describes why an exported function calls managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88f1b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88f1b-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCodeInvokePurpose  
{  
    CODE_INVOKE_PURPOSE_NONE,  
    CODE_INVOKE_PURPOSE_NATIVE_TO_MANAGED_TRANSITION,    
    CODE_INVOKE_PURPOSE_CLASS_INIT,  
    CODE_INVOKE_PURPOSE_INTERFACE_DISPATCH,  
} CorDebugCodeInvokePurpose;  
```  
  
## <a name="members"></a><span data-ttu-id="88f1b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="88f1b-105">Members</span></span>  
  
|<span data-ttu-id="88f1b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="88f1b-106">Member</span></span>|<span data-ttu-id="88f1b-107">Description</span><span class="sxs-lookup"><span data-stu-id="88f1b-107">Description</span></span>|  
|------------|-----------------|  
|`CODE_INVOKE_PURPOSE_NONE`|<span data-ttu-id="88f1b-108">Aucun ou inconnu.</span><span class="sxs-lookup"><span data-stu-id="88f1b-108">None or unknown.</span></span>|  
|`CODE_INVOKE_PURPOSE_NATIVE_TO_MANAGED_TRANSITION`|<span data-ttu-id="88f1b-109">Le code managé exécute n'importe quel point d'entrée managé, par exemple un p-invoke inverse.</span><span class="sxs-lookup"><span data-stu-id="88f1b-109">The managed code will run any managed entry point, such as a reverse p-invoke.</span></span> <span data-ttu-id="88f1b-110">Aucun objectif plus détaillé n'est indiqué au runtime.</span><span class="sxs-lookup"><span data-stu-id="88f1b-110">Any more detailed purpose is unknown by the runtime.</span></span>|  
|`CODE_INVOKE_PURPOSE_CLASS_INIT`|<span data-ttu-id="88f1b-111">Le code managé exécute un constructeur statique.</span><span class="sxs-lookup"><span data-stu-id="88f1b-111">The managed code will run a static constructor.</span></span>|  
|`CODE_INVOKE_PURPOSE_INTERFACE_DISPATCH`|<span data-ttu-id="88f1b-112">Le code managé exécute l'implémentation pour une méthode d'interface qui a été appelée.</span><span class="sxs-lookup"><span data-stu-id="88f1b-112">The managed code will run the implementation for some interface method that was called.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="88f1b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="88f1b-113">Remarks</span></span>  
 <span data-ttu-id="88f1b-114">Cette énumération est utilisée par le [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) méthode pour fournir des informations sur l’exécution pas à pas du code managé.</span><span class="sxs-lookup"><span data-stu-id="88f1b-114">This enumeration is used by the [ICorDebugProcess6::GetExportStepInfo](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md) method to provide information about stepping through managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="88f1b-115">Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.</span><span class="sxs-lookup"><span data-stu-id="88f1b-115">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88f1b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88f1b-116">Requirements</span></span>  
 <span data-ttu-id="88f1b-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="88f1b-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88f1b-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="88f1b-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="88f1b-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88f1b-119">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="88f1b-120">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="88f1b-120">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="88f1b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88f1b-121">See also</span></span>

- [<span data-ttu-id="88f1b-122">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="88f1b-122">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [<span data-ttu-id="88f1b-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="88f1b-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
