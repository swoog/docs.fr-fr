---
title: ICorDebugVariableHome::GetOffset (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetOffset
helpviewer_keywords:
- ICorDebugVariableHome::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: f025c2e5-3f6c-4be8-9ffe-c8b214617dfe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 864cb893511bceabd61ce0064065b3866ce01dfe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212594"
---
# <a name="icordebugvariablehomegetoffset-method"></a><span data-ttu-id="69c26-102">ICorDebugVariableHome::GetOffset (méthode)</span><span class="sxs-lookup"><span data-stu-id="69c26-102">ICorDebugVariableHome::GetOffset Method</span></span>
<span data-ttu-id="69c26-103">Obtient le décalage à partir du Registre de base pour une variable.</span><span class="sxs-lookup"><span data-stu-id="69c26-103">Gets the offset from the base register for a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69c26-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69c26-104">Syntax</span></span>  
  
```  
HRESULT GetOffset(  
    [out] LONG *pOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="69c26-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69c26-105">Parameters</span></span>  
 `pOffset`  
 <span data-ttu-id="69c26-106">[out] Le décalage à partir du Registre de base.</span><span class="sxs-lookup"><span data-stu-id="69c26-106">[out] The offset from the base register.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="69c26-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="69c26-107">Return Value</span></span>  
 <span data-ttu-id="69c26-108">La méthode retourne les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="69c26-108">The method returns the following values:</span></span>  
  
|<span data-ttu-id="69c26-109">Value</span><span class="sxs-lookup"><span data-stu-id="69c26-109">Value</span></span>|<span data-ttu-id="69c26-110">Description</span><span class="sxs-lookup"><span data-stu-id="69c26-110">Description</span></span>|  
|-----------|-----------------|  
|`S_OK`|<span data-ttu-id="69c26-111">La variable est dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="69c26-111">The variable is in a register-relative memory location.</span></span>|  
|`E_FAIL`|<span data-ttu-id="69c26-112">La variable n’est pas dans un emplacement de mémoire relative au Registre.</span><span class="sxs-lookup"><span data-stu-id="69c26-112">The variable is not in a register-relative memory location.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="69c26-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69c26-113">Requirements</span></span>  
 <span data-ttu-id="69c26-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="69c26-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="69c26-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="69c26-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="69c26-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="69c26-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="69c26-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="69c26-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="69c26-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69c26-118">See also</span></span>

- [<span data-ttu-id="69c26-119">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="69c26-119">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
