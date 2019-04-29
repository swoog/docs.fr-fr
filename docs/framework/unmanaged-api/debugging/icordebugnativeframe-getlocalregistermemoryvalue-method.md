---
title: ICorDebugNativeFrame::GetLocalRegisterMemoryValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalRegisterMemoryValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalRegisterMemoryValue method [.NET Framework debugging]
- GetLocalRegisterMemoryValue method [.NET Framework debugging]
ms.assetid: d350f69d-9aff-4f5a-8301-daea22dee2da
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 26cd30be591c4167fa6a6e4d19ba9d1c909c6428
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61927307"
---
# <a name="icordebugnativeframegetlocalregistermemoryvalue-method"></a><span data-ttu-id="9b957-102">ICorDebugNativeFrame::GetLocalRegisterMemoryValue, méthode</span><span class="sxs-lookup"><span data-stu-id="9b957-102">ICorDebugNativeFrame::GetLocalRegisterMemoryValue Method</span></span>
<span data-ttu-id="9b957-103">Obtient la valeur d’un argument ou une variable locale, dont le mot de poids faible et fort sont stockés dans l’emplacement de mémoire et le Registre spécifié, respectivement, pour ce frame natif.</span><span class="sxs-lookup"><span data-stu-id="9b957-103">Gets the value of an argument or local variable, of which the low word and high word are stored in the memory location and specified register, respectively, for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b957-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b957-104">Syntax</span></span>  
  
```  
HRESULT GetLocalRegisterMemoryValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CORDB_ADDRESS      lowWordAddress,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9b957-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b957-105">Parameters</span></span>  
 `highWordReg`  
 <span data-ttu-id="9b957-106">[in] Une valeur de l’énumération « CorDebugRegister » qui spécifie le Registre contenant le mot de poids fort de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9b957-106">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the high word of the value.</span></span>  
  
 `lowWordAddress`  
 <span data-ttu-id="9b957-107">[in] Un `CORDB_ADDRESS` valeur qui spécifie l’emplacement de mémoire contenant le mot de poids faible de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9b957-107">[in] A `CORDB_ADDRESS` value that specifies the memory location containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="9b957-108">[in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.</span><span class="sxs-lookup"><span data-stu-id="9b957-108">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="9b957-109">[in] Un `PCCOR_SIGNATURE` valeur pointe vers la signature de métadonnées binaires du type de valeur.</span><span class="sxs-lookup"><span data-stu-id="9b957-109">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="9b957-110">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée qui est stockée dans l’emplacement de Registre et de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="9b957-110">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register and memory location.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b957-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b957-111">Requirements</span></span>  
 <span data-ttu-id="9b957-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b957-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b957-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9b957-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9b957-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9b957-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9b957-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b957-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b957-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b957-116">See also</span></span>
