---
title: ICorDebugAssembly::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetName
helpviewer_keywords:
- ICorDebugAssembly::GetName method [.NET Framework debugging]
- GetName method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: cdeda721-b214-4503-a291-c70b68b5f36b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fe587f6356eec861c39c9eb0aa0b6476e0b9a232
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33407517"
---
# <a name="icordebugassemblygetname-method"></a><span data-ttu-id="45b5c-102">ICorDebugAssembly::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="45b5c-102">ICorDebugAssembly::GetName Method</span></span>
<span data-ttu-id="45b5c-103">Obtient le nom de l’assembly que cela `ICorDebugAssembly` représente l’instance.</span><span class="sxs-lookup"><span data-stu-id="45b5c-103">Gets the name of the assembly that this `ICorDebugAssembly` instance represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45b5c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45b5c-104">Syntax</span></span>  
  
```  
HRESULT GetName (  
    [in] ULONG32  cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="45b5c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45b5c-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="45b5c-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="45b5c-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="45b5c-107">[out] Pointeur vers un entier qui spécifie la longueur réelle du nom.</span><span class="sxs-lookup"><span data-stu-id="45b5c-107">[out] A pointer to an integer that specifies the actual length of the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="45b5c-108">[out] Tableau qui stocke le nom.</span><span class="sxs-lookup"><span data-stu-id="45b5c-108">[out] An array that stores the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="45b5c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="45b5c-109">Remarks</span></span>  
 <span data-ttu-id="45b5c-110">Le `GetName` méthode retourne le chemin d’accès et le nom complet de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="45b5c-110">The `GetName` method returns the full path and file name of the assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45b5c-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="45b5c-111">Requirements</span></span>  
 <span data-ttu-id="45b5c-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="45b5c-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45b5c-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="45b5c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="45b5c-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45b5c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45b5c-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45b5c-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
