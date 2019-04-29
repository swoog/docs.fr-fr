---
title: ICorDebugLoadedModule::GetName (méthode)
ms.date: 03/30/2017
ms.assetid: 88c304d5-edaa-4c0e-a8e1-144e8a76877e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9bf09c01d24315c3f239911326f1844a0b2cc101
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946261"
---
# <a name="icordebugloadedmodulegetname-method"></a><span data-ttu-id="12354-102">ICorDebugLoadedModule::GetName (méthode)</span><span class="sxs-lookup"><span data-stu-id="12354-102">ICorDebugLoadedModule::GetName Method</span></span>
<span data-ttu-id="12354-103">Obtient le nom du module chargé.</span><span class="sxs-lookup"><span data-stu-id="12354-103">Gets the name of the loaded module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12354-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12354-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,  
   [out] ULONG32 *pcchName,  
   [out, size_is(cchName),  
   length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12354-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12354-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="12354-106">[in] Nombre de caractères dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="12354-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="12354-107">[out] Pointeur vers le nombre de caractères réellement écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="12354-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="12354-108">[out] Tableau de caractères contenant le nom du module chargé.</span><span class="sxs-lookup"><span data-stu-id="12354-108">[out] An array of characters that contain the name of the loaded module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="12354-109">Notes</span><span class="sxs-lookup"><span data-stu-id="12354-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="12354-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="12354-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12354-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12354-111">Requirements</span></span>  
 <span data-ttu-id="12354-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12354-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12354-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="12354-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="12354-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="12354-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="12354-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12354-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12354-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12354-116">See also</span></span>

- [<span data-ttu-id="12354-117">ICorDebugLoadedModule, interface</span><span class="sxs-lookup"><span data-stu-id="12354-117">ICorDebugLoadedModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md)
- [<span data-ttu-id="12354-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="12354-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
