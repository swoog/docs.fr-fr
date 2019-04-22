---
title: ICorDebugVariableHome, interface
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
ms.openlocfilehash: 339a0f502b7e47f7bee82a0da92185481d909e64
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59202909"
---
# <a name="icordebugvariablehome-interface"></a><span data-ttu-id="50998-102">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="50998-102">ICorDebugVariableHome Interface</span></span>
<span data-ttu-id="50998-103">Représente une variable locale ou un argument d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="50998-103">Represents a local variable or argument of a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="50998-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="50998-104">Methods</span></span>  
  
|<span data-ttu-id="50998-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="50998-105">Method</span></span>|<span data-ttu-id="50998-106">Description</span><span class="sxs-lookup"><span data-stu-id="50998-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="50998-107">GetArgumentIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-107">GetArgumentIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getargumentindex-method.md)|<span data-ttu-id="50998-108">Obtient l’index d’un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="50998-108">Gets the index of a function argument.</span></span>|  
|[<span data-ttu-id="50998-109">GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-109">GetCode Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getcode-method.md)|<span data-ttu-id="50998-110">Obtient l’instance « ICorDebugCode » qui contient ce `ICorDebugVariableHome` objet.</span><span class="sxs-lookup"><span data-stu-id="50998-110">Gets the "ICorDebugCode" instance that contains this `ICorDebugVariableHome` object.</span></span>|  
|[<span data-ttu-id="50998-111">GetLiveRange, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-111">GetLiveRange Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getliverange-method.md)|<span data-ttu-id="50998-112">Obtient la plage native sur laquelle cette variable est en ligne.</span><span class="sxs-lookup"><span data-stu-id="50998-112">Gets the native range over which this variable is live.</span></span>|  
|[<span data-ttu-id="50998-113">GetLocationType, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-113">GetLocationType Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getlocationtype-method.md)|<span data-ttu-id="50998-114">Obtient le type d’emplacement native de la variable.</span><span class="sxs-lookup"><span data-stu-id="50998-114">Gets the type of the variable's native location.</span></span>|  
|[<span data-ttu-id="50998-115">GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-115">GetOffset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getoffset-method.md)|<span data-ttu-id="50998-116">Obtient le décalage à partir du Registre de base pour une variable.</span><span class="sxs-lookup"><span data-stu-id="50998-116">Gets the offset from the base register for a variable.</span></span>|  
|[<span data-ttu-id="50998-117">GetRegister, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-117">GetRegister Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getregister-method.md)|<span data-ttu-id="50998-118">Obtient le Registre qui contient une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.</span><span class="sxs-lookup"><span data-stu-id="50998-118">Gets the register that contains a variable with a location type of `VLT_REGISTER`, and the base register for a variable with a location type of `VLT_REGISTER_RELATIVE`.</span></span>|  
|[<span data-ttu-id="50998-119">GetSlotIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="50998-119">GetSlotIndex Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-getslotindex-method.md)|<span data-ttu-id="50998-120">Obtient l’index emplacement managé d’une variable locale.</span><span class="sxs-lookup"><span data-stu-id="50998-120">Gets the managed slot-index of a local variable.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="50998-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="50998-121">Example</span></span>  
 <span data-ttu-id="50998-122">Le fragment de code suivant utilise la [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) objet nommé `pCode4`.</span><span class="sxs-lookup"><span data-stu-id="50998-122">The following code fragment uses the [ICorDebugCode4](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-interface.md) object named `pCode4`.</span></span>  
  
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
  
## <a name="requirements"></a><span data-ttu-id="50998-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50998-123">Requirements</span></span>  
 <span data-ttu-id="50998-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50998-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50998-125">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="50998-125">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="50998-126">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50998-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="50998-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50998-127">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50998-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50998-128">See also</span></span>

- [<span data-ttu-id="50998-129">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="50998-129">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="50998-130">ICorDebugVariableHomeEnum, interface</span><span class="sxs-lookup"><span data-stu-id="50998-130">ICorDebugVariableHomeEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)
