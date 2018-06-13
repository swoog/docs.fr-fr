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
ms.openlocfilehash: 2fdace527194228dd6004a991950a80d23275650
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413294"
---
# <a name="icordebugmdagetdescription-method"></a><span data-ttu-id="dad06-102">ICorDebugMDA::GetDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="dad06-102">ICorDebugMDA::GetDescription Method</span></span>
<span data-ttu-id="dad06-103">Obtient une chaîne qui contient la description de l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="dad06-103">Gets a string containing the description of the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dad06-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dad06-104">Syntax</span></span>  
  
```  
HRESULT GetDescription (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dad06-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dad06-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="dad06-106">[in] La taille de la mémoire tampon de chaîne qui stockera la description.</span><span class="sxs-lookup"><span data-stu-id="dad06-106">[in] The size of the string buffer that will store the description.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="dad06-107">[out] Pointeur vers le nombre d’octets retournés dans la mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="dad06-107">[out] A pointer to the number of bytes returned in the string buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="dad06-108">[out] Une mémoire tampon de chaîne qui contient la description de l’Assistant Débogage MANAGÉ.</span><span class="sxs-lookup"><span data-stu-id="dad06-108">[out] A string buffer containing the description of the MDA.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dad06-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dad06-109">Remarks</span></span>  
 <span data-ttu-id="dad06-110">La chaîne peut être de longueur zéro.</span><span class="sxs-lookup"><span data-stu-id="dad06-110">The string can be zero in length.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dad06-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dad06-111">Requirements</span></span>  
 <span data-ttu-id="dad06-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dad06-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dad06-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dad06-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dad06-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dad06-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dad06-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dad06-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dad06-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad06-116">See Also</span></span>  
 [<span data-ttu-id="dad06-117">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="dad06-117">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)  
 [<span data-ttu-id="dad06-118">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="dad06-118">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
