---
title: ICorDebugDataTarget2::GetImageLocation, méthode
ms.date: 03/30/2017
ms.assetid: 696afe71-5852-478d-a33f-b2d2dbc4b91f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c6962c8063479b3b0279d771b1b0cd1df63f696b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416414"
---
# <a name="icordebugdatatarget2getimagelocation-method"></a><span data-ttu-id="18f2f-102">ICorDebugDataTarget2::GetImageLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="18f2f-102">ICorDebugDataTarget2::GetImageLocation Method</span></span>
<span data-ttu-id="18f2f-103">Retourne le chemin d’accès d’un module à partir de l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="18f2f-103">Returns the path of a module from the module's base address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18f2f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18f2f-104">Syntax</span></span>  
  
```  
HRESULT GetImageLocation(    [in] CORDB_ADDRESS baseAddress,  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="18f2f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18f2f-105">Parameters</span></span>  
 `baseAddress`  
 <span data-ttu-id="18f2f-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="18f2f-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `cchName`  
 <span data-ttu-id="18f2f-107">[in] Nombre de caractères dans la mémoire tampon qui reçoit le chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="18f2f-107">[in] The number of characters in the buffer that is to receive the module path.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="18f2f-108">[out] Pointeur vers le nombre de caractères écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="18f2f-108">[out] A pointer to the number of characters written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="18f2f-109">[out] Chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="18f2f-109">[out] The path of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="18f2f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="18f2f-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="18f2f-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="18f2f-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18f2f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="18f2f-112">Requirements</span></span>  
 <span data-ttu-id="18f2f-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="18f2f-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18f2f-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="18f2f-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="18f2f-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18f2f-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18f2f-116">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18f2f-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18f2f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f2f-117">See Also</span></span>  
 [<span data-ttu-id="18f2f-118">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="18f2f-118">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)  
 [<span data-ttu-id="18f2f-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="18f2f-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
