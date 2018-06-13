---
title: ICorDebugMDA::GetXML, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetXML
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetXML
helpviewer_keywords:
- ICorDebugMDA::GetXML method [.NET Framework debugging]
- GetXML method [.NET Framework debugging]
ms.assetid: 29746b24-3766-4255-8813-0426c45e73e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 874462e37aa10af589f39ed099de899ff7155d24
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33414643"
---
# <a name="icordebugmdagetxml-method"></a><span data-ttu-id="77c00-102">ICorDebugMDA::GetXML, méthode</span><span class="sxs-lookup"><span data-stu-id="77c00-102">ICorDebugMDA::GetXML Method</span></span>
<span data-ttu-id="77c00-103">Obtient le flux XML complet associé à l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="77c00-103">Gets the full XML stream associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77c00-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77c00-104">Syntax</span></span>  
  
```  
HRESULT GetXML (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="77c00-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77c00-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="77c00-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="77c00-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="77c00-107">[out] Pointeur vers la longueur du flux XML.</span><span class="sxs-lookup"><span data-stu-id="77c00-107">[out] A pointer to the length of the XML stream.</span></span>  
  
 `szName`  
 <span data-ttu-id="77c00-108">[out] Tableau dans lequel stocker le flux XML.</span><span class="sxs-lookup"><span data-stu-id="77c00-108">[out] An array in which to store the XML stream.</span></span> <span data-ttu-id="77c00-109">Le tableau peut être vide.</span><span class="sxs-lookup"><span data-stu-id="77c00-109">The array may be empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="77c00-110">Notes</span><span class="sxs-lookup"><span data-stu-id="77c00-110">Remarks</span></span>  
 <span data-ttu-id="77c00-111">Le `GetXML` méthode peut éventuellement affecter les performances, selon la taille du flux XML associé.</span><span class="sxs-lookup"><span data-stu-id="77c00-111">The `GetXML` method can potentially affect performance, depending on the size of the associated XML stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77c00-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77c00-112">Requirements</span></span>  
 <span data-ttu-id="77c00-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77c00-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77c00-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="77c00-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="77c00-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="77c00-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="77c00-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="77c00-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77c00-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77c00-117">See Also</span></span>  
 [<span data-ttu-id="77c00-118">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="77c00-118">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)  
 [<span data-ttu-id="77c00-119">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="77c00-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
