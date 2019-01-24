---
title: ICorDebugVariableHome Interface
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugVariableHome
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome
helpviewer_keywords:
- ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: 76f2bf3b-759f-4eed-bce7-119415b25915
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 78325236ab262c474e57b0d903033990b0e85f12
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721955"
---
# <a name="icordebugvariablehome-interface"></a><span data-ttu-id="a392a-102">ICorDebugVariableHome Interface</span><span class="sxs-lookup"><span data-stu-id="a392a-102">ICorDebugVariableHome Interface</span></span>
<span data-ttu-id="a392a-103">Représente une variable locale ou un argument d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="a392a-103">Represents a local variable or argument of a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a392a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a392a-104">Methods</span></span>  
  
|<span data-ttu-id="a392a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-105">Method</span></span>|<span data-ttu-id="a392a-106">Description</span><span class="sxs-lookup"><span data-stu-id="a392a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a392a-107">GetArgumentIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-107">GetArgumentIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getargumentindex-method.md)|<span data-ttu-id="a392a-108">Obtient l’index d’un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="a392a-108">Gets the index of a function argument.</span></span>|  
|[<span data-ttu-id="a392a-109">GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-109">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getcode-method.md)|<span data-ttu-id="a392a-110">Obtient l’instance « ICorDebugCode » qui contient ce `ICorDebugVariableHome` objet.</span><span class="sxs-lookup"><span data-stu-id="a392a-110">Gets the "ICorDebugCode" instance that contains this `ICorDebugVariableHome` object.</span></span>|  
|[<span data-ttu-id="a392a-111">GetLiveRange, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-111">GetLiveRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getliverange-method.md)|<span data-ttu-id="a392a-112">Obtient la plage native sur laquelle cette variable est en ligne.</span><span class="sxs-lookup"><span data-stu-id="a392a-112">Gets the native range over which this variable is live.</span></span>|  
|[<span data-ttu-id="a392a-113">GetLocationType, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-113">GetLocationType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md)|<span data-ttu-id="a392a-114">Obtient le type d’emplacement native de la variable.</span><span class="sxs-lookup"><span data-stu-id="a392a-114">Gets the type of the variable's native location.</span></span>|  
|[<span data-ttu-id="a392a-115">GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-115">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getoffset-method.md)|<span data-ttu-id="a392a-116">Obtient le décalage à partir du Registre de base pour une variable.</span><span class="sxs-lookup"><span data-stu-id="a392a-116">Gets the offset from the base register for a variable.</span></span>|  
|[<span data-ttu-id="a392a-117">GetRegister, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-117">GetRegister Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getregister-method.md)|<span data-ttu-id="a392a-118">Obtient le Registre qui contient une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.</span><span class="sxs-lookup"><span data-stu-id="a392a-118">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>|  
|[<span data-ttu-id="a392a-119">GetSlotIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="a392a-119">GetSlotIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getslotindex-method.md)|<span data-ttu-id="a392a-120">Obtient l’index emplacement managé d’une variable locale.</span><span class="sxs-lookup"><span data-stu-id="a392a-120">Gets the managed slot-index of a local variable.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a392a-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="a392a-121">Example</span></span>  
 <span data-ttu-id="a392a-122">Le fragment de code suivant utilise la [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) objet nommé `pCode4`.</span><span class="sxs-lookup"><span data-stu-id="a392a-122">The following code fragment uses the [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) object named `pCode4`.</span></span>  
  
```cpp  
ICorDebugCode4 *pCode4 = NULL;  
pCode->QueryInterface(IID_ICorDebugCode4, &pCode4);  
  
ICorDebugVariableEnum *pVarLocEnum = NULL;  
pCode4->EnumerateVariableHomes(&pVarLocEnum);  
  
// retrieve local variables and arguments  
ULONG celt = 0;  
pVarLocEnum->GetCount(&celt);  
ICorDebugVariableHome **homes = new ICorDebugVariableHome *[celt];  
ULONG celtFetched = 0;  
pVarLocEnum->Next(celt, homes, &celtFetched);  
  
for (int i = 0; i < celtFetched; i++)  
{  
    VariableLocationType locType = VLT_INVALID;  
    homes[i].GetLocationType(&locType);  
    switch (locType)  
    {  
    case VLT_REGISTER:  
        CorDebugRegister register = 0;  
        locals[i].GetRegister(&register);  
        // now we know which register it is in  
        break;  
    case VLT_REGISTER_RELATIVE:  
        CorDebugRegister baseRegister = 0;  
        LONG offset = 0;  
        locals[i].GetRegister(&register);  
        locals[i].GetOffset(&offset);  
        // now we know the register-relative offset  
        break;  
    case VLT_INVALID:  
        // handle case where we can't access the location  
        break;  
    }  
}  
```  
  
## <a name="requirements"></a><span data-ttu-id="a392a-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a392a-123">Requirements</span></span>  
 <span data-ttu-id="a392a-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a392a-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a392a-125">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a392a-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a392a-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a392a-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a392a-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a392a-127">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a392a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a392a-128">See also</span></span>
- [<span data-ttu-id="a392a-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a392a-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="a392a-130">ICorDebugVariableHomeEnum, interface</span><span class="sxs-lookup"><span data-stu-id="a392a-130">ICorDebugVariableHomeEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)
