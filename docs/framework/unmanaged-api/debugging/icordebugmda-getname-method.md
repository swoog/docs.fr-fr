---
title: ICorDebugMDA::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetName
helpviewer_keywords:
- ICorDebugMDA::GetName method [.NET Framework debugging]
- GetName method, ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 885bf5e8-00b7-4cd7-9d8d-e720d47918c4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5f62fa23d30a93f863cb2be0fa060bd2eba8dca1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59141729"
---
# <a name="icordebugmdagetname-method"></a><span data-ttu-id="42b8c-102">ICorDebugMDA::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="42b8c-102">ICorDebugMDA::GetName Method</span></span>
<span data-ttu-id="42b8c-103">Obtient une chaîne contenant le nom de l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span><span class="sxs-lookup"><span data-stu-id="42b8c-103">Gets a string containing the name of the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42b8c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42b8c-104">Syntax</span></span>  
  
```  
HRESULT GetName (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="42b8c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42b8c-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="42b8c-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="42b8c-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="42b8c-107">[out] Pointeur vers la longueur du nom.</span><span class="sxs-lookup"><span data-stu-id="42b8c-107">[out] A pointer to the length of the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="42b8c-108">[out] Tableau dans lequel stocker le nom.</span><span class="sxs-lookup"><span data-stu-id="42b8c-108">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="42b8c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="42b8c-109">Remarks</span></span>  
 <span data-ttu-id="42b8c-110">Noms de l’Assistant Débogage MANAGÉ sont des valeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="42b8c-110">MDA names are unique values.</span></span> <span data-ttu-id="42b8c-111">Le `GetName` méthode constitue une alternative de performance appropriée pour obtenir le flux XML et extraire le nom à partir du flux en fonction du schéma.</span><span class="sxs-lookup"><span data-stu-id="42b8c-111">The `GetName` method is a convenient performance alternative to getting the XML stream and extracting the name from the stream based on the schema.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="42b8c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42b8c-112">Requirements</span></span>  
 <span data-ttu-id="42b8c-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="42b8c-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42b8c-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="42b8c-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="42b8c-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="42b8c-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="42b8c-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="42b8c-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="42b8c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42b8c-117">See also</span></span>

- [<span data-ttu-id="42b8c-118">ICorDebugMDA, interface</span><span class="sxs-lookup"><span data-stu-id="42b8c-118">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [<span data-ttu-id="42b8c-119">Diagnostic d'erreurs avec les Assistants de débogage managés</span><span class="sxs-lookup"><span data-stu-id="42b8c-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
