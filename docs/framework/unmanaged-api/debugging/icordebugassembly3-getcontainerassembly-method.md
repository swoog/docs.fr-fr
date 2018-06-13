---
title: ICorDebugAssembly3::GetContainerAssembly, méthode
ms.date: 03/30/2017
ms.assetid: f5fddeb6-b82e-4ebb-b432-849ce8513c77
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acb34ac2568ac88797441306820e6e762b5ac46e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33409725"
---
# <a name="icordebugassembly3getcontainerassembly-method"></a><span data-ttu-id="d237d-102">ICorDebugAssembly3::GetContainerAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="d237d-102">ICorDebugAssembly3::GetContainerAssembly Method</span></span>
<span data-ttu-id="d237d-103">Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.</span><span class="sxs-lookup"><span data-stu-id="d237d-103">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d237d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d237d-104">Syntax</span></span>  
  
```  
HRESULT GetContainerAssembly(  
    ICorDebugAssembly **ppAssembly  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d237d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d237d-105">Parameters</span></span>  
 `ppAssembly`  
 <span data-ttu-id="d237d-106">Un pointeur vers l’adresse d’un objet ICorDebugAssembly qui représente l’assembly conteneur, ou **null** si l’appel de méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="d237d-106">A pointer to the address of an ICorDebugAssembly object that represents the container assembly, or **null** if the method call fails.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d237d-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d237d-107">Return Value</span></span>  
 <span data-ttu-id="d237d-108">`S_OK` Si l’appel de méthode a réussi ; dans le cas contraire, `S_FALSE`, et `ppAssembly` est **null**.</span><span class="sxs-lookup"><span data-stu-id="d237d-108">`S_OK` if the method call succeeds; otherwise, `S_FALSE`, and `ppAssembly` is **null**.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d237d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d237d-109">Remarks</span></span>  
 <span data-ttu-id="d237d-110">Si cet assembly a été fusionné avec d’autres assemblys dans un seul assembly conteneur, cette méthode retourne l’assembly conteneur.</span><span class="sxs-lookup"><span data-stu-id="d237d-110">If this assembly has been merged with others inside a single container assembly, this method returns the container assembly.</span></span> <span data-ttu-id="d237d-111">Pour plus d’informations et la terminologie, consultez le [ICorDebugProcess6::EnableVirtualModuleSplitting](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="d237d-111">For more information and terminology, see the [ICorDebugProcess6::EnableVirtualModuleSplitting](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md) topic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d237d-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="d237d-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d237d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d237d-113">Requirements</span></span>  
 <span data-ttu-id="d237d-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d237d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d237d-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d237d-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d237d-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d237d-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d237d-117">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d237d-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d237d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d237d-118">See Also</span></span>  
 [<span data-ttu-id="d237d-119">ICorDebugAssembly3, interface</span><span class="sxs-lookup"><span data-stu-id="d237d-119">ICorDebugAssembly3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-interface.md)  
 [<span data-ttu-id="d237d-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d237d-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
