---
title: ICorDebugAssembly3, interface
ms.date: 03/30/2017
ms.assetid: 17fc5d76-75a9-4933-83f0-594de7f973f3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eecb135e034c3565e805ea776115579488b2a4d5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59210306"
---
# <a name="icordebugassembly3-interface"></a><span data-ttu-id="7a427-102">ICorDebugAssembly3, interface</span><span class="sxs-lookup"><span data-stu-id="7a427-102">ICorDebugAssembly3 Interface</span></span>
<span data-ttu-id="7a427-103">Étend logiquement l’interface ICorDebugAssembly pour prendre en charge pour les assemblys conteneurs et leurs assemblys de relation contenant-contenus.</span><span class="sxs-lookup"><span data-stu-id="7a427-103">Logically extends the ICorDebugAssembly interface to provide support for container assemblies and their contained assemblies.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="7a427-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7a427-104">Methods</span></span>  
  
|<span data-ttu-id="7a427-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7a427-105">Method</span></span>|<span data-ttu-id="7a427-106">Description</span><span class="sxs-lookup"><span data-stu-id="7a427-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="7a427-107">EnumerateContainedAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="7a427-107">EnumerateContainedAssemblies Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-enumeratecontainedassemblies-method.md)|<span data-ttu-id="7a427-108">Obtient un énumérateur pour les assemblys contenus dans cet assembly.</span><span class="sxs-lookup"><span data-stu-id="7a427-108">Gets an enumerator for the assemblies contained in this assembly.</span></span>|  
|[<span data-ttu-id="7a427-109">GetContainerAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="7a427-109">GetContainerAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-getcontainerassembly-method.md)|<span data-ttu-id="7a427-110">Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.</span><span class="sxs-lookup"><span data-stu-id="7a427-110">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7a427-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7a427-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7a427-112">L'interface est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="7a427-112">The interface is available with .NET Native only.</span></span> <span data-ttu-id="7a427-113">Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.</span><span class="sxs-lookup"><span data-stu-id="7a427-113">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a427-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a427-114">Requirements</span></span>  
 <span data-ttu-id="7a427-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a427-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a427-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7a427-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7a427-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a427-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a427-118">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a427-118">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a427-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a427-119">See also</span></span>

- [<span data-ttu-id="7a427-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7a427-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="7a427-121">Débogage</span><span class="sxs-lookup"><span data-stu-id="7a427-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
