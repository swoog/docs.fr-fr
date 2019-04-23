---
title: Méthode ICorDebugVariableSymbol::GetName
ms.date: 03/30/2017
ms.assetid: c922b7d4-44e5-45e4-aef3-cc9c35a0be80
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3f514acbd772c9d33ec4372cfaccb778d6bb41eb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59170168"
---
# <a name="icordebugvariablesymbolgetname-method"></a><span data-ttu-id="51e36-102">Méthode ICorDebugVariableSymbol::GetName</span><span class="sxs-lookup"><span data-stu-id="51e36-102">ICorDebugVariableSymbol::GetName Method</span></span>
<span data-ttu-id="51e36-103">Obtient le nom d'une variable.</span><span class="sxs-lookup"><span data-stu-id="51e36-103">Gets the name of a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51e36-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51e36-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="51e36-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51e36-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="51e36-106">[in] Nombre de caractères dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="51e36-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="51e36-107">[out] Pointeur vers le nombre de caractères réellement écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="51e36-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="51e36-108">Pointeur vers un tableau de caractères qui contient le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="51e36-108">A pointer to a character array that contains the variable name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="51e36-109">Notes</span><span class="sxs-lookup"><span data-stu-id="51e36-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51e36-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="51e36-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51e36-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51e36-111">Requirements</span></span>  
 <span data-ttu-id="51e36-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="51e36-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="51e36-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="51e36-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="51e36-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="51e36-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="51e36-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="51e36-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51e36-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51e36-116">See also</span></span>

- [<span data-ttu-id="51e36-117">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="51e36-117">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="51e36-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="51e36-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
