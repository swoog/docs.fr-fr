---
title: ICorDebugMDA::GetDescription, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetDescription
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetDescription
helpviewer_keywords:
- GetDescription method [.NET Framework debugging]
- ICorDebugMDA::GetDescription method [.NET Framework debugging]
ms.assetid: 01d1b481-ca67-4712-8744-d342ec0df639
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 998d4baf03123f1ffc174b2a7aeed0ff4a25b001
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133475"
---
# <a name="icordebugmdagetdescription-method"></a><span data-ttu-id="09559-102">ICorDebugMDA::GetDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="09559-102">ICorDebugMDA::GetDescription Method</span></span>
<span data-ttu-id="09559-103">Obtient une chaîne qui contient la description de l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="09559-103">Gets a string containing the description of the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09559-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09559-104">Syntax</span></span>  
  
```  
HRESULT GetDescription (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="09559-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09559-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="09559-106">[in] La taille de la mémoire tampon de chaîne qui stockera la description.</span><span class="sxs-lookup"><span data-stu-id="09559-106">[in] The size of the string buffer that will store the description.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="09559-107">[out] Pointeur vers le nombre d’octets retournés dans la mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="09559-107">[out] A pointer to the number of bytes returned in the string buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="09559-108">[out] Un mémoire tampon de chaîne qui contient la description de l’Assistant Débogage MANAGÉ.</span><span class="sxs-lookup"><span data-stu-id="09559-108">[out] A string buffer containing the description of the MDA.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="09559-109">Notes</span><span class="sxs-lookup"><span data-stu-id="09559-109">Remarks</span></span>  
 <span data-ttu-id="09559-110">La chaîne peut être de longueur zéro.</span><span class="sxs-lookup"><span data-stu-id="09559-110">The string can be zero in length.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09559-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09559-111">Requirements</span></span>  
 <span data-ttu-id="09559-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="09559-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09559-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="09559-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="09559-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="09559-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="09559-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="09559-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="09559-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09559-116">See also</span></span>

- [<span data-ttu-id="09559-117">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="09559-117">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [<span data-ttu-id="09559-118">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="09559-118">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
