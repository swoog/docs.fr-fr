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
ms.openlocfilehash: 9de77f942a1b89b0ab11ef71229e491a5305cafc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420750"
---
# <a name="icordebugnativeframegetlocaldoubleregistervalue-method"></a><span data-ttu-id="9593e-102">ICorDebugNativeFrame::GetLocalDoubleRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="9593e-102">ICorDebugNativeFrame::GetLocalDoubleRegisterValue Method</span></span>
<span data-ttu-id="9593e-103">Obtient la valeur d’un argument ou une variable locale qui est stockée dans deux registres spécifiés pour ce frame natif.</span><span class="sxs-lookup"><span data-stu-id="9593e-103">Gets the value of an argument or local variable that is stored in the two specified registers for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9593e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9593e-104">Syntax</span></span>  
  
```  
HRESULT GetLocalDoubleRegisterValue (  
    [in] CorDebugRegister   highWordReg,  
    [in] CorDebugRegister   lowWordReg,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9593e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9593e-105">Parameters</span></span>  
 `highWordReg`  
 <span data-ttu-id="9593e-106">[in] Valeur de l’énumération « CorDebugRegister » qui spécifie le Registre contenant le mot de poids fort de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9593e-106">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the high word of the value.</span></span>  
  
 `lowWordReg`  
 <span data-ttu-id="9593e-107">[in] Une valeur de la `CorDebugRegister` énumération qui spécifie le Registre contenant le mot de poids faible de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9593e-107">[in] A value of the `CorDebugRegister` enumeration that specifies the register containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="9593e-108">[in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.</span><span class="sxs-lookup"><span data-stu-id="9593e-108">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="9593e-109">[in] A `PCCOR_SIGNATURE` valeur qui pointe vers la signature de métadonnées binaires du type de la valeur.</span><span class="sxs-lookup"><span data-stu-id="9593e-109">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="9593e-110">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée qui est stockée dans les registres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9593e-110">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified registers.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9593e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9593e-111">Remarks</span></span>  
 <span data-ttu-id="9593e-112">Le `GetLocalDoubleRegisterValue` méthode peut être utilisée dans un frame natif ou un juste-à-temps (JIT)-frame compilé.</span><span class="sxs-lookup"><span data-stu-id="9593e-112">The `GetLocalDoubleRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9593e-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9593e-113">Requirements</span></span>  
 <span data-ttu-id="9593e-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9593e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9593e-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9593e-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9593e-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9593e-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9593e-117">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9593e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9593e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9593e-118">See Also</span></span>  
 
