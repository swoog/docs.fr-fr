---
title: ICorDebugStaticFieldSymbol::GetName, méthode
ms.date: 03/30/2017
ms.assetid: e2be4af2-15d1-4e6a-8b68-1d78c93294a4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b5f52999c3f680fbccefe4681f83d473cdb86306
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59206484"
---
# <a name="icordebugstaticfieldsymbolgetname-method"></a><span data-ttu-id="a8629-102">ICorDebugStaticFieldSymbol::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="a8629-102">ICorDebugStaticFieldSymbol::GetName Method</span></span>
<span data-ttu-id="a8629-103">Obtient le nom du champ static.</span><span class="sxs-lookup"><span data-stu-id="a8629-103">Gets the name of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8629-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8629-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a8629-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8629-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="a8629-106">[in] Nombre de caractères dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="a8629-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="a8629-107">[out] Pointeur vers le nombre de caractères réellement écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="a8629-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="a8629-108">[out] Tableau de caractères qui stocke le nom retourné.</span><span class="sxs-lookup"><span data-stu-id="a8629-108">[out] A character array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8629-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a8629-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a8629-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="a8629-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8629-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8629-111">Requirements</span></span>  
 <span data-ttu-id="a8629-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8629-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8629-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a8629-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a8629-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8629-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a8629-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8629-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8629-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8629-116">See also</span></span>

- [<span data-ttu-id="a8629-117">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="a8629-117">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="a8629-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a8629-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
