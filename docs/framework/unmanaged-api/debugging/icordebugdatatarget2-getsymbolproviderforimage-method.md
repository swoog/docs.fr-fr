---
title: ICorDebugDataTarget2::GetSymbolProviderForImage, méthode
ms.date: 03/30/2017
ms.assetid: b7c0a2f0-e904-43b3-98e1-d669e8a589e8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1cdd2d0b6f6fbc8d3c2b1a14ca05a84d13c56331
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33411101"
---
# <a name="icordebugdatatarget2getsymbolproviderforimage-method"></a><span data-ttu-id="799c4-102">ICorDebugDataTarget2::GetSymbolProviderForImage, méthode</span><span class="sxs-lookup"><span data-stu-id="799c4-102">ICorDebugDataTarget2::GetSymbolProviderForImage Method</span></span>
<span data-ttu-id="799c4-103">Retourne le fournisseur de symboles d'un module à partir de l'adresse de base de ce module.</span><span class="sxs-lookup"><span data-stu-id="799c4-103">Returns the symbol-provider for a module from the base address of that module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="799c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="799c4-104">Syntax</span></span>  
  
```  
HRESULT GetSymbolProviderForImage(  
    [in] CORDB_ADDRESS imageBaseAddress,   
    [out] ICorDebugSymbolProvider **ppSymProvider  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="799c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="799c4-105">Parameters</span></span>  
 `imageBaseAddress`  
 <span data-ttu-id="799c4-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base d’un module.</span><span class="sxs-lookup"><span data-stu-id="799c4-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents the base address of a module.</span></span>  
  
 `ppSymProvider`  
 <span data-ttu-id="799c4-107">[out] Un pointeur vers l’adresse d’un [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="799c4-107">[out] A pointer to the address of an [ICorDebugSymbolProvider](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md) object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="799c4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="799c4-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="799c4-109">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="799c4-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="799c4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="799c4-110">Requirements</span></span>  
 <span data-ttu-id="799c4-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="799c4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="799c4-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="799c4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="799c4-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="799c4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="799c4-114">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="799c4-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="799c4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="799c4-115">See Also</span></span>  
 [<span data-ttu-id="799c4-116">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="799c4-116">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)  
 [<span data-ttu-id="799c4-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="799c4-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
