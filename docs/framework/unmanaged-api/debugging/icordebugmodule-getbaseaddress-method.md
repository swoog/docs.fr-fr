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
ms.openlocfilehash: 10e7da7711cd63579589fda416d0d3a4f777eefe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412538"
---
# <a name="icordebugmodulegetbaseaddress-method"></a><span data-ttu-id="39b44-102">ICorDebugModule::GetBaseAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="39b44-102">ICorDebugModule::GetBaseAddress Method</span></span>
<span data-ttu-id="39b44-103">Obtient l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="39b44-103">Gets the base address of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39b44-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39b44-104">Syntax</span></span>  
  
```  
HRESULT GetBaseAddress(  
    [out] CORDB_ADDRESS *pAddress  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="39b44-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39b44-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="39b44-106">[out] Un `CORDB_ADDRESS` qui spécifie l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="39b44-106">[out] A `CORDB_ADDRESS` that specifies the base address of the module.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="39b44-107">Notes</span><span class="sxs-lookup"><span data-stu-id="39b44-107">Remarks</span></span>  
 <span data-ttu-id="39b44-108">Si le module est natif de l’image (autrement dit, si le module a été généré par le Générateur d’images natives, NGen.exe), son adresse de base est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="39b44-108">If the module is a native image (that is, if the module was produced by the native image generator, NGen.exe), its base address will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39b44-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="39b44-109">Requirements</span></span>  
 <span data-ttu-id="39b44-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="39b44-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39b44-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="39b44-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="39b44-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="39b44-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="39b44-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39b44-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39b44-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b44-114">See Also</span></span>  
    
 
