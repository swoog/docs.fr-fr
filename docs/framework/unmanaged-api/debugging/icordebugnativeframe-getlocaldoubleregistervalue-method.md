---
title: ICorDebugNativeFrame::GetLocalDoubleRegisterValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalDoubleRegisterValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalDoubleRegisterValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalDoubleRegisterValue method [.NET Framework debugging]
- GetLocalDoubleRegisterValue method [.NET Framework debugging]
ms.assetid: 1f838215-ac8a-434f-8ce6-03021d3098d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 13e1e3369c4e7a185c2167facc8514b5cfc85a85
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994693"
---
# <a name="icordebugnativeframegetlocaldoubleregistervalue-method"></a><span data-ttu-id="0b2ae-102">ICorDebugNativeFrame::GetLocalDoubleRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="0b2ae-102">ICorDebugNativeFrame::GetLocalDoubleRegisterValue Method</span></span>
<span data-ttu-id="0b2ae-103">Obtient la valeur d’un argument ou une variable locale qui est stockée dans deux registres spécifiés pour ce frame natif.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-103">Gets the value of an argument or local variable that is stored in the two specified registers for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b2ae-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b2ae-104">Syntax</span></span>  
  
```  
HRESULT GetLocalDoubleRegisterValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CorDebugRegister   lowWordReg,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0b2ae-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b2ae-105">Parameters</span></span>  
 `highWordReg`  
 <span data-ttu-id="0b2ae-106">[in] Une valeur de l’énumération « CorDebugRegister » qui spécifie le Registre contenant le mot de poids fort de la valeur.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-106">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the high word of the value.</span></span>  
  
 `lowWordReg`  
 <span data-ttu-id="0b2ae-107">[in] Une valeur de la `CorDebugRegister` énumération qui spécifie le Registre contenant le mot de poids faible de la valeur.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-107">[in] A value of the `CorDebugRegister` enumeration that specifies the register containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="0b2ae-108">[in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-108">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="0b2ae-109">[in] Un `PCCOR_SIGNATURE` valeur pointe vers la signature de métadonnées binaires du type de valeur.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-109">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="0b2ae-110">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée stockée dans les registres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-110">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified registers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0b2ae-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0b2ae-111">Remarks</span></span>  
 <span data-ttu-id="0b2ae-112">Le `GetLocalDoubleRegisterValue` méthode peut être utilisée dans un frame natif ou un juste-à-temps (JIT)-frame compilé.</span><span class="sxs-lookup"><span data-stu-id="0b2ae-112">The `GetLocalDoubleRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0b2ae-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b2ae-113">Requirements</span></span>  
 <span data-ttu-id="0b2ae-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b2ae-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b2ae-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0b2ae-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0b2ae-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0b2ae-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0b2ae-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0b2ae-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b2ae-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b2ae-118">See also</span></span>
