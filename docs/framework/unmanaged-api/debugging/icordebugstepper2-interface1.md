---
title: ICorDebugStepper2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2
helpviewer_keywords:
- ICorDebugStepper2 interface [.NET Framework debugging]
ms.assetid: 7a191c2a-95ea-4d47-83b0-44de2b632d63
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 256f67d21a22ee4692d88311cc150736e61563a0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59073054"
---
# <a name="icordebugstepper2-interface"></a><span data-ttu-id="bf4e9-102">ICorDebugStepper2, interface</span><span class="sxs-lookup"><span data-stu-id="bf4e9-102">ICorDebugStepper2 Interface</span></span>
<span data-ttu-id="bf4e9-103">Prend en charge le débogage uniquement mon code (JMC).</span><span class="sxs-lookup"><span data-stu-id="bf4e9-103">Provides support for just my code (JMC) debugging.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="bf4e9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bf4e9-104">Methods</span></span>  
  
|<span data-ttu-id="bf4e9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="bf4e9-105">Method</span></span>|<span data-ttu-id="bf4e9-106">Description</span><span class="sxs-lookup"><span data-stu-id="bf4e9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="bf4e9-107">SetJMC, méthode</span><span class="sxs-lookup"><span data-stu-id="bf4e9-107">SetJMC Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper2-setjmc-method.md)|<span data-ttu-id="bf4e9-108">Définit une valeur qui spécifie si cette ICorDebugStepper exécute pas à pas uniquement le code créé par le développeur d’une application.</span><span class="sxs-lookup"><span data-stu-id="bf4e9-108">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bf4e9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bf4e9-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bf4e9-110">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="bf4e9-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf4e9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf4e9-111">Requirements</span></span>  
 <span data-ttu-id="bf4e9-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf4e9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf4e9-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bf4e9-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bf4e9-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bf4e9-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="bf4e9-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bf4e9-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bf4e9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf4e9-116">See also</span></span>

- [<span data-ttu-id="bf4e9-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="bf4e9-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
