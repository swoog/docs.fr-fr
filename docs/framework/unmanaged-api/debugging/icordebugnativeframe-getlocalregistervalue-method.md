---
title: ICorDebugNativeFrame::GetLocalRegisterValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalRegisterValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalRegisterValue
helpviewer_keywords:
- GetLocalRegisterValue method [.NET Framework debugging]
- ICorDebugNativeFrame::GetLocalRegisterValue method [.NET Framework debugging]
ms.assetid: 5ccb74f3-f891-430c-b70a-e370624edde2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f53c8290271391e52176f8364b592ce6b46faf71
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195941"
---
# <a name="icordebugnativeframegetlocalregistervalue-method"></a><span data-ttu-id="cc8ed-102">ICorDebugNativeFrame::GetLocalRegisterValue, méthode</span><span class="sxs-lookup"><span data-stu-id="cc8ed-102">ICorDebugNativeFrame::GetLocalRegisterValue Method</span></span>
<span data-ttu-id="cc8ed-103">Obtient la valeur d’un argument ou une variable locale qui est stockée dans le Registre spécifié pour ce frame natif.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-103">Gets the value of an argument or local variable that is stored in the specified register for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc8ed-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc8ed-104">Syntax</span></span>  
  
```  
HRESULT GetLocalRegisterValue (  
    [in]  CorDebugRegister   reg,  
    [in]  ULONG              cbSigBlob,  
    [in]  PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc8ed-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8ed-105">Parameters</span></span>  
 `reg`  
 <span data-ttu-id="cc8ed-106">[in] Une valeur de l’énumération « CorDebugRegister » qui spécifie le Registre contenant la valeur.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-106">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="cc8ed-107">[in] Entier qui spécifie la taille de la signature de métadonnées binaires qui est référencée par le `pvSigBlob` paramètre.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-107">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="cc8ed-108">[in] Un `PCCOR_SIGNATURE` valeur pointe vers la signature de métadonnées binaires du type de valeur.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-108">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="cc8ed-109">[out] Pointeur vers l’adresse d’un objet « ICorDebugValue » représentant la valeur récupérée qui est stockée dans le Registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-109">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc8ed-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cc8ed-110">Remarks</span></span>  
 <span data-ttu-id="cc8ed-111">Le `GetLocalRegisterValue` méthode peut être utilisée dans un frame natif ou un juste-à-temps (JIT)-frame compilé.</span><span class="sxs-lookup"><span data-stu-id="cc8ed-111">The `GetLocalRegisterValue` method can be used either in a native frame or a just-in-time (JIT)-compiled frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc8ed-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc8ed-112">Requirements</span></span>  
 <span data-ttu-id="cc8ed-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc8ed-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc8ed-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cc8ed-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cc8ed-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc8ed-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="cc8ed-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="cc8ed-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="cc8ed-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc8ed-117">See also</span></span>
