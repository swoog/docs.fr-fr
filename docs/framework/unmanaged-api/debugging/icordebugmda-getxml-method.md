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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59228820"
---
# <a name="icordebugmdagetxml-method"></a><span data-ttu-id="f032b-102">ICorDebugMDA::GetXML, méthode</span><span class="sxs-lookup"><span data-stu-id="f032b-102">ICorDebugMDA::GetXML Method</span></span>
<span data-ttu-id="f032b-103">Obtient le flux XML complet associé à l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f032b-103">Gets the full XML stream associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f032b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f032b-104">Syntax</span></span>  
  
```  
HRESULT GetXML (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f032b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f032b-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="f032b-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="f032b-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="f032b-107">[out] Pointeur vers la longueur du flux XML.</span><span class="sxs-lookup"><span data-stu-id="f032b-107">[out] A pointer to the length of the XML stream.</span></span>  
  
 `szName`  
 <span data-ttu-id="f032b-108">[out] Tableau dans lequel stocker le flux XML.</span><span class="sxs-lookup"><span data-stu-id="f032b-108">[out] An array in which to store the XML stream.</span></span> <span data-ttu-id="f032b-109">Le tableau peut être vide.</span><span class="sxs-lookup"><span data-stu-id="f032b-109">The array may be empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f032b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f032b-110">Remarks</span></span>  
 <span data-ttu-id="f032b-111">Le `GetXML` méthode peut affecter potentiellement les performances, selon la taille du flux XML associé.</span><span class="sxs-lookup"><span data-stu-id="f032b-111">The `GetXML` method can potentially affect performance, depending on the size of the associated XML stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f032b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f032b-112">Requirements</span></span>  
 <span data-ttu-id="f032b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f032b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f032b-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f032b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f032b-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f032b-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="f032b-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f032b-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f032b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f032b-117">See also</span></span>

- [<span data-ttu-id="f032b-118">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="f032b-118">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [<span data-ttu-id="f032b-119">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="f032b-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
