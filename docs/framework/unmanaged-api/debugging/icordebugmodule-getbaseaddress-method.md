---
title: ICorDebugModule::GetBaseAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetBaseAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetBaseAddress
helpviewer_keywords:
- GetBaseAddress method [.NET Framework debugging]
- ICorDebugModule::GetBaseAddress method [.NET Framework debugging]
ms.assetid: 26a82815-1982-4eb7-92d1-5c3d318d5be4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 763f2872099fac87138b7e1ab058c60475892b0c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59107417"
---
# <a name="icordebugmodulegetbaseaddress-method"></a><span data-ttu-id="13472-102">ICorDebugModule::GetBaseAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="13472-102">ICorDebugModule::GetBaseAddress Method</span></span>
<span data-ttu-id="13472-103">Obtient l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="13472-103">Gets the base address of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13472-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13472-104">Syntax</span></span>  
  
```  
HRESULT GetBaseAddress(  
    [out] CORDB_ADDRESS *pAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13472-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13472-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="13472-106">[out] Un `CORDB_ADDRESS` qui spécifie l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="13472-106">[out] A `CORDB_ADDRESS` that specifies the base address of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="13472-107">Notes</span><span class="sxs-lookup"><span data-stu-id="13472-107">Remarks</span></span>  
 <span data-ttu-id="13472-108">Si le module est natif de l’image (autrement dit, si le module a été généré par le Générateur d’images natives, NGen.exe), son adresse de base sera égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="13472-108">If the module is a native image (that is, if the module was produced by the native image generator, NGen.exe), its base address will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13472-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13472-109">Requirements</span></span>  
 <span data-ttu-id="13472-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="13472-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13472-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="13472-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="13472-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13472-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="13472-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="13472-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="13472-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13472-114">See also</span></span>
