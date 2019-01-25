---
title: ICorDebugNativeFrame::GetLocalMemoryValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalMemoryValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalMemoryValue
helpviewer_keywords:
- GetLocalMemoryValue method [.NET Framework debugging]
- ICorDebugNativeFrame::GetLocalMemoryValue method [.NET Framework debugging]
ms.assetid: b600b3a2-9908-42d8-8093-ab6f39e9a2c9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e8d0c16000c78fab0371b68c3a350bd2018aa1c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54664523"
---
# <a name="icordebugnativeframegetlocalmemoryvalue-method"></a><span data-ttu-id="ca11c-102">ICorDebugNativeFrame::GetLocalMemoryValue, méthode</span><span class="sxs-lookup"><span data-stu-id="ca11c-102">ICorDebugNativeFrame::GetLocalMemoryValue Method</span></span>
<span data-ttu-id="ca11c-103">Obtient la valeur d’un argument ou une variable locale qui est stocké dans l’emplacement de mémoire spécifié pour ce frame natif.</span><span class="sxs-lookup"><span data-stu-id="ca11c-103">Gets the value of an argument or local variable that is stored in the specified memory location for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca11c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca11c-104">Syntax</span></span>  
  
```  
HRESULT GetLocalMemoryValue (  
    [in]  CORDB_ADDRESS      address,  
    [in]  ULONG              cbSigBlob,  
    [in]  PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca11c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca11c-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="ca11c-106">[in] Un `CORDB_ADDRESS` valeur qui spécifie l’emplacement de mémoire qui contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="ca11c-106">[in] A `CORDB_ADDRESS` value that specifies the memory location containing the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="ca11c-107">[in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca11c-107">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="ca11c-108">[in] Un `PCCOR_SIGNATURE` valeur pointe vers la signature de métadonnées binaires du type de valeur.</span><span class="sxs-lookup"><span data-stu-id="ca11c-108">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="ca11c-109">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée qui est stockée dans l’emplacement de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="ca11c-109">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified memory location.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca11c-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca11c-110">Requirements</span></span>  
 <span data-ttu-id="ca11c-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca11c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca11c-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ca11c-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ca11c-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca11c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca11c-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca11c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca11c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca11c-115">See also</span></span>

