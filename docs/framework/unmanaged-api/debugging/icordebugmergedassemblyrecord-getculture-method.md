---
title: Icordebugmergedassemblyrecord::getculture, méthode
ms.date: 03/30/2017
ms.assetid: 030b2f8c-8c21-40b7-855d-3afa78975a17
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 093b21a439b96c9fe2f971300f314d1b75527f1f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207199"
---
# <a name="icordebugmergedassemblyrecordgetculture-method"></a><span data-ttu-id="e6cc5-102">Icordebugmergedassemblyrecord::getculture, méthode</span><span class="sxs-lookup"><span data-stu-id="e6cc5-102">ICorDebugMergedAssemblyRecord::GetCulture Method</span></span>
<span data-ttu-id="e6cc5-103">Obtient la chaîne de nom de culture de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e6cc5-103">Gets the culture name string of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6cc5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6cc5-104">Syntax</span></span>  
  
```  
HRESULT GetCulture(  
   [in] ULONG32 cchCulture,   
   [out] ULONG32 *pcchCulture,   
   [out, size_is(cchCulture), length_is(*pcchCulture)] WCHAR szCulture[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6cc5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6cc5-105">Parameters</span></span>  
 `cchCulture`  
 <span data-ttu-id="e6cc5-106">[in] Nombre de caractères dans la mémoire tampon `szCulture`.</span><span class="sxs-lookup"><span data-stu-id="e6cc5-106">[in] The number of characters in the `szCulture` buffer.</span></span>  
  
 `pcchCulture`  
 <span data-ttu-id="e6cc5-107">[out] Nombre de caractères réellement écrits dans le tampon `szCulture`.</span><span class="sxs-lookup"><span data-stu-id="e6cc5-107">[out] The number of characters actually written to the `szCulture` buffer.</span></span>  
  
 `szCulture`  
 <span data-ttu-id="e6cc5-108">[out] Tableau de caractères qui contient le nom de culture.</span><span class="sxs-lookup"><span data-stu-id="e6cc5-108">[out] A character array that contains the culture name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e6cc5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e6cc5-109">Remarks</span></span>  
 <span data-ttu-id="e6cc5-110">Le nom de culture est une chaîne unique qui identifie une culture, telle que « en-US » (pour la culture Anglais (États-Unis)) ou « neutre » (pour une culture neutre).</span><span class="sxs-lookup"><span data-stu-id="e6cc5-110">The culture name is a unique string that identifies a culture, such as "en-US" (for the English (United States) culture), or "neutral" (for a neutral culture).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e6cc5-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="e6cc5-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6cc5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6cc5-112">Requirements</span></span>  
 <span data-ttu-id="e6cc5-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e6cc5-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6cc5-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e6cc5-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e6cc5-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6cc5-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="e6cc5-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="e6cc5-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e6cc5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6cc5-117">See also</span></span>

- [<span data-ttu-id="e6cc5-118">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="e6cc5-118">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="e6cc5-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e6cc5-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
