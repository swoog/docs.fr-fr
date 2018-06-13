---
title: ICorDebugAssembly Interface1
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
ms.openlocfilehash: 88134fb7854091bb60e8084a6d776bdec922c7e1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406368"
---
# <a name="icordebugassembly-interface1"></a><span data-ttu-id="3e925-102">ICorDebugAssembly Interface1</span><span class="sxs-lookup"><span data-stu-id="3e925-102">ICorDebugAssembly Interface1</span></span>
<span data-ttu-id="3e925-103">Représente un assembly.</span><span class="sxs-lookup"><span data-stu-id="3e925-103">Represents an assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3e925-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3e925-104">Methods</span></span>  
  
|<span data-ttu-id="3e925-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-105">Method</span></span>|<span data-ttu-id="3e925-106">Description</span><span class="sxs-lookup"><span data-stu-id="3e925-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3e925-107">EnumerateModules, méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-107">EnumerateModules Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|<span data-ttu-id="3e925-108">Obtient un énumérateur pour les modules contenus dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3e925-108">Gets an enumerator for the modules contained in the assembly.</span></span>|  
|[<span data-ttu-id="3e925-109">GetAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-109">GetAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|<span data-ttu-id="3e925-110">Obtient un pointeur d’interface vers le domaine d’application qui contient cette `ICorDebugAssembly` instance.</span><span class="sxs-lookup"><span data-stu-id="3e925-110">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>|  
|[<span data-ttu-id="3e925-111">GetCodeBase, méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-111">GetCodeBase Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|<span data-ttu-id="3e925-112">Non implémenté dans la version actuelle du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3e925-112">Not implemented in the current version of the .NET Framework.</span></span>|  
|[<span data-ttu-id="3e925-113">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|<span data-ttu-id="3e925-114">Obtient le nom de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="3e925-114">Gets the name of the assembly.</span></span>|  
|[<span data-ttu-id="3e925-115">GetProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="3e925-115">GetProcess Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|<span data-ttu-id="3e925-116">Obtient l’instance ICorDebugProcess dans lequel l’assembly est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3e925-116">Gets the ICorDebugProcess instance in which the assembly is running.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e925-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3e925-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3e925-118">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="3e925-118">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e925-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3e925-119">Requirements</span></span>  
 <span data-ttu-id="3e925-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3e925-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e925-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3e925-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3e925-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3e925-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3e925-123">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e925-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e925-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e925-124">See Also</span></span>  
 [<span data-ttu-id="3e925-125">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3e925-125">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
