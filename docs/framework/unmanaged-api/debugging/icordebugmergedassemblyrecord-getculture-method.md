---
title: ICorDebugMergedAssemblyRecord::GetCulture, méthode
ms.date: 03/30/2017
ms.assetid: 030b2f8c-8c21-40b7-855d-3afa78975a17
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f2336c89a32b202c4226f1ed194d786be6fa020
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415355"
---
# <a name="icordebugmergedassemblyrecordgetculture-method"></a><span data-ttu-id="87285-102">ICorDebugMergedAssemblyRecord::GetCulture, méthode</span><span class="sxs-lookup"><span data-stu-id="87285-102">ICorDebugMergedAssemblyRecord::GetCulture Method</span></span>
<span data-ttu-id="87285-103">Obtient la chaîne de nom de culture de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="87285-103">Gets the culture name string of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87285-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87285-104">Syntax</span></span>  
  
```  
HRESULT GetCulture(  
   [in] ULONG32 cchCulture,   
   [out] ULONG32 *pcchCulture,   
   [out, size_is(cchCulture), length_is(*pcchCulture)] WCHAR szCulture[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="87285-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87285-105">Parameters</span></span>  
 `cchCulture`  
 <span data-ttu-id="87285-106">[in] Nombre de caractères dans la mémoire tampon `szCulture`.</span><span class="sxs-lookup"><span data-stu-id="87285-106">[in] The number of characters in the `szCulture` buffer.</span></span>  
  
 `pcchCulture`  
 <span data-ttu-id="87285-107">[out] Nombre de caractères réellement écrits dans le tampon `szCulture`.</span><span class="sxs-lookup"><span data-stu-id="87285-107">[out] The number of characters actually written to the `szCulture` buffer.</span></span>  
  
 `szCulture`  
 <span data-ttu-id="87285-108">[out] Tableau de caractères qui contient le nom de culture.</span><span class="sxs-lookup"><span data-stu-id="87285-108">[out] A character array that contains the culture name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="87285-109">Notes</span><span class="sxs-lookup"><span data-stu-id="87285-109">Remarks</span></span>  
 <span data-ttu-id="87285-110">Le nom de culture est une chaîne unique qui identifie une culture, telle que « en-US » (pour la culture Anglais (États-Unis)) ou « neutre » (pour une culture neutre).</span><span class="sxs-lookup"><span data-stu-id="87285-110">The culture name is a unique string that identifies a culture, such as "en-US" (for the English (United States) culture), or "neutral" (for a neutral culture).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="87285-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="87285-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87285-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="87285-112">Requirements</span></span>  
 <span data-ttu-id="87285-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="87285-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87285-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="87285-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="87285-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="87285-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="87285-116">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="87285-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87285-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87285-117">See Also</span></span>  
 [<span data-ttu-id="87285-118">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="87285-118">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)  
 [<span data-ttu-id="87285-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="87285-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
