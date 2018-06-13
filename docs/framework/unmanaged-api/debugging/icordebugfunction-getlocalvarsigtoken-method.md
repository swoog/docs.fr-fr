---
title: ICorDebugFunction::GetLocalVarSigToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetLocalVarSigToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetLocalVarSigToken
helpviewer_keywords:
- ICorDebugFunction::GetLocalVarSigToken method [.NET Framework debugging]
- GetLocalVarSigToken method [.NET Framework debugging]
ms.assetid: 31e53494-bcc9-4981-91a4-f7e0f02cad48
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9a09741ed778436f1cb35d094885bd3effa813a5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33411592"
---
# <a name="icordebugfunctiongetlocalvarsigtoken-method"></a><span data-ttu-id="ea553-102">ICorDebugFunction::GetLocalVarSigToken, méthode</span><span class="sxs-lookup"><span data-stu-id="ea553-102">ICorDebugFunction::GetLocalVarSigToken Method</span></span>
<span data-ttu-id="ea553-103">Obtient les métadonnées de jeton pour la signature de variable locale de la fonction qui est représentée par cette instance ICorDebugFunction.</span><span class="sxs-lookup"><span data-stu-id="ea553-103">Gets the metadata token for the local variable signature of the function that is represented by this ICorDebugFunction instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ea553-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea553-104">Syntax</span></span>  
  
```  
HRESULT GetLocalVarSigToken (  
    [out] mdSignature *pmdSig  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ea553-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea553-105">Parameters</span></span>  
 `pmdSig`  
 <span data-ttu-id="ea553-106">[out] Un pointeur vers le `mdSignature` jeton pour la signature de variable locale de cette fonction, ou `mdSignatureNil`, si cette fonction n’a pas de variables locales.</span><span class="sxs-lookup"><span data-stu-id="ea553-106">[out] A pointer to the `mdSignature` token for the local variable signature of this function, or `mdSignatureNil`, if this function has no local variables.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ea553-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea553-107">Requirements</span></span>  
 <span data-ttu-id="ea553-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ea553-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ea553-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ea553-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ea553-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ea553-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ea553-111">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ea553-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
