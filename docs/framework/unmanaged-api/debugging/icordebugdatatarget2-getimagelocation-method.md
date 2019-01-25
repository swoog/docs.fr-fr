---
title: ICorDebugDataTarget2::GetImageLocation, méthode
ms.date: 03/30/2017
ms.assetid: 696afe71-5852-478d-a33f-b2d2dbc4b91f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3b2d6db83f78cb76181c0b54a8e6f4157e51130b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648834"
---
# <a name="icordebugdatatarget2getimagelocation-method"></a><span data-ttu-id="db806-102">ICorDebugDataTarget2::GetImageLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="db806-102">ICorDebugDataTarget2::GetImageLocation Method</span></span>
<span data-ttu-id="db806-103">Retourne le chemin d’accès d’un module à partir de l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="db806-103">Returns the path of a module from the module's base address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db806-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db806-104">Syntax</span></span>  
  
```  
HRESULT GetImageLocation(    [in] CORDB_ADDRESS baseAddress,  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="db806-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db806-105">Parameters</span></span>  
 `baseAddress`  
 <span data-ttu-id="db806-106">[in] Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="db806-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `cchName`  
 <span data-ttu-id="db806-107">[in] Nombre de caractères dans la mémoire tampon qui reçoit le chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="db806-107">[in] The number of characters in the buffer that is to receive the module path.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="db806-108">[out] Pointeur vers le nombre de caractères écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="db806-108">[out] A pointer to the number of characters written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="db806-109">[out] Chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="db806-109">[out] The path of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="db806-110">Notes</span><span class="sxs-lookup"><span data-stu-id="db806-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="db806-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="db806-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db806-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db806-112">Requirements</span></span>  
 <span data-ttu-id="db806-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="db806-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="db806-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="db806-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="db806-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="db806-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="db806-116">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="db806-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db806-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db806-117">See also</span></span>
- [<span data-ttu-id="db806-118">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="db806-118">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [<span data-ttu-id="db806-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="db806-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
