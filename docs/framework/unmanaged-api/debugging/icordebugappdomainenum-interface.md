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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61989506"
---
# <a name="icordebugappdomainenum-interface"></a><span data-ttu-id="d1b59-102">ICorDebugAppDomainEnum, interface</span><span class="sxs-lookup"><span data-stu-id="d1b59-102">ICorDebugAppDomainEnum Interface</span></span>

<span data-ttu-id="d1b59-103">Fournit le `Next` (méthode), qui retourne un nombre spécifié de `ICorDebugAppDomainEnum` en commençant à l’emplacement suivant dans l’énumération de valeurs.</span><span class="sxs-lookup"><span data-stu-id="d1b59-103">Provides the `Next` method, which returns a specified number of `ICorDebugAppDomainEnum` values starting at the next location in the enumeration.</span></span> <span data-ttu-id="d1b59-104">Cette interface est une sous-classe de « ICorDebugEnum ».</span><span class="sxs-lookup"><span data-stu-id="d1b59-104">This interface is a subclass of "ICorDebugEnum".</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d1b59-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1b59-105">Methods</span></span>  
  
|<span data-ttu-id="d1b59-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="d1b59-106">Method</span></span>|<span data-ttu-id="d1b59-107">Description</span><span class="sxs-lookup"><span data-stu-id="d1b59-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d1b59-108">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="d1b59-108">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomainenum-next-method.md)|<span data-ttu-id="d1b59-109">Obtient le nombre spécifié de domaines d’application à partir de la collection, en commençant à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="d1b59-109">Gets the specified number of application domains from the collection, starting at the current cursor position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d1b59-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d1b59-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d1b59-111">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="d1b59-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1b59-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1b59-112">Requirements</span></span>  
 <span data-ttu-id="d1b59-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d1b59-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d1b59-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d1b59-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d1b59-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d1b59-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d1b59-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d1b59-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1b59-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1b59-117">See also</span></span>

- [<span data-ttu-id="d1b59-118">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="d1b59-118">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
- [<span data-ttu-id="d1b59-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d1b59-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
