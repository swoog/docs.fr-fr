---
title: ICorDebugProcess6::GetCode, méthode
ms.date: 03/30/2017
ms.assetid: faa538c2-60c9-4064-b996-1b4c24ebd751
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 572b279ddfdb1fb0eb9da4b0d1f8c2cb12c8a46b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420161"
---
# <a name="icordebugprocess6getcode-method"></a><span data-ttu-id="3f6ad-102">ICorDebugProcess6::GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="3f6ad-102">ICorDebugProcess6::GetCode Method</span></span>
<span data-ttu-id="3f6ad-103">Obtient des informations sur le code managé à une adresse de code particulière.</span><span class="sxs-lookup"><span data-stu-id="3f6ad-103">Gets information about the managed code at a particular code address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f6ad-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f6ad-104">Syntax</span></span>  
  
```  
HRESULT GetCode(  
    [in] CORDB_ADDRESS codeAddress,   
    [out] ICorDebugCode **ppCode);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3f6ad-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f6ad-105">Parameters</span></span>  
 `codeAddress`  
 <span data-ttu-id="3f6ad-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui spécifie l’adresse de départ du segment de code managé.</span><span class="sxs-lookup"><span data-stu-id="3f6ad-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that specifies the starting address of the managed code segment.</span></span>  
  
 `ppCode`  
 <span data-ttu-id="3f6ad-107">[out] Pointeur vers l’adresse d’un objet « ICorDebugCode » représente un segment de code managé.</span><span class="sxs-lookup"><span data-stu-id="3f6ad-107">[out] A pointer to the address of an "ICorDebugCode" object that represents a segment of managed code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f6ad-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3f6ad-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3f6ad-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="3f6ad-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f6ad-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f6ad-110">Requirements</span></span>  
 <span data-ttu-id="3f6ad-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ad-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f6ad-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3f6ad-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3f6ad-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3f6ad-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3f6ad-114">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f6ad-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f6ad-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f6ad-115">See Also</span></span>  
 [<span data-ttu-id="3f6ad-116">ICorDebugProcess6, interface</span><span class="sxs-lookup"><span data-stu-id="3f6ad-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)  
 [<span data-ttu-id="3f6ad-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3f6ad-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
