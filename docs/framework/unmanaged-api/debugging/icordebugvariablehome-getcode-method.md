---
title: ICorDebugVariableHome::GetCode (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetCode
helpviewer_keywords:
- ICorDebugVariableHome::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: ef002890-4a7b-4a5d-abbf-16c60083f794
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a4cadae7a43d0cd965e51535eae2c95e59900d0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59130011"
---
# <a name="icordebugvariablehomegetcode-method"></a><span data-ttu-id="41eeb-102">ICorDebugVariableHome::GetCode (méthode)</span><span class="sxs-lookup"><span data-stu-id="41eeb-102">ICorDebugVariableHome::GetCode Method</span></span>
<span data-ttu-id="41eeb-103">Obtient l’instance « ICorDebugCode » qui contient ce [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="41eeb-103">Gets the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41eeb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41eeb-104">Syntax</span></span>  
  
```  
HRESULT GetCode(  
    [out] ICorDebugCode **ppCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="41eeb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41eeb-105">Parameters</span></span>  
 `ppCode`  
 <span data-ttu-id="41eeb-106">[out] Un pointeur vers l’adresse de l’instance « ICorDebugCode » qui contient ce [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="41eeb-106">[out] A pointer to the address of the "ICorDebugCode" instance that contains this [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41eeb-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41eeb-107">Requirements</span></span>  
 <span data-ttu-id="41eeb-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41eeb-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41eeb-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="41eeb-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="41eeb-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="41eeb-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="41eeb-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="41eeb-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="41eeb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41eeb-112">See also</span></span>

- [<span data-ttu-id="41eeb-113">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="41eeb-113">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
