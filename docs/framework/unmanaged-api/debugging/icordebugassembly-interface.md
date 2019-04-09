---
title: ICorDebugAssembly, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3dd60defc1c003fa4b235ddcb0a78b9a819b1b0c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198021"
---
# <a name="icordebugassembly-interface"></a><span data-ttu-id="43ad5-102">ICorDebugAssembly, interface</span><span class="sxs-lookup"><span data-stu-id="43ad5-102">ICorDebugAssembly Interface</span></span>

<span data-ttu-id="43ad5-103">Représente un assembly.</span><span class="sxs-lookup"><span data-stu-id="43ad5-103">Represents an assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="43ad5-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="43ad5-104">Methods</span></span>  
  
|<span data-ttu-id="43ad5-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-105">Method</span></span>|<span data-ttu-id="43ad5-106">Description</span><span class="sxs-lookup"><span data-stu-id="43ad5-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="43ad5-107">EnumerateModules, méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-107">EnumerateModules Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|<span data-ttu-id="43ad5-108">Obtient un énumérateur pour les modules contenus dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="43ad5-108">Gets an enumerator for the modules contained in the assembly.</span></span>|  
|[<span data-ttu-id="43ad5-109">GetAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-109">GetAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|<span data-ttu-id="43ad5-110">Obtient un pointeur d’interface vers le domaine d’application qui contient ce `ICorDebugAssembly` instance.</span><span class="sxs-lookup"><span data-stu-id="43ad5-110">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>|  
|[<span data-ttu-id="43ad5-111">GetCodeBase, méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-111">GetCodeBase Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|<span data-ttu-id="43ad5-112">Non implémenté dans la version actuelle du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="43ad5-112">Not implemented in the current version of the .NET Framework.</span></span>|  
|[<span data-ttu-id="43ad5-113">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|<span data-ttu-id="43ad5-114">Obtient le nom de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="43ad5-114">Gets the name of the assembly.</span></span>|  
|[<span data-ttu-id="43ad5-115">GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="43ad5-115">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|<span data-ttu-id="43ad5-116">Obtient l’instance ICorDebugProcess dans lequel l’assembly est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="43ad5-116">Gets the ICorDebugProcess instance in which the assembly is running.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="43ad5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="43ad5-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="43ad5-118">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="43ad5-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43ad5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43ad5-119">Requirements</span></span>  
 <span data-ttu-id="43ad5-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="43ad5-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43ad5-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="43ad5-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="43ad5-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="43ad5-122">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="43ad5-123">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="43ad5-123">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="43ad5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43ad5-124">See also</span></span>

- [<span data-ttu-id="43ad5-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="43ad5-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
