---
title: ICorDebugAssembly3::GetContainerAssembly, méthode
ms.date: 03/30/2017
ms.assetid: f5fddeb6-b82e-4ebb-b432-849ce8513c77
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a9bd4cd44eca9b12ab8773fd75b6262579cfe8e8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59206081"
---
# <a name="icordebugassembly3getcontainerassembly-method"></a><span data-ttu-id="cd9e2-102">ICorDebugAssembly3::GetContainerAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="cd9e2-102">ICorDebugAssembly3::GetContainerAssembly Method</span></span>
<span data-ttu-id="cd9e2-103">Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-103">Returns the container assembly of this `ICorDebugAssembly3` object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd9e2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd9e2-104">Syntax</span></span>  
  
```  
HRESULT GetContainerAssembly(  
    ICorDebugAssembly **ppAssembly  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd9e2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd9e2-105">Parameters</span></span>  
 `ppAssembly`  
 <span data-ttu-id="cd9e2-106">Un pointeur vers l’adresse d’un objet ICorDebugAssembly qui représente l’assembly conteneur, ou **null** si l’appel de méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-106">A pointer to the address of an ICorDebugAssembly object that represents the container assembly, or **null** if the method call fails.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cd9e2-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cd9e2-107">Return Value</span></span>  
 <span data-ttu-id="cd9e2-108">`S_OK` Si l’appel de méthode réussit ; Sinon, `S_FALSE`, et `ppAssembly` est **null**.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-108">`S_OK` if the method call succeeds; otherwise, `S_FALSE`, and `ppAssembly` is **null**.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cd9e2-109">Notes</span><span class="sxs-lookup"><span data-stu-id="cd9e2-109">Remarks</span></span>  
 <span data-ttu-id="cd9e2-110">Si cet assembly a été fusionné avec d’autres assemblys dans un seul assembly conteneur, cette méthode retourne l’assembly conteneur.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-110">If this assembly has been merged with others inside a single container assembly, this method returns the container assembly.</span></span> <span data-ttu-id="cd9e2-111">Pour plus d’informations et de la terminologie, consultez le [ICorDebugProcess6::EnableVirtualModuleSplitting](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md) rubrique.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-111">For more information and terminology, see the [ICorDebugProcess6::EnableVirtualModuleSplitting](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md) topic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cd9e2-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="cd9e2-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd9e2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd9e2-113">Requirements</span></span>  
 <span data-ttu-id="cd9e2-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cd9e2-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd9e2-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cd9e2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cd9e2-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd9e2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd9e2-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd9e2-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd9e2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd9e2-118">See also</span></span>

- [<span data-ttu-id="cd9e2-119">ICorDebugAssembly3, interface</span><span class="sxs-lookup"><span data-stu-id="cd9e2-119">ICorDebugAssembly3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-interface.md)
- [<span data-ttu-id="cd9e2-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="cd9e2-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
