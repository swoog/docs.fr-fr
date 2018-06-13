---
title: ICorDebugStaticFieldSymbol::GetName, méthode
ms.date: 03/30/2017
ms.assetid: e2be4af2-15d1-4e6a-8b68-1d78c93294a4
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 095c84a5cb448803bbfa45e0fad8a494343ca7f9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422316"
---
# <a name="icordebugstaticfieldsymbolgetname-method"></a><span data-ttu-id="33a48-102">ICorDebugStaticFieldSymbol::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="33a48-102">ICorDebugStaticFieldSymbol::GetName Method</span></span>
<span data-ttu-id="33a48-103">Obtient le nom du champ static.</span><span class="sxs-lookup"><span data-stu-id="33a48-103">Gets the name of the static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="33a48-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33a48-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="33a48-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33a48-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="33a48-106">[in] Nombre de caractères dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="33a48-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="33a48-107">[out] Pointeur vers le nombre de caractères réellement écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="33a48-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="33a48-108">[out] Tableau de caractères qui stocke le nom retourné.</span><span class="sxs-lookup"><span data-stu-id="33a48-108">[out] A character array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="33a48-109">Notes</span><span class="sxs-lookup"><span data-stu-id="33a48-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="33a48-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="33a48-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33a48-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33a48-111">Requirements</span></span>  
 <span data-ttu-id="33a48-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33a48-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33a48-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="33a48-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="33a48-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="33a48-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="33a48-115">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33a48-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33a48-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33a48-116">See Also</span></span>  
 [<span data-ttu-id="33a48-117">ICorDebugStaticFieldSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="33a48-117">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)  
 [<span data-ttu-id="33a48-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="33a48-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
