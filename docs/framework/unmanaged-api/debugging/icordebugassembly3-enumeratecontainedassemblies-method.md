---
title: ICorDebugAssembly3::EnumerateContainedAssemblies, méthode
ms.date: 03/30/2017
ms.assetid: 98f15b05-afad-4616-9e2a-1a9af31948b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 54ccb52468a530280527252e0e0c43cc9edbb2c3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080954"
---
# <a name="icordebugassembly3enumeratecontainedassemblies-method"></a><span data-ttu-id="d0a97-102">ICorDebugAssembly3::EnumerateContainedAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a97-102">ICorDebugAssembly3::EnumerateContainedAssemblies Method</span></span>
<span data-ttu-id="d0a97-103">Obtient un énumérateur pour les assemblys contenus dans cet assembly.</span><span class="sxs-lookup"><span data-stu-id="d0a97-103">Gets an enumerator for the assemblies contained in this assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0a97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0a97-104">Syntax</span></span>  
  
```  
HRESULT EnumerateContainedAssemblies(  
    ICorDebugAssemblyEnum **ppAssemblies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0a97-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0a97-105">Parameters</span></span>  
 `ppAssemblies`  
 <span data-ttu-id="d0a97-106">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugAssemblyEnum qui est l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="d0a97-106">[out] A pointer to the address of an ICorDebugAssemblyEnum interface object that is the enumerator.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d0a97-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d0a97-107">Return Value</span></span>  
 `S_OK` <span data-ttu-id="d0a97-108">Si cette `ICorDebugAssembly3` objet est un conteneur ; sinon, `S_FALSE`, et l’énumération est vide.</span><span class="sxs-lookup"><span data-stu-id="d0a97-108">if this `ICorDebugAssembly3` object is a container; otherwise, `S_FALSE`, and the enumeration is empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d0a97-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d0a97-109">Remarks</span></span>  
 <span data-ttu-id="d0a97-110">Des symboles doivent être utilisés pour énumérer les assemblys contenus dans l'assembly.</span><span class="sxs-lookup"><span data-stu-id="d0a97-110">Symbols are needed to enumerate the contained assemblies.</span></span> <span data-ttu-id="d0a97-111">S'ils ne sont pas présents, la méthode retourne `S_FALSE`, et aucun énumérateur valide n'est fourni.</span><span class="sxs-lookup"><span data-stu-id="d0a97-111">If they aren't present, the method returns `S_FALSE`, and no valid enumerator is provided.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0a97-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="d0a97-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0a97-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0a97-113">Requirements</span></span>  
 <span data-ttu-id="d0a97-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0a97-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0a97-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d0a97-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d0a97-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d0a97-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="d0a97-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d0a97-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d0a97-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0a97-118">See also</span></span>

- [<span data-ttu-id="d0a97-119">ICorDebugAssembly3, interface</span><span class="sxs-lookup"><span data-stu-id="d0a97-119">ICorDebugAssembly3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-interface.md)
- [<span data-ttu-id="d0a97-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d0a97-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
