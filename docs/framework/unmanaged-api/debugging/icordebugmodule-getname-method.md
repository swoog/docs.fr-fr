---
title: ICorDebugModule::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetName
helpviewer_keywords:
- ICorDebugModule::GetName method [.NET Framework debugging]
- GetName method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: db499637-7ba9-421e-b8b1-35856995e80b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: efbcd6f9eca426cd230653e38d527e184b378fa0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57503149"
---
# <a name="icordebugmodulegetname-method"></a><span data-ttu-id="883d7-102">ICorDebugModule::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="883d7-102">ICorDebugModule::GetName Method</span></span>
<span data-ttu-id="883d7-103">Obtient le nom de fichier du module.</span><span class="sxs-lookup"><span data-stu-id="883d7-103">Gets the file name of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="883d7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="883d7-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="883d7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="883d7-105">Parameters</span></span>  
 `cchname`  
 <span data-ttu-id="883d7-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="883d7-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="883d7-107">[in] Pointeur vers la longueur du nom retourné.</span><span class="sxs-lookup"><span data-stu-id="883d7-107">[in] A pointer to the length of the returned name.</span></span>  
  
 `szName`  
 <span data-ttu-id="883d7-108">[out] Tableau qui stocke le nom retourné.</span><span class="sxs-lookup"><span data-stu-id="883d7-108">[out] An array that stores the returned name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="883d7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="883d7-109">Remarks</span></span>  
 <span data-ttu-id="883d7-110">Le `GetName` méthode retourne une valeur S_OK HRESULT si le nom de fichier du module correspond au nom sur le disque.</span><span class="sxs-lookup"><span data-stu-id="883d7-110">The `GetName` method returns an S_OK HRESULT if the module's file name matches the name on disk.</span></span> <span data-ttu-id="883d7-111">`GetName` Retourne une valeur HRESULT S_FALSE si le nom est créé, comme pour un module dynamique ou en mémoire.</span><span class="sxs-lookup"><span data-stu-id="883d7-111">`GetName` returns an S_FALSE HRESULT if the name is fabricated, such as for a dynamic or in-memory module.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="883d7-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="883d7-112">Requirements</span></span>  
 <span data-ttu-id="883d7-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="883d7-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="883d7-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="883d7-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="883d7-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="883d7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="883d7-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="883d7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="883d7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="883d7-117">See also</span></span>


