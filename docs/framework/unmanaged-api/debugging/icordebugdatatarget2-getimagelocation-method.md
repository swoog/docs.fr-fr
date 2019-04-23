---
title: ICorDebugDataTarget2::GetImageLocation, méthode
ms.date: 03/30/2017
ms.assetid: 696afe71-5852-478d-a33f-b2d2dbc4b91f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c7acf08262c73df00a96cfb5c244cdfc352e51ea
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080474"
---
# <a name="icordebugdatatarget2getimagelocation-method"></a><span data-ttu-id="e6dfa-102">ICorDebugDataTarget2::GetImageLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="e6dfa-102">ICorDebugDataTarget2::GetImageLocation Method</span></span>
<span data-ttu-id="e6dfa-103">Retourne le chemin d’accès d’un module à partir de l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-103">Returns the path of a module from the module's base address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6dfa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6dfa-104">Syntax</span></span>  
  
```  
HRESULT GetImageLocation(    [in] CORDB_ADDRESS baseAddress,  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6dfa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6dfa-105">Parameters</span></span>  
 `baseAddress`  
 <span data-ttu-id="e6dfa-106">[in] Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `cchName`  
 <span data-ttu-id="e6dfa-107">[in] Nombre de caractères dans la mémoire tampon qui reçoit le chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-107">[in] The number of characters in the buffer that is to receive the module path.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="e6dfa-108">[out] Pointeur vers le nombre de caractères écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-108">[out] A pointer to the number of characters written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="e6dfa-109">[out] Chemin d'accès du module.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-109">[out] The path of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6dfa-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e6dfa-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e6dfa-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6dfa-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6dfa-112">Requirements</span></span>  
 <span data-ttu-id="e6dfa-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e6dfa-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6dfa-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e6dfa-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e6dfa-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6dfa-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6dfa-116">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6dfa-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6dfa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6dfa-117">See also</span></span>

- [<span data-ttu-id="e6dfa-118">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="e6dfa-118">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [<span data-ttu-id="e6dfa-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e6dfa-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
