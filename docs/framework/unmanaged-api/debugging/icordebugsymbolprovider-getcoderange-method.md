---
title: ICorDebugSymbolProvider::GetCodeRange, méthode
ms.date: 03/30/2017
ms.assetid: 49a2451f-d250-4e73-aa96-9ff49d9f11c6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f60ba1c68e95363a59c5a1d217756664f63e5256
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420122"
---
# <a name="icordebugsymbolprovidergetcoderange-method"></a><span data-ttu-id="31de9-102">ICorDebugSymbolProvider::GetCodeRange, méthode</span><span class="sxs-lookup"><span data-stu-id="31de9-102">ICorDebugSymbolProvider::GetCodeRange Method</span></span>
<span data-ttu-id="31de9-103">Obtient l'adresse de début et la taille de la méthode pour une adresse virtuelle relative (RVA) donnée dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="31de9-103">Gets the method start address and size given a relative virtual address (RVA) in a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31de9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31de9-104">Syntax</span></span>  
  
```  
HRESULT GetCodeRange(  
   [in] ULONG32 codeRva,   
   [out] ULONG32* pCodeStartAddress,   
   [out] ULONG32* pCodeSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="31de9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31de9-105">Parameters</span></span>  
 `codeRva`  
 <span data-ttu-id="31de9-106">[in] Adresse virtuelle relative (RVA) dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="31de9-106">[in] The relative virtual address (RVA) in a method.</span></span>  
  
 `pCodeStartAddress`  
 <span data-ttu-id="31de9-107">[out] Pointeur vers l'adresse de début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="31de9-107">[out] A pointer to the starting address of the method.</span></span>  
  
 `pCodeSize`  
 <span data-ttu-id="31de9-108">Pointeur vers la taille du code de la méthode (nombre d'octets du code de la méthode).</span><span class="sxs-lookup"><span data-stu-id="31de9-108">A pointer to the method code size (the number of bytes of the method's code).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="31de9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="31de9-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="31de9-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="31de9-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="31de9-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="31de9-111">Requirements</span></span>  
 <span data-ttu-id="31de9-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="31de9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="31de9-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="31de9-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="31de9-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="31de9-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="31de9-115">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="31de9-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31de9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31de9-116">See Also</span></span>  
 [<span data-ttu-id="31de9-117">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="31de9-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="31de9-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="31de9-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
