---
title: Méthode ICorDebugVariableSymbol::GetValue
ms.date: 03/30/2017
ms.assetid: 90abece1-392e-4ade-94a1-30c75b0f7074
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 14412c11010b94fdc462c5aa29e9bc769b2633cc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54496752"
---
# <a name="icordebugvariablesymbolgetvalue-method"></a><span data-ttu-id="23b29-102">Méthode ICorDebugVariableSymbol::GetValue</span><span class="sxs-lookup"><span data-stu-id="23b29-102">ICorDebugVariableSymbol::GetValue Method</span></span>
<span data-ttu-id="23b29-103">Obtient la valeur d'une variable sous forme d'un tableau d'octets.</span><span class="sxs-lookup"><span data-stu-id="23b29-103">Gets the value of a variable as a byte array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23b29-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23b29-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
   [in] ULONG32 offset,  
   [in] ULONG32 cbContext,  
   [in, size_is(cbContext)] BYTE context[],  
   [in] ULONG32 cbValue,  
   [out] ULONG32 *pcbValue,  
   [out, size_is(cbValue), length_is(*pcbValue)] BYTE pValue[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="23b29-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23b29-105">Parameters</span></span>  
 `offset`  
 <span data-ttu-id="23b29-106">[in] Offset de démarrage dans la variable au niveau duquel lire la valeur.</span><span class="sxs-lookup"><span data-stu-id="23b29-106">[in] The starting offset in the variable from which to read the value.</span></span> <span data-ttu-id="23b29-107">Ce paramètre est utilisé lors de la lecture de champs membres d'un objet.</span><span class="sxs-lookup"><span data-stu-id="23b29-107">This parameter is used when reading member fields in an object.</span></span>  
  
 `cbContext`  
 <span data-ttu-id="23b29-108">[in] Taille en octets de l’argument `context`.</span><span class="sxs-lookup"><span data-stu-id="23b29-108">[in] The size in bytes of the `context` argument.</span></span>  
  
 `context`  
 <span data-ttu-id="23b29-109">[in] Contexte de thread utilisé pour lire la valeur.</span><span class="sxs-lookup"><span data-stu-id="23b29-109">[in] The thread context used to read the value.</span></span>  
  
 `cbValue`  
 <span data-ttu-id="23b29-110">[in] Taille en octets de la mémoire tampon `pValue`.</span><span class="sxs-lookup"><span data-stu-id="23b29-110">[in] The size in bytes of the `pValue` buffer.</span></span>  
  
 `pcbValue`  
 <span data-ttu-id="23b29-111">[out] Nombre d'octets réellement écrits dans la mémoire tampon `pValue`.</span><span class="sxs-lookup"><span data-stu-id="23b29-111">[out] The number of bytes actually written to the `pValue` buffer.</span></span>  
  
 `pValue`  
 <span data-ttu-id="23b29-112">[out] Tableau d'octets contenant la valeur de la variable.</span><span class="sxs-lookup"><span data-stu-id="23b29-112">[out] A byte array that contains the value of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="23b29-113">Notes</span><span class="sxs-lookup"><span data-stu-id="23b29-113">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="23b29-114">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="23b29-114">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="23b29-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23b29-115">Requirements</span></span>  
 <span data-ttu-id="23b29-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="23b29-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="23b29-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="23b29-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="23b29-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="23b29-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="23b29-119">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="23b29-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23b29-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23b29-120">See also</span></span>
- [<span data-ttu-id="23b29-121">ICorDebugVariableSymbol, interface</span><span class="sxs-lookup"><span data-stu-id="23b29-121">ICorDebugVariableSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="23b29-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="23b29-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
