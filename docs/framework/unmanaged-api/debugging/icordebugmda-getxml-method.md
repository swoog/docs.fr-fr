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
ms.openlocfilehash: 4e78b8a2069671d0fe790956ca914225325a78bc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228820"
---
# <a name="icordebugmdagetxml-method"></a><span data-ttu-id="38e26-102">ICorDebugMDA::GetXML, méthode</span><span class="sxs-lookup"><span data-stu-id="38e26-102">ICorDebugMDA::GetXML Method</span></span>
<span data-ttu-id="38e26-103">Obtient le flux XML complet associé à l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="38e26-103">Gets the full XML stream associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38e26-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38e26-104">Syntax</span></span>  
  
```  
HRESULT GetXML (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38e26-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38e26-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="38e26-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="38e26-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="38e26-107">[out] Pointeur vers la longueur du flux XML.</span><span class="sxs-lookup"><span data-stu-id="38e26-107">[out] A pointer to the length of the XML stream.</span></span>  
  
 `szName`  
 <span data-ttu-id="38e26-108">[out] Tableau dans lequel stocker le flux XML.</span><span class="sxs-lookup"><span data-stu-id="38e26-108">[out] An array in which to store the XML stream.</span></span> <span data-ttu-id="38e26-109">Le tableau peut être vide.</span><span class="sxs-lookup"><span data-stu-id="38e26-109">The array may be empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="38e26-110">Notes</span><span class="sxs-lookup"><span data-stu-id="38e26-110">Remarks</span></span>  
 <span data-ttu-id="38e26-111">Le `GetXML` méthode peut affecter potentiellement les performances, selon la taille du flux XML associé.</span><span class="sxs-lookup"><span data-stu-id="38e26-111">The `GetXML` method can potentially affect performance, depending on the size of the associated XML stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38e26-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38e26-112">Requirements</span></span>  
 <span data-ttu-id="38e26-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="38e26-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38e26-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="38e26-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="38e26-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="38e26-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="38e26-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38e26-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38e26-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e26-117">See also</span></span>

- [<span data-ttu-id="38e26-118">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="38e26-118">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [<span data-ttu-id="38e26-119">Diagnostic d’erreurs avec les Assistants Débogage managé</span><span class="sxs-lookup"><span data-stu-id="38e26-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
