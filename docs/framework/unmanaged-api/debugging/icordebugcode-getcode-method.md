---
title: ICorDebugCode::GetCode, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetCode
helpviewer_keywords:
- ICorDebugCode::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7137e3d1-1dad-48d8-8c37-16ac816534d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d057032f2a46ef29a903ae21ab13af02f9d657f1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728763"
---
# <a name="icordebugcodegetcode-method"></a><span data-ttu-id="bdb95-102">ICorDebugCode::GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="bdb95-102">ICorDebugCode::GetCode Method</span></span>
<span data-ttu-id="bdb95-103">Obtient tout le code pour la fonction spécifiée, la mise en forme pour le code machine.</span><span class="sxs-lookup"><span data-stu-id="bdb95-103">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="bdb95-104">Cette méthode a été déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="bdb95-104">This method has been deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="bdb95-105">Utilisez [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="bdb95-105">Use [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdb95-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb95-106">Syntax</span></span>  
  
```  
HRESULT GetCode (  
    [in] ULONG32     startOffset,   
    [in] ULONG32     endOffset,  
    [in] ULONG32     cBufferAlloc,  
    [out, size_is(cBufferAlloc),  
        length_is(*pcBufferSize)] BYTE buffer[],  
    [out] ULONG32    *pcBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bdb95-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb95-107">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="bdb95-108">[in] Le décalage du début de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bdb95-108">[in] The offset of the beginning of the function.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="bdb95-109">[in] Le décalage de la fin de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bdb95-109">[in] The offset of the end of the function.</span></span>  
  
 `cBufferAlloc`  
 <span data-ttu-id="bdb95-110">[in] La taille de la `buffer` de tableau dans lequel le code sera retourné.</span><span class="sxs-lookup"><span data-stu-id="bdb95-110">[in] The size of the `buffer` array into which the code will be returned.</span></span>  
  
 `buffer`  
 <span data-ttu-id="bdb95-111">[out] Tableau dans lequel le code sera retourné.</span><span class="sxs-lookup"><span data-stu-id="bdb95-111">[out] The array into which the code will be returned.</span></span>  
  
 `pcBufferSize`  
 <span data-ttu-id="bdb95-112">[out] Le nombre d’octets retournés.</span><span class="sxs-lookup"><span data-stu-id="bdb95-112">[out] The number of bytes returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdb95-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb95-113">Remarks</span></span>  
 <span data-ttu-id="bdb95-114">Si le code de fonction a été divisé en plusieurs segments, elles sont concaténées par ordre croissant d’offset natif.</span><span class="sxs-lookup"><span data-stu-id="bdb95-114">If the function's code has been divided into multiple chunks, they are concatenated in order of increasing native offset.</span></span> <span data-ttu-id="bdb95-115">Limites d’instruction ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="bdb95-115">Instruction boundaries are not checked.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdb95-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bdb95-116">Requirements</span></span>  
 <span data-ttu-id="bdb95-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bdb95-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdb95-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bdb95-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bdb95-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bdb95-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bdb95-120">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="bdb95-120">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdb95-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb95-121">See also</span></span>
- [<span data-ttu-id="bdb95-122">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="bdb95-122">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)

