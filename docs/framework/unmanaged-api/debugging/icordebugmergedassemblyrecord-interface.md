---
title: ICorDebugMergedAssemblyRecord, interface
ms.date: 03/30/2017
ms.assetid: fe280b11-9479-4e34-a07c-0d1ea8088422
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1118c879da4376bda0c73368a8b15df4f7a3d014
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59180464"
---
# <a name="icordebugmergedassemblyrecord-interface"></a><span data-ttu-id="e4349-102">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="e4349-102">ICorDebugMergedAssemblyRecord Interface</span></span>
<span data-ttu-id="e4349-103">Fournit des informations sur un assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="e4349-103">Provides information about a merged assembly.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e4349-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4349-104">Methods</span></span>  
  
|<span data-ttu-id="e4349-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-105">Method</span></span>|<span data-ttu-id="e4349-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4349-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e4349-107">GetCulture, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-107">GetCulture Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getculture-method.md)|<span data-ttu-id="e4349-108">Obtient la chaîne de nom de culture de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-108">Gets the culture name string of the assembly.</span></span>|  
|[<span data-ttu-id="e4349-109">GetIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-109">GetIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getindex-method.md)|<span data-ttu-id="e4349-110">Obtient l'index de préfixe de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-110">Gets the assembly's prefix index.</span></span>|  
|[<span data-ttu-id="e4349-111">GetPublicKey, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-111">GetPublicKey Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getpublickey-method.md)|<span data-ttu-id="e4349-112">Obtient la clé publique de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-112">Gets the assembly's public key.</span></span>|  
|[<span data-ttu-id="e4349-113">GetPublicKeyToken, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-113">GetPublicKeyToken Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getpublickeytoken-method.md)|<span data-ttu-id="e4349-114">Obtient le jeton de clé publique de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-114">Gets the assembly's public key token.</span></span>|  
|[<span data-ttu-id="e4349-115">GetSimpleName, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-115">GetSimpleName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getsimplename-method.md)|<span data-ttu-id="e4349-116">Obtient le nom simple de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-116">Gets the simple name of the assembly.</span></span>|  
|[<span data-ttu-id="e4349-117">GetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="e4349-117">GetVersion Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-getversion-method.md)|<span data-ttu-id="e4349-118">Obtient les informations de version de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e4349-118">Gets the assembly's version information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e4349-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e4349-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e4349-120">Cette interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="e4349-120">This interface is available with .NET Native only.</span></span> <span data-ttu-id="e4349-121">Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.</span><span class="sxs-lookup"><span data-stu-id="e4349-121">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4349-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4349-122">Requirements</span></span>  
 <span data-ttu-id="e4349-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4349-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4349-124">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e4349-124">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e4349-125">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4349-125">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e4349-126">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e4349-126">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e4349-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4349-127">See also</span></span>

- [<span data-ttu-id="e4349-128">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e4349-128">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="e4349-129">Débogage</span><span class="sxs-lookup"><span data-stu-id="e4349-129">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
