---
title: ICorDebugGuidToTypeEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum
helpviewer_keywords:
- ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: aa32b12b-05fc-4ea8-a904-adae25034269
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f2ea67c6e4d860d41cfe67aaab73babb51f3ce45
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210657"
---
# <a name="icordebugguidtotypeenum-interface"></a><span data-ttu-id="f0fdc-102">ICorDebugGuidToTypeEnum, interface</span><span class="sxs-lookup"><span data-stu-id="f0fdc-102">ICorDebugGuidToTypeEnum Interface</span></span>
<span data-ttu-id="f0fdc-103">Fournit un énumérateur qui définit le mappage entre un ensemble de GUID et leurs types correspondants, qui sont représentés par des instances de ICorDebugType.</span><span class="sxs-lookup"><span data-stu-id="f0fdc-103">Provides an enumerator that defines the mapping between a set of GUIDs and their corresponding types, which are represented by ICorDebugType instances.</span></span> <span data-ttu-id="f0fdc-104">Cette interface hérite des méthodes de l’interface de ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="f0fdc-104">This interface inherits the methods from the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f0fdc-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f0fdc-105">Methods</span></span>  
  
|<span data-ttu-id="f0fdc-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="f0fdc-106">Method</span></span>|<span data-ttu-id="f0fdc-107">Description</span><span class="sxs-lookup"><span data-stu-id="f0fdc-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f0fdc-108">ICorDebugGuidToTypeEnum::Next</span><span class="sxs-lookup"><span data-stu-id="f0fdc-108">ICorDebugGuidToTypeEnum::Next</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-next-method.md)|<span data-ttu-id="f0fdc-109">Obtient le nombre spécifié de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances qui mappent des GUID vers le type d’informations.</span><span class="sxs-lookup"><span data-stu-id="f0fdc-109">Gets the specified number of [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances that map GUIDs to type information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f0fdc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f0fdc-110">Remarks</span></span>  
 <span data-ttu-id="f0fdc-111">Un `ICorDebugGuidToTypeEnum` objet d’interface peut être récupérée en appelant le [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f0fdc-111">An `ICorDebugGuidToTypeEnum` interface object can be retrieved by calling the [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) method.</span></span> <span data-ttu-id="f0fdc-112">Un débogueur peut appeler de cette interface [suivant](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-next-method.md) méthode pour récupérer [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) les objets qui représentent les mappages de gérés représentations sous forme de [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types chargés dans le domaine d’application utilisé pour l’appel à la [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f0fdc-112">A debugger can call this interface's [Next](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-next-method.md) method to retrieve [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) objects that represent mappings of managed representations of [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types loaded in the application domain used for the call to the [ICorDebugAppDomain3::GetCachedWinRTTypes](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-getcachedwinrttypes-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0fdc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0fdc-113">Requirements</span></span>  
 **<span data-ttu-id="f0fdc-114">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="f0fdc-114">Platforms:</span></span>** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 <span data-ttu-id="f0fdc-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0fdc-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0fdc-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0fdc-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="f0fdc-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f0fdc-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f0fdc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0fdc-118">See also</span></span>

- [<span data-ttu-id="f0fdc-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="f0fdc-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
