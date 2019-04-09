---
title: ICorDebugAppDomainEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomainEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomainEnum
helpviewer_keywords:
- ICorDebugAppDomainEnum interface [.NET Framework debugging]
ms.assetid: e9226e6e-ca2c-428e-bb38-0c099210f507
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: da1fc949109455cf50767191a99a8a727116f77c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59155192"
---
# <a name="icordebugappdomainenum-interface"></a><span data-ttu-id="8dae3-102">ICorDebugAppDomainEnum, interface</span><span class="sxs-lookup"><span data-stu-id="8dae3-102">ICorDebugAppDomainEnum Interface</span></span>

<span data-ttu-id="8dae3-103">Fournit le `Next` (méthode), qui retourne un nombre spécifié de `ICorDebugAppDomainEnum` en commençant à l’emplacement suivant dans l’énumération de valeurs.</span><span class="sxs-lookup"><span data-stu-id="8dae3-103">Provides the `Next` method, which returns a specified number of `ICorDebugAppDomainEnum` values starting at the next location in the enumeration.</span></span> <span data-ttu-id="8dae3-104">Cette interface est une sous-classe de « ICorDebugEnum ».</span><span class="sxs-lookup"><span data-stu-id="8dae3-104">This interface is a subclass of "ICorDebugEnum".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8dae3-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8dae3-105">Methods</span></span>  
  
|<span data-ttu-id="8dae3-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="8dae3-106">Method</span></span>|<span data-ttu-id="8dae3-107">Description</span><span class="sxs-lookup"><span data-stu-id="8dae3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8dae3-108">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="8dae3-108">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomainenum-next-method.md)|<span data-ttu-id="8dae3-109">Obtient le nombre spécifié de domaines d’application à partir de la collection, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="8dae3-109">Gets the specified number of application domains from the collection, starting at the current cursor position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8dae3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8dae3-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8dae3-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="8dae3-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8dae3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dae3-112">Requirements</span></span>  
 <span data-ttu-id="8dae3-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8dae3-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8dae3-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8dae3-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8dae3-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8dae3-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="8dae3-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8dae3-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8dae3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dae3-117">See also</span></span>

- [<span data-ttu-id="8dae3-118">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="8dae3-118">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
- [<span data-ttu-id="8dae3-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="8dae3-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
